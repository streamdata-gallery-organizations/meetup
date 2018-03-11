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
  /:urlname/member/approvals:
    delete:
      summary: Membership Decline
      description: Declines one or more requests for group membership
      operationId: profiles
      parameters:
      - in: query
        name: anon
        description: Optional Boolean value indicating whether the declining member's
          email address should be hidden in the resulting response
        type: string
      - in: query
        name: ban
        description: Optional Boolean value indicating whether or not to ban the member
          in the future
        type: string
      - in: query
        name: explanation
        description: Optional explanation to send to the members being declined
        type: string
      - in: query
        name: member
        description: Comma-delimited numeric pending member IDs
        type: string
      - in: query
        name: send_copy
        description: Optional Boolean value indicating whether or not to send a copy
          to the member issuing the decline
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - members
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