---
swagger: "2.0"
x-collection-name: AWS Route 53
x-complete: 0
info:
  title: AWS Route 53 API Delete Hosted Zone
  version: 1.0.0
  description: Deletes a hosted zone. Send a DELETE request to the /Amazon Route 53API
    version/hostedzone/hosted zone ID             resource.ImportantDelete a hosted
    zone only if there are no resource record sets other than the defaultSOA record
    and NS resource record sets. If the hosted zone contains other resource recordsets,
    delete them before deleting the hosted zone. If you try to delete a hosted zone
    thatcontains other resource record sets, Amazon Route 53 denies your request with
    aHostedZoneNotEmpty error. For information about deleting records from yourhosted
    zone, see ChangeResourceRecordSets.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/delegationset?marker=Marker&amp;maxitems=MaxItems:
    get:
      summary: List Reusable Delegation Sets
      description: To retrieve a list of your reusable delegation sets, send a GET
        request tothe /2013-04-01/delegationset resource. The response to this request
        includes aDelegationSets element with zero, one, or multiple DelegationSetchild
        elements. By default, the list of delegation sets is displayed on a single
        page. You cancontrol the length of the page that is displayed by using the
        MaxItems parameter.You can use the Marker parameter to control the delegation
        set that the listbegins with. Note Amazon Route 53 returns a maximum of 100
        items. If you set MaxItems to a value greater than100, Amazon Route 53 returns
        only the first 100.
      operationId: listreusabledelegationsets
      x-api-path-slug: 20130401delegationsetmarkermarkerampmaxitemsmaxitems-get
      parameters:
      - in: path
        name: marker
        description: If youre making the second or subsequent call toListReusableDelegationSets,
          the Marker element matches the valuethat you specified in the marker parameter
          in the previous request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reusable Delegation Sets
  /2013-04-01/healthcheck:
    post:
      summary: Create Health Check
      description: Creates a new health check.To create a new health check, send a
        POST request to the/2013-04-01/healthcheck resource. The request body must
        include a documentwith a CreateHealthCheckRequest element. The response returns
        theCreateHealthCheckResponse element, containing the health check ID specifiedwhen
        adding health check to a resource record set. For information about adding
        health checksto resource record sets, see ResourceRecordSet:HealthCheckId
        in ChangeResourceRecordSets. If you are registering EC2 instances with an
        Elastic Load Balancing (ELB) loadbalancer, do not create Amazon Route 53 health
        checks for the EC2 instances. When you register anEC2 instance with a load
        balancer, you configure settings for an ELB health check, whichperforms a
        similar function to an Amazon Route 53 health check.You can associate health
        checks with failover resource record sets in a private hostedzone. Note the
        following:Amazon Route 53 health checkers are outside the VPC. To check the
        health of an endpointwithin a VPC by IP address, you must assign a public
        IP address to the instance in theVPC.You can configure a health checker to
        check the health of an external resource thatthe instance relies on, such
        as a database server.You can create a CloudWatch metric, associate an alarm
        with the metric, and then create ahealth check that is based on the state
        of the alarm. For example, you might create a CloudWatchmetric that checks
        the status of the Amazon EC2 StatusCheckFailed metric, add analarm to the
        metric, and then create a health check that is based on the state of thealarm.
        For information about creating CloudWatch metrics and alarms by using the
        CloudWatch console,see the Amazon CloudWatch User Guide.
      operationId: createhealthcheck
      x-api-path-slug: 20130401healthcheck-post
      parameters:
      - in: body
        name: CallerReference
        description: A unique string that identifies the request and that allows failedCreateHealthCheck
          requests to be retried without the risk of executing theoperation twice
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateHealthCheckRequest
        description: Root level tag for the CreateHealthCheckRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: HealthCheckConfig
        description: A complex type that contains the response to a CreateHealthCheck
          request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Health
  /2013-04-01/hostedzone/Id:
    delete:
      summary: Delete Hosted Zone
      description: Deletes a hosted zone. Send a DELETE request to the /Amazon Route
        53API version/hostedzone/hosted zone ID             resource.ImportantDelete
        a hosted zone only if there are no resource record sets other than the defaultSOA
        record and NS resource record sets. If the hosted zone contains other resource
        recordsets, delete them before deleting the hosted zone. If you try to delete
        a hosted zone thatcontains other resource record sets, Amazon Route 53 denies
        your request with aHostedZoneNotEmpty error. For information about deleting
        records from yourhosted zone, see ChangeResourceRecordSets.
      operationId: deletehostedzone
      x-api-path-slug: 20130401hostedzoneid-delete
      parameters:
      - in: path
        name: Id
        description: The ID of the hosted zone you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Hosted Zones
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