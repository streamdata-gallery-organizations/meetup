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
  /recommended/venues:
    get:
      summary: Recommended Venues
      description: Returns venues Meetup finds relevant to you based on location and
        category
      operationId: venues
      parameters:
      - in: query
        name: category
        description: Comma-delimited list of up to 200 category ids to help inform
          recommendations
        type: string
      - in: query
        name: country
        description: A valid two character country code, defaults to US
        type: string
      - in: query
        name: group_id
        description: Comma-delimited list of up to 200 group ids to help inform recommendations
        type: string
      - in: query
        name: group_urlname
        description: Comma-delimited list of up to 200 group urlnames to help inform
          recommendations
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
        name: min_groups
        description: The minimum number of groups that have hosted events at this
          venue
        type: string
      - in: query
        name: radius
        description: Radius in miles
        type: string
      - in: query
        name: used_between
        description: Return venues that have been used within the given time range,
          defined by two times separated with a single comma
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
      - venues
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