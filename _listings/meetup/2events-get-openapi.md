---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 0
info:
  title: Meetup Events
  description: Access Meetup events using a group, member, or event id. Events in
    private groups are available only to authenticated members of those groups. To
    search events by topic or location, see [Open Events](/meetup_api/docs/2/open_events).
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2/categories:
    get:
      summary: Categories
      description: Returns a list of Meetup group categories
      operationId: categories
      x-api-path-slug: 2categories-get
      parameters:
      - in: query
        name: fields
        description: Parameter for requesting optional response properties
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Categories
  /dashboard:
    get:
      summary: Dashboard
      description: A dashboard of aggregated Meetup information for the authorized
        member
      operationId: dashboard
      x-api-path-slug: dashboard-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Dashboard
  /2/topic_categories:
    get:
      summary: Topic Categories
      description: Returns a list of Meetup topic categories
      operationId: topics
      x-api-path-slug: 2topic-categories-get
      parameters:
      - in: query
        name: fields
        description: Parameter for requesting optional response properties
        type: string
      - in: query
        name: lat,lon,radius
        description: Use a given lat/lon/radius (miles) to search best_topics for
          instead of using the members lat/lon
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Categories
  /topics:
    get:
      summary: Topics
      description: API method for accessing meetup topics
      operationId: topics
      x-api-path-slug: topics-get
      parameters:
      - in: query
        name: member_id
        description: Return topics a target member is subscribed to
        type: string
      - in: query
        name: name
        description: Return topics that match the specified name (e
        type: string
      - in: query
        name: search
        description: Return topics related to a list of search terms [separate search
          keywords with +s]
        type: string
      - in: query
        name: topic
        description: Return topics for this topic urlkey
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Topics
  /events:
    get:
      summary: Events
      description: Deprecated API method for accessing meetup events. Please see [/2/events](/meetup_api/docs/2/events/)
        and [/2/open_events](/meetup_api/docs/2/open_events/) for replacements.
      operationId: deprecated
      x-api-path-slug: events-get
      parameters:
      - in: query
        name: after
        description: Return events that start after the specified date, formatted
          as either a relative date such as -1w for one week ago or by absolute time
          in milliseconds since the epoch
        type: string
      - in: query
        name: before
        description: Return events that started before the specified date, formatted
          as described by the after parameter
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: Return events from groups with the specified IDs, separated by
          commas
        type: string
      - in: query
        name: group_urlname
        description: Return events for the group with this custom URL path
        type: string
      - in: query
        name: id
        description: Return events with the specified IDs, separated by commas
        type: string
      - in: query
        name: member_id
        description: A member id number, limits results set to events in groups that
          the member specified by this id is currently a member of (excludes private
          groups, unless the member_id is the same as that of the member making the
          request)
        type: string
      - in: query
        name: rsvp_limit
        description: The number of yes rsvps an event can have before members will
          be added to the waiting list
        type: string
      - in: query
        name: status
        description: Return events matching one of the given status values, separated
          by commas
        type: string
      - in: query
        name: text_format
        description: Format of the description text, html, plain, or simplehtml
        type: string
      - in: query
        name: topic
        description: Return events in the specified topic(s), one topic allowed
        type: string
      - in: query
        name: topic, groupnum
        description: Return events for the group with given topic and number
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
  /2/open_events:
    get:
      summary: OpenEvents
      description: Searches for recent and upcoming public events hosted by Meetup
        groups. Its search window  is the past one month through the next three months,
        and is subject to change. Open Events is optimized to search for current events
        by location, category, topic, or text, and only lists Meetups that have **3
        or more RSVPs**. The number or results returned with each request is not guaranteed
        to be the same as the page size due to secondary filtering. If you're looking
        for a particular event or events within a particular group, use the standard
        [Events](/meetup_api/docs/2/events/) method.
      operationId: events
      x-api-path-slug: 2open-events-get
      parameters:
      - in: query
        name: and_text
        description: Changes the interpretation of the text field from ORd terms to
          ANDd terms
        type: string
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: category
        description: Return events in the specified category or categories specified
          by commas
        type: string
      - in: query
        name: city
        description: A valid city
        type: string
      - in: query
        name: country
        description: A valid country code
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: lat
        description: A valid latitude, limits the returned group events to those within
          radius miles
        type: string
      - in: query
        name: limited_events
        description: Include limited event information for private groups that wish
          to expose only a small amount of information about their events
        type: string
      - in: query
        name: lon
        description: A valid longitude, limits the returned group events to those
          within radius miles
        type: string
      - in: query
        name: radius
        description: Radius, in miles for geographic requests, default 25
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Return events with an mtime greater than the supplied time, in
          milliseconds since the epoch
        type: string
      - in: query
        name: state
        description: If searching in a country with states, a valid 2 character state
          code
        type: string
      - in: query
        name: status
        description: Status may be upcoming, past or both separated by a comma
        type: string
      - in: query
        name: text
        description: Events that contain the given term or terms somewhere in their
          content
        type: string
      - in: query
        name: text_format
        description: Format of the description text, html or plain
        type: string
      - in: query
        name: time
        description: Return events scheduled within the given time range, defined
          by two times separated with a single comma
        type: string
      - in: query
        name: topic
        description: Return events in the specified topic or topics specified by commas
        type: string
      - in: query
        name: zip
        description: A valid US zip code, limits the returned groups to those within
          radius miles
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
  /2/concierge:
    get:
      summary: Concierge
      description: Recommends upcoming meetups for the authorized member in a given
        location and in thier groups
      operationId: events
      x-api-path-slug: 2concierge-get
      parameters:
      - in: query
        name: category_id
        description: Comma delimited list of category ids to limit recommendations
          to
        type: string
      - in: query
        name: city
        description: A valid city
        type: string
      - in: query
        name: country
        description: A valid country code
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: lat
        description: A valid latitude, limits the returned group events to those within
          radius miles
        type: string
      - in: query
        name: lon
        description: A valid longitude, limits the returned group events to those
          within radius miles
        type: string
      - in: query
        name: page_token
        description: An opaque string used to page through results
        type: string
      - in: query
        name: radius
        description: Radius, in miles for geographic requests, defaults to the members
          preferred radius or 0
        type: string
      - in: query
        name: self_groups
        description: set to include or exclude groups the authorized member belongs
          to
        type: string
      - in: query
        name: state
        description: If searching in a country with states, a valid 2 character state
          code
        type: string
      - in: query
        name: text_format
        description: Format of the description text, html, plain, or simplehtml
        type: string
      - in: query
        name: time
        description: Return events scheduled within the given time range, defined
          by two times separated with a single comma
        type: string
      - in: query
        name: topic_id
        description: Comma delimited list of topics to help inform recommendation
        type: string
      - in: query
        name: with_friends
        description: Boolean parameter
        type: string
      - in: query
        name: zip
        description: A valid US zip code, limits the returned groups to those within
          radius miles
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
  /2/groups:
    get:
      summary: Groups
      description: Fetch information about Meetup Groups.
      operationId: groups
      x-api-path-slug: 2groups-get
      parameters:
      - in: query
        name: category_id
        description: Only return groups in the specified category
        type: string
      - in: query
        name: country, city, state
        description: A valid country code, city and for the US, State
        type: string
      - in: query
        name: domain
        description: one or more custom group domains, separated by commas
        type: string
      - in: query
        name: fields
        description: optional result fields, separated by commas
        type: string
      - in: query
        name: group_id
        description: one or more separated by commas
        type: string
      - in: query
        name: group_urlname
        description: one or more separated by commas, includes no slashes
        type: string
      - in: query
        name: lat,lon
        description: A valid latitude and longitude, limits the returned groups to
          those within radius miles
        type: string
      - in: query
        name: member_id
        description: one or more separated by commas, for groups this member belongs
          to
        type: string
      - in: query
        name: organizer_id
        description: one or more organizer IDs, separated by commas
        type: string
      - in: query
        name: radius
        description: Radius, in miles for geographic requests, default 25 -- maximum
          100
        type: string
      - in: query
        name: topic
        description: Only return groups in the specified topic [one topic allowed]
        type: string
      - in: query
        name: topic, groupnum
        description: Return the group with this topic and number
        type: string
      - in: query
        name: zip
        description: A valid US zip code, limits the returned groups to those within
          radius miles
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
  /2/events:
    get:
      summary: Events
      description: Access Meetup events using a group, member, or event id. Events
        in private groups are available only to authenticated members of those groups.
        To search events by topic or location, see [Open Events](/meetup_api/docs/2/open_events).
      operationId: events
      x-api-path-slug: 2events-get
      parameters:
      - in: query
        name: event_id
        description: Multiple ids may be separated with commas
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_domain
        description: Group custom domain
        type: string
      - in: query
        name: group_id
        description: Multiple ids may be separated with commas
        type: string
      - in: query
        name: group_urlname
        description: Path to group from meetup
        type: string
      - in: query
        name: limited_events
        description: Include limited event information for private groups that wish
          to expose only a small amount of information about their events
        type: string
      - in: query
        name: member_id
        description: Single member id, to find events in this members groups
        type: string
      - in: query
        name: rsvp
        description: Filters events by the currently authenticated members RSVP status
        type: string
      - in: query
        name: status
        description: Status may be upcoming, past, proposed, suggested, cancelled,
          draft or multiple separated by a comma
        type: string
      - in: query
        name: text_format
        description: Format of the description text, html or plain
        type: string
      - in: query
        name: time
        description: Return events scheduled within the given time range, defined
          by two times separated with a single comma
        type: string
      - in: query
        name: venue_id
        description: Multiple ids may be separated with commas
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
x-streamrank:
  polling_total_time_average: "0.11"
  polling_size_download_average: "1941.69"
  streaming_total_time_average: "0.06"
  streaming_size_download_average: "983.16"
  change_yes: "84"
  change_no: "1779"
  time_percentage: "45"
  size_percentage: "49"
  change_percentage: "5"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---