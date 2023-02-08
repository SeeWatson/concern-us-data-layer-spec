# Share

Fire whenever a user shares content via email or social. 

The parameters page_title and page_location are automatically sent along on each page view and will contextualize this event without any additional information being needed.

## HTML Data Attributes

```html
<a href="<link_url>"
  data-ga-event="share"
  data-ga-content_type="<content_type>"
  data-ga-method="<method>"
>
```

## Javascript Code

```js

window.dataLayer = window.dataLayer || [];
dataLayer.push({
  event: 'share',
  eventModel: {
    content_type: '<content_type>',
    count_share: 1,
    method: '<method>'
  }
});
```

## Variable Definitions

|Parameter|Type|Required|Description|Example|Pattern|Min Length|Max Length|
| --- | --- | --- | --- | --- | --- | --- | --- |
|content_type|string|required|The type of content shared|blog, content, home, landing, product|
|method|string|required|The platform used to share content|email, facebook, twitter|