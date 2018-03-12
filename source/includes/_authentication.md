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

## Getting An Authorization Token

In order to gain access to receive an authorization token, your must first register your application at our [developer portal](https://www.shoppewith.me/oauth/applications/).

An authorization token can be created by using several different auth flows.