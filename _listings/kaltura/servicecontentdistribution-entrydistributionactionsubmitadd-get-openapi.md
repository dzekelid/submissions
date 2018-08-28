---
swagger: "2.0"
x-collection-name: Kaltura
x-complete: 0
info:
  title: Kaltura VPaaS Get Service Contentdistribution Entrydistribution Action Submitadd
  description: Submits Entry Distribution to the remote destination
  version: 3.3.0
host: www.kaltura.com
basePath: /api_v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /service/contentdistribution_entrydistribution/action/submitAdd:
    get:
      summary: Get Service Contentdistribution Entrydistribution Action Submitadd
      description: Submits Entry Distribution to the remote destination
      operationId: entryDistribution.submitAdd
      x-api-path-slug: servicecontentdistribution-entrydistributionactionsubmitadd-get
      parameters:
      - in: query
        name: id
      - in: query
        name: No Name
      - in: query
        name: submitWhenReady
      responses:
        200:
          description: OK
      tags:
      - Service
      - Contentdistribution
      - Entrydistribution
      - Action
      - Submit
  /service/contentdistribution_entrydistribution/action/submitDelete:
    get:
      summary: Get Service Contentdistribution Entrydistribution Action Submitdelete
      description: Deletes Entry Distribution from the remote destination
      operationId: entryDistribution.submitDelete
      x-api-path-slug: servicecontentdistribution-entrydistributionactionsubmitdelete-get
      parameters:
      - in: query
        name: id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Contentdistribution
      - Entrydistribution
      - Action
      - Submit
  /service/contentdistribution_entrydistribution/action/submitUpdate:
    get:
      summary: Get Service Contentdistribution Entrydistribution Action Submitupdate
      description: Submits Entry Distribution changes to the remote destination
      operationId: entryDistribution.submitUpdate
      x-api-path-slug: servicecontentdistribution-entrydistributionactionsubmitupdate-get
      parameters:
      - in: query
        name: id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Contentdistribution
      - Entrydistribution
      - Action
      - Submit
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