swagger: "2.0"
x-collection-name: Factual
x-complete: 1
info:
  title: Factual
  description: access-to-the-places-and-business-data-available-at-factual-
  version: 1.0.0
host: api.v3.factual.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /t/{table_name}/submit:
    post:
      summary: Post Table Name Submit
      description: Post table name submit.
      operationId: postTTableNameSubmit
      x-api-path-slug: ttable-namesubmit-post
      parameters:
      - in: path
        name: table_name
      responses:
        200:
          description: OK
      tags:
      - Table
      - Name
      - Submit