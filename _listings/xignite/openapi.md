swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite VWAP
  description: provides-delayed-and-historical-volumeweightedaverage-price-vwap-information-
  version: 1.0.0
host: www.xignite.com
basePath: xVWAP.json/XigniteVWAP
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetBondCalculation:
    get:
      summary: Get Bond Calculation
      description: Returns Price, Yield, Accrued Interest and other bond analytics
        data for a specific bond reported by the price source selected in the input.
        Request against this operation counts as four hits.
      operationId: GetBondCalculation
      x-api-path-slug: getbondcalculation-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Bond
      - Calculation