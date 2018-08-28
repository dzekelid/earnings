---
swagger: "2.0"
x-collection-name: Twine
x-complete: 0
info:
  title: Twine List reward earnings
  description: Get a list of reward earnings matching the specified filters.
  version: 7.18.0
host: api.twinehealth.com
basePath: /pub
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /reward_earning:
    get:
      summary: List reward earnings
      description: Get a list of reward earnings matching the specified filters.
      operationId: fetchRewardEarnings
      x-api-path-slug: reward-earning-get
      parameters:
      - in: query
        name: filter[groups]
        description: Group identifiers
      - in: query
        name: filter[patient]
        description: Patient identifier
      - in: query
        name: filter[ready_for_fulfillment]
        description: If true, only returns those reward earnings for which ready_for_fulfillment
          is true and fulfilled_at is null
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - List
      - Reward
      - Earnings
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