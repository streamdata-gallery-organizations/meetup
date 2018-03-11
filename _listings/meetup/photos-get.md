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
  /photos:
    get:
      summary: Photos
      description: API method for accessing meetup photos
      operationId: deprecated
      parameters:
      - in: query
        name: '*album_id'
        description: return photos for the albums with the given id, separated by
          commas
        type: string
      - in: query
        name: '*group_id'
        description: Return photos in groups with these ID numbers [separated by commas]
        type: string
      - in: query
        name: '*group_urlname'
        description: return photos for the group with given custom URL path
        type: string
      - in: query
        name: '*topic'
        description: Return photos in this topic
        type: string
      - in: query
        name: '*topic, groupnum'
        description: return photos for the group with given topic and number
        type: string
      - in: query
        name: '*topic_id'
        description: Return photos in topics with this ID number
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - photos
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