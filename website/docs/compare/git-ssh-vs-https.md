---
tags:
  - git
---

# Connecting to Git: SSH vs HTTPS

> Git can use four distinct protocols to transfer data: Local, HTTP, Secure Shell (SSH), and Git.[^1]

[^1]: [Git on the Server - The Protocols](https://git-scm.com/book/ms/v2/Git-on-the-Server-The-Protocols)

This article will provide a comparison between the two most widely used options for authenticated connections with remote repositories: SSH and HTTPS.

## Feature Comparison

| Criteria | SSH | HTTPS |
| --- | --- | --- |
| Default Port | 22 | 443 |
| URL Format | `git@server:group/repo.git` or `ssh://...` | `https://server/group/repo.git` |
| Encryption | SSH-native encryption | TLS (HTTPS) |
| Credential Caching | `ssh-agent` | Git credential helpers |
| Firewall-Friendly | Usually blocked (port 22) | Usually allowed (HTTPS) |
| Anonymous Access | Requires SSH account and key for read-only clones | Supported with anonymous HTTP read-only |
| Setup Complexity | Key management and server config | Web server config; no client key setup required |
| Typical Use | Private repos, CI pipelines, automation | Public repos, proxy environments, general use |

## Recommendation

| Use Case | Recommendation |
| --- | --- |
| Controlled, private environments where managing user access with keys is acceptable and interactive credential prompts are undesirable (e.g., CI pipelines, automation). | SSH |
| Publicly exposed environments where ease of setup, firewall compatibility, and single-URL access for both read/write (with auth) and anonymous cloning are prioritized. | HTTPS |

---

## Secure Shell (SSH)

Secure Shell (SSH) provides an encrypted tunnel for Git traffic, using TCP port 22 by default. It authenticates users via public/private key pairs managed through the local `ssh-agent` and the server's `authorized_keys` file, allowing push and pull operations without interactive credential entry.

### SSH Setup

| Server-Side | Client-Side |
| --- | --- |
| Run an SSH daemon; configure `authorized_keys`; manage user accounts. | Generate key pair (`ssh-keygen`); add to agent; distribute public key. |

### SSH Authentication

Users generate an SSH key pair (`ssh-keygen`) and install the public key on the server. The client's private key, optionally protected by a passphrase and managed by an SSH agent, is used to authenticate each Git session automatically.

### SSH Encryption

Encryption is provided by the SSH protocol itself, protecting all data in transit and authenticating both client and server using key-based cryptography.

---

## HTTPS

Smart HTTP uses the HTTPS protocol (TCP port 443), wrapping Git operations in TLS encryption. Repositories served over HTTPS can require HTTP-based authentication mechanisms—such as username/password or personal access tokens—and leverage standard web server capabilities (e.g., `git-http-backend`) to handle both anonymous (read-only) and authenticated (read/write) requests over the same URL.

### HTTPS Setup

| Server-Side | Client-Side |
| --- | --- |
| Configure web server with `git-http-backend` CGI; enable TLS certificates. | No key management; clone via URL; optionally configure credential helper. |

### HTTPS Authentication

Clients authenticate using HTTP Basic Auth with a username and password or, more securely, a personal access token (PAT). Credentials can be cached locally using Git credential helpers (e.g., Keychain, Windows Credential Manager, or `git-credential-store`) to avoid repeated prompts.

### HTTPS Encryption

Git over HTTPS uses standard TLS encryption, ensuring confidentiality and integrity of data transfers. Since HTTPS is firewall-friendly, it passes through most proxies without additional configuration.
