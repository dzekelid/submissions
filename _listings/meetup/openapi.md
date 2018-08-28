swagger: "2.0"
x-collection-name: Meetup
x-complete: 1
info:
  title: Meetup
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /:urlname/abuse_reports:
    post:
      summary: Report Group
      description: Submits a new abuse report for a target group. Abuse reports will
        be followed up on by our Community Support team.
      operationId: abuse
      x-api-path-slug: urlnameabuse-reports-post
      parameters:
      - in: query
        name: type
        description: A required identifier for type of abuse you are reporting
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Groups