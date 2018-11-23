---
title: "OAuth & Scopes"  
category: "Profile"  
tags: ["oath", "profile", "login", "Developer Portal", "scopes"]  
description: "This page describes the authorizations and scopes"
---

## 1 Introduction

### 1.1 OAuth

OAuth is a standard for access delegation. It is commonly used as a way for users to grant websites or applications limited access (scopes) to their data without providing their credentials. Mendix uses [OAuth 2.0](https://oauth.net/2/).

In other words, OAuth allows a user with an account from one website/application to use those credentials to connect to another website/application. The process generally looks like this:

1. The user goes to the login page of website A and clicks the button for logging in with credentials from website B.
2. The user is asked to authenticate themselves on website B.
3. Website B confirms the identity of the user to website A.

### 1.2 Scopes

Once the user is authenticated by website/application B, website/application A has a guarantee of their real identity. OAuth also provides more complex functionality. For example, website/application B can communicate a set of information (for example, the email address or profile picture) and a set of rights to website/application A. This can only happen if the user grants certain rights.

For example, if the user grants website/application A permission to send their profile picture and last name to website/application B (through a specific authorization page), then website/application B can display that information on their website. The scopes are the access rights to that information granted manually by the user during the authentication process.

Here is an example page where a user is asked to accept scopes on their Mendix account so that Wikipedia can access their profile information and display their name:

![Authorize Page](attachments/authorize_page.png) 

## 2 Scopes

The following Mendix scopes provide access to data with user consent. They are generated automatically within the Developer Portal.

This information is provided so that you can make an informed decision on whether you want to authorize or cancel the request for access to your personal information or app.

### 2.1 Profile Scope {#profile}

With this scope, a website or application can access the user's basic profile information as recorded in Mendix. This scope contains the following data:

* User’s full name
* User’s preferred username
* User’s avatar
* URL of the user's personal website or blog

### 2.2 Email Scope {#email}

With this scope, a website or application has access to the user's email address.

### 2.3 OpenID Scope {#openid}

This is one of the most common scopes. With this scope, website A (for example, Mendix) is informed that website B (for example, Wikipedia) wants to authenticate the user. Website B then receives the user's unique identifier.

### 2.4 Mendix Profile Scope {#mx:user:profile:v1:read}

This scope is an extension of the [profile scope](#profile). With this scope, a website can access the user's Mendix profile for the following user data:

 * OpenID2 identifier
 * Username
 * Display name
 * Avatar
 * Biography
 * URL of the user's personal website or blog
 * Phone number
 * Job title
 * Name of the company the user belongs to
 * Mendix internal identifier of their company
 * Department (in their company)
 * Location (via their company)
 * Country (via their company)
 * LinkedIn profile
 * Twitter account
 * Skype account
 
### 2.5 Create a Mendix Application Scope {#mx:app:create}

This is a Mendix-specific scope. It is used by internal Mendix applications as well as by SAP and IBM (as strategic Mendix partners). This scope allows an application or partner to create a Mendix application on behalf of the user.

### 2.6 Change the Deployment Cloud Target of a Mendix Application Scope {#mx:app:cloudswitch}

This is a Mendix-specific scope. It is used by internal Mendix applications as well as by SAP and IBM (as strategic Mendix partners). This scope allows a website/application to change platform to which an app will be deployed.
