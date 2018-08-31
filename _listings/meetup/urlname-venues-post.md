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
  /:urlname/venues:
    post:
      summary: Venue Create
      description: Interface for creating new Meetup venues
      operationId: venues
      parameters:
      - in: query
        name: '*address_1'
        description: Primary address of the venue
        type: string
      - in: query
        name: '*city'
        description: City name of the venue
        type: string
      - in: query
        name: '*country'
        description: 2 character country code of the venue
        type: string
      - in: query
        name: '*name'
        description: Unique name of the venue
        type: string
      - in: query
        name: '*state'
        description: If in the US or CA, the state code for the venue
        type: string
      - in: query
        name: address_2
        description: Secondary address info
        type: string
      - in: query
        name: fields
        description: Comma-delimited list of optional fields to append to the response
        type: string
      - in: query
        name: hours
        description: Open hours information about the venue
        type: string
      - in: query
        name: phone
        description: Optional phone number for the venue
        type: string
      - in: query
        name: visibility
        description: Optional value indicating the venues visibility to others
        type: string
      - in: query
        name: web_url
        description: Optional web url for the venue
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - photos
      - veues
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