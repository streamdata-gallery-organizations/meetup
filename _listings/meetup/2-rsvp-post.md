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
  /2/rsvp:
    post:
      summary: RSVP Create/Update
      description: Creates or updates an existing RSVP
      operationId: rsvps
      parameters:
      - in: query
        name: '*event_id'
        description: The event that you are RSVP'ing to
        type: string
      - in: query
        name: '*rsvp'
        description: The RSVP setting - value must be either "yes", "no" or "waitlist"
        type: string
      - in: query
        name: agree_to_refund
        description: For events with fees, the authorized member must agree to the
          event's refund policy
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
        name: guests
        description: Number of guests also coming to the event
        type: string
      - in: query
        name: member_id
        description: ' Organizers and event hosts may RSVP on behalf of a member by
          specifying an ID here'
        type: string
      - in: query
        name: opt_to_pay
        description: For events with fees, the authorized member may opt to pay as
          part of the RSVP request
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