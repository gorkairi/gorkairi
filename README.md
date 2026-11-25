## Hi, I'm Gorka 👋

Business student at the University of Navarra who ended up building the product
instead of writing about it.

I'm the founder and sole developer of **[UniConnect](https://uniconnect.online)**,
an app where university students propose plans and join other people's. The
problem it solves is specific: in a group chat nobody proposes anything because
not getting a reply in front of everyone is embarrassing. Here you propose,
whoever wants joins, and nobody loses face. When a plan ends, the people who
were there can connect.

**Where it is today:** ~90 real users at the University of Navarra, one partner
business, an iOS app published on the App Store, and a B2B model where student
residences pay for a private space for their residents.

Everything you see there is mine: product, code, database and the sales calls.

---

### What I work with

**Next.js 16** (App Router) · **TypeScript** · **Supabase** (PostgreSQL, Auth,
Row Level Security, Storage) · **Vercel** · **Capacitor** for iOS and Android ·
**Resend** · **Tailwind**

### Problems I've enjoyed solving

**Multi-tenant isolation that actually holds.** Each residence pays for a closed
space: only their residents get in, and nothing inside is visible from outside.
That lives in the database with Row Level Security, not in the application
layer — and I learned the hard way that a Postgres view runs with the
permissions of whoever created it and quietly bypasses the RLS underneath it
unless you mark it `security_invoker`.

**Native iOS push with no dependencies.** Web Push doesn't exist inside a
Capacitor WebView, so the App Store build was the only version of the product
with no notifications. I wrote the APNs sender from scratch: an ES256 JWT with
`node:crypto` and HTTP/2 with `node:http2`, because `fetch` in Node doesn't
speak HTTP/2. No libraries.

**A mobile app that ships without app review.** The Capacitor wrapper loads the
web app rather than bundling it, so every deploy to Vercel reaches the phone
instantly. The trade-off is Apple's minimum functionality rule, which the real
native pieces — camera and push — are there to answer.

### Also

Running a product with real users means most of the interesting work isn't
code. Pricing, talking to residence directors, finding out why a lead said no,
and writing the legal pages. I've found I like that part more than I expected.

---

### Background

- **Business Administration (bilingual)** with a Diploma in Innovation and
  Entrepreneurship, University of Navarra · 2023–2027
- **NUCB, Nagoya University of Business and Commerce**, Japan · Sep–Dec 2025
- **Imperial College London** · May 2026
- AI automation and web development at **Innomat** · 2025–present
- Spanish (native) · English (C1, Cambridge CAE)

### Reach me

[uniconnect.online](https://uniconnect.online) ·
[LinkedIn](https://www.linkedin.com/in/gorka-irisarri-gil-15899a339) ·
irigor19@gmail.com

> Most of my commits live in a private repository, so the contribution graph
> below shows the activity but not the code. Happy to walk through any of it.
