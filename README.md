---
description: Formally Known as vNative
---

# Introduction

## **Before You Start**

The Trackier API is designed for developers, engineers, or anyone else who’s comfortable creating custom-coded solutions or integrating with **RESTful APIs**.

## **Authentication**

Go to your Network and Generate API Key from /admin/settings.html then after getting the API key, you need to whitelist your server IP Address to make requests to the network API

**Api End Point:**

`http://api.vnative.com/`

`http://{network}/`

When requesting the api you need to pass api key for authenticating the request in the Header **X-Api-Key** or **Query Parameter - apiKey**

```bash
curl -H "X-Api-Key: {key}" "http://api.vnative.com/api/affiliate"
```

```text
curl "http://api.vnative.com/api/affiliate?apiKey={key}"
```

## **JSON**

The API only supports JSON. HTTP POST parameters, most POST and PATCH requires json body.

## **HTTP Methods**

The API supports 5 [HTTP methods](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) for interacting with resources:

* **GET**

Make a GET request to retrieve data. GET requests will never cause an update or change to your data because they’re safe and [idempotent](http://restcookbook.com/HTTP%20Methods/idempotency/).

* **POST**

Use a POST request to create new resources. For example, make a POST request to a collection endpoint \(like \/lists\) where the body of your request JSON is a new list.

* **PUT**

Use a PUT request to update the resource with the new resource provided with the request body. The request body should be in JSON.

* **PATCH**

Make a PATCH request to update a resource. With PATCH requests, you only need to provide the data you want to change.

* **DELETE**

Make a DELETE request to remove a resource.

## **SSL**

We give a valid, signed certificate for all API methods. If you’re manually coding submit URLs, change http to https in the URL, and make sure your connection library supports HTTPS. We will Support SSL from January

## **Parameters**

There are 4 main categories of parameters for each endpoint in the Trackier API: path, query string, request body, and response body. The API Reference includes a list of all available parameters for each possible request, but these sections offer an overview of the 4 main categories and their subcategories.

## **Errors**

We expose API errors in two ways: standard HTTP response codes and human-readable messages in JSON format. For example, the following code snippet shows an HTTP 405 error in the response headers:

And this snippet shows the human-readable error as a JSON object, we recommend reviewing the Application Error Codes for more context to help you troubleshoot.

For HTTP response codes, 4xx codes suggest a bad request. If you receive a 4xx response, we recommend reviewing the Http Status Codes for more context to help you troubleshoot.

Otherwise, you’re welcome to contact our support team\[support@trackier.com\]. If you contact support, we recommend including the complete request you’re trying to make and the error code and response you’re receiving so they can help as quickly as possible.

## **Http Status Codes**

**Review all global errors for the Trackier API so you can get back to work fast.**

_**401**_

**API Key Invalid**

_Your API key may be invalid, or you’ve attempted to access the wrong data center._

The current request requires user authentication. For example, the user does not have the necessary credentials.

_**403**_

**No permissions visit this resource.**

_You are not permitted to access this resource._

The request was a valid request, but the server is refusing to respond to it. For example, the user does not have the necessary permissions for the resource.

_**404**_

**Resource Not Found**

_The requested resource could not be found._

This error tells you a specific resource doesn’t exist. It’s possible that the resource has been moved or deleted, or that there’s a typo in your request.

_**500**_

**Server error,Please contact your administrator**

_A generic error message, given when an unexpected condition was encountered and no more specific message is suitable.Please contact Support for more information._

This error lets you know our servers have experienced a problem. Although this is rare, please contact support@vnative.com to let us know that you’ve encountered this error.

_**501**_

**Request uri not found**

_The requested uri resource could not be found._

The server either does not recognize the request method, or it lacks the ability to fulfill the request.

## **Application Error Codes**

| **Code** | **Message** |
| :--- | :--- |
| 0 | Success |
| 5 | Insufficient Permission |
| 11 | Operation Not allowed |
| 12 | Unauthorized Request |
| 13 | Invalid API Key |
| 20 | Request Parameter Error |
| 30 | Bad Request |
| 31 | Resource Not Found |
| 32 | Invalid Request Method |
| 33 | Duplicated Resource |
| 40 | Too Many Request |
| 41 | Request IP Not Whitelisted |
| 42 | Account is locked |
| 50 | System upgrade |
| 51 | Server Internal Error |
| 60 | Illegal Operation |

