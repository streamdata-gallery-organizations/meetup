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
  /:urlname/photo_albums/:album_id/photos:
    post:
      summary: Album Photo Upload
      description: Support for uploading new Album photos
      operationId: photos
      parameters:
      - in: query
        name: '*photo'
        description: Photo upload data, encoded as multipart/form-data
        type: string
      - in: query
        name: await
        description: Optional boolean parameter that will defer a request's a response
          until confirmation that photo is immediately displayable is received
        type: string
      - in: query
        name: caption
        description: Caption for display
        type: string
      - in: query
        name: fields
        description: A comma-delimited list of optional response fields
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