---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 0
info:
  title: Mattermost API Get the jobs.
  description: |-
    Get a page of jobs. Use the query parameters to modify the behaviour of this endpoint.
    __Minimum server version: 4.1__
    ##### Permissions
    Must have `manage_jobs` permission.
  termsOfService: https://about.mattermost.com/default-terms/
  version: 4.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /jobs:
    get:
      summary: Get the jobs.
      description: |-
        Get a page of jobs. Use the query parameters to modify the behaviour of this endpoint.
        __Minimum server version: 4.1__
        ##### Permissions
        Must have `manage_jobs` permission.
      operationId: get-a-page-of-jobs-use-the-query-parameters-to-modify-the-behaviour-of-this-endpoint-minimum-server-
      x-api-path-slug: jobs-get
      parameters:
      - in: query
        name: page
        description: The page to select
      - in: query
        name: per_page
        description: The number of jobs per page
      responses:
        200:
          description: OK
      tags:
      - Jobs.
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