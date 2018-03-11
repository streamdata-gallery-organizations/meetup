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
  /2/event/:id:
    post:
      summary: Event Edit
      description: Update an existing Meetup
      operationId: events
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
        description: The information provided by the event host for "How will members
          find you there?"
        type: string
      - in: query
        name: lat,lon
        description: Updates to the venue's latitude and longitude
        type: string
      - in: query
        name: name
        description: Event name
        type: string
      - in: query
        name: publish_status
        description: If you are an organizer of the group, you may set this to "draft"
          or "published"
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