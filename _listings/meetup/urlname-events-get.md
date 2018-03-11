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
  /:urlname/events:
    get:
      summary: Group Events
      description: Gets a listing of all Meetup Events hosted by a target group, in
        ascending order by default
      operationId: events
      parameters:
      - in: query
        name: desc
        description: When true, sorts results in descending order
        type: string
      - in: query
        name: fields
        description: Comma-delimited list of optional fields to append to the response
        type: string
      - in: query
        name: page
        description: Number of results to return in a page
        type: string
      - in: query
        name: scroll
        description: A string representing an alias for a point on a timeline
        type: string
      - in: query
        name: status
        description: A comma-delimited list of event statuses
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