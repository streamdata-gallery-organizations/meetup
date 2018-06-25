---
name: Meetup
x-slug: meetup
description: Find Meetups so you can do more of what matters to you. Or create your
  own group and meet people near you who share your interests.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
x-kinRank: "9"
x-alexaRank: "917"
tags: Meetup
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/apis.md
specificationVersion: "0.14"
apis:
- name: Meetup Categories
  x-api-slug: meetup
  description: Returns a list of Meetup group categories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/categories
  tags: Events,Categories
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2categories-get-openapi.md
- name: Meetup Dashboard
  x-api-slug: meetup
  description: A dashboard of aggregated Meetup information for the authorized member
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////dashboard
  tags: Events,Dashboard
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/dashboard-get-openapi.md
- name: Meetup Topic Categories
  x-api-slug: meetup
  description: Returns a list of Meetup topic categories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/topic_categories
  tags: Events,Categories
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2topic-categories-get-openapi.md
- name: Meetup Topics
  x-api-slug: meetup
  description: API method for accessing meetup topics
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////topics
  tags: Events,Topics
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/topics-get-openapi.md
- name: Meetup Events
  x-api-slug: meetup
  description: Deprecated API method for accessing meetup events. Please see [/2/events](/meetup_api/docs/2/events/)
    and [/2/open_events](/meetup_api/docs/2/open_events/) for replacements.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////events
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/events-get-openapi.md
- name: Meetup OpenEvents
  x-api-slug: meetup
  description: Searches for recent and upcoming public events hosted by Meetup groups.
    Its search window  is the past one month through the next three months, and is
    subject to change. Open Events is optimized to search for current events by location,
    category, topic, or text, and only lists Meetups that have **3 or more RSVPs**.
    The number or results returned with each request is not guaranteed to be the same
    as the page size due to secondary filtering. If you're looking for a particular
    event or events within a particular group, use the standard [Events](/meetup_api/docs/2/events/)
    method.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/open_events
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2open-events-get-openapi.md
- name: Meetup Concierge
  x-api-slug: meetup
  description: Recommends upcoming meetups for the authorized member in a given location
    and in thier groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/concierge
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2concierge-get-openapi.md
- name: Meetup Groups
  x-api-slug: meetup
  description: Fetch information about Meetup Groups.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/groups
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2groups-get-openapi.md
- name: Meetup Events
  x-api-slug: meetup
  description: Access Meetup events using a group, member, or event id. Events in
    private groups are available only to authenticated members of those groups. To
    search events by topic or location, see [Open Events](/meetup_api/docs/2/open_events).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/events
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2events-get-openapi.md
- name: Meetup Event Create
  x-api-slug: meetup
  description: Create a new Meetup event within the system.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-post-openapi.md
- name: Meetup Event Edit
  x-api-slug: meetup
  description: Update an existing Meetup
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2eventid-post-openapi.md
- name: Meetup Event Delete
  x-api-slug: meetup
  description: Deletes a specified meetup
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2eventid-delete-openapi.md
- name: Meetup Photos
  x-api-slug: meetup
  description: API method for accessing meetup photos
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/photos-get-openapi.md
- name: Meetup Cities
  x-api-slug: meetup
  description: API method for accessing meetup cities
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////cities
  tags: Events,Cities
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/cities-get-openapi.md
- name: Meetup Cities
  x-api-slug: meetup
  description: Returns Meetup cities. This method supports search by latitude/longitude/radius,
    by country/state, by query term/zip, or a combination of all of these. Location-only
    searches by lat and lon return all cities within a radius of the provided coordinates.
    Searches with a query return up to 10 cities matching the term, and can be sorted
    by size or distance to a given coordinate. 'smart' ordering can be used to return
    the match(es) with the highest member_count, unless a smaller size match exists
    nearby the given coordinates. Query searches are supported for country but not
    country and state
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/cities
  tags: Events,Cities
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2cities-get-openapi.md
- name: Meetup Members
  x-api-slug: meetup
  description: API method for accessing members of Meetup Groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////members
  tags: Events,Groups,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/members-get-openapi.md
