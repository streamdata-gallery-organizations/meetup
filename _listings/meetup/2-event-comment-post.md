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
  /2/event_comment:
    post:
      summary: Event Comment v2
      description: This method posts messages that appear under Talk about this Meetup
      operationId: events
      parameters:
      - in: query
        name: '*comment'
        description: The comment text
        type: string
      - in: query
        name: '*event_id'
        description: The event related to this comment
        type: string
      - in: query
        name: '*in_reply_to'
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
      - events
      - comments
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