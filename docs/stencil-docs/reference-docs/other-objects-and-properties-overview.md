# Other Objects and Properties Overview

<div class="otp" id="no-index">

### On This Page
- [Product](#product)
- [Product Reviews](#product-reviews)
- [Related Products](#related-products)
- [Similar Products by Customer Views](#similar-products-by-customer-views)
- [Product Videos](#product-videos)
- [Compare](#compare)
- [Download Item](#download-item)
- [Product Other Details](#product-other-details)
- [Category](#category)
- [Category Products](#category-products)
- [Category Shop by Price](#category-shop-by-price)
- [Brand](#brand)
- [Brand List](#brand-list)
- [Shop by Brand](#shop-by-brand)
- [Cart](#cart)
- [Customer](#customer)
- [Order Details](#order-details)
- [Recent Items](#recent-items)
- [Customer Wishlists](#customer-wishlists)
- [Wishlist Details](#wishlist-details)
- [Account Order Shipments](#account-order-shipments)
- [Account Orders](#account-orders)
- [Account Returns](#account-returns)
- [Account New Return](#account-new-return)
- [Create Account](#create-account)
- [Shipping Addresses](#shipping-addresses)
- [Payment Methods](#payment-methods)
- [Edit Payment Methods](#edit-payment-methods)
- [Add Payment Methods](#add-payment-methods)
- [Blog](#blog)
- [Blog Post](#blog-post)
- [Forms](#forms)
- [Order Confirmation Objects](#order-confirmation-objects)

</div> 

<div class="HubBlock--callout">
<div class="CalloutBlock--info">
<div class="HubBlock-content">

<!-- theme: info -->

### Debugging Your Theme
> The Stencil framework provides built-in debugging tools to aid in your custom front-end development. When you want to see what data is available on the page you are working on, you can simply add the debug query string to your store’s localhost URL. Here is an example:
> ```http://localhost:3000/product/this-is-a-sample-product?debug=context```
> This will return a list of all the objects available on the page, in JSON syntax. If you want to view the available JSON objects and rendered page at the same time, simply change the debug value to bar. Below is an example:
> ```http://localhost:3000/product/this-is-a-sample-product?debug=bar```

</div>
</div>
</div>

## Product

<b>Description:</b> Default property that provides detailed product data. Called on the default `templates/pages/product.html`and `templates/pages/amp/product.html` templates, and on several partials in the `templates/components/` subdirectory:

* `account/returns-list.html`,
* `cart/item-options.html`,
* `products/add-to-cart.html`,
* `products/event-date.html`,
* `products/modals/writeReview.html`,
* `products/price.html`,
* `products/product-view.html`,
* `amp/products/product-options.html`,
* `amp/products/product-view.html`, and
* `amp/products/product-view-details.html`.

<b>Handlebars Expression:</b> `{{product}}`

<b>Object Properties:</b>

| Property              | Description      |
|-----------------------|-------------------------|
| id                    | Unique ID for the product                                                                                                                                                                                                                          |
| sku                   | Default product variant when no options are selected                                                                                                                                                                                               |
| mpn                   | Manufacturer Part Number                                                                                                                                                                                                                           |
| gtin                  | Global Trade Item Number                                                                                                                                                                                                                           |
| url                   | URL to the product detail page                                                                                                                                                                                                                     |
| upc                   | Optional UPC code for the product                                                                                                                                                                                                                  |
| title                 | Displayed name of the product                                                                                                                                                                                                                      |
| description           | (HTML) description of the product                                                                                                                                                                                                                  |
| detail_messages       | Status messages for display at the top of the product page                                                                                                                                                                                         |
| min_purchase_quantity | Minimum quantity that can be purchased at once                                                                                                                                                                                                     |
| max_purchase_quantity | Maximum quantity that can be purchased at once                                                                                                                                                                                                     |
| can_purchase          | Boolean that indicates whether the product is available for purchase                                                                                                                                                                               |
| out_of_stock          | Boolean that indicates whether the product is out of stock                                                                                                                                                                                         |
| out_of_stock_message  | Merchant-defined label to display when a product is out of stock                                                                                                                                                                                   |
| cart_url              | URL to the customer’s shopping cart                                                                                                                                                                                                                |
| add_to_wishlist_url   | URL to add the product to the customer’s wishlist                                                                                                                                                                                                  |
| customizations        | Product customizations (for example, a T-shirt size); these correspond to configurable fields and numeric-text product options in the BigCommerce control panel                                                                                    |
| id                    | Customization ID                                                                                                                                                                                                                                   |
| display_name          | Label for this customization, as displayed to customers                                                                                                                                                                                            |
| type                  | Customization type [text textarea Numbers OnlyText checkbox select file]                                                                                                                                                                           |
| required              | Boolean value that indicates whether customer must specify this customization in order to buy the product                                                                                                                                          |
| condition             | Boolean value indicating whether to display this product's condition (new, used, or refurbished)                                                                                                                                                   |
| prefill               | Optional string value to prefill this field                                                                                                                                                                                                        |
| <values>              | For select type, array of strings listing the available options                                                                                                                                                                                    |
| <file_types>          | For file type, string representing the types of allowed files                                                                                                                                                                                      |
| <file_size>           | For file type, string representing the maximum file size allowed                                                                                                                                                                                   |
| integer_only          | For NumbersOnlyText type, boolean value indicating whether to restrict customer's entries to whole numbers only                                                                                                                                    |
| default               | For NumbersOnlyText type, optional string representing a default number that customers can see and overwrite                                                                                                                                       |
| limit_input           | For NumbersOnlyText type, boolean indicating whether to impose any limits on the numeric values that customers can enter as strings                                                                                                                |
| limit_input_option    | For NumbersOnlyText type and limit_input = true, the type of limit: lowest or highest                                                                                                                                                              |
| lowest                | For NumbersOnlyText type and limit_input = true,  minimum allowable value; a value of 0 imposes no limit                                                                                                                                           |
| highest               | For NumbersOnlyText type and limit_input = true,  maximum allowable value; a value of 0 imposes no limit                                                                                                                                           |
| options               | Options for color and pattern swatches displayed for this product                                                                                                                                                                                  |
| id                    | Product ID                                                                                                                                                                                                                                         |
| type                  | String indicating size, color, swatch, etc.                                                                                                                                                                                                        |
| display_name          | Option Name displayed in control panel for this option                                                                                                                                                                                             |
| required              | Boolean value that indicates whether customer must specify this option in order to buy the product                                                                                                                                                 |
| condition             | Boolean value indicating whether to display this product's condition (new, used, or refurbished)                                                                                                                                                   |
| values                | Array of data (color) or image (pattern) values                                                                                                                                                                                                    |
| label                 | Internal label for this value (not normally displayed to shoppers)                                                                                                                                                                                 |
| id                    | ID for this value, unique within this values array                                                                                                                                                                                                 |
| selected              | Boolean indicating whether this value is preselected as the option's default value, upon page load                                                                                                                                                 |
| data                  | Each values member can contain either a data or an image member; data denotes a color                                                                                                                                                              |
| <color value>         | Hex code for this color                                                                                                                                                                                                                            |
| image                 | Each values member can contain either a data or an image member; image denotes a pattern, in Stencil image object format. (Note: This image value replaces the {{pattern}} property, which was limited to 18 x 18 pixels, and will be deprecated.) |
| price                 | References the catalog price object, to access the product’s price                                                                                                                                                                                 |
| weight                | Weight of the default variant                                                                                                                                                                                                                      |
| height                | Height of the default variant                                                                                                                                                                                                                      |
| width                 | Width of the default variant                                                                                                                                                                                                                       |
| depth                 | Depth of the default variant                                                                                                                                                                                                                       |
| rating                | Rating for the product                                                                                                                                                                                                                             |
| num_reviews           | Number of reviews the product has                                                                                                                                                                                                                  |
| bulk_discount_rates   | List of discount rates for the current product                                                                                                                                                                                                     |
| condition             | Condition of the product                                                                                                                                                                                                                           |
| stock_level           | Current stock level of the product; will be null if storefront stock display is disabled by the merchant, or if the product lacks inventory tracking                                                                                               |
| shipping              | Shipping properties for the product                                                                                                                                                                                                                |
| fixed                 | Boolean that indicates whether the product’s shipping price is fixed                                                                                                                                                                               |
| price                 | Price object that defines the shipping cost for this product (if shipping cost is fixed)                                                                                                                                                           |
| calculated            | Boolean that indicates whether the product’s shipping price is calculated at checkout                                                                                                                                                              |
| stock_label           | Shows whether the product stock level is for on-hand merchandise or pre-orders.                                                                                                                                                                    |
| availability          | Optional availability message set by the merchant                                                                                                                                                                                                  |
| pre_order             | Availability of the product for pre-order                                                                                                                                                                                                          |
| release_date          | Release date, if the product is set to pre-order status                                                                                                                                                                                            |
| error_message         | Potential error on the page (e.g.: out of stock, form validations)                                                                                                                                                                                 |
| gift_wrapping         | Whether or not gift wrapping is enabled                                                                                                                                                                                                            |
| brand                 | Brand of the product                                                                                                                                                                                                                               |
| name                  | Displayed name of the brand                                                                                                                                                                                                                        |
| url                   | URL to the brand page                                                                                                                                                                                                                              |
| main_image            | Primary image to display when the product details page loads                                                                                                                                                                                       |
| images                | List of all images for this product, in Stencil image format (as configured in config.json; used with the getImage Handlebars helper)                                                                                                              |
| pinterest_js          | Property to display Pinterest button                                                                                                                                                                                                               |
| facebook_like         | Property to display Facebook Like button                                                                                                                                                                                                           |
| warranty              | Optional warranty text set by the merchant                                                                                                                                                                                                         |
| meta_keywords         | Optional search keywords that merchants may enter in the control panel’s "Add a Product" or “Edit a Product” page, to characterize the product in meta tags and storefront searches                                                                |
| tags                  | Keywords by which this product can also be identified                                                                                                                                                                                              |
| name                  | Name of the tag                                                                                                                                                                                                                                    |
| custom_fields         | Extra details to display about the product                                                                                                                                                                                                         |
| name                  | Custom field name                                                                                                                                                                                                                                  |
| value                 | Custom field value                                                                                                                                                                                                                                 |
| event_date            | Property to handle a date-based product                                                                                                                                                                                                            |
| name                  | Name of the event                                                                                                                                                                                                                                  |
| date_start            | Event’s start date range                                                                                                                                                                                                                           |
| date_end              | Event’s end date range                                                                                                                                                                                                                             |
| earliest_year         | Event’s starting year                                                                                                                                                                                                                              |
| latest_year           | Event’s ending year                                                                                                                                                                                                                                |
| type                  | Type of event                                                                                                                                                                                                                                      |
| category              | An array of categories the product belongs to                                                                                                                                                                                                      |



## Related Products

<b>Description:</b> A list of products related to this product. (Called on the default `templates/components/products/tabs.html` partial.)

<b>Handlebars Expression:</b> `{{product.related_products}}`

<b>Object Properties: </b>References the <a href="/stencil-docs/stencil-object-model-reference/stencil-objects/common-objects/common-product-card-model">product card model</a>.

## Similar Products by Customer Views

**Description:** A list of products similar to a given product, based on customer’s product browsing history. (Called on the default <code>&lt;theme-name&gt;/templates/components/products/tabs.html</code> partial.)

<b>Handlebars Expression:</b> <code>{{product.similar_by_views}}</code>

<b>Object Properties:</b> References the <a href="/stencil-docs/stencil-object-model-reference/stencil-objects/common-objects/common-product-card-model">product card model</a>.

## Product Videos

<b>Description:</b> A list of videos for a given product. (Called on the default <code>&lt;theme-name&gt;/templates/pages/product.html</code> template, and on the <code>&lt;theme-name&gt;/templates/components/amp/products/product-view.html</code> partial.)

<b>Handlebars Expression:</b> <code>{{product.videos}}</code>

<b>Object Properties:</b>

| Property          | Description                            |
|-------------------|----------------------------------------|
| id                | ID of the product video                |
| title_short       | Short title of the product video       |
| title_long        | Long title of the product video        |
| description_long  | Long description of the product video  |
| description_short | Short description of the product video |
| length            | Duration of the product video          |


## Compare

**Description:** Property to display an array of products on product comparison pages. (Called on the default <code>&lt;theme-name&gt;/templates/pages/compare.html</code> template.)

**Handlebars Expression:** <code>{{comparisons}}</code>

**Object Properties:**
References the product card model, plus the additional fields listed here:

| Property      | Description    |
|---------------|----------------|
| availability  | How long this product usually takes to ship                                                                    |
| brand         | Object containing brand data for this product                                                                  |
|  url          | Brand URL for this product                                                                                     |
|  name         | Brand name for this product                                                                                    |
| remove_url    | URL to remove this product/column from the comparison                                                          |
| custom_fields | Array of additional product details – size, color, book's ISBN, DVD's release date, etc. – as name/value pairs |
|  name         | Displayed name for this custom field                                                                           |
|  value        | Value for this custom field’s entry                                                                            |


## Download Item

**Description:** Property for digital (non-physical) products. (Called on the default <code>&lt;theme-name&gt;/templates/pages/account/download-item.html</code>template.)

**Handlebars Expression:** <code>{{downloads}}</code>

**Object Properties:**

| Property               | Description       |
|------------------------|-------------------|
| order_id               | ID for this order |
| product_name           | Name of the digital product |
| items                  | Array of product components |
| name                   | Name of this digital item   |
| expired                | Boolean indicating whether customer’s access/subscription to this item has expired |
| days_remaining         | Number of days left in customer’s access/subscription to this item |
| downloads_remaining    | Number of times customer may download this item |
| size                   | File size of this digital item (string, responsively formatted as: 240 KB, 1.1 MB, etc.) |
| description            | Description (if entered by merchant) for this item |
| id                     | ID for this item |
| images                 | List of all images for the product associated with this list of downloadable items (in Stencil image format) |
| thumbnail              | "Primary" image for the product associated with this list of downloadable items (in Stencil image format) |
| Property               | Description |
| name                   | Displayed name for this category of information |
| value                  | Displayed value for this product’s entry |
| Property               | Description |
| id                     | Unique ID for the category |
| name                   | Merchant-defined category name |
| url                    | URL for the category-specific page |
| description            | Merchant-defined description of the category |
| image                  | Image representing this category, in Stencil image format |
| subcategories          | List of any child categories |
| id                     | Unique ID for the subcategory |
| name                   | Name of the subcategory |
| url                    | URL to the subcategory |
| description            | Merchant-defined description of the subcategory |
| image                  | Image representing this subcategory, in Stencil image format |
| product_count          | Number of products in the subcategory. (Counts at the current level only – not recursive to deeper levels.) |
| detail_messages        | Message displayed when a product is out of stock, and inventory settings are configured to redirect to a category: "Sorry, the product you tried to view is currently out of stock, here are some similar products we have available." (This phrasing is set by the BigCommerce App.) |
| show_compare           | Boolean that defines whether to show controls for product comparison |
| show_add_to_cart       | Boolean that defines whether to show an Add to Cart button for this category |
| total_products         | Count of the number of products in the category |
| faceted_search_enabled | Boolean that defines whether product-filtering search is enabled for the store |
| facets                 | Available search facets |
| pagination             | References the pagination model |
| selected               | Selected search facets  |


## Category Products

**Description:** A list of products associated with this category. (Called on the default `templates/pages/category.html` template, and on the `templates/components/category/product-listing.html` partial.)

**Handlebars Expression:** `{{category.products}}`

**Object Properties:** References the  [product card model](/stencil-docs/stencil-object-model-reference/stencil-objects/common-objects/common-product-card-model).

## Category Shop by Price

<b>Description:</b> A list of price ranges, to enable customers to set price limits within a product category. Called on the default<code>&lt;theme-name&gt;/templates/components/category/shop-by-price.html</code> and <code>&lt;theme-name&gt;/templates/components/category/sidebar.html</code> partials.)

<b>Handlebars Expression:</b> `{{category.shop_by_price}}`

<b>Object Properties:</b>

| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| url      | URL of price-filtered product results for this category      |
| low      | Price object that defines the minimum price boundary         |
| high     | Price object that defines the maximum price boundary         |
| selected | Price object that defines the currently selected price range |


## Brand

**Description:** The brand object for the page calling the object. (Called on the default `templates/pages/brand.html` template.)

**Handlebars Expression:** `{{brand}}`

<b>Object Properties:</b>

| Property               | Description                                                                                              |
|------------------------|----------|
| show_compare           | Boolean corresponding to merchant’s control panel selection whether or not to enable product comparisons |
| url                    | URL of the brand page                                                                                    |
| name                   | Name of the brand                                                                                        |
| pagination             | References the pagination model                                                                          |
| image                  | Image used to visually represent the brand (i.e., logo)                                                  |
| faceted_search_enabled | Boolean that defines whether product-filtering search is enabled for the store                           |
| facets                 | A list of all possible search filters for this brand                                                     |
| products               | An array of product card models                                                                          |
| selected               | An array of selected facets                                                                              |
| Property               | Description                                                                                              |
| url                    | URL to this brand’s products listing                                                                     |
| name                   | Name of the brand                                                                                        |
| id                     | Internal identifier for the brand                                                                        |
| image                  | Stencil image object (if any) for the brand                                                              |


## Shop by Brand

**Description:** Objects to enable customers to shop by brand. Returns top 10 brands, by product count. (Called on the default `templates/components/brand/sidebar.html` and `templates/components/common/footer.html` partials.)

<b>Handlebars Expression:</b> `{{shop_by_brand}}`

<b>Object Properties:</b>

| Property | Description                            |
|----------|----------------------------------------|
| links    | Array of links to individual brands    |
| id       | ID for this brand                      |
| url      | URL for this brand                     |
| name     | Name of this brand                     |
| count    | Number of products matching this brand |


## Cart

<b>Description:</b> The cart-specific properties for the current session

**Handlebars Expression:** `{{cart}}`

**Object Properties:**

| Property                   | Description          |
|----------------------------|-------------------------------------------|
| id                         | Unique system ID for the item in the cart                                                                                                                                       |
| remove_url                 | URL to remove this item from the cart                                                                                                                                           |
| quantity                   | Quantity of the item being ordered                                                                                                                                              |
| min_purchase_quantity      | Quantity of the item being ordered                                                                                                                                              |
| max_purchase_quantity      | Maximum quantity the customer can order of the given item (if applicable)                                                                                                       |
| type                       | String indicating the type of purchase: either "Item" or "GiftCertificate"                                                                                                      |
| If type == Item            | If the item in the cart is a purchasable product, these properties are available:                                                                                               |
| product_id                 | Product ID for the cart item                                                                                                                                                    |
| brand                      | Brand details for this cart item                                                                                                                                                |
|  name                      | The product’s brand name                                                                                                                                                        |
| name                       | Product name of the cart item                                                                                                                                                   |
| url                        | Link to the product page for the cart item                                                                                                                                      |
| sku                        | SKU value for this cart item                                                                                                                                                    |
| availability               | An optional availability message set by the merchant                                                                                                                            |
| image                      | Product image for the cart item                                                                                                                                                 |
| can_modify                 | Boolean indicating whether the customer may modify the quantity of, or remove, this cart item                                                                                   |
| event_date                 | Chosen event date for event-based products                                                                                                                                      |
| show_gift_wrapping         | Boolean indicating whether the wrapping options are shown                                                                                                                       |
| gift_wrapping              | Gift-wrapping options                                                                                                                                                           |
|  name                      | Name of the gift-wrapping option                                                                                                                                                |
|  price                     | Price object that defines the price of the gift-wrapping option                                                                                                                 |
|  message                   | Customer-defined message for the gift wrapping                                                                                                                                  |
|  remove_url                | URL to remove the gift-wrapping option                                                                                                                                          |
| rrp                        | Price object that defines the cart item's list price (MSRP); can be used to display struck-out list prices, as explained here                                                   |
| price                      | Price object that defines the unit price of the cart item, after discounts; to see how this and the next three price properties relate to each other, see Cart Price Properties |
| price_discounted           | Price object that defines the unit price, after all cart discounts and promotions                                                                                               |
| total                      | Price object that defines the total price (price * quantity) of the cart item                                                                                                   |
| total_discounted           | Price object that defines the total price (price * quantity), after all cart discounts and promotions                                                                           |
| release_date               | If a pre-order product was added to the cart,  displays a message about when the item is expected to ship to the customer                                                       |
| options                    | Options chosen when product was added to cart                                                                                                                                   |
|  name                      | Name of the option                                                                                                                                                              |
|  value                     | Value of the option                                                                                                                                                             |
| bulk_pricing               | Properties for applying bulk-pricing discounts to cart items                                                                                                                    |
|  base_price                | The lowest calculated price on an item. For example, 2 items are $99, 3 items are $98 and 4 items are $97. There are 3 items in the cart, the base price will be $98.           |
|  discount_amount           | Bulk-discount amount per item, if applicable; otherwise, null                                                                                                                   |
|  discount_percentage       | Bulk-discount percentage per item, if applicable; otherwise, null                                                                                                               |
| custom_fields              | Custom product fields set when product was added to cart                                                                                                                        |
| configurable_fields        | Custom product fields set when product was added to cart                                                                                                                        |
| If type == GiftCertificate | If the item in the cart is a gift certificate, these properties are available:                                                                                                  |
|  name                      | Sender’s name                                                                                                                                                                   |
|  edit_url                  | URL to edit the gift certificate                                                                                                                                                |
|  recipient                 | Recipient’s name                                                                                                                                                                |
|  price                     | Price object that defines the gift certificate’s basic price                                                                                                                    |
|  total                     | Price object that defines the gift certificate’s total cost, with applicable taxes included  |

### Strikeout Pricing Example

As a theme developer, you can use the `{{cart.items.rrp}}` property to display strike-out pricing in the Cart context. Here is the general approach:

In your `templates/components/cart/content.html` file, as you iterate over the list of items in the cart, you would check each item's `type`. (No `rrp` property is available where the `type` is `GiftCertificate`.)

If the type is `Item`, then you would check the {{cart.items.rrp}} value. If the value is _not_ `null`, then you would know that you can display a strike-out price for the item. Below is a sample code skeleton:

```html
{{#each cart.items}}
   <!--...-->
  {{#if type '==' 'GiftCertificate'}}
      {{#if rrp}}
          <!-- your code to display strike-thru pricing -->
      {{else}}
          <!-- your code to display normal pricing -->
      {{/if}}
  {{/if}}
 ```

For further details about catalog price properties, please see [Catalog Price Object: How Properties Interact](/stencil-docs/conditional-logic-examples/catalog-price-object). For usage examples of the `{{cart.items}}` `price` and `total` properties, please see [Cart Price Properties](/stencil-docs/conditional-logic-examples/cart-price-relationships).

### Cart Status Message

**Description:** A list of relevant messages for the cart in the current session

**Handlebars Expression:** `{{cart.status_messages}}`

**Object Properties:**

| Property  | Description  |
|-|-|
| message  | System-generated messages for the cart  |
|type|Type of message: error, info, or success	|

### Suggested Products

<b>Description:</b> A list of suggested products, based on cart contents; displays only if enabled by the `cart.suggestions` front-matter attribute, and only immediately after a product is added to the cart

<b>Handlebars Expression:</b> `{{cart.suggested_products}}`

<b>Object Properties:</b> References standard product card model.

## Customer

**Description:** Customer-specific properties for a storefront customer object. When filtering/limiting, customers' default sorting is by customer id, from lowest to highest. (Called on several partials in the `templates/components/` subdirectory:
`page/contact-us-form.html`,
`common/subscription-form.html`,
`account/address-list.html`,
`account/messages-form.html`, and
`account/wishlist-list.html`.)

**Handlebars Expression:** `{{customer}}`

**Object Properties:**

| Property            | Description                                                                         |
|---------------------|-------------------------------------------------------------------------------------|
| id                  | Customer’s ID                                                                       |
| name                | Customer’s name                                                                     |
| email               | Customer’s email address                                                            |
| phone               | Customer’s phone number                                                             |
| store_credit        | Customer’s store credit                                                             |
| customer_group_id   | ID of this customer's group                                                         |
| customer_group_name | Name of this customer's group                                                       |
| num_new_messages    | Number of unread messages for this customer                                         |
| num_wishlists       | Number of wishlists for this customer                                               |
| shipping_address    | Shipping address used for the order                                                 |
|  id                 | Unique, system-generated ID                                                         |
|  first_name         | Customer’s shipping (first) name                                                    |
|  last_name          | Customer’s shipping (last) name                                                     |
|  company            | Customer's shipping company name                                                    |
|  address1           | Customer's shipping address, first line                                             |
|  address2           | Customer's shipping address, second line                                            |
|  city               | Customer's shipping city                                                            |
|  state              | Customer's shipping state                                                           |
|  zip                | Customer's shipping zip                                                             |
|  country            | Customer's shipping country                                                         |
|  phone              | Customer's shipping phone number                                                    |
|  state_id           | ID for customer's shipping state/province/region
            |
|  country_id         | ID for customer's shipping country                                                  |
|  destination        | Type of delivery destination: residential or business/commercial                    |
|  last_used          | Timestamp when this address was last used as a shipping address                     |
|  form_session_id    | Used for custom shipping forms                                                      |
| payment_methods     | Used on the payment methods page to render list of customer's saved payment methods |


## Order Details

**Description:** The order properties for a specific order, usable on the order details page. (Called on the default `templates/pages/account/orders/details.html` and `<theme-name&gt;/templates/pages/account/orders/invoice.html` templates, and on the `<theme-name&gt;/templates/components/account/order-contents.html` partial.)

**Handlebars Expression:** `{{order}}`

**Object Properties:**

| Property               | Description                                                                                                        |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| date                   | Date of the order                                                                                                  |
| id                     | Unique, system-generated ID                                                                                        |
| total                  | Price object that defines the order’s total value                                                                  |
| status                 | Order status code                                                                                                  |
| status_text            | Status text associated with the status code for the order                                                          |
| returns_enabled        | Boolean that indicates whether merchant allows products from the order to be returned                              |
| reorder_url            | URL to place reorders for items in this order                                                                      |
| invoice_url            | URL to display an invoice for this order                                                                           |
| is_complete            | Boolean indicating that the order has been completed                                                               |
| comments               | Customer’s message about the order                                                                                 |
| items                  | List of items for the order                                                                                        |
|  order_product_id      | Product ID                                                                                                         |
|  name                  | Product Name                                                                                                       |
|  quantity              | Quantity Ordered                                                                                                   |
|  refunded              | Price object that defines the value of this product that has been refunded                                         |
|  event_date            | A chosen event date for the product                                                                                |
|  price                 | Price object that defines the product’s price                                                                      |
| shipping_rows          | Array of shipping addresses, for each item in the order                                                            |
| address                | Street address to ship to                                                                                          |
| city                   | City to ship to                                                                                                    |
| state                  | State to ship to                                                                                                   |
| zip                    | Postal/ZIP code to ship to                                                                                         |
| country                | Country to ship to                                                                                                 |
|  gift_wrapping_name    | Name of the gift-wrapping option used                                                                              |
|  type                  | Type of purchase; value is one of: physical, digital, giftcertificate                                              |
|  download_url          | URL at which customer can download digital item                                                                    |
|  image                 | The image of the order’s first product, in Stencil image format                                                    |
| show_reorder | Boolean indicating whether the customer should see a button for reordering items on the Account Order Details page |
|  reorder_message       | An error message to be displayed when the customer attempts to reorder items that can’t be reordered               |
|  options               | A list of options selected when this product was purchased                                                         |
|  name                  | Display name for the option ("Small", “Medium”, etc.)                                                              |
|  value                 | Value that customer selected for the option                                                                        |
| billing_address        | Billing address used for the order                                                                                 |
|  full_name             | Customer's billing name                                                                                            |
|  company               | Customer's billing company name                                                                                    |
|  address_lines         | Customer's billing address                                                                                         |
|  city                  | Customer's billing city                                                                                            |
|  state                 | Customer's billing state                                                                                           |
|  country               | Customer billing country                                                                                           |
|  zip                   | Customer billing ZIP                                                                                               |
|  phone                 | Customer billing phone number                                                                                      |
| shipping_address_count | Number of shipping addresses the customer has specified for this order                                             |
| shipping_address       | Shipping address used for the order                                                                                |
|  full_name             | Customer's shipping name                                                                                           |
|  company               | Customer's shipping company name                                                                                   |
|  address_lines         | Customer's shipping address                                                                                        |
|  city                  | Customer's shipping city                                                                                           |
|  state                 | Customer's shipping state                                                                                          |
|  country               | Customer's shipping country                                                                                        |
|  zip                   | Customer's shipping zip                                                                                            |
|  phone                 | Customer's shipping phone number                                                                                   |
| payment_method         | Customer’s payment method for this order (payment gateway)                                                         |
| card_number_last_four  | Last four digits of customer’s credit card                                                                         |
| total_rows             | A list of “total” rows containing total pricing information                                                        |
|  label                 | The label of the total row (Subtotal, Tax, Grand Total, etc.)                                                      |

## Recent Items

**Description:** Items the customer has recently viewed. (Called on the default `templates/pages/account/recent-items.html` template.)

**Handlebars Expression:** `{{customer.recently_viewed_products}}`

**Object Properties:** References the standard [product card model](/stencil-docs/stencil-object-model-reference/stencil-objects/common-objects/common-product-card-model).

## Customer Wishlists

**Description:** Array of product wishlists, specific to this store, for the customer. (Called on the default `templates/components/account/wishlist-list.html` partial.)

**Handlebars Expression:** `{{customer.wishlists}}`

**Object Properties:**

| Property    | Description                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| id          | Unique system ID of the wishlist                                                                                                                                               |
| num_items   | Number of items in the wishlist                                                                                                                                                |
| name        | Customer-defined name of the wishlist                                                                                                                                          |
| is_public   | Boolean value indicating whether the wishlist is publicly available                                                                                                            |
| is_editable | Boolean indicating whether the "Remove Item" button, and account navigation controls, are displayed (i.e., whether the customer viewing the wishlist is this wishlist’s owner) |
| token       | Unique public token for the wishlist                                                                                                                                           |
| view_url    | URL to view the wishlist                                                                                                                                                       |
| edit_url    | URL to edit the wishlist                                                                                                                                                       |
| delete_url  | URL to delete the wishlist                                                                                                                                                     |
| share_url   | URL to share the wishlist                                                                                                                                                      |
| Property    | Description                                                                                                                                                                    |
| id          | Unique system ID for the wishlist                                                                                                                                              |
| name        | Customer-defined name of the wishlist                                                                                                                                          |
| is_public   | Boolean value indicating whether the wishlist is publicly available                                                                                                            |
| token       | Unique public token for the wishlist                                                                                                                                           |
| share_url   | URL used to share the wishlist                                                                                                                                                 |
| items       | List of items in the wishlist; extends the product card model, adding the extra properties below:                                                                              |
|  id         | Unique system ID for this wishlist item                                                                                                                                        |
|  product_id | Product ID for the item                                                                                                                                                        |
|  remove_url | URL to remove the product from the wishlist                                                                                                                                    |


## Account Order Shipments

<b>Description:</b> Objects to manage shipments associated with a specific order details for the current customer. (Called on the default `<theme-name&gt;/templates/pages/account/orders/details.html` template.)

**Handlebars Expression:** `{{shipments}}`

<b>Object Properties:</b>

| Property             | Description                                                               |
|----------------------|---------------------------------------------------------------------------|
| date_shipped         | Shipping date for this shipment                                           |
| shipping_provider    | Carrier for this shipment                                                 |
| shipping_method      | Shipping method for this shipment                                         |
| show_shipping_method | Boolean indicating whether to display the shipping method to the customer |
| shipping_track       | Tracking information for this shipment                                    |
| url                  | Tracking URL for this shipment                                            |
| number               | Tracking number for this shipment                                         |


## Account Orders

**Description:** Objects to manage completed orders for the current customer. By default, orders sort by order id, from lowest to highest. (Called on the default `templates/pages/account/orders/all.html`and `<theme-name&gt;/templates/pages/account/orders/completed.html`  templates, and on the `templates/components/account/orders-list.html` partial.)

**Handlebars Expression:** `{{customer.orders}}`

<b>Object Properties:</b>

| Property              | Description                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------|
| pagination            | References pagination model                                                                          |
| date                  | Date this order was placed                                                                           |
| last_update_date      | Date this order was last updated                                                                     |
| id                    | ID for this order                                                                                    |
| total                 | Total value of this order                                                                            |
| status                | Status of this order ("Completed" or other)                                                          |
| return_url            | URL for returning items in this order                                                                |
| reorder_url           | URL for reordering items in this order                                                               |
| details_url           | URL for details about this order                                                                     |
| payment_instructions  | Text field defined by merchant as to payment instructions for manual gateways such as “Bank Deposit” |
| image                 | Image of the order’s first product, in Stencil image format                                          |
| items                 | Array of products in this order                                                                      |
| name                  | Name of this product                                                                                 |
| quantity              | Quantity of this product ordered                                                                     |
| refunded              | Price object that defines the amount of this product that has been refunded                          |
| expected_release_date | Expected ship date if the product is set to pre-order status                                         |
| type                  | Type of purchase; value is one of: physical, digital, giftcertificate                                |
| download_url          | URL for customer to download a digital product                                                       |
| image                 | The image for this ordered product                                                                   |
| options               | Array of additional product details (size, color, etc.), as name/value pairs                         |
| name                  | Displayed name for this category of information                                                      |
| value                 | Displayed value for this product’s entry                                                             |


## Account Returns

**Description:** Objects to manage returns for the current customer. (Called on the default `templates/pages/account/returns.html` template.)

**Handlebars Expression:** `{{customer.returns}}`

**Object Properties:**

| Property       | Description                                                                                                                                                                                                                            |
|----------------|---------------------------------|
| date_requested | Date on which the customer requested this return                                                                                                                                                                                       |
| id             | The ID for this return                                                                                                                                                                                                                 |
| quantity       | Quantity of items returned                                                                                                                                                                                                             |
| reason         | Reason for return; merchants can define actions beyond the default strings created with each store, which are: Received Wrong Product, Wrong Product Ordered, Not Satisfied With The Product, and There Was A Problem With The Product |
| action         | Return action; merchants can define actions beyond the default set created with each store (Repair, Replacement, or Store Credit)                                                                                                      |
| comments       | Comments that the customer entered with the return request                                                                                                                                                                             |
| status         | Status of the return: Pending, Received, Authorized, Repaired, Refunded, Rejected, or Cancelled            |
| product        | Array of products included in the return                                                                                                                                                                                               |
| url            | URL for this product                                                                                                                                                                                                                   |
| name           | Name of this product                                                                                                                                                                                                                   |
| options        | Array of additional product details (size, color, etc.), as name/value pairs                                                                                                                                                           |
| name           | Displayed name for this category of information                                                                                                                                                                                        |
| value          | Displayed value for this product’s entry                                                                                                                                                                                               |
| image          | Image for this product              |


## Account New Return

**Description:** Objects to handle a new return for the current customer. (Called on the default `templates/pages/account/add-return.html` template.)

**Handlebars Expression:** `{{forms.return}}`

**Object Properties:**

| Property       | Description                                                                                             |
|----------------|---------|
| order_id       | ID for the original order                                                                               |
| reasons        | Reasons for return                                                                                      |
| actions        | Return actions: an array of strings arbitrarily defined by the merchant: refund, exchange, credit, etc. |
| order_products | Array of products from the order that are available to return                                           |
| id             | ID for the product                                                                                      |
| name           | Name of this product                                                                                    |
| product_id     | ID for this product                                                                                     |
| price          | Price object that defines this product’s price                                                          |
| quantity       | Quantity of the product returned                                                                        |
| options        | Array of additional product details (size, color, etc.), as name/value pairs                            |
| name           | Displayed name for this category of information                                                         |
| value          | Displayed value for this product’s entry                                                                |


## Shipping Addresses

**Description:** Object to enable the customer to enter shipping and contact information. (Called on the default `templates/components/account/address-list.html` partial.)

**Handlebars Expression:**`{{customer.addresses}}`

**Object Properties:**

| Property    | Description                                                                           |
|-------------|---------------------------------------------------------------------------------------|
| id          | ID for this shipping address                                                          |
| customer_id | ID for this customer                                                                  |
| first_name  | First name to ship to                                                                 |
| last_name   | Last name to ship to                                                                  |
| company     | Company name to ship to                                                               |
| address1    | Street (etc.) address, first line                                                     |
| address2    | Street (etc.) address, second line                                                    |
| city        | City to ship to                                                                       |
| state       | State/province/region to ship to                                                      |
| zip         | Postal/ZIP code to ship to                                                            |
| country     | Country to ship to                                                                    |
| phone       | Addressee’s phone number                                                              |
| state_id    | ID for destination state/province/region                                              |
| country_id  | ID for destination country                                                            |
| destination | residential or commercial                                                             |
| last_used   | Boolean, indicating whether this was the last-used shipping address for this customer |
| full_name   | Full name of addressee                                                                |
| edit_url    | URL for customer to edit this shipping address                                        |
| delete_url  | URL for customer to delete this shipping address                                      |

## Payment Methods

**Description:** Object to view stored customer payment methods.

**Called on:** [`[templates/pages/account/payment-methods.html`](https://github.com/bigcommerce/cornerstone/blob/master/templates/pages/account/payment-methods.html)

**Handlebars Expression:**`{{customer.payment_methods}}`

**Object Properties:**

| Property | Description  |
|--|--|
| add_url | URL to add a payment method to this provider |
| display_name | display name set on the payment settings page for the gateway |
| methods | array |
| ↳ bigpay_token | unique ID identifying the payment method |
| ↳ billing_address | object |
|&nbsp; &nbsp; ↳ address_line_1 | Address Line One |
|&nbsp; &nbsp; ↳ address_line_2 | Address Line Two |
|&nbsp; &nbsp; ↳ city | City |
|&nbsp; &nbsp; ↳ company | Company |
|&nbsp; &nbsp; ↳ country_code |Country code |
|&nbsp; &nbsp; ↳ country_name | Country name |
|&nbsp; &nbsp; ↳ first_name | First name |
|&nbsp; &nbsp; ↳ last_name | Last name |
|&nbsp; &nbsp; ↳ phone | Phone |
|&nbsp; &nbsp; ↳ postal_code | Postal Code |
|&nbsp; &nbsp; ↳ state | State |
|  ↳ brand | Brand of card. visa. mastercard etc. |
| ↳ default_instrument | Boolean, whether the card is the default payment method for the shopper |
| ↳ delete_url | URL to delete this specific payment method |
| ↳ edit_url | URL to edit this specific payment method |
| ↳ expiry_month | Expiration month |
| ↳ expiry_year | Expiration Year |
| ↳ last_4 | Last four of card |
| ↳ provider | ID of the provider to add a vaulted card |
| ↳ expiry_year | Expiration Year |

## Edit Payment Methods

**Description:** Object to view stored customer payment methods.

**Called on:** [`templates/pages/account/payment-methods.html`](https://github.com/bigcommerce/cornerstone/blob/master/templates/pages/account/payment-methods.html)

**Handlebars Expression:**`{{customer.payment_methods}}`

**Object Properties:**

| Property | Description  |
|--|--|
| bigpay_token | unique ID identifying the payment method |
| billing_address | object |
| ↳ address_line_1 | Address Line One |
| ↳ address_line_2 | Address Line Two |
| ↳ city | City |
| ↳ company | Company |
| ↳ country_code |Country code |
| ↳ country_name | Country name |
| ↳ first_name | First name |
| ↳ last_name | Last name |
| ↳ phone | Phone |
| ↳ postal_code | Postal Code |
| ↳ state | State |
|brand | Brand of card. visa. mastercard etc. |
|default_instrument | Boolean, whether the card is the default payment method for the shopper |
| forms | Contains all the availble form fields on the update payments page. Object |
| &nbsp; ↳ action | The url to update payment methods. `/account.php?action=update_payment_method` |
| &nbsp; ↳  billing_fields | Array. The drop down for the billing country selection. |
| &nbsp; &nbsp; ↳  chooseprefix | Appears at the top of the country drop-down. Ex. `Choose a Country` |
| &nbsp; &nbsp; ↳  class_name | Field identifier Ex. `Field200` |
| &nbsp; &nbsp; ↳  id | Id of the Field Ex. `FormField_11`  |
| &nbsp; &nbsp; ↳  label | Field Label . Appears above the field. Ex. `Country`|
| &nbsp; &nbsp; ↳  name | Field identifier `FormField[2][11]` |
| &nbsp; &nbsp; ↳  options | Only returns if the field has a dropdown value |
| &nbsp; &nbsp;  &nbsp; &nbsp; ↳  label | Country label Ex. `United States` |
| &nbsp; &nbsp;  &nbsp; &nbsp; ↳  selected | This only appears in the results if the field is selected. Boolean Ex. `true` |
| &nbsp; &nbsp;  &nbsp; &nbsp; ↳  value | Country value Ex. `United States` |
| &nbsp; &nbsp; ↳  partial | The type of field. `select`, `text`, `multiline` |
| &nbsp; &nbsp; ↳  private_id | The ID of the field. (Used by the backend to identify what type of value has been provided.) e.g. "City"  |
| &nbsp; &nbsp; ↳  required |  Boolean value to indicate whether the field is required or not.|
| &nbsp; &nbsp; ↳  type |  The type of field e.g. "singleline" for a First Name text entry or "singleselect" for a Country drop down |
| &nbsp; &nbsp; ↳  validation | A JSON string used by the front-end to provide validation and error cues. |
| &nbsp; &nbsp; ↳  size |  This indicates the size of the field's box. Not used. Always empty. (Theme styles will override this anyway.)|
| &nbsp; &nbsp; ↳  value | Returns if there is a current value for the field e.g. 90210 |
| last_four | last four of the credit card |
| provider | Credit card provider |

## Add Payment Methods

**Description:** Object to add stored customer payment methods.

**Called on:** [`templates/pages/account/payment-methods.html`](https://github.com/bigcommerce/cornerstone/blob/master/templates/pages/account/add-payment-method.html)

**Handlebars Expression:**
* `{{vault}}`
* `{{countries}}`
* `{{forms}}`

**Object Properties:**

| Property | Description  |
|--|--|
| vault | Object |
|&nbsp;↳ access_token | token needed to submit with the ADD payment method form otherwise form submission will fail with 401 Unauthorized |
|&nbsp;↳ expires_at | Expiration Date in Unix Timestamp|
| countries |  countries with state information, used in the country and state drop downs when submitting the ADD payment form |
| &nbsp; ↳ code | country code |
| &nbsp; ↳ label | country name that appears in the dropdown |
| &nbsp; ↳ value | country name |
| &nbsp; ↳ name | state name |
| forms | Object |
| &nbsp; ↳ provider | ID of the provider to add a vaulted card. Ex. stripe |

## Blog

_These objects are called on the default `templates/components/blog/post.html` partial._

**Description:** Blog-specific properties for the blog feature within BigCommerce storefronts

**Handlebars Expression:** `{{blog}}`

**Object Properties:**

| Property       | Description                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------|
| name           | Blog name                                                                                              |
| url            | Blog custom url                                                                                        |
| pagination     | References pagination model                                                                            |
| posts          | A list of posts for the blog index; default sorting is by date_published, from most-recent to earliest |
| author         | Author of the blog post                                                                                |
| title          | Title of the blog post                                                                                 |
| url            | URL of the blog entry                                                                                  |
| body           | Body of the blog entry                                                                                 |
| thumbnail      | Image thumbnail for the blog entry, in Stencil image format                                            |
| date_published | Date the blog entry was published                                                                      |
| social         | Social media tags for the blog entry                                                                   |
| tags           | Tags for the blog                                                                                      |
| name           | Name for the tag                                                                                       |
| url            | URL for the tag                                                                                        |

## Blog Post

<b>Description:</b> Individual blog post object

<b>Handlebars Expression:</b> `{{blog.post}}`

<b>Object Properties:</b>

| Property       | Description                                                 |
|----------------|-------------------------------------------------------------|
| author         | Author of the blog post                                     |
| title          | Title of the blog post                                      |
| url            | URL of the blog entry                                       |
| body           | Body of the blog entry                                      |
| thumbnail      | Image thumbnail for the blog entry, in Stencil image format |
| date_published | Date the blog entry was published                           |
| social         | Social media tags for the blog entry                        |
| tags           | Tags for the blog                                           |
|  name          | Name for the tag                                            |
|  url           | URL for the tag                                             |

## Forms

### Account Form

<b>Description:</b> The form object used to edit a customer object. <br>

<b>Handlebars Expression:</b> <code>{{forms.edit_account}}</code>

<b>Object Properties:</b>

| Property     | Description     |
|--------------|-----------------|
| first_name   | First name of the customer being edited                                                     |
| last_name    | Last name of the customer being edited                                                      |
| company_name | Company of the customer being edited                                                        |
| phone        | Phone number of the customer being edited                                                   |
| error        | Message to display (generated by the BigCommerce App) when customer’s account edit fails    |
| success      | Message to display (generated by the BigCommerce App) when customer’s account edit succeeds |


### Account Address Form

<b>Description:</b> Form object presented to customers in the Add/Edit Address page. Called on the default <NOBR><span class="inline-code">&lt;theme-name&gt;/templates/components/account/address-list.html</span></nobr> partial and <NOBR><span class="inline-code">&lt;theme-name&gt;/templates/pages/account/add-address.html</span></nobr> template. <br>

<b>Handlebars Expression:</b> <code>{{forms.address}}</code>

<b>Object Properties:</b>

| Property        | Description            |
|-----------------|------------------------------|
| address_id      | ID for this shipping address         |
| shipping_fields | Array of form fields that define each shipping address for this customer; for details, see this repo: https://github.com/bigcommerce/cornerstone/tree/master/templates/components/common/forms |
| action          | URL to the proper handler (Update Address versus Save New Address)    |
| error           | Message to display when form entry fails (defined by the BigCommerce App)     |

### Wishlist Form

<b>Description:</b> Form object presented to customers on the Add/Edit Wishlist page. Called on the default <code>&lt;theme-name&gt;/templates/components/account/add-wishlist.html</code> partial and <code>&lt;theme-name&gt;/templates/pages/account/add-wishlist.html</code> template.

<b>Handlebars Expression:</b> `{{forms.wishlist}}`

<b>Object Properties:</b>

| Property  | Description                                                                   |
|-----------|-------------------------------------------------------------------------------|
| name      | Displayed name for this wishlist                                              |
| id        | ID for this wishlist                                                          |
| is_public | Boolean indicating whether this wishlist is displayed to other store visitors |
| errors    | Message to display when form entry fails (generated by the BigCommerce App)   |
| action    | URL to the proper handler (Update Wish List versus Save New Wish List)        |

### Gift Certificate Form

<b>Description:</b><b><em> </em></b>Form object used to create and edit a gift certificate object for the merchant's store. Called on the default <NOBR><span class="inline-code">&lt;theme-name&gt;templates/pages/gift-certificate/purchase.html</span></nobr> template. <br>

<b>Handlebars Expression:</b> <code>{{forms.gift_certificate}}</code>

<b>Object Properties:</b>

| Property              | Description                              |
|-----------------------|---------|
| editing               | Whether the current context is editing a gift certificate in the cart, or adding a new gift certificate                                                       |
| can_use_custom_amount | Whether the customer can enter free-text input (otherwise, must select from a drop-down list)                                                                 |
| amount_options        | If can_use_custom_amount is disabled, this variable fills the dropdown with the available options, in price object form                                       |
| minimum               | Price object that defines the minimum amount a customer can enter (when can_use_custom_amount is enabled)                                                     |
| maximum               | Price object that defines the minimum amount a customer can enter  (when can_use_custom_amount is enabled)                                                    |
| expires_in_days       | If the gift certificates expire, this will be non-0 numerical days                                                                                            |
| errors                | Server-side validation errors from the form’s submission                                                                                                      |
| themes                | A list of active gift-certificate themes (Birthday, Celebration, General, etc.), each stored as an object containing corresponding display and value children |
| display               | Birthday, Celebration, General, etc.                                                                                                                          |
| value                 | Birthday.html, Celebration.html, General.html, etc.                                                                                                           |
| action                | The action for the form                                                                                                                                       |
| cart_item_id          | If editing, this is the cart item id being edited.                                                                                                            |
| values                | An array of the form values for prefilling                                                                                                                    |
| to_name               | The recipient's name                                                                                                                                          |
| to_email              | To email address                                                                                                                                              |
| from_name             | The sender’s name                                                                                                                                             |
| from_email            | From email address                                                                                                                                            |
| message               | An optional custom message                                                                                                                                    |
| amount                | Price object that defines the amount of the gift certificate                                                                                                  |

### Contact Us Form

<b>Description:</b>Form object used to manage merchants’ "Contact Us" pages. Called on the default <code>&lt;theme-name&gt;/templates/pages/contact-us.html</code>template.

<b>Handlebars Expression:</b> <code>{{forms.contact}}</code>

<b>Object Properties:</b>

| Property         | Description    |
|------------------|-|
| success          | Boolean indicating whether form was just submitted                                              |
| name             | Boolean indicating whether name input is enabled for the form                                   |
| company          | Boolean indicating whether company-name input is enabled for the form                           |
| phone            | Boolean indicating whether phone-number input is enabled for the form                           |
| order            | Boolean indicating whether order-number input is enabled for the form                           |
| rma              | Boolean indicating whether RMA (Return Merchandise Authorization) input is enabled for the form |
| page_id          | Page ID for this contact page (there can be multiple contact pages)                             |
| captcha_url      | URL to provide an image file for a CAPTCHA field                                                |
| text             | Text content to display above the form                                                          |
| error            | Potential error that occurred during previous form submission                                   |
| recaptcha.markup | Adds reCaptcha V2                                                                               |

### Login Account Form

<b>Description:</b> Form object used to manage merchants’ "Login" page. Called on the default <code>&lt;theme-name&gt;/templates/pages/create-login.html</code>template.

<b>Handlebars Expression:</b> <code>{{forms.login}}</code>

<b>Object Properties:</b>

| Property   | Description                                                                                       |
|------------|---------------------------------------------------------------------------------------------------|
| error      | BigCommerce defined message to display when customer’s login action fails                         |
| success    | BigCommerce defined message to display when customer’s login action succeeds                      |
| reCAPTCHA  |                                                                                                   |
| enabled    | Returns 1 when reCAPTCHA is enabled and 0 when it's disabled within the BigCommerce control panel |
| public_key | Optional key used for all reCAPTCHA in your store if specified in the BigCommerce control panel   |
| markup     | HTML that adds reCAPTCHA V2                                                                       |

<div class="HubBlock--callout">
<div class="CalloutBlock--">
<div class="HubBlock-content">

<!-- theme:  -->

### Customizing Login Form Content
> Login form content can be customized in templates/components/common/alert-success.html

</div>
</div>
</div>

## Order Confirmation Objects

### Checkout Object

**Description:** Used to access checkout content and data in `templates\pages\order-confirmation.html`

**Handlebars Expression:** `{{checkout.*}}`

**Object Properties:**

| Property                     | Description                            |
|-|-|
| checkout                     |                                        |
| ↳ order_confirmation_content | default content from checkout template |
| ↳ checkout_head              | default content from checkout `<head>` |
| ↳ order                      | an order object                        |
|   ↳ id                       | the `id` of the order                  |
| ↳ header_image               | img `src` for header                   |
