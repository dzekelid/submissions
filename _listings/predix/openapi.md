swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
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