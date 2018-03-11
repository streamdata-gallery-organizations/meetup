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
  /self/events:
    get:
      summary: Member Events
      description: |-
        Gets a listing of all scheduled Meetup Events the authenticated member has RSVP'd to
        that have been announced to the group
      operationId: events
      parameters:
      - in: query
        name: desc
        description: When true, sorts results in descending order
        type: string
      - in: query
        name: fields
        description: A comma-delimited list of optional fields names which may be
          appended to the response
        type: string
      - in: query
        name: page
        description: Number of results to return
        type: string
      - in: query
        name: rsvp
        description: Comma-delimited list of RSVP responses
        type: string
      - in: query
        name: scroll
        description: A string representing an alias for a point on a timeline
        type: string
      - in: query
        name: status
        description: Comma-delimited list of event statuses
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - members
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