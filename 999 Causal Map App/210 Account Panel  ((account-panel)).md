<div class="user-guide-callout">
<strong>👤 What you can do here:</strong> View and manage your personal account settings. Change your password, update your project information, and control your privacy and security settings. This is also where you can export your data or delete your account if needed.
</div>

<span class="badge bg-info text-dark" style="margin-left:6px;">Making projects private requires a Private subscription</span>

User account management and project settings.

**Onboarding (first sign-up):** When you sign up, we ask a few questions including whether you want AI options switched on and active right at the start, and what you want to do first in the app. If you choose an AI-first workflow, AI is switched on automatically. If AI is off, there are no AI services at all (except basic MapCat help); you can change this anytime in Account settings. If AI is on, you get 100 free AI credits per month, and the AI switch is turned on by default; you can turn it off later in Account settings.

**AI coding toggle ("AI options switched on and active"):** Turn on to use AI; turn off and there are no AI services at all (except basic MapCat help). You can change this anytime in Account settings. When you turn it **on**, a warning modal appears: your data is sent to AI providers when you use AI; it is **not** used to train models; OpenAI (GPT) may retain data for up to 30 days for abuse monitoring; Vertex AI and DashScope do not retain data; see our [privacy policy](https://www.causalmap.app/privacy-policy/). Credits when on depend on your plan; see [AI credits](../account-panel/). **Plans without AI** (e.g. Private Manual) can turn on to try with the free allowance (free credits do not stack with paid AI plans).

**Where AI runs is a project setting, not a user setting.** Each project has an **AI Processing Region** (Project → Edit project → AI Processing Region) with three options: **EU (Belgium, europe-west1)**, **UK (London, europe-west2)**, or **US (Virginia, us-east5)**. New projects default to EU.

When the region is **EU or UK**, the app guarantees every AI call stays in Europe:

- The coding model picker offers the European-resident Geminis only: **Gemini 3.5 Flash** (the coding default), **Gemini 3.6 Flash**, **Gemini 3.5 Flash-Lite**, **Gemini 3.1 Flash-Lite**, **Gemini 3.1 Pro Preview** and **Gemini 2.5 Flash**. Gemini 2.5 runs in a single European region and every Gemini 3 model runs in Google's EU multiregion, so processing stays inside the EU. Models with no European route (GPT-5, Qwen) are hidden.
- Any AI request that would process data outside Europe is blocked client-side before it leaves the browser. A notification explains which model or region caused the block and how to fix it.
- Document embeddings (used by RAG and similarity search) automatically route to `europe-west1` (or `europe-west2` for UK), instead of the default `us-central1`.

When the region is **US**, the model picker shows the full list, including GPT-5, Qwen and others. These process your prompts and data outside Europe.

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
- Seats are billed straight per-seat: total = unit × seats (no volume discount; ad-hoc discounts are handled by Lemon Squeezy codes)
- Price display updates when Add AI is toggled to include AI price
-->

There are three dimensions to the subscriptions, 

Manual vs AI,  

Type:
- private
- pro
- team

Monthly vs Annual.

**AI credits (when you have AI):** Free users who opt in get 100 credits/month. Private AI: 1000. Pro AI: 2000. Team, Academic and Corporate: 4000. Credits renew at the start of each month and do not roll over. See [Responses Panel](../responses-panel/) for usage. Plans without AI (e.g. Private Manual) can turn on the AI toggle in Account to try with the free 100 credits/month. These figures are the user-facing copy of `subscription-prices.json`, which is the source of truth; update them together. 

User can purchase multiples of one or more subs to distribute to colleagues. 

<!--
Types are selectable with options in the gallery; purchases are simulated for now to streamline evaluation.

Underlying storage uses Supabase tables. Each user can buy more than one subscription and allocate seats to colleagues' emails. Data captured includes manager email, subscriber emails (JSON), date, duration, and number of seats.


Each subscription row has a seat-count dropdown (1–100). After purchase, a modal collects subscriber emails, prefilling the first with the current user's email. 



-->

#### Subscriptions Table


The Subscriptions card shows a simple table of the subscriptions where you are the manager or a subscriber, with the manager and subscriber emails. If you manage a subscription, an **Edit** button lets you change who has a seat.

**Renewals:** your renewal date updates automatically whenever you open or refresh the app while signed in.

**Reminder emails:** we email you before a subscription ends, 7 days before, 1 day before, and when it expires.

<!--- Maintainer/tech notes (Subscriptions Table)
- Renewal dates sync from Lemon Squeezy when you open/refresh the app; admins can force a per-row sync from the table.
- Reminder emails go via Loops date-based automations, driven by the `end_date` on each `subscriptions_purchased` row (covers both Lemon Squeezy and admin/manual rows). Only a few safe contact properties sync to Loops (`subscriptionEndDate`, `subscriptionStatus`, etc.), never message content.
--->


#### Private projects and subscription expiry {#private-projects-and-subscription-expiry}

The paid value is privacy: a **private** project is one that only you, and the people you invite, can see. Keeping a project private needs an active paid plan.

**On the free plan,** projects are **public**: anyone with the link can view them. You cannot make a project private without a paid plan.

**On a paid plan that includes private projects** (Private, Pro, Team and similar), you can make projects **private** and work on them privately.

**If your paid plan expires,** your private projects cannot be opened, viewed or edited, until you do one of these:

- **Renew** your plan: the projects stay private and open normally again, or
- **Make a project public:** you can do this without a plan, behind a confirmation. After that anyone can view it, and you can open and edit it again.

Your private projects are never published for you. Turning a project public is always your own explicit choice.

When you allocate seats, the email box pre-fills your own email in the first slot and tells you how many seats are left, or if you have added too many emails.

<!--- Maintainer/tech notes (private projects, expiry, purchasing)
- Privacy is gated on `public.project_plan_ok(name)` = `is_public OR user_has_active_paid_plan(owner_id) OR owner-is-admin`. RLS on links/sources/source_chunks/prompts (read and write) and on bookmark writes requires it, so an unpaid owner (and their collaborators) cannot read or edit a private project until it is renewed or made public. The admin-owner clause stops staff being locked out of their own private projects.
- `read_only` (lock) and `archived` are independent manual flags with no billing meaning. There is no nightly job and no client backstop touching them (both removed June 2026).
- Toggle direction: making a project private needs a plan (trigger `projects_require_plan_for_private` plus the `toggle_project_public_status` RPC); making it public is always allowed for the owner/editor and is the unpaid owner's way back in.
- Client: `ProjectManager.isPrivateProjectLockedForCurrentUser` and `handlePrivateProjectLocked` give the owner a Renew / Make-public choice on open; the Projects list shows a locked badge for the owner's private projects when their plan is inactive.
- Admin Subscriptions overview is a Tabulator table with header filters, sorting and server-side pagination; the Reminders preview subtab projects 7-day/1-day/expiry reminders from `subscriptions_purchased.end_date` (Loops sends the actual emails).
- Lemon Squeezy purchase flow: an Account-tab button opens the LS checkout (Private/Monthly/Manual variant) in a new tab; on success the app records the purchase via the existing subscriptions flow so the allocation shows immediately. Only admins can purchase (same gating as the simulated buttons); the existing email modal allocates the first seat. Minimal frontend-only integration (no webhooks yet).
- Frontend config (override in `webapp/env-config.local.js`):
      window.ENV = {
        LEMONSQUEEZY_STORE_DOMAIN: 'causal-map', // LS store subdomain
        LS_VARIANT_ID_PRIVATE_MONTHLY_MANUAL: ''  // variant ID slug or UUID
      }
--->

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