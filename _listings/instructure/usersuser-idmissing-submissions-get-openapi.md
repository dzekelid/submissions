---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Users API List Missing Submissions
  description: List missing submissions.
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
  /users/{user_id}/missing_submissions:
    get:
      summary: List Missing Submissions
      description: List missing submissions.
      operationId: list-missing-submissions
      x-api-path-slug: usersuser-idmissing-submissions-get
      parameters:
      - in: query
        name: user_id
        description: the student&#39;s ID
      responses:
        200:
          description: OK
      tags:
      - Users
      - User
      - Id
      - Missing
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