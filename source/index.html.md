---
title: comvalue v1.0.0
language_tabs:
  - "'ruby": Ruby'
  - "'python": Python'
language_clients:
  - "'ruby": ""
  - "'python": ""
toc_footers: []
includes: []
search: false
highlight_theme: darkula
headingLevel: 2
generator: widdershins v4.0.1

---

<h1 id="comvalue">comvalue v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

This is a sample server

Base URLs:

* <a href="http://api.comvalue.com/v2">http://api.comvalue.com/v2</a>

<a href="http://comvalue.com/terms/">Terms of service</a>
Email: <a href="mailto:apiteam@comvalue.com">Support</a> 
License: <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache 2.0</a>

<h1 id="comvalue-orders">orders</h1>

Access to orders

## summary: get all orders

<a id="opIdgetOrders"></a>

> Code samples

`GET /order/all`

Desc: get all Orders 

<h3 id="summary:-get-all-orders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|loginToken|header|string|true|loginToken|
|lastOrderId|query|number|false|none|
|startOrderId|query|number|false|all orderID <=|
|status|query|array[integer]|false|status filter like [60,61,62] for canceled orders|
|limit|query|number|false|none|

> Example responses

> 200 Response

```json
[
  {
    "orders": [
      {
        "orderId": 0,
        "pharmacyId": 0,
        "pharmacyCustomerId": "string",
        "status": 0,
        "timeStamp": "string",
        "readByPharmacy": 0
      }
    ]
  }
]
```

<h3 id="summary:-get-all-orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid status value|None|

<h3 id="summary:-get-all-orders-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ordersRes](#schemaordersres)]|false|none|none|
|» orders|[[orderEntry](#schemaorderentry)]|false|none|none|
|»» orderId|number|true|none|none|
|»» pharmacyId|number|true|none|none|
|»» pharmacyCustomerId|string|false|none|comes from qr code|
|»» status|number|true|none|none|
|»» timeStamp|string|true|none|none|
|»» readByPharmacy|number|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_ordersRes">ordersRes</h2>

<a id="schemaordersres"></a>
<a id="schema_ordersRes"></a>
<a id="tocSordersres"></a>
<a id="tocsordersres"></a>

```json
{
  "orders": [
    {
      "orderId": 0,
      "pharmacyId": 0,
      "pharmacyCustomerId": "string",
      "status": 0,
      "timeStamp": "string",
      "readByPharmacy": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|orders|[[orderEntry](#schemaorderentry)]|false|none|none|

<h2 id="tocS_orderEntry">orderEntry</h2>

<a id="schemaorderentry"></a>
<a id="schema_orderEntry"></a>
<a id="tocSorderentry"></a>
<a id="tocsorderentry"></a>

```json
{
  "orderId": 0,
  "pharmacyId": 0,
  "pharmacyCustomerId": "string",
  "status": 0,
  "timeStamp": "string",
  "readByPharmacy": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|orderId|number|true|none|none|
|pharmacyId|number|true|none|none|
|pharmacyCustomerId|string|false|none|comes from qr code|
|status|number|true|none|none|
|timeStamp|string|true|none|none|
|readByPharmacy|number|true|none|none|

<h2 id="tocS_ApiResponse">ApiResponse</h2>

<a id="schemaapiresponse"></a>
<a id="schema_ApiResponse"></a>
<a id="tocSapiresponse"></a>
<a id="tocsapiresponse"></a>

```json
{
  "code": 0,
  "type": "string",
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|type|string|false|none|none|
|message|string|false|none|none|

