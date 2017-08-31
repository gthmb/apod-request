[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/gthmb/apod-request)
# \<apod-request\>

Simple Polymer 2.0 element for integrating with NASA&#39;s Astromony Picture of the Date API

## Default usage
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="scatter-image.html">
    <div class="result-container">
        <pre id="foo-result" class="result"></pre>
    </div>
    <next-code-block></next-code-block>
    <script>
        document.querySelector('#foo').addEventListener('request-complete', (evt) => {
            document.querySelector("#foo-result").innerHTML = JSON.stringify(evt.detail, null, 4);
        });
    </script>
    
  </template>
</custom-element-demo>
```
-->
```html
<apod-request 
        id="foo" 
        api-key="MY_API_KEY"
 ></apod-request>
```

##Configuration Attributes

| Attribute | Type | Description | Default |
| --------- | ---- | ----------- | ------- |
| **api-key** | String | Your NASA api key. [Get one here](https://api.nasa.gov/index.html#apply-for-an-api-key) | |
| **hd** | boolean | Flag to request High Definition version of the image (if available) | `false` |
| **date** | String in format: *YYYY-MM-DD* | The date for which you'd like the image | today |

### Read Only, Reflected Attributes.
| Attribute | Description | Type | Default | 
| --------- | ----------- | ---- | ------- | 
| `status` | Reflects the current status of the request. Options are: `loading`, `success`, `error`, `cancelled`. | `String` | `loading` |

##Events

| Event | Desrciption |
| ----- | ----------- |
| `request-complete` | the request completed successfully |
| `request-crror` | the request completed with an error |

Example Useage
```html
<apod-request api-key="XXX"></apod-request>

<!-- to listen for an event -->
<script>
    const request = document.querySelector('apod-request');
    request.addEventListener('request-complete', (data) => {
        console.log(data.detail.url);
        ...
    }
</script>
```
