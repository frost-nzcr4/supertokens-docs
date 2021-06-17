---
id: overview
title: Overview
hide_title: true
---

<!-- COPY DOCS -->
<!-- ./thirdpartyemailpassword/docs/advanced-customizations/overview.md -->

# Overview

This section will guide you on overriding our default behaviour to achieve custom auth experiences. Specifically, we we will show you how to:

- **Override any UI / React component within the widgets that we provide** (if applicable): This will allow you to customize parts of the default UI without having to implement that whole UI widget from scratch

- **Override frontend functions**: This will allow you to change the way our widgets query the backend. This can be useful for operations like implementing your own session management system that works with our auth widgets.

- **Override backend functions**: This will allow you to change the behaviour of the functions that are used by the backend APIs exposed via our SDK. It can be useful for migration, using your own userID format, custom validation logic etc...

- **Override APIs**: This will allow you to override the behaviour of any of the backend APIs our SDK exposes. It can be used for post / pre API callbacks or handling custom API input / output that deviate from our API specifications.

- **Frontend Hooks**: This allows you to change the request (body, headers, url etc) that is sent to your server, handle events fired by various user actions, and control how a recipe redirects a user.

## Example use cases
Using a combination of these, it should be possible to implement functionality that we don't provide out of the box:
- Adding reCAPTCHA to the login UI
- Using your own userID format
- Splitting sign in requests across SuperTokens and your database of existing users (useful for migration)
- Custom validation of emails for auth recipes in which we don't provide a config option for email validation.
- Changing the login form to first ask the user for their email, and show different methods for signing in based on their input (useful for migration)
- Implementing your own session management flow
- Adding post API callbacks
- Disabling sign up feature entirely
- Updating the online / offline status of a user post successful session verification
- And much more...