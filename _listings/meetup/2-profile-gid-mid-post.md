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
  /2/profile/:gid/:mid:
    post:
      summary: Profile Edit
      description: Update a member's group profile
      operationId: profiles
      parameters:
      - in: query
        name: add_role
        description: 'Allows those with permission to assign one of the following
          roles: coorganizer, event_organizer, assistant_organizer'
        type: string
      - in: query
        name: answer_{qid}
        description: Answers to questions from groups API join_info question fields
        type: string
      - in: query
        name: intro
        description: Provides a Member an opportunity to tell the group about themselves
        type: string
      - in: query
        name: new_photo
        description: file upload for a new member photo
        type: string
      - in: query
        name: photo_id
        description: photo_id of the photo to use for this profile
        type: string
      - in: query
        name: remove_role
        description: 'Allows those with permission to remove one of the following
          roles: coorganizer, event_organizer, assistant_organizer'
        type: string
      - in: query
        name: site_name
        description: Name of member's site
        type: string
      - in: query
        name: site_url
        description: Link to member's site
        type: string
      - in: query
        name: title
        description: An organizer-defined member title
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