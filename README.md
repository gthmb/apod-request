[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/gthmb/apod-request)
# \<apod-request\>

Simple Polymer 2.0 element for integrating with NASA&#39;s Astromony Picture of the Date API

<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="scatter-image.html">
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
<apod-request id="myRequest" api-key="Q2S9UOPbcMVSPCCL8uIjI7Mq7dTgGnW4VBUiiuo1"></apod-request>

<!-- exmaple handling -->
<script>
  document.querySelector('#myRequest').addEventListener('request-complete', (evt) => {
    document.querySelector("#results").innerHTML = JSON.stringify(evt.detail, null, 2);
  });
  document.querySelector('#bar').addEventListener('request-error', (evt) => {
    document.querySelector("#results").innerHTML = JSON.stringify(evt.detail, null, 2);
  });
</script>
```

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
