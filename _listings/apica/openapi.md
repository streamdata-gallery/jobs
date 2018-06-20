---
swagger: "2.0"
x-collection-name: Apica
x-complete: 1
info:
  title: Checks Job API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '/checks/{checkId}/job ':
    ' get ':
      summary: Checks {checkId} Job
      description: DEPRECATED. Gets the current job status for a check.
      operationId: -checks-checkid-job-
      x-api-path-slug: checkscheckidjob-get
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Jobs
    ' post ':
      summary: Checks {checkId} Job
      description: Executes a check.
      operationId: -checks-checkid-job-
      x-api-path-slug: checkscheckidjob-post
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Jobs
---