- name: Meetup Members
  x-api-slug: meetup
  description: API method for accessing members of Meetup Groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/members
  tags: Events,Groups,Member
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2members-get-openapi.md
- name: Meetup Member Get
  x-api-slug: meetup
  description: Retrieve a single member
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/member/:id
  tags: Events,Groups,Member
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2memberid-get-openapi.md
- name: Meetup Member Edit
  x-api-slug: meetup
  description: Edit the authorized member's attributes
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/member/:id
  tags: Events,Groups,Member
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2memberid-post-openapi.md
- name: Meetup Profiles
  x-api-slug: meetup
  description: This method returns member *profiles* associated with a particular
    group. Meetup members have separate profiles for each group they join.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/profiles
  tags: Events,Profile
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2profiles-get-openapi.md
- name: Meetup Profile Create (Group Join)
  x-api-slug: meetup
  description: This method allows an authenticated member to join a group by creating
    a profile
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/profile
  tags: Events,Profile
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2profile-post-openapi.md
- name: Meetup Profile Edit
  x-api-slug: meetup
  description: Update a member's group profile
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/profile/:gid/:mid
  tags: Events,Profile
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2profilegidmid-post-openapi.md
- name: Meetup Profile Get
  x-api-slug: meetup
  description: Retrieves a single group profile
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/profile/:gid/:mid
  tags: Events,Profile
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2profilegidmid-get-openapi.md
- name: Meetup Profile Delete (Leave Group)
  x-api-slug: meetup
  description: Deletes a member's group profile
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/profile/:gid/:mid
  tags: Events,Profile
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2profilegidmid-delete-openapi.md
- name: Meetup Event Photo Delete
  x-api-slug: meetup
  description: Deletes a specified event photo
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo/:id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photoid-delete-openapi.md
- name: Meetup Event Photo Edit
  x-api-slug: meetup
  description: Edits a specified event photo
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo/:id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photoid-post-openapi.md
- name: Meetup Member Photo Delete
  x-api-slug: meetup
  description: Delete the specified member photo
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/member_photo/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2member-photoid-delete-openapi.md
- name: Meetup Comments
  x-api-slug: meetup
  description: API method for accessing meetup group comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////comments
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/comments-get-openapi.md
- name: Meetup Comments v2
  x-api-slug: meetup
  description: This method returns messages that appear under Talk about this Meetup.
    To post messages, see the corresponding write method.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comments
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comments-get-openapi.md
- name: Meetup Event Comment v2
  x-api-slug: meetup
  description: This method posts messages that appear under Talk about this Meetup.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-post-openapi.md
- name: Meetup Event Comment Get
  x-api-slug: meetup
  description: Retrieve a single event comment or reply
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment/:id
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-commentid-get-openapi.md
- name: Meetup Event Comment Delete
  x-api-slug: meetup
  description: Delete a single event comment or reply
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment/:id
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-commentid-delete-openapi.md
- name: Meetup Event Comment Flag
  x-api-slug: meetup
  description: This method creates a spam report for comment content
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment_flag
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-flag-post-openapi.md
- name: Meetup Event Comment Unsubscribe
  x-api-slug: meetup
  description: Unsubscribe to notifications for updates to a given comment thread
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment_subscribe/:id
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-subscribeid-delete-openapi.md
- name: Meetup Event Comment Subscribe
  x-api-slug: meetup
  description: Subscribe to notifications on updates to a given comment thread
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment_subscribe/:id
  tags: Events,Ratings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-subscribeid-post-openapi.md
- name: Meetup Event Comment Like
  x-api-slug: meetup
  description: Like a given Event comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment_like/:id
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-likeid-post-openapi.md
- name: Meetup Event Comment Unlike
  x-api-slug: meetup
  description: Unlike a given Event comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment_like/:id
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-likeid-delete-openapi.md
- name: Meetup Comment Likes
  x-api-slug: meetup
  description: Api for listing likes of a given event comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comment_likes
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comment-likes-get-openapi.md
- name: Meetup Photo Comments v2
  x-api-slug: meetup
  description: This method returns comments on meetup photos. To post messages, see
    the corresponding write method
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo_comments
  tags: Events,Profile
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photo-comments-get-openapi.md
- name: Meetup Photo Comment v2
  x-api-slug: meetup
  description: This method posts comments that appear below photos
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo_comment
  tags: Events,Photos,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photo-comment-post-openapi.md
