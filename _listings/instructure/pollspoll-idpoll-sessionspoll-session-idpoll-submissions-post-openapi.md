---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Polls API Create a single poll submission
  description: Create a single poll submission.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /polls/{poll_id}/poll_sessions/poll_session_id/poll_submissions:
    post:
      summary: Create a single poll submission
      description: Create a single poll submission.
      operationId: create-a-single-poll-submission
      x-api-path-slug: pollspoll-idpoll-sessionspoll-session-idpoll-submissions-post
      parameters:
      - in: query
        name: poll_submissions[][poll_choice_id]
        description: The chosen poll choice for this submission
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Poll
      - Session
      - Id
      - Poll
      - Submissions
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