---
swagger: "2.0"
x-collection-name: Apica
x-complete: 0
info:
  title: Checks Job API Get Checks Job
  version: 1.0.0
  description: Executes a check.
host: api.pingdom.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
basePath: /
paths:
  '/checks/{checkId}/job ':
    ' get ':
      summary: Get Checks Job
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
      summary: Get Checks Job
      description: Executes a check.
      operationId: -checks-checkid-job-
      x-api-path-slug: checkscheckidjob-post
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Jobs
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