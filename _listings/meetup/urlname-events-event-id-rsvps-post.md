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
  /:urlname/events/:event_id/rsvps:
    post:
      summary: RSVP Create and Update
      description: Creates or updates an existing RSVP
      operationId: rsvps
      parameters:
      - in: query
        name: '*response'
        description: The authenticated Member's RSVP response
        type: string
      - in: query
        name: agree_to_refund
        description: A boolean indicator used for Events with ticketing feeds to imply
          the Member has agreed to the Event's refund policy
        type: string
      - in: query
        name: answer_{qid}
        description: Answers to Event survey questions
        type: string
      - in: query
        name: guests
        description: The number of guests Member will be attending with
        type: string
      - in: query
        name: opt_to_pay
        description: A boolean indicator used for Events with ticketing fees to imply
          the Member has opted to pay as part of the RSVP request
        type: string
      - in: query
        name: pro_email_share_optin
        description: The authenticated Member's email opt in status
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - rsvp
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