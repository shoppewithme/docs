# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: Bearer [authorizationtoken]"
```

> Make sure to replace `[authorizationtoken]` with your API key.

Shoppe uses app credentials to get authorization tokens to allow access to the API. You can register a new app at our [developer portal](https://www.shoppewith.me/oauth/applications/) to recieve your app credentials.

Shoppe expects for the authorization token to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer [authorizationtoken]`

<aside class="notice">
You must replace <code>[authorizationtoken]</code> with your personal API key.
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

## Permissions

Shoppe uses scoped permissions to gain access to certain types of endpoints. The following scopes are available and will need to be requested at the time that an auth token is created:

Scope | Resources
--------- | -------
user | User
user_items | Item, Category, Item Option
user_orders | Order, Sale
user_popups | PopupSale
user_lives | LiveSale
user_albums | AlbumSale

## Getting An Authorization Token

> To get an authorization token, use this code:

```shell
curl "https://www.shoppewith.me/oauth/token/"
  -X POST
  -d "grant_type=password&username=[useremail]&password=[userpassword]&scope=user user_items user_orders user_popups user_lives user_albums"
  -u "[yourclientid]:[yourclientsecret]"
```

> Make sure to replace `[useremail]` with the user's email, `[userpassword]` with the user's password, `[yourclientid]` with your app's client id, and `[yourclientsecret]` with your app's client secret.

> The above command returns JSON structured like this:

```json
{
  "access_token": "Hbdf7cBzYjx5a0yv2uMxqNfHCTC0c7",
  "expires_in": 36000,
  "token_type": "Bearer",
  "scope": "user user_items user_orders user_popups user_lives user_albums",
  "refresh_token": "0MjrdEKsNhlxXtnhEGemUiZ7BnebZp"
}
```

In order to gain access to receive an authorization token, your must first register your application at our [developer portal](https://www.shoppewith.me/oauth/applications/) and follow the steps to register your application.

An authorization token can be created by using several different auth flows. The curl command to the right shows you an example request that will convert a user's email/password combo into an auth token.

## Refreshing an Auth Token

## Revoking an Auth Token