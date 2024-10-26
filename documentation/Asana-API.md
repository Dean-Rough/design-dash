---
created: 2024-10-25T23:34:17 (UTC +01:00)
tags: []
source: https://developers.asana.com/reference/rest-api-reference
author: 
---

# Overview

> ## Excerpt
> This is the interface for interacting with the Asana platform. This reference is generated from our OpenAPI Specification , and contains a comprehensive reference for objects, schemas, and endpoints available in the API. For contextual information, guides, and tutorials regarding API usage, visit ou...

---
This is the interface for interacting with the Asana platform. This reference is generated from our [OpenAPI Specification](https://raw.githubusercontent.com/Asana/openapi/master/defs/asana_oas.yaml), and contains a comprehensive reference for objects, schemas, and endpoints available in the API.

For contextual information, guides, and tutorials regarding API usage, visit our [guides](https://developers.asana.com/docs/overview).

To view the API reference for [app components](https://developers.asana.com/docs/overview-of-app-components), click [here](https://developers.asana.com/reference/ac-api-reference).

> ## 📘
> 
> Quick start
> 
> To begin making requests against the REST API, see the [quick start](https://developers.asana.com/docs/quick-start) guide.

## [](https://developers.asana.com/reference/rest-api-reference#usage)

The Asana API is a [REST](https://developer.mozilla.org/en-US/docs/Glossary/REST)ful interface with predictable resource-oriented URLs, accepts [JSON](https://www.json.org/json-en.html) or [form-encoded](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data) requests, returns JSON, and uses standard [HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview) features ([verbs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods), [response codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status), etc.)

API endpoints are relative to the following [base URL](https://swagger.io/docs/specification/api-host-and-base-path/):

```
<span data-testid="SyntaxHighlighter">https://app.asana.com/api/1.0
</span>
```

Some requests return _compact_ representations of objects in order to conserve resources and complete the request more efficiently. See [input/output options](https://developers.asana.com/docs/inputoutput-options) to customize your responses.

## [](https://developers.asana.com/reference/rest-api-reference#navigation)

-   Objects (i.e., resources in the API) are ordered alphabetically in the sidebar of this API reference
-   Object schemas can be found by selecting the object in the sidebar (e.g., [Attachments](https://developers.asana.com/reference/attachments))
-   Select an endpoint (e.g., [get a task](https://developers.asana.com/reference/gettask)) to see code samples, example requests, and responses

## [](https://developers.asana.com/reference/rest-api-reference#api-explorer)

Each API endpoint features a built-in, in-context [API explorer](https://developers.asana.com/docs/api-explorer) through which you can make requests (and see responses). For notes on enumerated values (i.e., on request properties), see [this documentation](https://developers.asana.com/docs/api-explorer#enumerated-values).

___

## [](https://developers.asana.com/reference/rest-api-reference#additional-resources)

-   [Terms & policies](https://asana.com/terms)
-   [Developer forum](https://forum.asana.com/c/api/24)
-   [Asana support](https://asana.com/support)
-   [Asana status](https://status.asana.com/)
-   [Changelog](https://developers.asana.com/docs/change-log)

-   [Table of Contents](https://developers.asana.com/reference/rest-api-reference#)
-   -   [Usage](https://developers.asana.com/reference/rest-api-reference#usage)
    -   [Navigation](https://developers.asana.com/reference/rest-api-reference#navigation)
    -   [API explorer](https://developers.asana.com/reference/rest-api-reference#api-explorer)
    -   [Additional resources](https://developers.asana.com/reference/rest-api-reference#additional-resources)
