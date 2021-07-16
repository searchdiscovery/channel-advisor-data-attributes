# Channel Advisor URL Attributes

Add these HTML data attributes to each outbound retailer link to enable Google Tag Manager to easily pick up the data.

## HTML Data Attributes

```html
<a href="whatever.com" 
  data-layer-wtb_link="true"
  data-layer-link_cta_type="wtb_retailer" 
  data-layer-affiliation="amazon"
  <!-- other attributes here -->
>
```

## Variable Definitions

|Field|Type|Description|Example|
| --- | --- | --- | --- |
|affiliation|string|This attribute will be used to report on which retailers users are visiting to buy products. This should always follow a consistent naming convention, as determined by Channel Advisor. For example, it should not be "amazon" in one widget/location and "amazon.com" in another. If domain names are to be used, use them consistently.|amazon, walmart|
|link_cta_type|string|This attribute will be used to report on which type of where to buy link was clicked.|wtb_add_to_cart, wtb_buy_now, wtb_local_buy_online|
|wtb_link|static|This attribute is used to identify this as a where to buy exit link. While a value isn't explicitly required here to get tracking working, it is probably good practice to add it. Always set this to the string "true".|"true"|

## Example
```html
<a href="whatever.com" data-layer-wtb_link="true" data-layer-link_cta_type="wtb_buy_now" data-layer-affiliation="amazon">
```