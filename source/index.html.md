--- 

title: 1derful Episode Six API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

1derful Integration APIs 

Welcome to the 1derful API. Our API will help you to create your own financial system.

**Version:** 3.0 

# TOKENS
## ***POST*** 

### HTTP Request 
`***POST*** /api/episode-six/tokens` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| X-Correlation-ID | header | Internal Request ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Customer token generated |
| 401 | Client is unauthenticated. |
| 403 | Client is unauthorised. |
| 409 | No card registered against customer. |
| 500 | Internal Server Error. |

# CREATE CARD
###The Create Card Service enables you to order a card for a customer account.
## ***POST*** 
### HTTP Request path
***POST*** `/api/episode-six/cards`
>{
  "brandId": "string",
  "userId": "string"
 } 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| X-Correlation-ID | header | Internal Request ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Card successfully ordered |
| 401 | Client is unauthenticated. |
| 403 | Client is unauthorised. |
| 415 | Bad Request. Unsupported Media Type. |
| 500 | Internal Server Error. |

# ACTIVATE-CARD
###The Activate Card endpoint can activate the card you ordered for your customer account. 
## ***POST*** 

### HTTP Request 
`***POST*** /api/episode-six/cards/{id}/activate-card` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | The internal card's id. | Yes |  |
| X-Correlation-ID | header | Internal Request ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Card pin successfully set |
| 400 | Bad request. |
| 401 | Client is unauthenticated. |
| 403 | Client is unauthorised. |
| 404 | Internal User Card not found. |
| 409 | Card is already Activated. |
| 415 | Bad Request. Unsupported Media Type. |
| 500 | Internal Server Error. |


# PUSH NOTIFICATION SUBSCRIPTION
###The Push Notification Subscription Service enables you subscribe your device to the notification feature using the mobile application.
## ***POST*** 
### HTTP Request path
***POST*** `/api/notifications/push/subscriptions`
>{
  "entityId": "string",
  "pushToken": "string"
 } 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| X-Correlation-ID | header | Internal Request ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Card successfully ordered |
| 401 | Client is unauthenticated. |
| 403 | Client is unauthorised. |
| 400 | Bad Request. Unsupported Media Type. |
| 500 | Internal Server Error. |

# PUSH NOTIFICATION
###The Push Notification Service enables you to send a notification to your mobile application.
## ***POST*** 
### HTTP Request path
***POST*** `/api/notifications/push`
>{
  "entityId": "string",
  "message": "string",
  "title": "string"
 } 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| X-Correlation-ID | header | Internal Request ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Card successfully ordered |
| 401 | Client is unauthenticated. |
| 403 | Client is unauthorised. |
| 400 | Bad Request. Unsupported Media Type. |
| 500 | Internal Server Error. |


# EVENTS
## ***POST*** 

### HTTP Request 
`***POST*** /api/episode-six/events` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| X-Correlation-ID | header | Internal Request ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Transaction event received |
| 400 | Bad request. |
| 401 | Client is unauthenticated. |
| 403 | Client is unauthorised. |
| 415 | Bad Request. Unsupported Media Type. |
| 500 | Internal Server Error. |

# HEALTH CHECK
## ***GET*** 

### HTTP Request 
`***GET*** /api/episode-six/health` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Health check successful |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
