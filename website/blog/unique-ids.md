---
title: On the Max Length of Unique IDs
authors: pyoung
tags:
  - tech
  - auth
---

# On the Max Length of Unique Identifiers

Drawing from OAuth, there is no universal maximum for the length of an ID; user ID (`uid`), client ID, subject (`sub`), object ID (`oid`), etc. There is a technical limit that is the maximum length of a URL, but this varies such as by the browser being used.

:::info

The maximum length of a unique ID is constrained by the maximum length of a URL, which varies by the interface (i.e., browser), but can be considered a defacto limit of 2000 characters.[^4]

:::

[^4]: [StackOverflow | What is the maximum length of a URL in different browsers?](https://stackoverflow.com/a/417184/7706917)

However, OpenID v1.0 does mention limits under [Appendix D. Limits](https://openid.net/specs/openid-authentication-1_1.html#limits):

> Identifier URL: 255 max bytes Identity Provider URL: 2047 max bytes, after Consumer-added URL arguments. The raw endpoint URL SHOULD be kept well below this. return_to URL: 2047 max bytes, after Identity Provider added URL arguments. The raw return_to URL SHOULD be kept well below this. assoc_handle: 255 characters or less, and consist only of ASCII characters in the range 33-126 inclusive (ie printable non-whitespace characters).

Some providers document length limits, such as in the [Google API Documentation](https://developers.google.com/identity/protocols/oauth2#size) where the maximum length of an access token is 2048 bytes. But other documentation within the same provider can conflict[^1]; the only consistency is that lenghts may vary. For example, Facebook's API documentation warns:

> Expect that the length of all access token types will change over time as Facebook makes changes to what is stored in them and how they are encoded. You can expect that they will grow and shrink over time. Please use a variable length data type without a specific maximum size to store access tokens.[^2]

[^2]: [Facebook Login Docs | Access Token Guide](https://developers.facebook.com/docs/facebook-login/guides/access-tokens#size)

[^1]: [Google Cloud Documentation | IAM Tokens](https://cloud.google.com/iam/docs/reference/sts/rest/v1/TopLevel/token#response-body). _"Tokens can vary in size, depending in part on the size of mapped claims, up to a maximum of 12288 bytes (12 KB). Google reserves the right to change the token size and the maximum length at any time."_

As of this writing, the most direct answer found was by Auth0, who _suggested_ using a 32 characters random UUID.[^3]

[^3]: [Auth0 Community | Is 256 a safe max length for a user_id?](https://community.auth0.com/t/is-256-a-safe-max-length-for-a-user-id/34040/6)

In conclusion, **64-bits** (20 digits) are enough for current application and **128-bits** (32 digits) are recommended for future proofing (e.g., with `VARCHAR(128)`).
