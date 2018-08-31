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
  /2/groups:
    get:
      summary: Groups
      description: Fetch information about Meetup Groups
      operationId: groups
      parameters:
      - in: query
        name: '*category_id'
        description: Only return groups in the specified category
        type: string
      - in: query
        name: '*country, city, state'
        description: A valid country code, city and for the US, State
        type: string
      - in: query
        name: '*domain'
        description: one or more custom group domains, separated by commas
        type: string
      - in: query
        name: '*group_id'
        description: one or more separated by commas
        type: string
      - in: query
        name: '*group_urlname'
        description: one or more separated by commas, includes no slashes
        type: string
      - in: query
        name: '*lat,lon'
        description: A valid latitude and longitude, limits the returned groups to
          those within radius miles
        type: string
      - in: query
        name: '*member_id'
        description: one or more separated by commas, for groups this member belongs
          to
        type: string
      - in: query
        name: '*organizer_id'
        description: one or more organizer IDs, separated by commas
        type: string
      - in: query
        name: '*topic'
        description: Only return groups in the specified topic [one topic allowed]
        type: string
      - in: query
        name: '*topic, groupnum'
        description: Return the group with this topic and number
        type: string
      - in: query
        name: '*zip'
        description: A valid US zip code, limits the returned groups to those within
          radius miles
        type: string
      - in: query
        name: fields
        description: optional result fields, separated by commas
        type: string
      - in: query
        name: radius
        description: Radius, in miles for geographic requests, default 25 -- maximum
          100
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