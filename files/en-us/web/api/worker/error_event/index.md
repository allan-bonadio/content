---
title: 'Worker: error event'
slug: Web/API/Worker/error_event
page-type: web-api-event
tags:
  - API
  - Worker
  - EventHandler
  - Event
  - Reference
  - Web Workers
  - Workers
  - onerror
browser-compat: api.Worker.error_event
---

{{APIRef("Web Workers API")}}

The **`error`** event of the {{domxref("Worker")}} interface fires when an error occurs in the worker.

## Syntax

Use the event name in methods like {{domxref("EventTarget.addEventListener", "addEventListener()")}}, or set an event handler property.

```js
addEventListener('error', (event) => { });

onerror = (event) => { };
```

## Event type

A generic {{domxref("ErrorEvent")}}.  It should have a field `message`, which is the error message.  It also has fields `filename`, `lineno`, `colno`, and `erro`r, although some of those might be null.

If you don't get these fields, and you're using webpack, see https://webpack.js.org/guides/web-workers/, or look up 'Web Workers' in the Webpack documentation.

## Example

The following code snippet creates a {{domxref("Worker")}} object using the {{domxref("Worker.Worker", "Worker()")}} constructor and sets up an `onerror` handler on the resulting object:

```js
const myWorker = new Worker('worker.js');

myWorker.onerror = (ev) => {
  console.error(`Error in Worker: ${ev.filename}:${ev.lineno}:${ev.colno} - ${ev.message}`);
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
