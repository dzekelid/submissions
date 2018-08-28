---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API Submit an assignment
  description: Submit an assignment.
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
  /courses/{course_id}/assignments/assignment_id/submissions:
    get:
      summary: List assignment submissions
      description: List assignment submissions.
      operationId: list-assignment-submissions
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissions-get
      parameters:
      - in: query
        name: grouped
        description: If this argument is true, the response will be grouped by student
          groups
      - in: query
        name: include[]
        description: Associations to include with the group
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
    post:
      summary: Submit an assignment
      description: Submit an assignment.
      operationId: submit-an-assignment
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissions-post
      parameters:
      - in: query
        name: comment[text_comment]
        description: Include a textual comment with the submission
      - in: query
        name: submission[body]
        description: Submit the assignment as an HTML document snippet
      - in: query
        name: submission[file_ids][]
        description: Submit the assignment as a set of one or more previously uploaded
          filesnresiding in the submitting user&#39;s files section (or the group&#39;snfiles
          section, for group assignments)
      - in: query
        name: submission[media_comment_id]
        description: The media comment id to submit
      - in: query
        name: submission[media_comment_type]
        description: The type of media comment being submitted
      - in: query
        name: submission[submission_type]
        description: The type of submission being made
      - in: query
        name: submission[url]
        description: Submit the assignment as a URL
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
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