---
swagger: "2.0"
info:
  title: Meetup
  description: 'The Meetup API provides simple RESTful HTTP and streaming interfaces
    for exploring and interacting Meetup platform from your own apps. The API is a
    set of core methods and a common request format. These are combined to form a
    URL that returns the information you want. '
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
  /pro/:urlname/groups:
    get:
      summary: Search Pro Groups
      description: Name and statistics range search for the meetup groups belonging
        to Pro organization
      operationId: pro
      parameters:
      - in: query
        name: active_within_days
        description: 'Positive Integer: including only those groups that had event
          in the last specified days'
        type: string
      - in: query
        name: average_age_max
        description: 'Positive Integer: Maximum range of the average age of the members'
        type: string
      - in: query
        name: average_age_min
        description: 'Positive Integer: Minumum range of the average age of the members'
        type: string
      - in: query
        name: category
        description: 'List of Integers: the ids of the category of the group'
        type: string
      - in: query
        name: chapters
        description: 'List of Integer: the chapter ids that may belong to the organization'
        type: string
      - in: query
        name: chapter_urlname
        description: 'List of String: the urlnames of chapters that may belong to
          the organization'
        type: string
      - in: query
        name: country
        description: 'String: Country'
        type: string
      - in: query
        name: desc
        description: 'List of Boolean: whether to sort ascending or decending on each
          attributes in `order`'
        type: string
      - in: query
        name: excluded_chapters
        description: 'List of Integer: the chapters to exclude from the result'
        type: string
      - in: query
        name: founded_date_max
        description: 'Milliseconds since epoch: Maximum range of the founded dates
          of the groups'
        type: string
      - in: query
        name: founded_date_min
        description: 'Milliseconds since epoch: Minumum range of the founded dates
          of the groups'
        type: string
      - in: query
        name: inactive_within_days
        description: 'Positive Integer: including only those groups that did not have
          event in the last specified days'
        type: string
      - in: query
        name: last_event_max
        description: 'Milliseconds since epoch: Maximum range of the date that the
          last meetup happened'
        type: string
      - in: query
        name: last_event_min
        description: 'Milliseconds since epoch: Minumum range of the date that the
          last meetup happened'
        type: string
      - in: query
        name: lat
        description: 'Float: Latitude'
        type: string
      - in: query
        name: location
        description: 'String: Raw location'
        type: string
      - in: query
        name: lon
        description: 'Float: Longitude'
        type: string
      - in: query
        name: member_count_max
        description: 'Positive Integer: Maximum range of the number of members'
        type: string
      - in: query
        name: member_count_min
        description: 'Positive Integer: Minimum range of the number of members'
        type: string
      - in: query
        name: name
        description: 'String: Name of the group looking for'
        type: string
      - in: query
        name: next_event_max
        description: 'Milliseconds since epoch: Maximum range of the date that the
          next meetup is scheduled'
        type: string
      - in: query
        name: next_event_min
        description: 'Milliseconds since epoch: Minumum range of the date that the
          next meetup is scheduled'
        type: string
      - in: query
        name: offset
        description: 'Positive Integer: the page offset'
        type: string
      - in: query
        name: order
        description: 'List of String: attributes to sort on'
        type: string
      - in: query
        name: page
        description: 'Positive Integer: the size of page window'
        type: string
      - in: query
        name: past_events_max
        description: 'Positive Integer: Maximum range of the number of the past events
          held'
        type: string
      - in: query
        name: past_events_min
        description: 'Positive Integer: Minumum range of the number of the past events
          held'
        type: string
      - in: query
        name: past_rsvps_max
        description: 'Positive Integer: Maximum range of the total number of past
          RSVPs'
        type: string
      - in: query
        name: past_rsvps_min
        description: 'Positive Integer: Minumum range of the total number of past
          RSVPs'
        type: string
      - in: query
        name: pro_join_date_max
        description: 'Milliseconds since epoch: Maximum range of the dates the groups
          joined Pro organization'
        type: string
      - in: query
        name: pro_join_date_min
        description: 'Milliseconds since epoch: Minumum range of the dates the groups
          joined Pro organization'
        type: string
      - in: query
        name: query
        description: 'String: raw query to search from group name, description, leadership
          member name, or city'
        type: string
      - in: query
        name: radius
        description: 'String: `global`, `smart`, or search radius in Float'
        type: string
      - in: query
        name: repeat_rsvpers_max
        description: 'Positive Integer: Maximum range of the average number of repeat
          rsvpers'
        type: string
      - in: query
        name: repeat_rsvpers_min
        description: 'Positive Integer: Minumum range of the average number of repeat
          rsvpers'
        type: string
      - in: query
        name: rsvps_per_event_max
        description: 'Positive Integer: Maximum range of the average number of RSVPs
          per event'
        type: string
      - in: query
        name: rsvps_per_event_min
        description: 'Positive Integer: Minumum range of the average number of RSVPs
          per event'
        type: string
      - in: query
        name: topics
        description: 'List of Integers: the ids of topic of the group'
        type: string
      - in: query
        name: upcoming_events_max
        description: 'Positive Integer: Maximum range of the number of the upcoming
          events'
        type: string
      - in: query
        name: upcoming_events_min
        description: 'Positive Integer: Minumum range of the number of the upcoming
          events'
        type: string
      - in: query
        name: zip
        description: 'String: Zip code'
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - groups
definitions: []
x-collection-name: Meetup
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