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
  /find/topics:
    get:
      summary: Find Topics
      description: Find topics by name
      operationId: topics
      parameters:
      - in: query
        name: '*query'
        description: The text to topic text search for
        type: string
      - in: query
        name: page
        description: Number of results to return in a single set of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - search
      - topics
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