- name: Meetup Ratings v2
  x-api-slug: meetup
  description: API method for accessing Meetup comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_ratings
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-ratings-get-openapi.md
- name: Meetup Event Rating
  x-api-slug: meetup
  description: This method allows members to posts rating for an event after it's
    occurred. Only permitted for members who rsvp'd yes or maybe to the event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_rating
  tags: Events,Ratings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-rating-post-openapi.md
- name: Meetup Photo Albums
  x-api-slug: meetup
  description: This method returns photo albums associated with Meetup groups. To
    create albums, see the corresponding write method.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo_albums
  tags: Events,Photos,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photo-albums-get-openapi.md
- name: Meetup Photos
  x-api-slug: meetup
  description: This method returns photos by member, group, album, event, photo ID,
    or tagged member.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photos-get-openapi.md
- name: Meetup Photo Album2
  x-api-slug: meetup
  description: This method creates photo albums within a Meetup group
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo_album
  tags: Events,Photos,Albums
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photo-album-post-openapi.md
- name: Meetup OpenVenues
  x-api-slug: meetup
  description: Searches for public venues within a given geo space. To search for
    specific venues that your group has used, use the [Venues](/meetup_api/docs/2/venues)
    method
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/open_venues
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2open-venues-get-openapi.md
- name: Meetup Venues
  x-api-slug: meetup
  description: Search for Meetup venues by one of your groups, events, or venue identifiers.
    For a full text search on public venues use [OpenVenues](/meetup_api/docs/2/open_venues).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/venues
  tags: Events,Venues
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2venues-get-openapi.md
- name: Meetup Rsvps
  x-api-slug: meetup
  description: API method for accessing meetup rsvps
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////rsvps
  tags: Events,RSVP
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/rsvps-get-openapi.md
- name: Meetup RSVP
  x-api-slug: meetup
  description: Creates a new Rsvp
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////rsvp
  tags: Events,RSVP
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/rsvp-post-openapi.md
- name: Meetup RSVPs v2
  x-api-slug: meetup
  description: Query for Event RSVPs by event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/rsvps
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2rsvps-get-openapi.md
- name: Meetup RSVP Create/Update
  x-api-slug: meetup
  description: Creates or updates an existing RSVP
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/rsvp
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2rsvp-post-openapi.md
- name: Meetup RSVP Get
  x-api-slug: meetup
  description: Retrieve a single RSVP
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/rsvp/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2rsvpid-get-openapi.md
- name: Meetup Group Photo Upload
  x-api-slug: meetup
  description: Uploads a new Meetup Group photo. To change other Group settings use
    the [Group Edit](/meetup_api/docs/:urlname/#edit) endpoint
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/group_photo
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2group-photo-post-openapi.md
- name: Meetup Member Photo Upload
  x-api-slug: meetup
  description: Uploads a photo to be associated with a Member
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/member_photo
  tags: Events,Groups,Member
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2member-photo-post-openapi.md
- name: Meetup Event Photo Upload
  x-api-slug: meetup
  description: Uploads a photo for a given event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photo
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photo-post-openapi.md
- name: Meetup Groups
  x-api-slug: meetup
  description: API method for accessing meetup groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////groups
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/groups-get-openapi.md
- name: Meetup ActivityFeed
  x-api-slug: meetup
  description: API method for retrieving the activity feed for a member's groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////activity
  tags: Events,Activity,Feeds
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/activity-get-openapi.md
- name: Meetup oEmbed
  x-api-slug: meetup
  description: oEmbed implementation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////oembed
  tags: Events,oEmbed,Media
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/oembed-get-openapi.md
- name: Meetup WebSockets RSVP Stream
  x-api-slug: meetup
  description: |-
    For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
    efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
    any messages received from the client after the socket is open.

    Because browser support for WebSockets is limited, we recommend that you consume this stream
    through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/rsvps
  tags: Events,Streaming,Websockets
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2rsvps-ws-openapi.md
- name: Meetup WebSocket Photo Stream
  x-api-slug: meetup
  description: |-
    For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
    efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
    any messages received from the client after the socket is open.

    Because browser support for WebSockets is limited, we recommend that you consume this stream
    through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/photos
  tags: Events,Photos,Albums
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2photos-ws-openapi.md
- name: Meetup WebSockets Event Comments Stream
  x-api-slug: meetup
  description: |-
    For browsers that support it, [WebSockets](http://dev.w3.org/html5/websockets/) is a more
    efficient alternative to the long-polling stream. This is a **push only** endpoint and will discard
    any messages received from the client after the socket is open.

    Because browser support for WebSockets is limited, we recommend that you consume this stream
    through the [must.js](https://github.com/meetup/must.js#readme) client, which can fallback to long-polling.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////2/event_comments
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/2event-comments-ws-openapi.md
- name: Meetup API Status
  x-api-slug: meetup
  description: Returns the current API service status
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////status
  tags: Events,Status
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/status-get-openapi.md
- name: Meetup Block status
  x-api-slug: meetup
  description: Checks the block status for a target member relative to the authenticated
    member
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/blocks/:member_id
  tags: Events,Abuse,Status
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfblocksmember-id-get-openapi.md
- name: Meetup Block member
  x-api-slug: meetup
  description: Blocks a target member from various interactions with the authenticated
    member on the platform
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/blocks/:member_id
  tags: Events,Abuse,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfblocksmember-id-post-openapi.md
- name: Meetup Report Abuse
  x-api-slug: meetup
  description: Submits a new abuse report for a target member. Abuse reports will
    be followed up on by our Community Support team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/abuse_reports
  tags: Events,Abuse
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfabuse-reports-post-openapi.md
- name: Meetup Report Group
  x-api-slug: meetup
  description: Submits a new abuse report for a target group. Abuse reports will be
    followed up on by our Community Support team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/abuse_reports
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameabuse-reports-post-openapi.md
- name: Meetup Unblock member
  x-api-slug: meetup
  description: Unblocks a previously blocked member from various interactions with
    the authenticated member on the platform
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/blocks/:member_id
  tags: Events,Abuse,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfblocksmember-id-delete-openapi.md
- name: Meetup Membership Approval
  x-api-slug: meetup
  description: Approves one or more requests for group membership
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/member/approvals
  tags: Events,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamememberapprovals-post-openapi.md
- name: Meetup Attendance
  x-api-slug: meetup
  description: Lists attendance records for Meetup events. Limited for use by administrative
    members.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:id/attendance
  tags: Events,Attendance
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsidattendance-get-openapi.md
- name: Meetup Attendance Taking
  x-api-slug: meetup
  description: Takes member attendance for an event. Limited for use by administrative
    members.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:id/attendance
  tags: Events,Attendance
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsidattendance-post-openapi.md
- name: Meetup batch
  x-api-slug: meetup
  description: Performs multiple API requests in batch, useful for reducing HTTP network
    requests. This method is only available for OAuth authentication
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////batch
  tags: Events,Batch
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/batch-post-openapi.md
- name: Meetup Discussion Boards
  x-api-slug: meetup
  description: Listings of Group discussion boards
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/boards
  tags: Events,Discussions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameboards-get-openapi.md
- name: Meetup Group Venues
  x-api-slug: meetup
  description: Returns venues a group has previously hosted events at
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/venues
  tags: Events,Photos,Veues
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamevenues-get-openapi.md
- name: Meetup Venue Create
  x-api-slug: meetup
  description: Interface for creating new Meetup venues
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/venues
  tags: Events,Photos,Veues
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamevenues-post-openapi.md
- name: Meetup Membership Decline
  x-api-slug: meetup
  description: Declines one or more requests for group membership
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/member/approvals
  tags: Events,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamememberapprovals-delete-openapi.md
- name: Meetup Discussions
  x-api-slug: meetup
  description: Listings of group discussions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/boards/:bid/discussions
  tags: Events,Discussions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameboardsbiddiscussions-get-openapi.md
- name: Meetup Discussion Posts
  x-api-slug: meetup
  description: Listing Group discussion posts
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/boards/:bid/discussions/:did
  tags: Events,Discussions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameboardsbiddiscussionsdid-get-openapi.md
- name: Meetup Member Events
  x-api-slug: meetup
  description: |-
    Gets a listing of all scheduled Meetup Events the authenticated member has RSVP'd to
    that have been announced to the group.
    This listing is ordered from oldest to most recent by default
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/events
  tags: Events,Members
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfevents-get-openapi.md
- name: Meetup Create Event
  x-api-slug: meetup
  description: Creates a new Meetup group event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameevents-post-openapi.md
- name: Meetup Update Event
  x-api-slug: meetup
  description: Updates an existing Meetup group event's details
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsid-patch-openapi.md
- name: Meetup Event Delete
  x-api-slug: meetup
  description: Cancels or removes an event from a groups calendar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsid-delete-openapi.md
- name: Meetup Open Rsvps
  x-api-slug: meetup
  description: Opens rsvps for an event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/rsvps/open
  tags: Events,RSVP
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idrsvpsopen-post-openapi.md
- name: Meetup Close Rsvps
  x-api-slug: meetup
  description: Closes rsvps for an event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/rsvps/close
  tags: Events,RSVP
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idrsvpsclose-post-openapi.md
- name: Meetup Event Hosts
  x-api-slug: meetup
  description: Returns the list of hosts for a given event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/hosts
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idhosts-get-openapi.md
- name: Meetup Event Comments List
  x-api-slug: meetup
  description: |-
    Lists the comments and replies posted in a given Meetup Event.

    To view the list of likes for a comment or reply
    see the [likes](/meetup_api/docs/:urlname/events/:event_id/comments/:comment_id/likes/)
    endpoint
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/comments
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idcomments-get-openapi.md
- name: Meetup Event comment and reply
  x-api-slug: meetup
  description: Creates new comments and replies to existing comments within an Meetup
    event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/comments
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idcomments-post-openapi.md
- name: Meetup Event comment delete
  x-api-slug: meetup
  description: Deletes comments posted in events
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/comments/:comment_id
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idcommentscomment-id-delete-openapi.md
- name: Meetup Get Event
  x-api-slug: meetup
  description: Fetches a Meetup Event by group urlname and event_id
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:id
  tags: Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsid-get-openapi.md
- name: Meetup Event Payments
  x-api-slug: meetup
  description: Allows organizers of a group to note payments made by members for an
    event. This is the 'Mark Paid' feature seen in the RSVP listings on event details
    pages and affects the 'pay_status' response fields in [2/rsvps](/meetup_api/docs/2/rsvps/#response)
    for paid events
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:id/payments
  tags: Events,Payments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsidpayments-post-openapi.md
- name: Meetup Album Photos
  x-api-slug: meetup
  description: Lists photos for a given photo album
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/photo_albums/:album_id/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamephoto-albumsalbum-idphotos-get-openapi.md
- name: Meetup Album Photo Upload
  x-api-slug: meetup
  description: Support for uploading new Album photos
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/photo_albums/:album_id/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamephoto-albumsalbum-idphotos-post-openapi.md
- name: Meetup Event Photos
  x-api-slug: meetup
  description: Lists photos for a given event
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotos-get-openapi.md
- name: Meetup Event Photo
  x-api-slug: meetup
  description: Gets information about a specific photo
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos/:photo_id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotosphoto-id-get-openapi.md
- name: Meetup Event Photo Edit
  x-api-slug: meetup
  description: Edits photo details
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos/:photo_id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotosphoto-id-patch-openapi.md
- name: Meetup Event Photo Delete
  x-api-slug: meetup
  description: Deletes a specified event photo
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos/:photo_id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotosphoto-id-delete-openapi.md
- name: Meetup Event Photo Upload
  x-api-slug: meetup
  description: Support for uploading new Event photos
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotos-post-openapi.md
- name: Meetup Find Events
  x-api-slug: meetup
  description: Returns list of upcoming events based on location
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/events
  tags: Events,Search
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findevents-get-openapi.md
- name: Meetup Find Upcoming Events
  x-api-slug: meetup
  description: Returns a list of upcoming events
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/upcoming_events
  tags: Events,Search
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findupcoming-events-get-openapi.md
- name: Meetup Find Groups
  x-api-slug: meetup
  description: Text, location, category and friend-based group searches
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/groups
  tags: Events,Search,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findgroups-get-openapi.md
- name: Meetup Find Venues
  x-api-slug: meetup
  description: Returns list of venues based on location
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/venues
  tags: Events,Search,Venues
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findvenues-get-openapi.md
- name: Meetup Album Photos
  x-api-slug: meetup
  description: Lists of all photos uploaded for the group
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamephotos-get-openapi.md
- name: Meetup Group Profile list
  x-api-slug: meetup
  description: Get a list of Meetup group members
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/members
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamemembers-get-openapi.md
- name: Meetup Group Profile search
  x-api-slug: meetup
  description: |-
    Find group member profiles by name.
    Member's who very recently joined or left the group may not be immediately searchable
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/:urlname/members
  tags: Events,Groups,Search
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findurlnamemembers-get-openapi.md
- name: Meetup Get Group
  x-api-slug: meetup
  description: Fetches a Meetup group by urlname
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlname-get-openapi.md
- name: Meetup Group Edit
  x-api-slug: meetup
  description: Allows organizers to edit their Meetup group information. To change
    group topics, see the [add](/meetup_api/docs/:urlname/topics/#add) and [remove](/meetup_api/docs/:urlname/topics/#remove)
    topics endpoints. To change group photo use the [Group photo upload](/meetup_api/docs/2/group_photo/#create)
    endpoint. OAuth authenticated requests require an additional [group_edit](/meetup_api/auth/#oauth2-scopes)
    permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlname-post-openapi.md
- name: Meetup Group Topics Add
  x-api-slug: meetup
  description: Associates topics with a given Meetup group. Limited to organizers
    of the group. OAuth authenticated requests require an additional [group_edit](/meetup_api/auth/#oauth2-scopes)
    permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/topics
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnametopics-post-openapi.md
- name: Meetup Group Topics Remove
  x-api-slug: meetup
  description: Disassociates topics with a given Meetup group. Limited to organizers
    of the group. OAuth authenticated requests require an additional [group_edit](/meetup_api/auth/#oauth2-scopes)
    permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/topics
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnametopics-delete-openapi.md
- name: Meetup Find locations
  x-api-slug: meetup
  description: Provides a query interface for finding known locations
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/locations
  tags: Events,Search,Location
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findlocations-get-openapi.md
- name: Meetup Member Calendar
  x-api-slug: meetup
  description: Get a listing of all upcoming Meetup events for the authenticated member
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/calendar
  tags: Events,Members,Calendardars
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfcalendar-get-openapi.md
- name: Meetup Member groups
  x-api-slug: meetup
  description: |-
    Lists the authenticated member's groups in the order of leadership,
    next upcoming event, then alphabetical order by name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////self/groups
  tags: Events,Members,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/selfgroups-get-openapi.md
- name: Meetup Event Comment and Reply Likes
  x-api-slug: meetup
  description: Returns lists of likes for an event comment or reply
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/comments/:comment_id/likes
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idcommentscomment-idlikes-get-openapi.md
- name: Meetup Event Comment Like
  x-api-slug: meetup
  description: Like a given event comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/comments/:comment_id/likes
  tags: Events,Hosts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idcommentscomment-idlikes-post-openapi.md
- name: Meetup Event Comment Unlike
  x-api-slug: meetup
  description: Unlike a given event comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/comments/:comment_id/likes
  tags: Events,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idcommentscomment-idlikes-delete-openapi.md
- name: Meetup Member Photo Delete
  x-api-slug: meetup
  description: Deletes a member photo by id
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////members/:member_id/photos/:photo_id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/membersmember-idphotosphoto-id-delete-openapi.md
- name: Meetup Member Photo Upload
  x-api-slug: meetup
  description: Support for uploading new Member photos
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////members/:member_id/photos
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/membersmember-idphotos-post-openapi.md
- name: Meetup Search Pro Groups
  x-api-slug: meetup
  description: Name and statistics range search for the meetup groups belonging to
    Pro organization.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////pro/:urlname/groups
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/prourlnamegroups-get-openapi.md
- name: Meetup Search Pro Members
  x-api-slug: meetup
  description: Name, location, and time based search for the members of the meetups
    belonging to Pro organization.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////pro/:urlname/members
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/prourlnamemembers-get-openapi.md
- name: Meetup Search Issued Pro Tickets
  x-api-slug: meetup
  description: Redeemed chapter, redeemed member, status, and timestamp for tickets
    belonging to Pro organization.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////pro/:urlname/tickets
  tags: Events,Tickets
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/prourlnametickets-get-openapi.md
- name: Meetup Notifications
  x-api-slug: meetup
  description: Returns all recent Meetup notifications for the authorized member.
    To mark notifications read use [/notifications/read](/meetup_api/docs/notifications/read/)
    endpoint. To get the authenticated Member's current unread count, request it in
    an [HTTP header](/meetup_api/docs/#meta-headers).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////notifications
  tags: Events,Notifications
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/notifications-get-openapi.md
- name: Meetup Read Notifications
  x-api-slug: meetup
  description: Marks groups of [notifications](/meetup_api/docs/notifications/) as
    read.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////notifications/read
  tags: Events,Notifications
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/notificationsread-post-openapi.md
- name: Meetup Clicked Notifications
  x-api-slug: meetup
  description: Marks groups of [notifications](/meetup_api/docs/notifications/) as
    clicked.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////notifications/clicked
  tags: Events,Notifications
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/notificationsclicked-post-openapi.md
- name: Meetup Photo Album
  x-api-slug: meetup
  description: Gets information about a specific photo album
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/photo_albums/:album_id
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamephoto-albumsalbum-id-get-openapi.md
- name: Meetup Photo Album List
  x-api-slug: meetup
  description: Gets a list a group photo albums in ascending order based on the time
    they were created
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/photo_albums
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamephoto-albums-get-openapi.md
- name: Meetup Get Member Profile
  x-api-slug: meetup
  description: |-
    Gets Member Profiles.
    For Group Profiles, see [this endpoint](/meetup_api/docs/:urlname/members/:member_id)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////members/:member_id
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/membersmember-id-get-openapi.md
- name: Meetup Member Profile Edit
  x-api-slug: meetup
  description: Edits Member Profiles.For Group Profiles, see [this endpoint](/meetup_api/docs/:urlname/members/:member_id)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////members/:member_id
  tags: Events,Profiles
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/membersmember-id-patch-openapi.md
- name: Meetup Group Join
  x-api-slug: meetup
  description: This method allows an authenticated member to join a group by creating
    a profile
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/members
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamemembers-post-openapi.md
- name: Meetup Get Group Member Profile
  x-api-slug: meetup
  description: |-
    Gets Group Profiles.
    For Member Profiles, see [this endpoint](/meetup_api/docs/members/:member_id)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/members/:member_id
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamemembersmember-id-get-openapi.md
- name: Meetup Edit Group Member Profile
  x-api-slug: meetup
  description: |-
    Edits Group Profiles.
    To fetch Group Member Profiles,
    see [this endpoint](/meetup_api/docs/:urlname/members/:member_id#get)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/members/:member_id
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamemembersmember-id-patch-openapi.md
- name: Meetup Delete Group Member Profile (Leave Group)
  x-api-slug: meetup
  description: Deletes a member's group profiles.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/members/:member_id
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamemembersmember-id-delete-openapi.md
- name: Meetup Photo Comment
  x-api-slug: meetup
  description: Creates a new photo comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos/:photo_id/comments
  tags: Events,Photos,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotosphoto-idcomments-post-openapi.md
- name: Meetup Photo Comment Delete
  x-api-slug: meetup
  description: Deletes photo comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos/:photo_id/comments/:comment_id
  tags: Events,Photos,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotosphoto-idcommentscomment-id-delete-openapi.md
- name: Meetup Photo Comments
  x-api-slug: meetup
  description: Lists photo comments associated with a photo
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/photos/:photo_id/comments
  tags: Events,Photos,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idphotosphoto-idcomments-get-openapi.md
- name: Meetup RSVP Create and Update
  x-api-slug: meetup
  description: Creates or updates an existing RSVP
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/rsvps
  tags: Events,RSVP
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idrsvps-post-openapi.md
- name: Meetup Event RSVP list
  x-api-slug: meetup
  description: Retrieves list of event RSVPs
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events/:event_id/rsvps
  tags: Events,RSVP
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameeventsevent-idrsvps-get-openapi.md
- name: Meetup Topic Categories
  x-api-slug: meetup
  description: Returns a list high level topic categories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/topic_categories
  tags: Events,Search,Topic Categories
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findtopic-categories-get-openapi.md
- name: Meetup Recommended Events
  x-api-slug: meetup
  description: Returns a list of upcoming recommended events
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////recommended/events
  tags: Events,Recomendations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/recommendedevents-get-openapi.md
- name: Meetup Recommend Group Topics
  x-api-slug: meetup
  description: Recommends suggestions for group topics based on a text search or other
    topics
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////recommended/group_topics
  tags: Events,Recomendations,Groups,Topics
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/recommendedgroup-topics-get-openapi.md
- name: Meetup Recommended Groups
  x-api-slug: meetup
  description: Returns groups Meetup finds relevant to you
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////recommended/groups
  tags: Events,Recomendations,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/recommendedgroups-get-openapi.md
- name: Meetup Recommended Groups Ignore
  x-api-slug: meetup
  description: Provides a form of feedback by requesting to remove a group from future
    recommendations
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////recommended/groups/ignores/:urlname
  tags: Events,Recomendations,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/recommendedgroupsignoresurlname-post-openapi.md
- name: Meetup Recommended Venues
  x-api-slug: meetup
  description: Returns venues Meetup finds relevant to you based on location and category.
    This method does not yet support sorting or pagination.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////recommended/venues
  tags: Events,Recomendations,Venues
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/recommendedvenues-get-openapi.md
- name: Meetup Similar groups
  x-api-slug: meetup
  description: Renders a list of similar groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/similar_groups
  tags: Events,Photos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnamesimilar-groups-get-openapi.md
- name: Meetup Find Topics
  x-api-slug: meetup
  description: Find topics by name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////find/topics
  tags: Events,Search,Topics
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/findtopics-get-openapi.md
- name: Meetup Group Events
  x-api-slug: meetup
  description: Gets a listing of all Meetup Events hosted by a target group, in ascending
    order by default
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com////:urlname/events
  tags: Events,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/urlnameevents-get-openapi.md
- name: Meetup
  x-api-slug: meetup
  description: Find Meetups so you can do more of what matters to you. Or create your
    own group and meet people near you who share your interests.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Meetup
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/meetup/master/_listings/meetup/openapi.md
x-common:
- type: x-base
  url: http://api.meetup.com
- type: x-crunchbase
  url: https://crunchbase.com/organization/meetup
- type: x-developer
  url: http://www.meetup.com/meetup_api/
- type: x-email
  url: privacy@meetup.com
- type: x-email
  url: abuse@meetup.com
- type: x-email
  url: api_license@meetup.com
- type: x-email
  url: arbitration-opt-out@meetup.com
- type: x-email
  url: legal@meetup.com
- type: x-github
  url: https://github.com/meetup
- type: x-pricing
  url: http://www.meetup.com/pricing/
- type: x-privacy
  url: http://www.meetup.com/privacy/
- type: x-support
  url: http://www.meetup.com/help/
- type: x-terms-of-service
  url: http://www.meetup.com/terms/
- type: x-twitter
  url: https://twitter.com/MeetupAPI
- type: x-twitter
  url: https://twitter.com/Meetup
- type: x-website
  url: http://meetup.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---