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
  /2/event_rating:
    post:
      summary: Event Rating
      description: This method allows members to posts rating for an event after it's
        occurred
      operationId: events
      parameters:
      - in: query
        name: '*event_id'
        description: The ID of the event to fetch ratings data for
        type: string
      - in: query
        name: '*rating'
        description: The member's rating (either 1, 2, 3, 4, or 5)
        type: string
      - in: query
        name: attendee_count
        description: 'DEPRECATED: The number of attendees for the event (organizers/assistant
          organizers/co-organizers/event organizers/event hosts only)'
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - ratings
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