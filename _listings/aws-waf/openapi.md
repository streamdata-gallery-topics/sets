swagger: "2.0"
x-collection-name: AWS WAF
x-complete: 1
info:
  title: AWS WAF API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListByteMatchSets:
    get:
      summary: List Byte Match Sets
      description: 'Service: AWS WAFReturns an array of.'
      operationId: listByteMatchSets
      x-api-path-slug: actionlistbytematchsets-get
      parameters:
      - in: query
        name: Limit
        description: Specifies the number of ByteMatchSet objects that you want AWS
          WAF to return for this request
        type: string
      - in: query
        name: NextMarker
        description: If you specify a value for Limit and you have more ByteMatchSets
          than the value of Limit, AWS WAF returns a NextMarker value in the response
          that allows you to list another group of ByteMatchSets
        type: string
      responses:
        200:
          description: OK
      tags:
      - Byte Match Sets
  /?Action=ListIPSets:
    get:
      summary: List IP Sets
      description: 'Service: AWS WAFReturns an array of.'
      operationId: listIPSets
      x-api-path-slug: actionlistipsets-get
      parameters:
      - in: query
        name: Limit
        description: Specifies the number of IPSet objects that you want AWS WAF to
          return for this request
        type: string
      - in: query
        name: NextMarker
        description: If you specify a value for Limit and you have more IPSets than
          the value of Limit, AWS WAF returns a NextMarker value in the response that
          allows you to list another group of IPSets
        type: string
      responses:
        200:
          description: OK
      tags:
      - IP Sets
  /?Action=ListSizeConstraintSets:
    get:
      summary: List Size Constraint Sets
      description: 'Service: AWS WAFReturns an array of.'
      operationId: listSizeConstraintSets
      x-api-path-slug: actionlistsizeconstraintsets-get
      parameters:
      - in: query
        name: Limit
        description: Specifies the number of SizeConstraintSet objects that you want
          AWS WAF to return for this request
        type: string
      - in: query
        name: NextMarker
        description: If you specify a value for Limit and you have more SizeConstraintSets
          than the value of Limit, AWS WAF returns a NextMarker value in the response
          that allows you to list another group of SizeConstraintSets
        type: string
      responses:
        200:
          description: OK
      tags:
      - Size Constraint Sets
  /?Action=ListSqlInjectionMatchSets:
    get:
      summary: List SQL Injection Match Sets
      description: 'Service: AWS WAFReturns an array of.'
      operationId: listSqlInjectionMatchSets
      x-api-path-slug: actionlistsqlinjectionmatchsets-get
      parameters:
      - in: query
        name: Limit
        description: Specifies the number of SqlInjectionMatchSet objects that you
          want AWS WAF to return for this request
        type: string
      - in: query
        name: NextMarker
        description: If you specify a value for Limit and you have more SqlInjectionMatchSet
          objects than the value of Limit, AWS WAF returns a NextMarker value in the
          response that allows you to list another group of SqlInjectionMatchSets
        type: string
      responses:
        200:
          description: OK
      tags:
      - SQL Injection Match Sets
  /?Action=ListXssMatchSets:
    get:
      summary: List Xss Match Sets
      description: 'Service: AWS WAFReturns an array of.'
      operationId: listXssMatchSets
      x-api-path-slug: actionlistxssmatchsets-get
      parameters:
      - in: query
        name: Limit
        description: Specifies the number of XssMatchSet objects that you want AWS
          WAF to return for this request
        type: string
      - in: query
        name: NextMarker
        description: If you specify a value for Limit and you have more XssMatchSet
          objects than the value of Limit, AWS WAF returns a NextMarker value in the
          response that allows you to list another group of XssMatchSets
        type: string
      responses:
        200:
          description: OK
      tags:
      - XSS Match Set