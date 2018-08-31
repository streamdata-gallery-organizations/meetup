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
  /events:
    get:
      summary: Events
      description: Deprecated API method for accessing meetup events
      operationId: deprecated
      parameters:
      - in: query
        name: '*group_id'
        description: Return events from groups with the specified IDs, separated by
          commas
        type: string
      - in: query
        name: '*group_urlname'
        description: Return events for the group with this custom URL path
        type: string
      - in: query
        name: '*id'
        description: Return events with the specified IDs, separated by commas
        type: string
      - in: query
        name: '*member_id'
        description: A member id number, limits results set to events in groups that
          the member specified by this id is currently a member of (excludes private
          groups, unless the member_id is the same as that of the member making the
          request)
        type: string
      - in: query
        name: '*topic'
        description: Return events in the specified topic(s), one topic allowed
        type: string
      - in: query
        name: '*topic, groupnum'
        description: Return events for the group with given topic and number
        type: string
      - in: query
        name: after
        description: Return events that start after the specified date, formatted
          as either a relative date such as "-1w" for one week ago or by absolute
          time in milliseconds since the epoch
        type: string
      - in: query
        name: before
        description: Return events that started before the specified date, formatted
          as described by the "after" parameter
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: rsvp_limit
        description: The number of "yes" rsvps an event can have before members will
          be added to the waiting list
        type: string
      - in: query
        name: status
        description: Return events matching one of the given status values, separated
          by commas
        type: string
      - in: query
        name: text_format
        description: Format of the description text, "html", "plain", or "simplehtml"
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
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