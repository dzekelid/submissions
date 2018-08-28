---
swagger: "2.0"
x-collection-name: Digital River
x-complete: 0
info:
  title: Digital River Shopper API Post Shoppers Me Carts Active Submit Cart
  description: Post shoppers me carts active submit cart.
  version: v1
host: store.digitalriver.com
basePath: /store/{mysite}
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/shoppers/me/carts/active/submit-cart:
    post:
      summary: Post Shoppers Me Carts Active Submit Cart
      description: Post shoppers me carts active submit cart.
      operationId: postV1ShoppersMeCartsActiveSubmitCart
      x-api-path-slug: v1shoppersmecartsactivesubmitcart-post
      responses:
        200:
          description: OK
      tags:
      - Shoppers
      - Me
      - Carts
      - Active
      - Submit
      - Cart
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