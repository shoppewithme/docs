# Introduction

Welcome to the Shoppe API! You can use our API to access Shoppe API endpoints, which can get information on various users, items, orders, and sales in our database.

We have language bindings in HTTP! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

<aside class="notice">
All requests to the api should be made to <code>https://api.shoppewith.me/1.1/[api_endpoint]</code>
</aside>

## Registering Your App With Shoppe

Registering your application is the first step to get started using the Shoppe API.

To get started, go to our [developer portal](https://www.shoppewith.me/oauth/applications/), and follow these steps:

1. Go to our [developer portal](https://www.shoppewith.me/oauth/applications/)
2. If you don't already have a Shoppe account, you will need to register an account.
  1. Click "Register" down at the bottom of the login form
  2. Click the "Buy" button
  3. Fill in the required information and follow the prompts
3. Click the "New Application" button on the ["Your Applications page"](https://www.shoppewith.me/oauth/applications/)
4. Fill in the following information and click "Save":
  1. <code>Name</code> should be the name of your application
  2. <code>Client id</code> keep default
  3. <code>Client secret</code> keep default
  4. <code>Client type</code> change to `confidential`
  5. <code>Authorization grant type</code> change to `Resource owner password-based`
  6. <code>Redirect uris</code> leave blank
5. Take note of your `client id` and `client secret` as those will be used to get a user access token