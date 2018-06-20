---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 0
info:
  title: Meetup API Status
  description: Returns the current API service status
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
  /2/event:
    post:
      summary: Event Create
      description: Create a new Meetup event within the system.
      operationId: events
      x-api-path-slug: 2event-post
      parameters:
      - in: query
        name: description
        description: Longer description of the event, in HTML
        type: string
      - in: query
        name: duration
        description: Event duration in milliseconds
        type: string
      - in: query
        name: group_id
        description: Group hosting the event
        type: string
      - in: query
        name: group_urlname
        description: URL name of the Group hosting the event
        type: string
      - in: query
        name: guest_limit
        description: Number of guests members may include in their RSVP, 0 or more
        type: string
      - in: query
        name: hosts
        description: Up to 5 comma-separated valid member ids to be hosts for the
          event
        type: string
      - in: query
        name: how_to_find_us
        description: The information provided by the event host for How will members
          find you there?
        type: string
      - in: query
        name: name
        description: Name of the event
        type: string
      - in: query
        name: publish_status
        description: If you are an organizer of the group, you may set this to draft
          to save the event as a draft
        type: string
      - in: query
        name: question_{index}
        description: Those with permission may include up to 6 survey questions for
          the event with each being up to 250 characters
        type: string
      - in: query
        name: rsvp_close
        description: Users with permission may set the RSVP close time for the event
        type: string
      - in: query
        name: rsvp_limit
        description: Total number of RSVPs available for the event
        type: string
      - in: query
        name: rsvp_open
        description: Users with permission may set the RSVP open time for the event
        type: string
      - in: query
        name: simple_html_description
        description: Description of the event, in simple HTML format
        type: string
      - in: query
        name: time
        description: Event start time in milliseconds since the epoch, or relative
          to the current time in the d/w/m format
        type: string
      - in: query
        name: venue_id
        description: Numeric identifier of a venue
        type: string
      - in: query
        name: venue_visibility
        description: Controls the visibility of the event venue for non members of
          the hosting group
        type: string
      - in: query
        name: why
        description: We should do this because
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
  /2/event/:id:
    post:
      summary: Event Edit
      description: Update an existing Meetup
      operationId: events
      x-api-path-slug: 2eventid-post
      parameters:
      - in: query
        name: announce
        description: Organizers and hosts may set this to true to announce a Meetup
        type: string
      - in: query
        name: description
        description: Longer description of the event, in HTML
        type: string
      - in: query
        name: duration
        description: Event duration in milliseconds
        type: string
      - in: query
        name: group_id
        description: Group to hold the event
        type: string
      - in: query
        name: guest_limit
        description: number of guests members may include in their RSVP, 0 or more
        type: string
      - in: query
        name: hosts
        description: Up to 5 valid member ids to be hosts for the event
        type: string
      - in: query
        name: how_to_find_us
        description: The information provided by the event host for How will members
          find you there?
        type: string
      - in: query
        name: lat,lon
        description: Updates to the venues latitude and longitude
        type: string
      - in: query
        name: name
        description: Event name
        type: string
      - in: query
        name: publish_status
        description: If you are an organizer of the group, you may set this to draft
          or published
        type: string
      - in: query
        name: question_edit_{id}
        description: Those with permission may include up to 6 survey questions with
          each being up to 250 characters, including new questions
        type: string
      - in: query
        name: question_{index}
        description: Those with permission may include up to 6 survey questions with
          each being up to 250 characters, including edited questions, for the event
        type: string
      - in: query
        name: rsvp_close
        description: Users with permission may set the RSVP close time for the event
        type: string
      - in: query
        name: rsvp_limit
        description: Total number of RSVPs available for the event
        type: string
      - in: query
        name: rsvp_open
        description: Users with permission may set the RSVP open time for the event
        type: string
      - in: query
        name: simple_html_description
        description: Description of the event, in simple HTML format
        type: string
      - in: query
        name: time
        description: event start time in milliseconds since the epoch, or relative
          to the current time in the d/w/m format
        type: string
      - in: query
        name: venue_id
        description: Numeric identifier of a venue
        type: string
      - in: query
        name: venue_visibility
        description: Controls the visibility of venue
        type: string
      - in: query
        name: why
        description: We should do this because
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
    delete:
      summary: Event Delete
      description: Deletes a specified meetup
      operationId: events
      x-api-path-slug: 2eventid-delete
      responses:
        200:
          description: OK
      tags:
      - Events
  /photos:
    get:
      summary: Photos
      description: API method for accessing meetup photos
      operationId: deprecated
      x-api-path-slug: photos-get
      parameters:
      - in: query
        name: album_id
        description: return photos for the albums with the given id, separated by
          commas
        type: string
      - in: query
        name: group_id
        description: Return photos in groups with these ID numbers [separated by commas]
        type: string
      - in: query
        name: group_urlname
        description: return photos for the group with given custom URL path
        type: string
      - in: query
        name: topic
        description: Return photos in this topic
        type: string
      - in: query
        name: topic, groupnum
        description: return photos for the group with given topic and number
        type: string
      - in: query
        name: topic_id
        description: Return photos in topics with this ID number
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
  /cities:
    get:
      summary: Cities
      description: API method for accessing meetup cities
      operationId: deprecated
      x-api-path-slug: cities-get
      parameters:
      - in: query
        name: country
        description: Return cities in these countries [separate countries with commas]
        type: string
      - in: query
        name: state
        description: Return cities in these states [separate states with commas]
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Cities
  /2/cities:
    get:
      summary: Cities
      description: Returns Meetup cities. This method supports search by latitude/longitude/radius,
        by country/state, by query term/zip, or a combination of all of these. Location-only
        searches by lat and lon return all cities within a radius of the provided
        coordinates. Searches with a query return up to 10 cities matching the term,
        and can be sorted by size or distance to a given coordinate. 'smart' ordering
        can be used to return the match(es) with the highest member_count, unless
        a smaller size match exists nearby the given coordinates. Query searches are
        supported for country but not country and state
      operationId: cities
      x-api-path-slug: 2cities-get
      parameters:
      - in: query
        name: country
        description: A valid country code
        type: string
      - in: query
        name: lat
        description: Latitude to search
        type: string
      - in: query
        name: lon
        description: Longitude to search
        type: string
      - in: query
        name: query
        description: Search term and/or zip to look for (if this is specified, max
          result size limited to 10)
        type: string
      - in: query
        name: radius
        description: When searching by lat/lon only, specify a radius to search (default
          50 miles)
        type: string
      - in: query
        name: state
        description: A valid state code for the given country, if the country has
          states
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Cities
  /members:
    get:
      summary: Members
      description: API method for accessing members of Meetup Groups
      operationId: deprecated
      x-api-path-slug: members-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: Return members in groups with these ID numbers, separated by
          commas
        type: string
      - in: query
        name: group_urlname
        description: Return members for the group with the given custom URL path
        type: string
      - in: query
        name: member_id
        description: Return the member with this ID
        type: string
      - in: query
        name: relation
        description: Supply the string self as the value for this parameter to get
          the information of the member linked to the API key making the request
        type: string
      - in: query
        name: service
        description: Match users by the external services theyve linked to their member
          account, specified as servicename:identifier
        type: string
      - in: query
        name: topic,groupnum
        description: Return members for the group with given topic and number
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
      - Members
  /2/members:
    get:
      summary: Members
      description: API method for accessing members of Meetup Groups
      operationId: members
      x-api-path-slug: 2members-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: Return members in groups with these ID numbers, separated by
          commas
        type: string
      - in: query
        name: group_urlname
        description: Return members for the group with the given custom URL path
        type: string
      - in: query
        name: member_id
        description: Return the member with this ID
        type: string
      - in: query
        name: service
        description: Match users by the external services theyve linked to their member
          account, specified as servicename:identifier
        type: string
      - in: query
        name: topic,groupnum
        description: Return members for the group with given topic and number
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
      - Member
  /2/member/:id:
    get:
      summary: Member Get
      description: Retrieve a single member
      operationId: members
      x-api-path-slug: 2memberid-get
      parameters:
      - in: query
        name: fields
        description: comma-separate list of optional fields
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
      - Member
    post:
      summary: Member Edit
      description: Edit the authorized member's attributes
      operationId: members
      x-api-path-slug: 2memberid-post
      parameters:
      - in: query
        name: add_topics
        description: Comma-delimited list of topics ids to add to your alert list
        type: string
      - in: query
        name: bio
        description: Free form text passage about you
        type: string
      - in: query
        name: bio_privacy
        description: Controls the visibility of the members bio
        type: string
      - in: query
        name: birthday
        description: Day you were born
        type: string
      - in: query
        name: city
        description: City name for your location
        type: string
      - in: query
        name: city_id
        description: Valid city id from /2/cities method
        type: string
      - in: query
        name: country
        description: Valid country code for your location
        type: string
      - in: query
        name: facebook_privacy
        description: Controls the visibility of the members facebook connection
        type: string
      - in: query
        name: gender
        description: Your gender (used for better recommendations)
        type: string
      - in: query
        name: groups_privacy
        description: Controls the visibility of the members groups
        type: string
      - in: query
        name: hometown
        description: Hometown of member
        type: string
      - in: query
        name: lang
        description: Language preference used on the site
        type: string
      - in: query
        name: lat
        description: latitude of city
        type: string
      - in: query
        name: lon
        description: longitude of city
        type: string
      - in: query
        name: messaging_pref
        description: This specifies the members preference for being contacted from
          members on the site
        type: string
      - in: query
        name: name
        description: The name of the current member
        type: string
      - in: query
        name: photos_privacy
        description: Controls the visibility of the members photos
        type: string
      - in: query
        name: photo_id
        description: A valid photo_id from the members photos to set as the main profile
          photo
        type: string
      - in: query
        name: radius
        description: radius, in miles to search for city given a lat and lon
        type: string
      - in: query
        name: remove_topics
        description: Comma-delimited list of topic ids to remove from your alert list
        type: string
      - in: query
        name: sync_photo
        description: When set to true, this parameter will sync all of the group profile
          photos for the member with the provided photo_id
        type: string
      - in: query
        name: topics_privacy
        description: Controls the visibility of the members topics
        type: string
      - in: query
        name: zip
        description: Valid zip code for city
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
      - Member
  /2/profiles:
    get:
      summary: Profiles
      description: This method returns member *profiles* associated with a particular
        group. Meetup members have separate profiles for each group they join.
      operationId: profiles
      x-api-path-slug: 2profiles-get
      parameters:
      - in: query
        name: fields
        description: comma delimited list of optional response properties
        type: string
      - in: query
        name: group_id
        description: Return profiles in the group with this ID
        type: string
      - in: query
        name: group_urlname
        description: Return profiles for the group with the given custom URL path
        type: string
      - in: query
        name: member_id
        description: Return the profiles for members with these IDs, separated by
          commas
        type: string
      - in: query
        name: role
        description: if leads, only profiles for members of the leadership team are
          included
        type: string
      - in: query
        name: status
        description: Status filter for members
        type: string
      - in: query
        name: topic, groupnum
        description: Group identification by topic, deprecated
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Profile
  /2/profile:
    post:
      summary: Profile Create (Group Join)
      description: This method allows an authenticated member to join a group by creating
        a profile
      operationId: profiles
      x-api-path-slug: 2profile-post
      parameters:
      - in: query
        name: answer_{qid}
        description: Answers to questions from groups API join_info question fields
        type: string
      - in: query
        name: group_id
        description: Id of group to join
        type: string
      - in: query
        name: group_urlname
        description: Urlname of group to join
        type: string
      - in: query
        name: intro
        description: Provides a Member an opportunity to tell the group about themselves
        type: string
      - in: query
        name: new_photo
        description: file upload for a new member photo
        type: string
      - in: query
        name: photo_id
        description: photo_id of the photo to use for this profile
        type: string
      - in: query
        name: site_name
        description: Name of members site
        type: string
      - in: query
        name: site_url
        description: Link to members site
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Profile
  /2/profile/:gid/:mid:
    post:
      summary: Profile Edit
      description: Update a member's group profile
      operationId: profiles
      x-api-path-slug: 2profilegidmid-post
      parameters:
      - in: query
        name: add_role
        description: 'Allows those with permission to assign one of the following
          roles: coorganizer, event_organizer, assistant_organizer'
        type: string
      - in: query
        name: answer_{qid}
        description: Answers to questions from groups API join_info question fields
        type: string
      - in: query
        name: intro
        description: Provides a Member an opportunity to tell the group about themselves
        type: string
      - in: query
        name: new_photo
        description: file upload for a new member photo
        type: string
      - in: query
        name: photo_id
        description: photo_id of the photo to use for this profile
        type: string
      - in: query
        name: remove_role
        description: 'Allows those with permission to remove one of the following
          roles: coorganizer, event_organizer, assistant_organizer'
        type: string
      - in: query
        name: site_name
        description: Name of members site
        type: string
      - in: query
        name: site_url
        description: Link to members site
        type: string
      - in: query
        name: title
        description: An organizer-defined member title
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Profile
    get:
      summary: Profile Get
      description: Retrieves a single group profile
      operationId: profiles
      x-api-path-slug: 2profilegidmid-get
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
      - Profile
    delete:
      summary: Profile Delete (Leave Group)
      description: Deletes a member's group profile
      operationId: profiles
      x-api-path-slug: 2profilegidmid-delete
      parameters:
      - in: query
        name: exit_comment
        description: Optional message to the organizer when leaving
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Profile
  /2/photo/:id:
    delete:
      summary: Event Photo Delete
      description: Deletes a specified event photo
      operationId: photos
      x-api-path-slug: 2photoid-delete
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
    post:
      summary: Event Photo Edit
      description: Edits a specified event photo
      operationId: photos
      x-api-path-slug: 2photoid-post
      parameters:
      - in: query
        name: caption
        description: Photo caption of up to 255 characters
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
  /2/member_photo/:id:
    delete:
      summary: Member Photo Delete
      description: Delete the specified member photo
      operationId: members
      x-api-path-slug: 2member-photoid-delete
      responses:
        200:
          description: OK
      tags:
      - Events
  /comments:
    get:
      summary: Comments
      description: API method for accessing meetup group comments
      operationId: groups
      x-api-path-slug: comments-get
      parameters:
      - in: query
        name: group_id
        description: Return comments in groups with these ID numbers [separated by
          commas]
        type: string
      - in: query
        name: group_urlname
        description: Return comments for the group with this custom URL path
        type: string
      - in: query
        name: topic, groupnum
        description: Return comments for the group with given topic and number
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/event_comments:
    get:
      summary: Comments v2
      description: This method returns messages that appear under Talk about this
        Meetup. To post messages, see the corresponding write method.
      operationId: events
      x-api-path-slug: 2event-comments-get
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: callback
        description: Name of a function to be called with an array of Event Comment
          notification objects
        type: string
      - in: query
        name: comment_id
        description: Return comments for a given set of comment IDs, separated by
          commas
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: event_id
        description: Return comments on these events, separated by commas
        type: string
      - in: query
        name: fields
        description: Optionally accepts the value member_photo or notifications
        type: string
      - in: query
        name: group_id
        description: Return comments in groups with these ID numbers, separated by
          commas
        type: string
      - in: query
        name: member_id
        description: Return comments for the given member_ids, separated by commas
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Should be supplied for all but the first polling request, so
          that any missed notifications are can be sent in an immediate response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
    ws:
      summary: WebSockets Event Comments Stream
      description: |-
        For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
        efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
        any messages received from the client after the socket is open.

        Because browser support for WebSockets is limited, we recommend that you consume this stream
        through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
      operationId: streams
      x-api-path-slug: 2event-comments-ws
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Return recent Event Comments with an mtime greater than the supplied
          time, in milliseconds since the epoch
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/event_comment:
    post:
      summary: Event Comment v2
      description: This method posts messages that appear under Talk about this Meetup.
      operationId: events
      x-api-path-slug: 2event-comment-post
      parameters:
      - in: query
        name: comment
        description: The comment text
        type: string
      - in: query
        name: event_id
        description: The event related to this comment
        type: string
      - in: query
        name: in_reply_to
        description: If this comment is a reply, the ID of the comment being replied
          to
        type: string
      - in: query
        name: notifications
        description: Notification control for authorized member on this comment thread
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/event_comment/:id:
    get:
      summary: Event Comment Get
      description: Retrieve a single event comment or reply
      operationId: events
      x-api-path-slug: 2event-commentid-get
      parameters:
      - in: query
        name: fields
        description: comma-separate list of optional fields
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
    delete:
      summary: Event Comment Delete
      description: Delete a single event comment or reply
      operationId: events
      x-api-path-slug: 2event-commentid-delete
      parameters:
      - in: query
        name: fields
        description: comma-separate list of optional fields
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/event_comment_flag:
    post:
      summary: Event Comment Flag
      description: This method creates a spam report for comment content
      operationId: events
      x-api-path-slug: 2event-comment-flag-post
      parameters:
      - in: query
        name: comment_id
        description: The id of the comment
        type: string
      - in: query
        name: reason
        description: Reason for flagging the comment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/event_comment_subscribe/:id:
    delete:
      summary: Event Comment Unsubscribe
      description: Unsubscribe to notifications for updates to a given comment thread
      operationId: events
      x-api-path-slug: 2event-comment-subscribeid-delete
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
    post:
      summary: Event Comment Subscribe
      description: Subscribe to notifications on updates to a given comment thread
      operationId: events
      x-api-path-slug: 2event-comment-subscribeid-post
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ratings
  /2/event_comment_like/:id:
    post:
      summary: Event Comment Like
      description: Like a given Event comment
      operationId: events
      x-api-path-slug: 2event-comment-likeid-post
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
    delete:
      summary: Event Comment Unlike
      description: Unlike a given Event comment
      operationId: events
      x-api-path-slug: 2event-comment-likeid-delete
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/event_comment_likes:
    get:
      summary: Comment Likes
      description: Api for listing likes of a given event comment
      operationId: events
      x-api-path-slug: 2event-comment-likes-get
      parameters:
      - in: query
        name: comment_id
        description: Return likes for a given comment_id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Comments
  /2/photo_comments:
    get:
      summary: Photo Comments v2
      description: This method returns comments on meetup photos. To post messages,
        see the corresponding write method
      operationId: photos
      x-api-path-slug: 2photo-comments-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: member_id
        description: Return comments for the given member_ids, separated by commas
        type: string
      - in: query
        name: photo_id
        description: Return comments on these photos, separated by commas
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Profile
  /2/photo_comment:
    post:
      summary: Photo Comment v2
      description: This method posts comments that appear below photos
      operationId: photos
      x-api-path-slug: 2photo-comment-post
      parameters:
      - in: query
        name: comment
        description: The comment text
        type: string
      - in: query
        name: photo_id
        description: The photo related to this comment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
      - Comments
  /2/event_ratings:
    get:
      summary: Ratings v2
      description: API method for accessing Meetup comments
      operationId: events
      x-api-path-slug: 2event-ratings-get
      parameters:
      - in: query
        name: event_id
        description: The ID of the event to fetch ratings data for
        type: string
      - in: query
        name: member_id
        description: The ID of a member to filter ratings on
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
  /2/event_rating:
    post:
      summary: Event Rating
      description: This method allows members to posts rating for an event after it's
        occurred. Only permitted for members who rsvp'd yes or maybe to the event
      operationId: events
      x-api-path-slug: 2event-rating-post
      parameters:
      - in: query
        name: attendee_count
        description: 'DEPRECATED: The number of attendees for the event (organizers/assistant
          organizers/co-organizers/event organizers/event hosts only)'
        type: string
      - in: query
        name: event_id
        description: The ID of the event to fetch ratings data for
        type: string
      - in: query
        name: rating
        description: The members rating (either 1, 2, 3, 4, or 5)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ratings
  /2/photo_albums:
    get:
      summary: Photo Albums
      description: This method returns photo albums associated with Meetup groups.
        To create albums, see the corresponding write method.
      operationId: photos
      x-api-path-slug: 2photo-albums-get
      parameters:
      - in: query
        name: event_id
        description: Return photo albums for these event ids, separated by commas
        type: string
      - in: query
        name: group_id
        description: Return albums in groups with these ID, separated by commas
        type: string
      - in: query
        name: photo_album_id
        description: Return albums with these IDs, separated by commas
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
      - Comments
  /2/photos:
    get:
      summary: Photos
      description: This method returns photos by member, group, album, event, photo
        ID, or tagged member.
      operationId: photos
      x-api-path-slug: 2photos-get
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: callback
        description: Name of a function to be called with an array of photo notification
          objects
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: event_id
        description: Event ids, separated by commas
        type: string
      - in: query
        name: fields
        description: comma-delimited optional response properties such as member_country,
          member_city, member_state, and self
        type: string
      - in: query
        name: group_id
        description: Group IDs, separated by commas
        type: string
      - in: query
        name: group_urlname
        description: Group urlnames, separated by commas
        type: string
      - in: query
        name: member_id
        description: Uploaded by members with these IDs, separated by commas
        type: string
      - in: query
        name: photo_album_id
        description: Photo Album IDs, separated by commas
        type: string
      - in: query
        name: photo_id
        description: Photo IDs, separated by commas
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Should be supplied for all but the first polling request, so
          that any missed notifications are can be sent in an immediate response
        type: string
      - in: query
        name: tagged
        description: Tagged with members with these IDs, separated by commas
        type: string
      - in: query
        name: time
        description: Return photos uploaded within the given time range, defined by
          two times separated with a single comma
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
    ws:
      summary: WebSocket Photo Stream
      description: |-
        For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
        efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
        any messages received from the client after the socket is open.

        Because browser support for WebSockets is limited, we recommend that you consume this stream
        through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
      operationId: streams
      x-api-path-slug: 2photos-ws
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Return recent photos with an mtime greater then the supplied
          time, in millisends since the epoch
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
      - Albums
  /2/photo_album:
    post:
      summary: Photo Album2
      description: This method creates photo albums within a Meetup group
      operationId: photos
      x-api-path-slug: 2photo-album-post
      parameters:
      - in: query
        name: group_id
        description: Group to create the album in
        type: string
      - in: query
        name: title
        description: Title of the new album
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
      - Albums
  /2/open_venues:
    get:
      summary: OpenVenues
      description: Searches for public venues within a given geo space. To search
        for specific venues that your group has used, use the [Venues](/meetup_api/docs/2/venues)
        method
      operationId: venues
      x-api-path-slug: 2open-venues-get
      parameters:
      - in: query
        name: api_version
        description: "2"
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
        name: group_urlname
        description: Returns venues with location relative to the group associated
          with this urlname
        type: string
      - in: query
        name: lat
        description: A valid latitude, limits the returned venues to those within
          radius miles
        type: string
      - in: query
        name: lon
        description: A valid longitude, limits the returned venues to those within
          radius miles
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
        description: Return recent open venues with an mtime greater then the supplied
          time, in milliseconds since the epoch
        type: string
      - in: query
        name: state
        description: For the US, a valid 2 character state code
        type: string
      - in: query
        name: text
        description: Venues that contain the given term or terms somewhere in their
          content
        type: string
      - in: query
        name: trickle
        description: When supplied with a request, the Meetup API will push your client
          the entire Meetup database of public venues in batches of 512
        type: string
      - in: query
        name: zip
        description: A valid US zip code, limits the returned venues to those within
          radius miles
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
  /2/venues:
    get:
      summary: Venues
      description: Search for Meetup venues by one of your groups, events, or venue
        identifiers. For a full text search on public venues use [OpenVenues](/meetup_api/docs/2/open_venues).
      operationId: venues
      x-api-path-slug: 2venues-get
      parameters:
      - in: query
        name: event_id
        description: multiple ids may be separated with commas
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: multiple ids may be separated with commas
        type: string
      - in: query
        name: group_urlname
        description: path to group from meetup
        type: string
      - in: query
        name: venue_id
        description: multiple ids may be separated with commas
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Venues
  /rsvps:
    get:
      summary: Rsvps
      description: API method for accessing meetup rsvps
      operationId: deprecated
      x-api-path-slug: rsvps-get
      parameters:
      - in: query
        name: event_id
        description: Return members that RSVPd to events with these ID numbers [separated
          by commas]
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - RSVP
  /rsvp:
    post:
      summary: RSVP
      description: Creates a new Rsvp
      operationId: deprecated
      x-api-path-slug: rsvp-post
      parameters:
      - in: query
        name: answer_{qid}
        description: Answers to event survey questions
        type: string
      - in: query
        name: comments
        description: A comment to post along with the RSVP
        type: string
      - in: query
        name: event_id
        description: The event that you are RSVPing to
        type: string
      - in: query
        name: guests
        description: Number of guests also coming to the event
        type: string
      - in: query
        name: member_id
        description: Organizers and event hosts may RSVP on behalf of a member by
          specifying an ID here
        type: string
      - in: query
        name: rsvp
        description: The RSVP setting - value must be either yes
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - RSVP
  /2/rsvps:
    get:
      summary: RSVPs v2
      description: Query for Event RSVPs by event
      operationId: rsvps
      x-api-path-slug: 2rsvps-get
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: callback
        description: Name of a function to be called with an array of RSVP notification
          objects
        type: string
      - in: query
        name: event_id
        description: Multiple alphanumeric ids may be separated with commas
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: fields
        description: Parameter for requesting optional response properties, set to
          other_services for a list of third party services
        type: string
      - in: query
        name: rsvp
        description: Filters response on RSVP status
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Should be supplied for all but the first polling request, so
          that any missed notifications are can be sent in an immediate response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
    ws:
      summary: WebSockets RSVP Stream
      description: |-
        For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
        efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
        any messages received from the client after the socket is open.

        Because browser support for WebSockets is limited, we recommend that you consume this stream
        through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
      operationId: streams
      x-api-path-slug: 2rsvps-ws
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Return recent RSVPs with an mtime greater than the supplied time,
          in milliseconds since the epoch
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Streaming
      - Websockets
  /2/rsvp:
    post:
      summary: RSVP Create/Update
      description: Creates or updates an existing RSVP
      operationId: rsvps
      x-api-path-slug: 2rsvp-post
      parameters:
      - in: query
        name: agree_to_refund
        description: For events with fees, the authorized member must agree to the
          events refund policy
        type: string
      - in: query
        name: answer_{qid}
        description: Answers to event survey questions
        type: string
      - in: query
        name: comments
        description: A comment to post along with the RSVP
        type: string
      - in: query
        name: event_id
        description: The event that you are RSVPing to
        type: string
      - in: query
        name: guests
        description: Number of guests also coming to the event
        type: string
      - in: query
        name: member_id
        description: Organizers and event hosts may RSVP on behalf of a member by
          specifying an ID here
        type: string
      - in: query
        name: opt_to_pay
        description: For events with fees, the authorized member may opt to pay as
          part of the RSVP request
        type: string
      - in: query
        name: rsvp
        description: The RSVP setting - value must be either yes, no or waitlist
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
  /2/rsvp/:id:
    get:
      summary: RSVP Get
      description: Retrieve a single RSVP
      operationId: rsvps
      x-api-path-slug: 2rsvpid-get
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
  /2/group_photo:
    post:
      summary: Group Photo Upload
      description: Uploads a new Meetup Group photo. To change other Group settings
        use the [Group Edit](/meetup_api/docs/:urlname/#edit) endpoint
      operationId: groups
      x-api-path-slug: 2group-photo-post
      parameters:
      - in: query
        name: await
        description: If true, this ensures a response will not be returned until the
          upload is accessible
        type: string
      - in: query
        name: group_id
        description: Group ID for the target group
        type: string
      - in: query
        name: group_urlname
        description: Group urlname
        type: string
      - in: query
        name: main
        description: Set to true to have this photo become the groups main photo
        type: string
      - in: query
        name: photo
        description: The photo, encoded as multipart/form-data
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
  /2/member_photo:
    post:
      summary: Member Photo Upload
      description: Uploads a photo to be associated with a Member
      operationId: members
      x-api-path-slug: 2member-photo-post
      parameters:
      - in: query
        name: await
        description: If true, this ensures a response will not be returned until the
          upload is accessible
        type: string
      - in: query
        name: main
        description: Set to true to have this photo become the members main profile
          photo
        type: string
      - in: query
        name: photo
        description: The photo, encoded as multipart/form-data
        type: string
      - in: query
        name: sync_matching_photo
        description: When set to true and main is set to true, this will replace all
          group profile photos matching the current photo with the provided replacement
        type: string
      - in: query
        name: sync_photo
        description: When set to true, this parameter will sync all of the group profile
          photos for the member with the provided photo_id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups
      - Member
  /2/photo:
    post:
      summary: Event Photo Upload
      description: Uploads a photo for a given event
      operationId: photos
      x-api-path-slug: 2photo-post
      parameters:
      - in: query
        name: await
        description: If true, this ensures a response will not be returned until the
          upload is accessible
        type: string
      - in: query
        name: caption
        description: Caption for the photo
        type: string
      - in: query
        name: event_id
        description: Identifier of an event
        type: string
      - in: query
        name: photo
        description: The photo, encoded as multipart/form-data
        type: string
      - in: query
        name: photo_album_id
        description: Identifier of an existing photo album, which may be an event
          or group album
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Photos
  /groups:
    get:
      summary: Groups
      description: API method for accessing meetup groups
      operationId: deprecated
      x-api-path-slug: groups-get
      parameters:
      - in: query
        name: country, city, state
        description: A valid country code, city and for the US, State
        type: string
      - in: query
        name: fields
        description: Set to short_link to include shortened group URLs in response
          items
        type: string
      - in: query
        name: group_urlname
        description: Return the group with this custom url path (e
        type: string
      - in: query
        name: id
        description: Only return groups with the specified IDs [separate ID numbers
          with commas]
        type: string
      - in: query
        name: lat,lon
        description: A valid latitude and longitude, limits the returned groups to
          those within radius miles
        type: string
      - in: query
        name: member_id
        description: A member id number, limits results set to only those groups that
          the member specified by this id is currently a member of (excludes private
          groups, unless the member_id is the same as that of the member making the
          request)
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
        name: visibility
        description: Set to members or public to restrict to groups of a particular
          visibility
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
  /activity:
    get:
      summary: ActivityFeed
      description: API method for retrieving the activity feed for a member's groups
      operationId: feeds
      x-api-path-slug: activity-get
      parameters:
      - in: query
        name: member_id
        description: Returns activity from this members groups
        type: string
      - in: query
        name: page_start
        description: Starting timestamp for item to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Activity
      - Feeds
  /oembed:
    get:
      summary: oEmbed
      description: oEmbed implementation
      operationId: oembed
      x-api-path-slug: oembed-get
      parameters:
      - in: query
        name: maxwidth
        description: maximum width to display
        type: string
      - in: query
        name: url
        description: url of resource to be embedded
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - oEmbed
      - Media
  /status:
    get:
      summary: API Status
      description: Returns the current API service status
      operationId: meta
      x-api-path-slug: status-get
      responses:
        200:
          description: OK
      tags:
      - Events
      - Status
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---