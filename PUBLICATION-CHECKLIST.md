# Publication Safety Checklist

Use this checklist before changing this repository from private to public and before adding major new content later.

## Repository history

- [ ] Confirm this repository was created independently and does not contain Git history copied from the private operational repository.
- [ ] Review every commit currently in this repository for sensitive content.
- [ ] Confirm no previously committed secret or private operational detail exists only in history.

## Content review

- [ ] No passwords, API keys, tokens, private keys, cookies, recovery codes, or VPN credentials.
- [ ] No private IP addresses or internal DNS records.
- [ ] No personal email addresses, phone numbers, home addresses, or other unnecessary personal identifiers.
- [ ] No internal access URLs or remote-management endpoints.
- [ ] No detailed firewall rules, ACLs, VPN configuration, or security policy that would materially aid unauthorized access.
- [ ] No exact backup locations or recovery credentials.
- [ ] No private storage mount paths unless they are demonstrably harmless and intentionally public.
- [ ] No raw logs or screenshots containing identifiers, tokens, URLs, paths, or session information.
- [ ] No copied configuration files that may contain secrets or hidden operational detail.
- [ ] No references or links that expose the private documentation repository.

## Architecture review

- [ ] Diagrams remain conceptual rather than publishing exact network topology and addressing.
- [ ] Service descriptions explain purpose without publishing administration details.
- [ ] Planned projects are appropriate to disclose publicly.
- [ ] Hardware details do not reveal unnecessary physical-location or access information.

## Final checks

- [ ] Browse the repository as if you were an unknown internet visitor.
- [ ] Check README, all Markdown files, images, attachments, Actions logs, issues, pull requests, and releases.
- [ ] Search the repo for common sensitive patterns such as `172.`, `192.168.`, `10.`, `token`, `password`, `secret`, `key`, `vpn`, `http://`, and `https://` and manually review every match.
- [ ] Confirm repository visibility is still **Private** until this review is complete.
- [ ] Only then change visibility to **Public**.

> The goal is not to remove all technical detail. The goal is to publish enough architecture and project information to be useful while keeping operational access, security, identity, and private infrastructure data out of the public record.
