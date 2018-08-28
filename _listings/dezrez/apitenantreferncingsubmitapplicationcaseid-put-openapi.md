---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Submits an individual referencing application for processing
  version: 1.0.0
  description: Submits an individual referencing application for processing.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/Peppermint:
    post:
      summary: Submits a referral to dezrez legal
      description: Submits a referral to dezrez legal.
      operationId: Peppermint_SubmitReferralByreferralDataContract
      x-api-path-slug: apipeppermint-post
      parameters:
      - in: body
        name: referralDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Submits
      - Referral
      - To
      - Dezrez
      - Legal
  /api/tenantreferncing/submitapplication/{caseId}:
    put:
      summary: Submits an individual referencing application for processing
      description: Submits an individual referencing application for processing.
      operationId: TenantReferencing_SubmitApplicationForReferencingBycaseId
      x-api-path-slug: apitenantreferncingsubmitapplicationcaseid-put
      parameters:
      - in: path
        name: caseId
        description: The id of the case to submit the application for
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Submits
      - Individual
      - Referencing
      - Applicationprocessing
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