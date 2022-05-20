---
title: OAuth2
description: 
published: 1
date: 2022-05-20T04:50:03.784Z
tags: 
editor: markdown
dateCreated: 2022-05-20T04:50:03.784Z
---

# 🎫 OAuth2
<br>

> 🚧 ***Under construction*** 🚧
{.is-warning}


> OAuth2 can only be used intern. This page is for internal use only.
> All endpoints **can not be accessed** outside from our system. 
{.is-danger}

> All of this endpoints don’t require an authorization token.
{.is-info}

<br>

## Callback
> 🟡 **POST** `/oauth2/callback`
{.is-success}

The callback route for authorizing the user. This will be used for the callback from Discord.

If no code is provided, the login will fail and the user will be redirected to the homepage. Otherwise you should be redirected to the dashboard.

**Query**
| Value | Description                                    | Required |
|-------|------------------------------------------------|----------|
| code  | The code from Discord for authorizing the user | True     |
<br>

## Invite
> 🔵 **GET** `/oauth2/invite`
{.is-succes}

Generates an invite URL for inviting Aiko.

If a guild_id is provided, the user cannot change the guild anymore.

**Query**
| Value     | Description                                    | Required |
|-----------|------------------------------------------------|----------|
| guild_id  | The id of the guild Aiko should be invited to  | False    |
<br>

## Login
> 🔵 **GET** `/oauth2/login`
{.is-success}

Redirect you to Discord to allow us to get data from our account.
<br>

## Logout
> 🔵 **GET** `/oauth2/logout`
{.is-success}

Logs the user out and redirects you to the homepage.
<br>