---
title: API - Reference
description: 
published: 1
date: 2022-05-19T19:47:07.772Z
tags: 
editor: markdown
dateCreated: 2022-05-19T19:47:07.772Z
---

# 📋 Reference
Aiko’s API is a HTTPS/REST API to get data from Aiko.

**_Base URL_**

```html
https://aikobot.ga/api
```
<br>

## ♻️ Versioning
> Some API versions are non-functioning anymore, and are labeled as discontinued in the table below. Trying to use these versions will fail and return **400 Bad Request**.
{.is-danger}

Aiko exposes different versions of our API. You can specify which version to use by including it in the request path like `https://aiko.disgroupdev.de/api/v{versionNumber}`. Omitting the version number from the route will route requests to the current default version (marked below accordingly). You can find the change log for the newest API version [here](/en/api/changelog).

**_API Versions_**
| Version | Status 💡       | Default ❌ |
|---------|-----------------|-------------|
| 2       | In development  |             |
| 1       | Intern only     |             |
<br>

## 🔐 Authentication

For all requests to the Aiko API must be a authorization token provided. You can get an auth token through our dashboard (Profile → API) ***Soon™***. There is an HTTP header in the format:

```html
Authorization: {authorizationToken}
```
<br>

## 🔓 Encryption

The complete API uses `TLS 1.3`. More information about `TLS 1.3` can be found [here](https://de.wikipedia.org/wiki/Transport_Layer_Security).
<br>

## 🛑 Errors

If you make a bad or invalid request to our API you’ll get an error. A full list of all errors can be found [here](/en/api/topics/errors). Here is a example error and the structure:

```json

{
	"code": 40014,
	"errors": [
		{
			"code": "INVALID_AUTHORIZATION_TOKEN",
			"message": "An invalid or unknown authorization token was provided"
		}
	],
	"message": "Unauthorized"
}

```
<br>

## 🌍 Locales
Here is a table with all locales from guilds and users:
| Code 🌐 | Language 🌍             |
|---------|--------------------------|
| de-DE   | German (Deutschland)     |
| en-US   | Englisch (United States) |
| lol-CAT | LOLCAT (Cat Kingdom)     |
<br>

## 💻 API

### Booleans
There are endpoints of this API which needs Booleans in the request. Since there is no standard case for Booleans, this API accepts for true: `True`, `true`, `1` and for false: `False`, `false`, `0`.
<br>

### Rate Limits
This API has a process for limiting and preventing excessive requests. More information about rate limits of requests can be found [here](/en/api/topics/rate-limits).