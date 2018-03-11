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
  /groups:
    get:
      summary: Groups
      description: API method for accessing meetup groups
      operationId: deprecated
      parameters:
      - in: query
        name: '*country, city, state'
        description: A valid country code, city and for the US, State
        type: string
      - in: query
        name: '*group_urlname'
        description: Return the group with this custom url path (e
        type: string
      - in: query
        name: '*id'
        description: Only return groups with the specified ID's [separate ID numbers
          with commas]
        type: string
      - in: query
        name: '*lat,lon'
        description: A valid latitude and longitude, limits the returned groups to
          those within radius miles
        type: string
      - in: query
        name: '*member_id'
        description: A member id number, limits results set to only those groups that
          the member specified by this id is currently a member of (excludes private
          groups, unless the member_id is the same as that of the member making the
          request)
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
        description: Set to "short_link" to include shortened group URLs in response
          items
        type: string
      - in: query
        name: radius
        description: Radius, in miles for geographic requests, default 25 -- maximum
          100
        type: string
      - in: query
        name: visibility
        description: Set to "members" or "public" to restrict to groups of a particular
          visibility
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