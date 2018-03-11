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
  /2/profiles:
    get:
      summary: Profiles
      description: This method returns member *profiles* associated with a particular
        group
      operationId: profiles
      parameters:
      - in: query
        name: '*group_id'
        description: Return profiles in the group with this ID
        type: string
      - in: query
        name: '*group_urlname'
        description: Return profiles for the group with the given custom URL path
        type: string
      - in: query
        name: '*member_id'
        description: Return the profiles for members with these IDs, separated by
          commas
        type: string
      - in: query
        name: '*topic, groupnum'
        description: Group identification by topic, deprecated
        type: string
      - in: query
        name: fields
        description: comma delimited list of optional response properties
        type: string
      - in: query
        name: role
        description: if "leads", only profiles for members of the leadership team
          are included
        type: string
      - in: query
        name: status
        description: Status filter for members
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - profile
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