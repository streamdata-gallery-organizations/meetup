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
  /:urlname/events/:id:
    patch:
      summary: Update Event
      description: Updates an existing Meetup group event's details
      operationId: events
      parameters:
      - in: query
        name: announce
        description: Boolean value indicating whether or not Meetup should announce
          this event to group members
        type: string
      - in: query
        name: description
        description: String setting the description of the event, in simple HTML format
        type: string
      - in: query
        name: duration
        description: Positive long representing event duration in milliseconds
        type: string
      - in: query
        name: event_hosts
        description: String containing up to 5 comma-separated valid member ids for
          members who will be hosts of the event
        type: string
      - in: query
        name: featured_photo_id
        description: Positive integer representing a numeric identifier for a photo,
          which must be one associated with this group
        type: string
      - in: query
        name: guest_limit
        description: Positive integer representing the number of guests that members
          may include in their RSVP, 0 inclusive
        type: string
      - in: query
        name: how_to_find_us
        description: String setting the description for the location of the host(s)
          at the event venue
        type: string
      - in: query
        name: lat
        description: Float representing adjusted venue latitude
        type: string
      - in: query
        name: lon
        description: Float representing adjusted venue longitude
        type: string
      - in: query
        name: name
        description: String setting the name of the event
        type: string
      - in: query
        name: publish_status
        description: String indicating whether an event will be published to the group
          or as a draft visible only to the leadership team
        type: string
      - in: query
        name: question
        description: String setting or replacing the RSVP survey question for the
          event
        type: string
      - in: query
        name: rsvp_close_time
        description: Positive long representing the time before which members will
          be allowed to RSVP to the event in milliseconds since the epoch
        type: string
      - in: query
        name: rsvp_limit
        description: Positive integer representing total number of RSVP slots available
          for the event
        type: string
      - in: query
        name: rsvp_open_time
        description: Positive long representing the time after which members will
          be allowed to RSVP to the event in milliseconds since the epoch
        type: string
      - in: query
        name: time
        description: Positive long representing event start time in milliseconds since
          the epoch
        type: string
      - in: query
        name: venue_id
        description: Positive integer representing a numeric identifier for a venue
        type: string
      - in: query
        name: venue_visibility
        description: String indicating whether the event venue and host location description
          will be visible to non-members of the hosting group
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