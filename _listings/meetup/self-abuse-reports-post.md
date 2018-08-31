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
  /self/abuse_reports:
    post:
      summary: Report Abuse
      description: Submits a new abuse report for a target member
      operationId: abuse
      parameters:
      - in: query
        name: '*type'
        description: A required identifier for type of abuse you are reporting
        type: string
      - in: query
        name: comments
        description: An optional string of text that describes why you are submitting
          this report
        type: string
      - in: query
        name: content_tag
        description: An optional identifier for flagged content that identifies both
          the type and id, where possible, of the content reported
        type: string
      - in: query
        name: member_id
        description: A numeric identifier for the member being reported
        type: string
      - in: query
        name: url
        description: An optional URL for the location of the reported content if one
          exists
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - abuse
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