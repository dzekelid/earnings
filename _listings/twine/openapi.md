swagger: "2.0"
x-collection-name: Twine
x-complete: 1
info:
  title: Twine
  description: -overviewthe-twine-health-api-is-restful-api--the-requests-and-responses-are-formated-according-to-the-json-apihttpjsonapi-orgformat1-0-specification-in-addition-to-this-documentation-we-also-provide-an-openapihttpsgithub-comoaiopenapispecificationblobmasterversions2-0-md-yaml-file-describing-the-api-twine-api-specificationswagger-yaml--authenticationauthentication-for-the-twine-api-is-based-on-the-oauth-2-0-authorization-frameworkhttpstools-ietf-orghtmlrfc6749--twine-currently-supports-grant-types-of-client-credentials-and-refresh-token-see-post-oauthtokenoperationcreatetoken-for-details-on-the-request-and-response-formats--redocinject-securitydefinitions-
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