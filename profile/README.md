# BinDist

### Distribute software to your business customers

Stop emailing builds. BinDist gives every customer their own API-keyed feed,
so they get exactly the releases they've licensed and nothing else.
Hosted in the EU 🇪🇺.

[Website](https://www.bindist.eu) · [Documentation](https://docs.bindist.eu) · [Pricing](https://www.bindist.eu/pricing.html) · [Start free](https://www.bindist.eu/signup.html)

## Who it's for

- **Software vendors and ISVs** who ship to specific customers rather than the public. Each
  customer gets an API key that only unlocks the applications they've bought.
- **Bespoke software developers** delivering to many clients. One dashboard with permanent
  download links and a full version history for every customer.
  [More →](https://www.bindist.eu/bespoke-software-delivery.html)
- **Apps that update themselves.** Ask BinDist for the latest version and download it from
  inside your application, without building your own update server.
  [More →](https://www.bindist.eu/software-update-api.html)

## Security first

Your builds are your product, and the release pipeline is an attack target. BinDist is built
so that one leaked credential can't ship a bad build to your customers.

- 📱 **2FA to release.** Uploading a build doesn't make it live. With 2FA on, promoting it to
  your customers needs a TOTP second factor, so a stolen CI token can upload but can't publish.
- 🧪 **Test before anyone sees it.** New versions sit on a test channel, which only clients that
  explicitly ask for test builds can see, until you promote them to everyone.
- 🗝️ **Split admin roles.** Publishing uses one admin key; billing, backups, the audit log and
  tenant settings use another. A leaked publishing key can't take over your account or cover
  its tracks.
- 🎯 **Per-customer access you control.** Every customer has their own key, scoped to what
  they've licensed. Revoke one customer or rotate their key without affecting anyone else.
- ⏱️ **Links that don't travel.** Downloads go through signed URLs that expire after
  30 minutes, so a forwarded link stops working.
- ✅ **Verifiable downloads.** Every file has a checksum, and the client libraries can check
  it as they download.
- 📜 **Audit log** of every administrative action, so you can see exactly what changed and when.
- 🇪🇺 **EU-hosted** on Scaleway, a European cloud provider, with data stored in the EU.

## What you get

- 🔑 **Per-customer API keys**: each customer only sees the applications they're entitled to
- 📦 **Version management**: multi-file releases, release notes and checksums, plus a test
  channel for pre-releases
- 🚀 **CI/CD friendly**: upload straight from your build pipeline.
  [More →](https://www.bindist.eu/ci-cd-software-distribution.html)
- 📊 **Download analytics and audit logs**: see who downloaded what, and when
- 🔗 **Expiring share links** for one-off downloads
- 🤖 **Optional AI documentation assistant**: answers questions from your own docs and
  release notes

## Open source

BinDist's core is open source: [**bindist-terraform**](https://github.com/BinDist/bindist-terraform)
runs it on your own AWS or Scaleway account. You can also use the hosted service and let us run
the infrastructure.

Client libraries are available for **Go, JavaScript/TypeScript, Rust, Python, Delphi
and others**. Pick one from the repositories below, or see the
[SDK docs](https://docs.bindist.eu).

Using another language? BinDist is a plain REST/JSON API with API-key authentication, so
writing your own client takes very little code. The
[API reference](https://docs.bindist.eu/api/overview.html) has everything you need.
