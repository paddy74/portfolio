---
description: How to configure GPG agent caching.
tags:
  - gpg
  - git
  - guide
---

# Configuring SSH Agent Caching

If your Git commit signing uses a GPG key, use `gpg-agent` &mdash; the GPG equivalent to `ssh-agent`.

Git supports multiple signing backends, including SSH and GPG. If you signing backend is not GPG, then this article will not help with commit signing. Check your signing backend by running `git config --global --get gpg.format`. If `gpg.format` is unset or `openpgp`, then the `gpg-agent` is the right path. If it is `ssh`, then you want to use [`ssh-agent` caching](./setup-ssh-caching.mdx) instead.

The GnuPG documentation identifies the relevant settings `default-cache-ttl`, `max-cache-ttl`, and separate SSH-related cache settings like `default-cache-ttl-ssh`; defaults are 600 seconds for regular cache and 1800 seconds for SSH cache.[^5]

[^5]: [Agent Options (Using the GNU Privacy Guard)](https://www.gnupg.org/documentation/manuals/gnupg/Agent-Options.html)

A typical setup looks like:

```ini
# ~/.gnupg/gpg-agent.conf
default-cache-ttl 28800
max-cache-ttl 28800
default-cache-ttl-ssh 28800
max-cache-ttl-ssh 28800
```

Restart the agent to apply any changes: `gpgconf --kill gpg-agent`.
