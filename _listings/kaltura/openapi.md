---
swagger: "2.0"
x-collection-name: Kaltura
x-complete: 1
info:
  title: Kaltura VPaaS
  description: building-video-experiences-consists-of-ingesting-media-files-playing-back-videos-and-reviewing-usage-and-engagement-analytics--in-between-there-is-a-world-of-nuances-required-for-your-unique-usecase-and-application--kaltura-vpaas-is-built-on-the-principles-of-atomic-services-sdks-and-tools-that-allow-you-full-control-and-flexibility-over-every-element-and-process-in-your-medias-life-cycle-
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
---