---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 0
info:
  title: Meetup Topic Categories
  description: Returns a list of Meetup topic categories
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
  /2/categories:
    get:
      summary: Categories
      description: Returns a list of Meetup group categories
      operationId: categories
      x-api-path-slug: 2categories-get
      parameters:
      - in: query
        name: fields
        description: Parameter for requesting optional response properties
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Categories
  /dashboard:
    get:
      summary: Dashboard
      description: A dashboard of aggregated Meetup information for the authorized
        member
      operationId: dashboard
      x-api-path-slug: dashboard-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Dashboard
  /2/topic_categories:
    get:
      summary: Topic Categories
      description: Returns a list of Meetup topic categories
      operationId: topics
      x-api-path-slug: 2topic-categories-get
      parameters:
      - in: query
        name: fields
        description: Parameter for requesting optional response properties
        type: string
      - in: query
        name: lat,lon,radius
        description: Use a given lat/lon/radius (miles) to search best_topics for
          instead of using the members lat/lon
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Categories
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