---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Insights Get Instances Instanceid Submit Logs
  description: Get instances instanceid submit logs.
  termsOfService: urn:tos
  version: 1.0.0
host: insights-api.data-services.predix.io
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /instances/{instanceId}/submit-logs:
    get:
      summary: Get Instances Instanceid Submit Logs
      description: Get instances instanceid submit logs.
      operationId: getSparkSubmitLogsUsingGET
      x-api-path-slug: instancesinstanceidsubmitlogs-get
      parameters:
      - in: path
        name: instanceId
        description: instanceId
      - in: query
        name: length
        description: length
      - in: query
        name: offset
        description: offset
      responses:
        200:
          description: Successful response
      tags:
      - Instances
      - Instanceid
      - Submit
      - Logs
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