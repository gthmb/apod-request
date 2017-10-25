[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/gthmb/apod-request)
# \<apod-request\>

Simple Polymer 2.0 element for integrating with NASA&#39;s Astromony Picture of the Date API

<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="apod-request.html">
    <div class="result-container">
    <pre id="results" class="result">Result will show here</pre>
    </div>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<!-- the tag -->
<apod-request id="myRequest" api-key="my-nasa-api-key"></apod-request>

<!-- example handling -->
<script>
  const request = document.querySelector('#myRequest'),
  results = document.querySelector("#results");

  request.addEventListener('data-changed', (evt) => {
    results.innerHTML = JSON.stringify(myRequest.data, null, 2);
  });

  request.addEventListener('request-error', (evt) => {
    results.innerHTML = JSON.stringify(evt.detail, null, 2);
  });
</script>
```

## Default usage
```html
<apod-request api-key="my-nasa-api-key"></apod-request>
<!-- to listen for an event -->
<script>
    const request = document.querySelector('apod-request');
    request.addEventListener('data-changed', (data) => {
        console.log(data.detail.url);
        ...
    }
</script>
```
