# Restyle Optimized One-Page Checkout

<div class="otp" id="no-index">

### On This Page
- [Working with the Optimized Checkout SCSS File](#working-with-the-optimized-checkout-scss-file)
- [Configuring the Desktop Viewport](#configuring-the-desktop-viewport)
- [Classes Available for Customization](#classes-available-for-customization)
- [Providing Customizable Options in Store Design](#providing-customizable-options-in-store-design)
- [Currency Conversion Options](#currency-conversion-options)
- [Resources](#resources)

</div> 

## Working with the Optimized Checkout SCSS File

Cornerstone includes an SCSS file that styles the Optimized Checkout page. In your local installation, this file is located at <span class="fn">cornerstone/assets/scss/optimized-checkout.scss</span>.s

You can access the most recent version of this file in the [Cornerstone repository](https://github.com/bigcommerce/cornerstone/blob/master/assets/scss/optimized-checkout.scss) (Github). All themes share the same stylesheet for the Optimized One-Page checkout, even those not based on Cornerstone, so this stylesheet applies universally across Stencil themes.

<div class="HubBlock--callout">
<div class="CalloutBlock--error">
<div class="HubBlock-content">

<!-- theme: error -->

### Customizing Checkout Restrictions
> When customizing the checkout page, you are free to change classes' contents, however, **do not** nest elements or change any class names. BigCommerce imposes these restrictions because each class here maps to multiple Optimized Checkout elements. Changing the structure or naming would break updates available in future Optimized Checkout enhancements.

</div>
</div>
</div>

## Configuring the Desktop Viewport

Within the <span class="fn">optimized-checkout.scss</span> file, to set up Optimized Checkout's responsive features, you should configure the following breakpoint to define your preferred desktop viewport size:

```css
    // TODO:
    // Configure media query to be 'desktop' breakpoint size
    // --
    @media (min-width: 801px) {
        text-align: stencilString("optimizedCheckout-logo-position");
    }
```

## Classes Available for Customization

Below are the classes provided in Cornerstone's <span class="fn">optimized-checkout.scss</span>, with the corresponding page elements that they style. _These class names and mappings are subject to change, so please check the inline comments in the <span class="fn">optimized-checkout.scss</span> file that you downloaded with your current Cornerstone release._

| **Class** | **Styles This Optimized One-Page Checkout Element:** |
|-|-|
| `.optimizedCheckout-header` | Page header. |
| `.optimizedCheckout-headingPrimary` | Top-level headings. |
| `.optimizedCheckout-headingSecondary` | Certain lower-level elements, such as descriptions of cart items. |
| `.optimizedCheckout-overlay` | Shipping Method box. |
| `.optimizedCheckout-contentPrimary` | Body text in the desktop `Order Summary`/`Order Confirmation` (cart contents); drop-down-list items; and text that summarizes completed steps. |
| `.optimizedCheckout-contentSecondary` | Text labels on check boxes, and lower-level text in the desktop Order Summary. |
| `.optimizedCheckout-button--primary` | `CONTINUE` button and final `PAY` button. |
| `.optimizedCheckout-button--secondary` | `Edit` buttons.
| `.optimizedCheckout-orderSummary` | Colors in the `Order Summary` mobile drawer/modal.
| `.optimizedCheckout-step` | Large step-number indicators on the page's left side. |
| `.optimizedCheckout-form-label` | Styles form fields like `Email Address` – the field's text-label color. |
| `.optimizedCheckout-form-input` | Styles form fields like `Email Address` – the entry box's background and border colors. |

## Providing Customizable Options in Store Design

You can determine which aspects of Optimized One-Page Checkout merchants will be able to customize with the Store Design tool.

In Cornerstone's <span class="fn">optimized-checkout.scss</span>, each SCSS class and property available has a corresponding key/value pair in the <span class="fn">config.json</span> file, which can be used as the `id` value in schema.json when [creating customizable Store Design options](/stencil-docs/store-design/schema-json-metadata).

<a id="optimized_currency"></a>

## Currency Conversion Options

You can enable the display of alternate currencies on your Stencil theme’s Optimized One-Page Checkout and order confirmation pages.

<div class="HubBlock--callout">
<div class="CalloutBlock--warning">
<div class="HubBlock-content">

<!-- theme: warning -->

### Restrictions
> The options on this page require that you first enable Optimized One-Page Checkout. Find instructions on how to do this in Enable and Restyle Optimized One-Page Checkout.

</div>
</div>
</div>

Note that regardless of the display options that you set below, transactions will always be processed in the store’s single default currency. To change that setting, see Changing Your Default Currency.

To allow shoppers to view prices in multiple currencies, you will need to add the desired currencies via the BigCommerce control panel.

Shoppers will then be able to use the Currency drop-down list, throughout the storefront, to switch displayed prices among the currencies you have enabled.

At checkout, the shopper will still be billed in the store’s default currency. As shown below, the checkout and cart templates will show an annotation about this, while flagging any converted total (in a shopper’s selected alternate currency) as an Estimated Total:

<!--
    title:
    data: //s3.amazonaws.com/user-content.stoplight.io/6116/1562870949093
-->

![](//s3.amazonaws.com/user-content.stoplight.io/6116/1562870949093 "")

## Resources

### Related Articles
* [The Complete Guide to Checkout Customization on BigCommerce](https://medium.com/bigcommerce-developer-blog/the-complete-guide-to-checkout-customization-on-bigcommerce-6b566bc36fa9) (Developer Blog)
