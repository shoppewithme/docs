# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: Bearer [authorizationtoken]"
```

> Make sure to replace `[authorizationtoken]` with your API key.

Shoppe uses API keys to allow access to the API. You can register a new Shoppe API key at our [developer portal](https://www.shoppewith.me/oauth/applications/).

Shoppe expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer [authorizationtoken]`

<aside class="notice">
You must replace <code>[authorizationtoken]</code> with your personal API key.
</aside>

## Getting An Authorization Token

