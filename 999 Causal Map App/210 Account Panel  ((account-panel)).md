<div class="user-guide-callout">
<strong>👤 What you can do here:</strong> View and manage your personal account settings. Change your password, update your project information, and control your privacy and security settings. This is also where you can export your data or delete your account if needed.
</div>

<span class="badge bg-info text-dark" style="margin-left:6px;">Making projects private requires a Private subscription</span>

User account management and project settings.

**Onboarding (first sign-up):** When you sign up, we ask a few questions including whether you want AI options switched on and active right at the start, and what you want to do first in the app. If you choose an AI-first workflow, AI is switched on automatically. If AI is off, there are no AI services at all (except basic MapCat help); you can change this anytime in Account settings. If AI is on, you get 10 free AI credits per month, and the AI switch is turned on by default; you can turn it off later in Account settings.

**AI coding toggle ("AI options switched on and active"):** Turn on to use AI; turn off and there are no AI services at all (except basic MapCat help). You can change this anytime in Account settings. When you turn it **on**, a warning modal appears: your data is sent to AI providers when you use AI; it is **not** used to train models; OpenAI (GPT) may retain data for up to 30 days for abuse monitoring; Vertex AI and DashScope do not retain data; see our [privacy policy](https://www.causalmap.app/privacy-policy/). Credits when on depend on your plan (Free: 10, Private: 100, Pro: 1000, Team: 2000/month). **Plans without AI** (e.g. Private Manual) can turn on to try with 10 credits/month (free credits do not stack with paid AI plans).

**Where AI runs is a project setting, not a user setting.** Each project has an **AI Processing Region** (Project → Edit project → AI Processing Region) with three options: **EU (Belgium, europe-west1)**, **UK (London, europe-west2)**, or **US (Virginia, us-east5)**. New projects default to EU.

When the region is **EU or UK**, the app guarantees every AI call stays in Europe:

- The model picker is filtered to **Gemini 2.5 Pro** and **Gemini 2.5 Flash** only. Faster models like Gemini 3.5 Flash and Gemini 3.1 Pro are hidden because they route through Google's global endpoint, not a European region.
- Any AI request that would process data outside Europe is blocked client-side before it leaves the browser. A notification explains which model or region caused the block and how to fix it.
- Document embeddings (used by RAG and similarity search) automatically route to `europe-west1` (or `europe-west2` for UK), instead of the default `us-central1`.

When the region is **US**, the model picker shows the full list, including Gemini 3.5 Flash, Gemini 3.1 Pro Preview, GPT-5, Qwen and others. These are faster or more capable, but they process your prompts and data outside Europe.

Switching the region for an existing project takes effect immediately — the dropdowns re-render and the gate updates without a reload.

You can change this toggle anytime.

**Account Features:**
- <i class="fas fa-user"></i> project information and settings
- <i class="fas fa-key"></i> Password and security management
- Account deletion and data export
- Subscription and billing information

### 2FA (beginner guide)

If your organisation asks you to use 2FA, do this in **Account → Two-factor authentication**:

1. Turn on **Require two-factor authentication on sign-in**.
2. Sign out, then sign in again.
3. If asked, scan the QR code in your authenticator app.
4. Enter the 6-digit code to finish setup.

If codes do not work:
- Try a different Causal Map entry in your authenticator (you may have old entries).
- Use **Delete all 2FA factors** in the same card, then sign out/in and set up again.

For strict org policy:
- Click **Require 2FA permanently**.
- This is one-way in the app UI and keeps 2FA locked on for that account.

### Image export resolution

Controls resolution for all image capture (map copy/download, bookmarks, pivot/table screenshots, PDF export). Options: 1× (default), 2×, 3×. Resets to 1× on page load. **1× is already very good** for most uses; higher values produce larger files and may hit clipboard limits on large maps.

### Subscriptions

#### Subscriptions List

Users without a subscription are either:
- anonymous (not logged in) (this is disabled at present)
- free (logged in)

Subscriptions (via LemonSqueezy) are available in the Account panel. Monthly and Annual plans are recurring subscriptions: a Monthly plan renews and is charged each month until the subscription manager cancels it.

To manage billing, update payment details, or cancel a subscription, open **Account → Your subscriptions** and click **Manage in LS**. This opens the Lemon Squeezy customer portal. Only the subscription manager/purchaser sees this button; users who only have a seat on someone else's subscription should ask the manager to make billing changes.

Admins can also create **manual subscriptions** (for testing/support). These are stored in the same `subscriptions_purchased` table but do **not** come from Lemon Squeezy.

The subscriptions list uses one row per type (private, pro, team) with seat-count, square radio buttons for monthly/annual and Manual/AI, and a live-updating price (from a JSON price file). Each row includes a text description.

<!-- Pricing details:
- Annual price = 8 × monthly rate
- Seats dropdown: 1–100
- Multi-seat discount: total × n^0.9
- Price display updates when Add AI is toggled to include AI price
-->

There are three dimensions to the subscriptions, 

Manual vs AI,  

Type:
- private
- pro
- team

Monthly vs Annual.

**AI credits (when you have AI):** Free users who opt in get 10 credits/month. Private AI: 100. Pro AI: 1000. Team: 2000. Credits renew at the start of each month and do not roll over. See [Responses Panel](../responses-panel/) for usage. Plans without AI (e.g. Private Manual) can turn on the AI toggle in Account to try with 10 credits/month. 

User can purchase multiples of one or more subs to distribute to colleagues. 

<!--
Types are selectable with options in the gallery; purchases are simulated for now to streamline evaluation.

Underlying storage uses Supabase tables. Each user can buy more than one subscription and allocate seats to colleagues' emails. Data captured includes manager email, subscriber emails (JSON), date, duration, and number of seats.


Each subscription row has a seat-count dropdown (1–100). After purchase, a modal collects subscriber emails, prefilling the first with the current user's email. 



--#### Subscriptions Table


The Subscriptions card shows a single simple table listing subscriptions where you are manager or subscriber, including manager email, subscriber emails, and other details, with an Edit button (for subscriptions you manage) that opens the subscriber-email modal.

**Renewals (Lemon Squeezy):** your renewal dates are synced automatically when you open/refresh the app while signed in. Admins can also manually trigger a sync per subscription from the table.

**Expiry reminder emails:** subscription rows sync a few safe contact properties to Loops (`subscriptionEndDate`, `subscriptionStatus`, etc.). Loops date-based automations can then send 7-day, 1-day, and expired reminders. This covers both Lemon Squeezy rows and admin/manual rows because both use `subscriptions_purchased`.

#### Private projects and subscription expiry {#private-projects-and-subscription-expiry}

**Free plan:** new projects are created **public** by default.

**Paid plans with Private capability** (Private, Pro, Team, etc.): you can create and keep **private** projects (`is_public = false`).

**When that paid plan expires:**

- Existing private projects **stay private**. The app and database **never** auto-set `is_public = true` on a project that was private.
- Those projects are **archived and locked** (read-only) so collaborators cannot keep editing after expiry.
- They remain visible to the owner (and collaborators) in the Projects list when **Show archived** is on, but **cannot be opened** while archived.
- Renew the subscription, then unarchive and unlock to edit again.

**Making a project public** is always explicit (toggle + consent modal) and requires an active paid plan. A private project cannot be flipped to public without one.

**Enforcement:** a daily database job (`secure_private_projects_for_expired_subscriptions`, 03:15 UTC) plus a client backstop when the owner loads the app. See [Project privacy and subscription expiry (maintainers)](../project-privacy-and-subscription-expiry-maintainers/).

The subscriber-email modal pre-fills the first slot with the current user's email and validates against the purchased seat count, indicating if there are remaining seats or too many emails.


The admin tab includes a Subscriptions overview table (Tabulator) with header filters, sorting, and server-side pagination. Its **Reminders preview** subtab shows projected 7-day, 1-day, and expiry reminders from `subscriptions_purchased.end_date`; Loops still sends the actual emails.

See also Gating in Technical dletails section below

Lemon Squeezy (LS) integration (first step):
- A new button appears in the Account tab: "Buy Private (Monthly, no AI) via Lemon Squeezy".
- On click, it opens the Lemon Squeezy checkout in a new tab for the Private/Monthly/Manual variant.
- On success, the app records the purchase using the existing subscriptions flow (same as the simulated purchase), so your allocation shows up immediately.

Frontend configuration (override in `webapp/env-config.local.js`):
```js
window.ENV = {
    LEMONSQUEEZY_STORE_DOMAIN: 'causal-map', // your LS store subdomain
    LS_VARIANT_ID_PRIVATE_MONTHLY_MANUAL: ''   // the variant ID slug or UUID
}
```

Notes:
- Only administrators can click purchase (same gating as the simulated buttons).
- We reuse the existing email collection modal to allocate the first seat.
- This is a minimal frontend-only integration (no webhooks yet). Renewals are synced on app load via an Edge Function; admins can manually force a sync for any subscription row.

<!--
Renewal sync (LS → Supabase DB):
- Edge Function: `supabase/functions/lemonsqueezy` action `sync_customer_subscriptions`
- Security: requires a valid Supabase user JWT; allowed only for:
  - admins, OR
  - the user syncing their own email
- What it updates: `subscriptions_purchased.end_date` only (do NOT sync LS `status` because DB has a strict check constraint)
- IMPORTANT: Manual/admin-created subscriptions exist and are not tied to LS. The sync is designed to be safe:
  - It will never set `end_date` earlier than the local row’s `start_date` (prevents end<start).
  - It will never shorten `end_date` (sync is renewal-only).
- Automatic trigger: app boot `loadProjects` calls `DataService.syncMyCustomerSubscriptions()` before computing `getEffectiveSubscriptionStatus()`
- Throttle: client-side localStorage TTL (currently 6 hours per user per mode) to avoid frequent LS API calls
- Admin UX: "Your subscriptions" table shows an admin-only "Sync LS" button per row (syncs by that row’s manager email)
-->

-->