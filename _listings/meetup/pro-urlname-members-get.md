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
  /pro/:urlname/members:
    get:
      summary: Search Pro Members
      description: Name, location, and time based search for the members of the meetups
        belonging to Pro organization
      operationId: pro
      parameters:
      - in: query
        name: active_within_days
        description: 'Positive Integer: The range of date from the past until today,
          for the recent activity'
        type: string
      - in: query
        name: chapters
        description: 'List of Integers: The chapters which the member belongs to'
        type: string
      - in: query
        name: country
        description: 'String: Country'
        type: string
      - in: query
        name: desc
        description: 'Boolean: whether to sort ascending or decending'
        type: string
      - in: query
        name: email_received
        description: 'Integers: The id of a previous emails that the member received'
        type: string
      - in: query
        name: events_attended_max
        description: 'Positive Integer: Maximum number of attended events'
        type: string
      - in: query
        name: events_attended_min
        description: 'Positive Integer: Minimum number of attended events'
        type: string
      - in: query
        name: is_organizer
        description: 'Boolean: To limit to only organizers or non-organizers'
        type: string
      - in: query
        name: join_time_max
        description: 'Milliseconds since epoch: The latest time limit for member join'
        type: string
      - in: query
        name: join_time_min
        description: 'Milliseconds since epoch: The oldest time limit for member join'
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
        name: member_name
        description: 'String: Name of the member'
        type: string
      - in: query
        name: offset
        description: 'Positive Integer: the page offset'
        type: string
      - in: query
        name: order
        description: 'String: attribute to sort on'
        type: string
      - in: query
        name: page
        description: 'Positive Integer: the size of page window'
        type: string
      - in: query
        name: query
        description: 'String: raw query string to search from member name or city'
        type: string
      - in: query
        name: radius
        description: 'String: `global`, `smart`, or search radius in Float'
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