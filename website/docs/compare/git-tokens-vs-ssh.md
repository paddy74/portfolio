---
tags:
  - git
---

# Comparing Tokens and SSH Keys for Git Authentication

Although both SSH keys and tokens are **unique**, **revocable**, and **random** - tokens are also **limited** in comparison to SSH keys in that the have their own [scoped permissions](https://docs.github.com/en/developers/apps/scopes-for-oauth-apps#available-scopes).

SSH keys can be read-only, read-write enabled, or scoped to specific repositories. In comparison, personal access tokens have a finer-grained permissions model. This is why GitHub recommends tokens instead of SSH keys[^1].

[^1]: [GitHub Blog | Token authentication requirements for Git operations](https://github.blog/security/application-security/token-authentication-requirements-for-git-operations/)

> Tokens offer a number of security benefits over password-based authentication:
>
> - Unique - tokens are specific to GitHub and can be generated per use or per device
> - Revocable - tokens can can be individually revoked at any time without needing to update unaffected credentials
> - Limited - tokens can be narrowly scoped to allow only the access necessary for the use case
> - Random - tokens are not subject to the types of dictionary or brute force attempts that simpler passwords that you need to remember or enter regularly might be
