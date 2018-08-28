swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 1
info:
  title: AWS EC2 API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ReportInstanceStatus:
    get:
      summary: Report Instance Status
      description: Submits feedback about the status of an instance.
      operationId: reportinstancestatus
      x-api-path-slug: actionreportinstancestatus-get
      parameters:
      - in: query
        name: Attribute
        description: The attribute to reset
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance