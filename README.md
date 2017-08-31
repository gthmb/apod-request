[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/gthmb/apod-request)
# \<apod-request\>

Simple Polymer 2.0 element for integrating with NASA&#39;s Astromony Picture of the Date API

## Default usage
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
