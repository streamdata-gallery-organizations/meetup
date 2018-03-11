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
  /:urlname/members:
    get:
      summary: Group Profile list
      description: Get a list of Meetup group members
      operationId: profiles
      parameters:
      - in: query
        name: desc
        description: Boolean value controling sort order of results
        type: string
      - in: query
        name: fields
        description: A comma-delimited list of optional fields to append to the response
        type: string
      - in: query
        name: filter
        description: May be set to 'stepup_eligible' to return only members eligible
          to step up as organizer
        type: string
      - in: query
        name: order
        description: Orders results according to definitions listed below
        type: string
      - in: query
        name: page
        description: Number of requested members to return
        type: string
      - in: query
        name: role
        description: May be set to "leads" to filter returned members on the lead
          team
        type: string
      - in: query
        name: status
        description: A comma-delimited list of member statuses
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