# Services, Stack, and Cost Estimate

## 1. Planning note

This document estimates likely third-party services for SBBC.

The exact stack should stay lean at the beginning. Do not buy everything up front. Some services should only be added when the corresponding version is being built.

## 2. Recommended baseline stack

### Core

- Vercel: application hosting
- Cloudflare: DNS, WAF, domain layer
- Supabase: database, auth, storage, realtime
- Resend: transactional email
- Stripe: online payment

### Add later for online learning

- Video hosting: Cloudflare Stream or Mux
- Live classes: LiveKit or third-party meeting links first

## 3. Estimated service plan by phase

### V1 baseline

- Vercel Pro
- Cloudflare Pro or Free + selected add-ons
- Supabase Pro
- Resend free or entry paid tier
- Stripe pay-as-you-go

### V2-V3 baseline

- Vercel Pro with team seats as needed
- Cloudflare Pro
- Supabase Pro with possible storage / compute increase
- Resend paid tier
- Stripe

### V4 online learning baseline

- Add video hosting
- Add live class infrastructure or managed provider
- Increase storage and bandwidth allowance

## 4. Service pricing snapshot

These prices should be rechecked before purchase.

### Vercel

- Pro: `$20/month` per developer seat
- Official source: [Vercel pricing](https://vercel.com/pricing)

### Supabase

- Pro: `from $25/month`
- Micro compute: `$10/month`
- Small compute: `$15/month`
- Medium compute: `$60/month`
- Custom domain add-on: `$10/domain/month/project`
- Official source: [Supabase pricing](https://supabase.com/pricing)

### Resend

- Scale: `$90/month` for `100,000 emails/month`
- Official source: [Resend pricing](https://resend.com/pricing)

Note:

- Resend also offers smaller tiers, but the official page content retrieved here clearly exposed the `Scale` plan. For early SBBC use, the actual starting cost may be lower depending on email volume.

### Cloudflare

- Pro: `$20/month billed annually` or `$25/month billed monthly`
- Business: `$200/month billed annually` or `$250/month billed monthly`
- Stream: `starting at $5/month`
- Official source: [Cloudflare pricing](https://www.cloudflare.com/plans/)

### LiveKit

- Ship: `starting at $50/month`
- Scale: `starting at $500/month`
- Official source: [LiveKit pricing](https://livekit.com/pricing)

## 5. Practical monthly budget scenarios

### Scenario A: V1 lean launch

Assumption:

- One main production app
- Low to moderate traffic
- CRM and forms active
- No built-in live/video platform yet

Estimated monthly tools cost:

- Vercel Pro: `$20`
- Supabase Pro: `$25`
- Cloudflare Pro: `$20 to $25`
- Resend: `$0 to $30+` depending on volume and chosen tier
- Stripe: variable transaction fees only

Estimated total:

- Roughly `$65 to $100+ / month`, excluding payment fees

### Scenario B: V2-V3 operations platform

Assumption:

- Admin and teacher workflows are active
- Student portal is active
- Storage and email usage grow

Estimated monthly tools cost:

- Vercel Pro: `$20 to $40`
- Supabase Pro plus compute/storage growth: `$25 to $100+`
- Cloudflare Pro: `$20 to $25`
- Resend: `$20 to $90+`
- Stripe: variable

Estimated total:

- Roughly `$85 to $255+ / month`, excluding payment fees

### Scenario C: V4 with online learning

Assumption:

- Recorded lessons available
- Live classes supported
- Higher storage, delivery, and media usage

Estimated monthly tools cost:

- Vercel Pro: `$20 to $40`
- Supabase: `$60 to $210+`
- Cloudflare: `$20 to $25`, plus optional media products
- Email: `$20 to $90+`
- Video / live: `$50 to $500+` depending on provider and usage
- Stripe: variable

Estimated total:

- Roughly `$170 to $865+ / month`, excluding payment fees and heavy media overages

## 6. Recommended purchasing order

Buy in this order:

1. Domain and DNS
2. Hosting
3. Database/auth
4. Transactional email
5. Payment gateway
6. Video/live services only when V4 is ready

## 7. Services SBBC probably does not need immediately

- Enterprise observability tools
- Separate BI warehouse
- Dedicated search engine cluster
- Full LMS vendor subscription
- Separate finance ERP

## 8. Source links

- [Vercel pricing](https://vercel.com/pricing)
- [Supabase pricing](https://supabase.com/pricing)
- [Resend pricing](https://resend.com/pricing)
- [Cloudflare pricing](https://www.cloudflare.com/plans/)
- [LiveKit pricing](https://livekit.com/pricing)
