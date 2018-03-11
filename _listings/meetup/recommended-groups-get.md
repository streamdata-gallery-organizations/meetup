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
  /recommended/groups:
    get:
      summary: Recommended Groups
      description: Returns groups Meetup finds relevant to you
      operationId: groups
      parameters:
      - in: query
        name: category
        description: A valid category id which limits recommended groups to a particular
          category
        type: string
      - in: query
        name: country
        description: A valid two character country code, defaults to US
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: instant_join_only
        description: Recommend only groups without join requirements and that can
          be joined instantly
        type: string
      - in: query
        name: lat
        description: Approximate latitude
        type: string
      - in: query
        name: location
        description: Raw text location query
        type: string
      - in: query
        name: lon
        description: Approximate longitude
        type: string
      - in: query
        name: radius
        description: Radius in miles
        type: string
      - in: query
        name: sort
        description: How to order the results
        type: string
      - in: query
        name: topic_id
        description: Comma delimited list of up to 100 topic ids to help inform recommendations
        type: string
      - in: query
        name: zip
        description: Zip code you are searching for recommendations in
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - recomendations
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