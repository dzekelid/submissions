---
swagger: "2.0"
x-collection-name: Digital River
x-complete: 1
info:
  title: Digital River Shopper API
  description: the-dr-connect-shopper-api-operates-on-a-store-and-products-that-are-set-up-in-global-commerce--
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
---