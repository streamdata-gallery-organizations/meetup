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
  /:urlname/members/:member_id:
    patch:
      summary: Edit Group Member Profile
      description: Edits Group Profiles
      operationId: profiles
      parameters:
      - in: query
        name: add_role
        description: |-
          Allows those with permission to assign one of the following roles:
          "assistant_organizer", "coorganizer", or "event_organizer"
        type: string
      - in: query
        name: answer_{qid}
        description: Answers to questions from group's API join_info question fields
        type: string
      - in: query
        name: fields
        description: A comma-delimited string of optional response field names
        type: string
      - in: query
        name: intro
        description: |-
          Provides a Member an opportunity to tell the group about themselves,
          in at most 255 characters
        type: string
      - in: query
        name: photo_id
        description: Numeric id of the photo to use for this profile
        type: string
      - in: query
        name: remove_role
        description: |-
          Allows those with permission to remove one of the following roles:
          "assistant_organizer", "coorganizer", or "event_organizer"
        type: string
      - in: query
        name: title
        description: |-
          An organizer-defined title,
          in at most 255 characters
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