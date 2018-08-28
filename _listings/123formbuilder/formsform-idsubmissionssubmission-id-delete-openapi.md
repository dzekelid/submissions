---
swagger: "2.0"
x-collection-name: 123FormBuilder
x-complete: 0
info:
  title: 123FormBuilder Delete one form submission
  version: 1.0.0
  description: Delete one form submission
host: api.123contactform.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /forms/{form_id}/submissions:
    get:
      summary: Get submissions
      description: Get all submissions received through a form
      operationId: get-all-submissions-received-through-a-form
      x-api-path-slug: formsform-idsubmissions-get
      parameters:
      - in: path
        name: form_id
        description: The ID of the form
      - in: query
        name: include_recipients
        description: Returns the recipient(s) who should receive the submissions
      - in: query
        name: JWT
        description: JWT authentication token
      - in: query
        name: page
        description: Page number
      - in: query
        name: per_page
        description: The number of submissions to get per page in a request
      - in: query
        name: start_date
        description: List submissions starting with a specific date
      - in: query
        name: start_submission_id
        description: List all submissions starting with the specified submission ID
      responses:
        200:
          description: OK
      tags:
      - Submissions
  /forms/{form_id}/submissions/{submission_id}:
    get:
      summary: Get submission details
      description: Get the details of a single submission
      operationId: get-the-details-of-a-single-submission
      x-api-path-slug: formsform-idsubmissionssubmission-id-get
      parameters:
      - in: path
        name: form_id
        description: The ID of the form
      - in: query
        name: include_recipients
        description: Returns the recipient(s) who should receive the submission
      - in: query
        name: JWT
        description: JWT authentication token
      - in: path
        name: submission_id
        description: The ID of the submission
      responses:
        200:
          description: OK
      tags:
      - Submission
      - Details
    put:
      summary: Update Submission
      description: Update Submission
      operationId: update-submission
      x-api-path-slug: formsform-idsubmissionssubmission-id-put
      parameters:
      - in: query
        name: approved
        description: Approval status
      - in: path
        name: form_id
        description: The ID of the form
      - in: query
        name: JWT
        description: JWT authentication token
      - in: query
        name: payed
        description: Payment status
      - in: path
        name: submission_id
        description: The ID of the submission
      responses:
        200:
          description: OK
      tags:
      - Submission
    delete:
      summary: Delete one form submission
      description: Delete one form submission
      operationId: delete-one-form-submission
      x-api-path-slug: formsform-idsubmissionssubmission-id-delete
      parameters:
      - in: path
        name: form_id
        description: The ID of the form
      - in: query
        name: JWT
        description: JWT authentication token
      - in: path
        name: submission_id
        description: The ID of the submission
      responses:
        200:
          description: OK
      tags:
      - Form
      - Submission
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