---
swagger: "2.0"
x-collection-name: AWS Batch
x-complete: 1
info:
  title: AWS Batch API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CancelJob:
    get:
      summary: Cancel Job
      description: Cancels jobs in an AWS Batch job queue.
      operationId: cancelJob
      x-api-path-slug: actioncanceljob-get
      parameters:
      - in: query
        name: jobId
        description: A list of up to 100 job IDs to cancel
        type: string
      - in: query
        name: reason
        description: A message to attach to the job that explains the reason for cancelling
          it
        type: string
      responses:
        200:
          description: OK
      tags:
      - Jobs
  /?Action=ListJobs:
    get:
      summary: List Jobs
      description: Returns a list of task jobs for a specified job queue.
      operationId: listJobs
      x-api-path-slug: actionlistjobs-get
      parameters:
      - in: query
        name: jobQueue
        description: The name or full Amazon Resource Name (ARN) of the job queue
          with which to list jobs
        type: string
      - in: query
        name: jobStatus
        description: The job status with which to filter jobs in the specified queue
        type: string
      - in: query
        name: maxResults
        description: The maximum number of results returned by ListJobs in paginated
          output
        type: string
      - in: query
        name: nextToken
        description: The nextToken value returned from a previous paginated            ListJobs
          request where maxResults was used and the results         exceeded the value
          of that parameter
        type: string
      responses:
        200:
          description: OK
      tags:
      - Jobs
  /?Action=SubmitJob:
    get:
      summary: Submit Job
      description: Submits an AWS Batch job from a job definition.
      operationId: submitJob
      x-api-path-slug: actionsubmitjob-get
      parameters:
      - in: query
        name: containerOverrides
        description: A list of container overrides in JSON format that specify the
          name of a container in         the specified job definition and the overrides
          it should receive
        type: string
      - in: query
        name: dependsOn
        description: A list of job names or IDs on which this job depends
        type: string
      - in: query
        name: jobDefinition
        description: The job definition used by this job
        type: string
      - in: query
        name: jobName
        description: The name of the job
        type: string
      - in: query
        name: jobQueue
        description: The job queue into which the job will be submitted
        type: string
      - in: query
        name: parameters
        description: Additional parameters passed to the job that replace parameter
          substitution         placeholders that are set in the job definition
        type: string
      responses:
        200:
          description: OK
      tags:
      - Jobs
  /?Action=TerminateJob:
    get:
      summary: Terminate Job
      description: Terminates jobs in a job queue.
      operationId: terminateJob
      x-api-path-slug: actionterminatejob-get
      parameters:
      - in: query
        name: jobId
        description: Job IDs to be terminated
        type: string
      - in: query
        name: reason
        description: A message to attach to the job that explains the reason for cancelling
          it
        type: string
      responses:
        200:
          description: OK
      tags:
      - Jobs
---