# Reference
## Billing
<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getBalanceSummary</a>() -> Talkif.BalanceSummaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/balances
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getBalanceSummary();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">listCharges</a>({ ...params }) -> Talkif.ChargeListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Paginated, filterable charge history for an account.
Returns charges with entity context (phone number, flow name, contact name)
from the first associated cost line item.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.listCharges();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListChargesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getChargeDetail</a>({ ...params }) -> Talkif.ChargeDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Detailed charge view with cost line items breakdown.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getChargeDetail({
    chargeId: "chargeId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetChargeDetailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getBillingCostBreakdown</a>({ ...params }) -> Talkif.AnalyticsCostBreakdownResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get account-level cost breakdown by category with drill-down to calls.

## Query Parameters
- `period`: `today`, `week`, `month`, or `custom` (default: `week`)
- `startDate`: Required when `period=custom`
- `endDate`: Required when `period=custom`

## Response
Returns total costs, breakdown by category (LLM, STT, TTS, telephony),
breakdown by flow, and recent calls with individual cost breakdowns.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getBillingCostBreakdown();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetBillingCostBreakdownRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getBillingCallCostBreakdown</a>({ ...params }) -> Talkif.CallCostBreakdownResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get detailed cost breakdown for a single call with line items.

Returns all cost line items including usage data (tokens, seconds, characters)
and rate information for each cost component.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getBillingCallCostBreakdown({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetBillingCallCostBreakdownRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">listInvoices</a>({ ...params }) -> Talkif.InvoiceListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/invoices
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.listInvoices();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListInvoicesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getInvoice</a>({ ...params }) -> Talkif.InvoiceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/invoices/{invoiceId}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getInvoice({
    invoiceId: "invoiceId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetInvoiceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getTransactionHistory</a>({ ...params }) -> Talkif.BalanceTransactionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/billing/transactions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getTransactionHistory();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetTransactionHistoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.billing.<a href="/src/api/resources/billing/client/Client.ts">getPublicPricing</a>() -> Talkif.PublicPricingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Public endpoint — no authentication required.
Returns telephony rates, phone number pricing, and recording storage pricing.

LLM/STT/TTS pricing is served by `GET /api/v1/models/*` with richer data
(capabilities, languages, use-case filtering).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.billing.getPublicPricing();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BillingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Calls
<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">listCalls</a>({ ...params }) -> Talkif.CallListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the account's calls, newest first, with optional filters. Use `status` to narrow to live calls (for example `in_progress`), `flowId` / `campaignId` / `contactId` to scope by resource, and `startDate` / `endDate` for a time window.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.listCalls();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListCallsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">makeCall</a>({ ...params }) -> Talkif.MakeCallResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/calls

SECURITY: Verifies account access, phone ownership, provider ownership, flow ownership

Returns:
- 201 Created: Call initiated immediately (capacity available)
- 202 Accepted: Call queued for later processing (at capacity/rate limited)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.makeCall({
    flowId: "550e8400-e29b-41d4-a716-446655440000",
    fromNumber: "+15559876543",
    providerId: "550e8400-e29b-41d4-a716-446655440000",
    toNumber: "+15551234567"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.MakeCallRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallDetails</a>({ ...params }) -> Talkif.CallResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/calls/:callId
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallDetails({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallDetailsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">analyzeCall</a>({ ...params }) -> Talkif.CallInsights | null</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/calls/:callId/analyze

Generates AI-powered insights from the call transcript:
- Summary (2-3 sentences)
- Sentiment analysis (positive/neutral/negative + confidence)
- Detected intents
- Key topics discussed
- Action items
- Call outcome

This endpoint is always available regardless of account auto-analysis settings.
Can be used to:
- Analyze calls that weren't auto-analyzed
- Re-analyze calls with updated AI model

Requires the call to be in a terminal state (COMPLETED/FAILED/etc.)
and have a transcript available.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.analyzeCall({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AnalyzeCallRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallRecording</a>({ ...params }) -> Talkif.RecordingUrlResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a time-limited presigned URL for recording playback. Fetch the
audio directly from that URL.

Requires the call to belong to the account and to have
`recordingStatus = ready`; recording must be enabled for the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallRecording({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallRecordingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">deleteCallRecording</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/calls/:callId/recording → 204

Charges for actual storage duration before deletion (billing at lifecycle end).
Uses idempotency key to prevent double-charging if racing with retention job.

Owner or admin only: deleting a recording destroys data the account may
need to keep. With an API key, the key's creator must be an owner or admin.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.deleteCallRecording({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteCallRecordingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.calls.<a href="/src/api/resources/calls/client/Client.ts">getCallTranscript</a>({ ...params }) -> Talkif.CallTranscriptResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/calls/:callId/transcript
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.calls.getCallTranscript({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallTranscriptRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Campaigns
<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">listCampaigns</a>({ ...params }) -> core.Page&lt;Talkif.CampaignResponse, Talkif.CampaignListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.campaigns.listCampaigns();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.campaigns.listCampaigns();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListCampaignsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">createCampaign</a>({ ...params }) -> Talkif.CampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.createCampaign({
    flowId: "550e8400-e29b-41d4-a716-446655440000",
    fromPhoneNumber: "+15551234567",
    name: "January Outreach",
    providerId: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">getCampaign</a>({ ...params }) -> Talkif.CampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.getCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">updateCampaign</a>({ ...params }) -> Talkif.CampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.updateCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">deleteCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.deleteCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">cancelCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.cancelCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CancelCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">listCampaignContacts</a>({ ...params }) -> core.Page&lt;Talkif.CampaignContactResponse, Talkif.CampaignContactListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.campaigns.listCampaignContacts({
    campaignId: "campaignId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.campaigns.listCampaignContacts({
    campaignId: "campaignId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListCampaignContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">addCampaignContacts</a>({ ...params }) -> Talkif.AddedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.addCampaignContacts({
    campaignId: "campaignId",
    contactIds: ["contactIds"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AddCampaignContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">removeCampaignContacts</a>({ ...params }) -> Talkif.RemovedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.removeCampaignContacts({
    campaignId: "campaignId",
    campaignContactIds: ["campaignContactIds"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RemoveCampaignContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">bulkAddCampaignContacts</a>({ ...params }) -> Talkif.BulkAddContactsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Bulk add contacts to a campaign using filter criteria.

Instead of passing individual contact IDs, pass filter criteria:
- `tags`: Filter by contact tags (with `tagMode` for ANY/ALL matching)
- `company`: Filter by company name (exact match)
- `search`: Full-text search across name, company, occupation, email

This allows adding thousands of contacts in a single request efficiently.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.bulkAddCampaignContacts({
    campaignId: "campaignId",
    filter: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.BulkAddContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">bulkRemoveCampaignContacts</a>({ ...params }) -> Talkif.BulkRemoveContactsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Bulk remove contacts from a campaign using the same filter criteria as bulk add.

Contacts that already have a call record, or that are sitting in an active
queue slot, are never removed — the response reports `matched` and `removed`
separately so a partial removal is visible rather than silent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.bulkRemoveCampaignContacts({
    campaignId: "campaignId",
    filter: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.BulkRemoveContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">skipCampaignContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark a campaign contact as skipped (e.g., DNC, opt-out, manual skip).
The contact will be excluded from future claiming and calling.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.skipCampaignContact({
    campaignId: "campaignId",
    contactId: "contactId",
    reason: "manual"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SkipContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">pauseCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initiates the draining process for a running campaign:
- Status changes to Draining (stops feeding new contacts to queue)
- Active calls are allowed to complete naturally
- When active_calls_count reaches 0, status transitions to Paused
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.pauseCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PauseCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">restartCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Restarts a campaign for non-called contacts. Resets failed/pending/not-called
contacts back to pending and starts the campaign from Paused/Completed/Cancelled state.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.restartCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RestartCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">resumeCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Resumes a paused campaign, transitioning it back to Running state.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.resumeCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ResumeCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.campaigns.<a href="/src/api/resources/campaigns/client/Client.ts">startCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.campaigns.startCampaign({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.StartCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Analytics
<details><summary><code>client.analytics.<a href="/src/api/resources/analytics/client/Client.ts">getCampaignAnalytics</a>({ ...params }) -> Talkif.CampaignAnalyticsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get deep analytics for a single campaign.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.analytics.getCampaignAnalytics({
    campaignId: "campaignId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCampaignAnalyticsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AnalyticsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.analytics.<a href="/src/api/resources/analytics/client/Client.ts">getFlowStats</a>({ ...params }) -> Talkif.FlowStatsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get statistics for a specific flow.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.analytics.getFlowStats({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowStatsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AnalyticsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Contacts
<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">listContacts</a>({ ...params }) -> core.Page&lt;Talkif.Contact, Talkif.ContactListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.contacts.listContacts();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.contacts.listContacts();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createContact({
    name: "Jane Smith",
    primaryPhone: "+15551234567"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">exportContacts</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.exportContacts({
    format: "format"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ExportContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">importContacts</a>({ ...params }) -> Talkif.ImportResult</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.importContacts({
    fileContent: "Sm9obiBEb2UsKzE1NTUxMjM0NTY3",
    format: "vcf"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ImportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">searchByPhone</a>({ ...params }) -> Talkif.ContactSearchResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.searchByPhone({
    phone: "phone"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SearchByPhoneRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">listTags</a>() -> Talkif.TagsListResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.listTags();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContactCalls</a>({ ...params }) -> core.Page&lt;Talkif.CallResponse, Talkif.CallListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.contacts.getContactCalls({
    contactId: "contactId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.contacts.getContactCalls({
    contactId: "contactId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetContactCallsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">restoreContact</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.restoreContact({
    contactId: "contactId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RestoreContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">addTags</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.addTags({
    contactId: "contactId",
    tags: ["vip", "priority"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AddTagsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">removeTags</a>({ ...params }) -> Talkif.Contact</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.removeTags({
    contactId: "contactId",
    tags: ["vip"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RemoveTagsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Do Not Call
<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">listDncEntries</a>({ ...params }) -> core.Page&lt;Talkif.DncEntryResponse, Talkif.DncListResponse&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List DNC entries for an account with pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.doNotCall.listDncEntries();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.doNotCall.listDncEntries();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListDncEntriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">addDncEntry</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a phone number to the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.addDncEntry({
    phoneNumber: "+15551234567"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateDncEntryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">bulkImportDnc</a>({ ...params }) -> Talkif.BulkDncImportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Bulk import phone numbers to the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.bulkImportDnc({
    phoneNumbers: ["+15551234567", "+15559876543"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.BulkDncImportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">checkDncStatus</a>({ ...params }) -> Talkif.CheckDncResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Check if phone numbers are on the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.checkDncStatus({
    phoneNumbers: ["+15551234567", "+15559876543"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CheckDncRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.doNotCall.<a href="/src/api/resources/doNotCall/client/Client.ts">removeDncEntry</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a phone number from the DNC list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.doNotCall.removeDncEntry({
    phoneNumber: "phoneNumber"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RemoveDncEntryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DoNotCallClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Errors
<details><summary><code>client.errors.<a href="/src/api/resources/errors/client/Client.ts">errorCatalog</a>() -> Talkif.ErrorCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all API error codes and field validation codes with descriptions, HTTP status codes, and categories. Use this to build error reference documentation or implement client-side error handling.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.errors.errorCatalog();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ErrorsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Flow Functions
<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">listFlowFunctions</a>({ ...params }) -> Talkif.FlowFunctionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-functions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.listFlowFunctions();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListFlowFunctionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">createFlowFunction</a>({ ...params }) -> Talkif.FlowFunctionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flow-functions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.createFlowFunction({
    description: "Create a new customer order",
    name: "create_order",
    request: {
        method: "POST",
        url: "https://api.example.com/orders/{orderId}"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">getFlowFunction</a>({ ...params }) -> Talkif.FlowFunctionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-functions/{id}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.getFlowFunction({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">updateFlowFunction</a>({ ...params }) -> Talkif.FlowFunctionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PUT /api/v1/flow-functions/{id}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.updateFlowFunction({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowFunctions.<a href="/src/api/resources/flowFunctions/client/Client.ts">deleteFlowFunction</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/flow-functions/{id}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowFunctions.deleteFlowFunction({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteFlowFunctionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowFunctionsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Flow Templates
<details><summary><code>client.flowTemplates.<a href="/src/api/resources/flowTemplates/client/Client.ts">listSystemTemplates</a>({ ...params }) -> Talkif.FlowTemplateListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-templates
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowTemplates.listSystemTemplates();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListSystemTemplatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowTemplates.<a href="/src/api/resources/flowTemplates/client/Client.ts">getFlowTemplate</a>({ ...params }) -> Talkif.FlowTemplate</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flow-templates/:slug

Note: This is a public endpoint that doesn't require auth, but if the user is logged in,
they can also see their account-specific templates
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowTemplates.getFlowTemplate({
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flowTemplates.<a href="/src/api/resources/flowTemplates/client/Client.ts">instantiateTemplate</a>({ ...params }) -> Record&lt;string, unknown&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/from-template/:templateSlug
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flowTemplates.instantiateTemplate({
    templateSlug: "templateSlug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.InstantiateTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Flows
<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">listFlows</a>({ ...params }) -> Talkif.FlowListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flows

Returns lightweight flow list with connected phones.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.listFlows();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListFlowsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">createFlow</a>({ ...params }) -> Talkif.FlowDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows

Definition is optional — omit to create an empty draft for the builder UI,
or provide it to create a flow with initial content.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.createFlow({
    name: "Appointment Reminder"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">getFlow</a>({ ...params }) -> Talkif.FlowDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flows/:flowId

Returns full flow details including definition, layout, and connected phones.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.getFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">updateFlow</a>({ ...params }) -> Talkif.FlowDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PUT /api/v1/flows/:flowId
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.updateFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">deleteFlow</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/flows/:flowId

Returns 204 No Content on success.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.deleteFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">publishFlow</a>({ ...params }) -> Talkif.PublishFlowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/:flowId/publish
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.publishFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PublishFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">rollbackFlow</a>({ ...params }) -> Talkif.RollbackResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/:flowId/rollback/:version
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.rollbackFlow({
    flowId: "flowId",
    version: "version"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RollbackFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">validateFlow</a>({ ...params }) -> Talkif.ValidationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/flows/:flowId/validate
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.validateFlow({
    flowId: "flowId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ValidateFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.flows.<a href="/src/api/resources/flows/client/Client.ts">getFlowVersion</a>({ ...params }) -> Talkif.FlowVersionDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/flows/:flowId/versions/:version
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.flows.getFlowVersion({
    flowId: "flowId",
    version: "version"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetFlowVersionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FlowsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## AI Models
<details><summary><code>client.aiModels.<a href="/src/api/resources/aiModels/client/Client.ts">listProvidersPublic</a>({ ...params }) -> Talkif.FlowProvidersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/models
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aiModels.listProvidersPublic();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListProvidersPublicRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AiModelsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.aiModels.<a href="/src/api/resources/aiModels/client/Client.ts">listTtsVoices</a>({ ...params }) -> Talkif.VoicesDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/models/tts/voices

When any of gender, age, language, accent, or sort are present, routes to
the ElevenLabs /v1/shared-voices endpoint (rich filtering, offset pagination).
Otherwise routes to /v2/voices (simpler, cursor pagination).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.aiModels.listTtsVoices();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListTtsVoicesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AiModelsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Accounts
<details><summary><code>client.accounts.<a href="/src/api/resources/accounts/client/Client.ts">getPermissions</a>() -> Talkif.PermissionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Your role in the account and the permissions it grants, for showing or
hiding actions. The server enforces them regardless.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.accounts.getPermissions();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AccountsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.accounts.<a href="/src/api/resources/accounts/client/Client.ts">getRoles</a>() -> Talkif.RolesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Every built-in role with the permissions it grants in the selected
account, for showing what each role may do.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.accounts.getRoles();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AccountsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Phone Numbers
<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">listPhoneNumbers</a>({ ...params }) -> Talkif.PhoneNumberListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.listPhoneNumbers();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListPhoneNumbersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">listAvailableNumbers</a>({ ...params }) -> Talkif.AvailableNumbersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/twilio/available

Query Parameters:
- `providerId` (required): Provider ID
- `countryCode` (required): ISO country code (e.g., "US", "GB")
- `numberType` (optional): "local", "toll_free", or "mobile" (default: "local")
- `areaCode` (optional): Area code filter (US/Canada only)
- `contains` (optional): Pattern to match (supports wildcards: *, %)
- `inPostalCode` (optional): Filter by postal/ZIP code
- `inRegion` (optional): Filter by state/region
- `inRateCenter` (optional): Filter by rate center
- `inLata` (optional): Filter by LATA
- `inLocality` (optional): Filter by city
- `nearNumber` (optional): Find numbers near this phone number
- `nearLatLong` (optional): Find numbers near lat,long
- `distance` (optional): Radius in miles (default: 25, max: 500)
- `smsEnabled` (optional): Filter SMS-capable numbers
- `mmsEnabled` (optional): Filter MMS-capable numbers
- `voiceEnabled` (optional): Filter voice-capable numbers
- `faxEnabled` (optional): Filter fax-capable numbers
- `beta` (optional): Filter beta numbers
- `excludeAllAddressRequired` (optional): Exclude numbers requiring any address
- `excludeLocalAddressRequired` (optional): Exclude numbers requiring local address
- `excludeForeignAddressRequired` (optional): Exclude numbers requiring foreign address
- `limit` (optional): Max results (default: 20, max: 1000)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.listAvailableNumbers({
    providerId: "providerId",
    countryCode: "countryCode"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListAvailableNumbersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">listAvailableCountries</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/twilio/available-countries
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.listAvailableCountries({
    providerId: "providerId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListAvailableCountriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">getPricing</a>({ ...params }) -> Talkif.PhoneNumberPricing</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/twilio/pricing
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.getPricing({
    providerId: "providerId",
    countryCode: "countryCode"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetPricingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">purchasePhoneNumber</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/phone/numbers/twilio/purchase
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.purchasePhoneNumber({
    phoneNumber: "+15551234567",
    providerId: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PurchasePhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">getPhoneNumber</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/numbers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.getPhoneNumber({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetPhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">updatePhoneNumber</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PUT /api/v1/phone/numbers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.updatePhoneNumber({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdatePhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">releasePhoneNumber</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

DELETE /api/v1/phone/numbers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.releasePhoneNumber({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ReleasePhoneNumberRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">connectFlow</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PATCH /api/v1/phone/numbers/:phoneNumberId/connect-flow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.connectFlow({
    phoneNumberId: "phoneNumberId",
    flowId: "550e8400-e29b-41d4-a716-446655440000"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ConnectFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneNumbers.<a href="/src/api/resources/phoneNumbers/client/Client.ts">disconnectFlow</a>({ ...params }) -> Talkif.PhoneNumberResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PATCH /api/v1/phone/numbers/:phoneNumberId/disconnect-flow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneNumbers.disconnectFlow({
    phoneNumberId: "phoneNumberId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DisconnectFlowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneNumbersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Phone Providers
<details><summary><code>client.phoneProviders.<a href="/src/api/resources/phoneProviders/client/Client.ts">listPhoneProviders</a>({ ...params }) -> Talkif.PhoneProviderListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/providers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneProviders.listPhoneProviders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListPhoneProvidersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneProvidersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.phoneProviders.<a href="/src/api/resources/phoneProviders/client/Client.ts">getProvider</a>({ ...params }) -> Talkif.PhoneProviderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/phone/providers/:id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.phoneProviders.getProvider({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetProviderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PhoneProvidersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## PublicCalls
<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">createCall</a>() -> Talkif.CreateWebRtcCallResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.createCall();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">getIceServers</a>() -> Talkif.IceServersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/public/calls/ice-servers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.getIceServers();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">createSession</a>({ ...params }) -> Talkif.CreatePublicSessionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls/session
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.createSession({
    publishableKey: "pk_live_AbCdEf123456"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreatePublicSessionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">getCallStatus</a>({ ...params }) -> Talkif.PublicCallStatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET /api/v1/public/calls/{callId}
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.getCallStatus({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetCallStatusRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">endCall</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls/{callId}/end
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.endCall({
    callId: "callId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.EndCallRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.publicCalls.<a href="/src/api/resources/publicCalls/client/Client.ts">relayOffer</a>({ ...params }) -> Talkif.WebRtcOfferResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST /api/v1/public/calls/{callId}/offer
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.publicCalls.relayOffer({
    callId: "callId",
    sdp: "v=0\r\no=- 0 0 IN IP4 127.0.0.1\r\n..."
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.WebRtcOfferRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PublicCallsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Schedules
<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">listSchedules</a>({ ...params }) -> core.Page&lt;Talkif.ScheduleResponse, Talkif.ScheduleListResponse&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.schedules.listSchedules();
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.schedules.listSchedules();
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListSchedulesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">createSchedule</a>({ ...params }) -> Talkif.ScheduleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.createSchedule({
    contactId: "550e8400-e29b-41d4-a716-446655440000",
    flowId: "550e8400-e29b-41d4-a716-446655440000",
    frequency: "once",
    fromPhoneNumber: "+15551234567",
    name: "Daily Follow-up Call",
    providerId: "550e8400-e29b-41d4-a716-446655440000",
    scheduleTime: "09:00"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">getSchedule</a>({ ...params }) -> Talkif.ScheduleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.getSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">updateSchedule</a>({ ...params }) -> Talkif.ScheduleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.updateSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">deleteSchedule</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.deleteSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">pauseSchedule</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.pauseSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.PauseScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules.<a href="/src/api/resources/schedules/client/Client.ts">resumeSchedule</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.schedules.resumeSchedule({
    scheduleId: "scheduleId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ResumeScheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SchedulesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Transfers
<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">listGroups</a>({ ...params }) -> Talkif.DestinationGroupListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Destination groups are named sets of destinations that ring together as one
transfer target.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.listGroups();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListGroupsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">createGroup</a>({ ...params }) -> Talkif.DestinationGroup</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A destination group is a named set of destinations that ring together as
one transfer target. With the `simultaneous` strategy every member rings at
once and the first to answer is connected.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.createGroup({
    members: [{
            destinationId: "destinationId"
        }],
    name: "Sales team"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateDestinationGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">getGroup</a>({ ...params }) -> Talkif.DestinationGroup</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A named set of destinations that ring together as one transfer target.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.getGroup({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">updateGroup</a>({ ...params }) -> Talkif.DestinationGroup</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Omitted fields keep their value; `members` replaces the whole list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.updateGroup({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateDestinationGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">deleteGroup</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refused with `in_use` while a published flow transfers to it; `meta.flows`
names them.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.deleteGroup({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">listDestinations</a>({ ...params }) -> Talkif.TransferDestinationListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Destinations are the places a flow's Transfer node can send a call: a phone
number, the people who are available for calls in the dashboard, or your
own app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.listDestinations();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListDestinationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">createDestination</a>({ ...params }) -> Talkif.TransferDestination</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A destination is somewhere a Transfer node can send a call: a phone number,
the people who are available for calls in the dashboard, or your own app
(`app`: offers arrive as signed `transfer.offer` webhooks; the response
carries the signing secret once, in `signingSecret`). Emergency,
special-service and premium-rate numbers are refused.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.createDestination({
    config: {
        "key": "value"
    },
    kind: "phone",
    name: "Sales desk"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.CreateTransferDestinationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">getDestination</a>({ ...params }) -> Talkif.TransferDestination</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

One place a flow's Transfer node can send a call.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.getDestination({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetDestinationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">updateDestination</a>({ ...params }) -> Talkif.TransferDestination</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The kind cannot change. Sending `config` replaces the whole settings object.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.updateDestination({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.UpdateTransferDestinationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">deleteDestination</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refused with `in_use` while a destination group lists it or a published
flow transfers to it; `meta.groups` and `meta.flows` name them.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.deleteDestination({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteDestinationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">listDeliveries</a>({ ...params }) -> Talkif.TransferAppDeliveryListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The last 20 webhook deliveries (test sends and real offers), newest first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.listDeliveries({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.ListDeliveriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">rotateSecret</a>({ ...params }) -> Talkif.TransferDestination</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replaces the secret that signs `transfer.offer` webhooks and returns the new
one once, in `signingSecret`. For 24 hours, until `previousSecretExpiresAt`,
webhooks carry a second signature made with the previous secret
(`Talkif-Signature: t=…,v1=<new>,v1=<previous>`), so your server can switch
secrets without missing an offer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.rotateSecret({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.RotateSecretRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">testDestination</a>({ ...params }) -> Talkif.TransferAppDeliveryResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sends a sample `transfer.offer` webhook (fake caller, `"test": true`),
signed like a real one, and reports how your server answered. Test offers
cannot be accepted. The delivery is logged. At most 5 test sends per
destination per minute and 30 per account per hour.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.testDestination({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.TestDestinationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">listMemberTags</a>() -> Talkif.MemberTagCatalogResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Every tag at least one member of your organization carries, with how many
members carry it. Use these in an `available_humans` destination's `tags`
to ring only that team. Empty on a personal account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.listMemberTags();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">listMembers</a>() -> Talkif.TransferMemberListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Every member of your organization, with the tags and weekly available
hours that decide which transfers to people ring them. Tags and hours
belong to the organization: the same member has the same tags and hours
in every account of the organization. On a personal account the list is
empty.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.listMembers();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">getMemberAvailability</a>({ ...params }) -> Talkif.MemberAvailability</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Whether the member takes transferred calls: `available`, `away` or
`offline` (with the end time, who set it, and whether they are on a call
right now). An away/offline whose end time passed reads as `available`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.getMemberAvailability({
    memberId: "memberId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetMemberAvailabilityRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">setMemberAvailability</a>({ ...params }) -> Talkif.MemberAvailability</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Turns transferred calls on or off for a member, in every account of the
organization: `away` or `offline`, optionally `until` a moment (then the
member is available again by itself), or `available`. The member may set
any status. An owner or admin may set another member `away` or
`offline`, and may make them `available` again only if the member did not
turn calls off themselves.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.setMemberAvailability({
    memberId: "memberId",
    status: "available"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SetMemberAvailabilityRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">getMemberHours</a>({ ...params }) -> Talkif.MemberHoursResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.getMemberHours({
    memberId: "memberId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetMemberHoursRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">setMemberHours</a>({ ...params }) -> Talkif.MemberHoursResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sets the weekly schedule inside which transfers to people ring this
member. Outside it the member is skipped even when available for calls;
if nobody is left, the destination's nobody-available path runs. Hours
belong to the organization and apply in every account of it. The member
themselves, or an owner or admin.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.setMemberHours({
    memberId: "memberId",
    body: {
        timezone: "Europe/Istanbul",
        weekly: {}
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SetMemberHoursRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">deleteMemberHours</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the schedule: the member is always within hours again. The member
themselves, or an owner or admin.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.deleteMemberHours({
    memberId: "memberId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeleteMemberHoursRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">getMemberTags</a>({ ...params }) -> Talkif.MemberTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.getMemberTags({
    memberId: "memberId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetMemberTagsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">setMemberTags</a>({ ...params }) -> Talkif.MemberTagsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sets the member's complete tag list. Tags group members into teams for
transfers: an `available_humans` destination with `tags` rings only
members carrying at least one of them. Tags belong to the organization,
so the change applies in every account of the organization. Owner or
admin only.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.setMemberTags({
    memberId: "memberId",
    tags: ["sales", "billing"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.SetMemberTagsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">getOffer</a>({ ...params }) -> Talkif.TransferOffer</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A ringing offer to one of your app destinations: the same body as the
`transfer.offer` webhook. Only offers to app destinations of this account
are visible. Requires an API key with the `transfer_offers:read` scope.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.getOffer({
    offerId: "offerId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.GetOfferRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">acceptOffer</a>({ ...params }) -> Talkif.TransferOfferAcceptResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The first accept wins; accept before `acceptUntil`. Without a body the
reply carries a single-use WebSocket `joinUrl` for the call's audio; with
`{"sdpOffer": "<SDP>"}` the call joins over WebRTC and the reply carries
the SDP answer and ICE servers. Join within 10 seconds (20 for WebRTC) or
the offer counts as unanswered. Requires an API key with the
`transfer_offers:write` scope; repeating the accept with the same key
returns a new join.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.acceptOffer({
    offerId: "offerId",
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.AcceptOfferRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transfers.<a href="/src/api/resources/transfers/client/Client.ts">declineOffer</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Your app will not take this call: the transfer stops ringing it at once.
Declining an offer that already ended, or that was already accepted, does
nothing. Requires an API key with the `transfer_offers:write` scope.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transfers.declineOffer({
    offerId: "offerId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Talkif.DeclineOfferRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransfersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

