# CORS-Anywhere Server

[CORS-Anywhere](https://www.npmjs.com/package/cors-anywhere) is a Node.js package that adds [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) headers to a proxied request. This is useful when the API provider does not natively support CORS. Without altering the headers, a request to such a provider would cause an error and prevent the request from being fulfilled.

**Tip:** You can test out the server in this repo locally by using ports `3000` or `5000` in your application and prepending `https://proxy-ibmasyzzya-uc.a.run.app/` to your API request [like this](https://github.com/Isoaxe/ravenous/blob/master/src/util/searchYelp.js#L10). However, if you want to use for a hosted website, then follow the implementation steps below.

## Implementation

The server can be implemented in one of three ways. Is is recommended to use Firebase.

### Heroku

Navigate to the [`heroku`](https://github.com/Isoaxe/cors-server/tree/master/heroku) directory and follow the steps within the `README.md` therein. Note that Heroku will [withdraw](https://devcenter.heroku.com/articles/free-dyno-hours) provision of free Dynos on 28th of November 2022. The [cost](https://www.heroku.com/pricing) will be $7 per Dyno per month thereafter.

### Firebase

Navigate to the [`functions`](https://github.com/Isoaxe/cors-server/tree/master/functions) directory and follow the steps within the `README.md` therein. This is the recommended implementation due to the issues outlined in the others above and below.

### Railway

Navigate to the [`railway`](https://github.com/Isoaxe/cors-server/tree/master/railway) directory and follow the steps within the `README.md` therein. Unfortunately the free allowance gets reached before the end of the month, so best to go with Firebase.
