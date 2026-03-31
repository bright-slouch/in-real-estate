# Orchestrator — Example Prompts

## Scenario 1: New Listing Start to Finish

Starting a brand-new listing and walking through the full workflow from appointment prep to marketing launch.

```
I'm working as Jane Smith — I have a listing appointment tomorrow at 8812 Maple Ridge Lane, Fishers IN 46038. Help me get ready.
```

**Orchestrator behavior:**
1. Loads jane-smith-fc-tucker config
2. Confirms: "Ready to run New Listing Setup for 8812 Maple Ridge Lane?"
3. Begins with re-seller-consultation → proceeds through all 8 stages
4. Passes CMA pricing into listing creation, listing description into marketing

---

## Scenario 2: New Buyer Start to Finish

Onboarding a new buyer client from consultation through offer acceptance.

```
I'm working as Mike Davis. I have a new buyer consultation in 2 hours — the Johnsons, looking in Hamilton County, budget $450K-$550K, need good schools, moving from Broad Ripple.
```

**Orchestrator behavior:**
1. Loads mike-davis-kw config
2. Runs re-buyer-consultation with Hamilton County context
3. Follows with re-neighborhood-research for Carmel, Fishers, Westfield
4. Sets up re-showing-coordinator for tour planning
5. After showings: routes to re-offer-writer when buyer is ready

---

## Scenario 3: Mid-Transaction Pickup

Picking up a transaction already in progress, assessing state and recommending next action.

```
Working as Jane Smith. We went under contract on 3301 Cherry Creek Blvd, Noblesville last Friday. Close date is April 30. What do we need to be doing right now?
```

**Orchestrator behavior:**
1. Loads config
2. Assesses transaction state (Friday acceptance → current date → ~30-day window to April 30)
3. Determines: inspection deadline imminent if not yet completed
4. Recommends: run re-transaction-manager to set up full deadline calendar
5. Flags: if inspection done, check inspection response deadline next

---

## Scenario 4: "I Have a New Client" Routing

Agent mentions a new client without specifying buyer or seller — orchestrator clarifies and routes.

```
Jane Smith here. I just got a referral — the Garcias, newlyweds, first-time homebuyers. Not sure where to start.
```

**Orchestrator behavior:**
1. Loads config
2. Identifies: buyer scenario, first-timers (needs agency explanation emphasis)
3. Recommends Workflow 2: New Buyer Intake
4. Notes: first-time buyers need extra time on written buyer agreement explanation (post-July 2024 requirement)
5. Routes to re-buyer-consultation with first-time buyer context

---

## Scenario 5: Market Update Request

Quick standalone market data request ahead of a listing presentation.

```
Working as Jane Smith. I need current market data for Carmel 46033 — I have a listing presentation tomorrow and want current stats.
```

**Orchestrator behavior:**
1. Loads config (confirms Carmel is in market-areas.yaml)
2. Routes directly to re-market-update (no workflow needed)
3. Confirms: "Ready to run re-market-update for Carmel 46033?"
4. Produces: median price, DOM, inventory, absorption rate, year-over-year comparison

---

## Scenario 6: Inspection Negotiation Mid-Stream

Agent is mid-transaction and the inspection came back with significant issues.

```
Jane Smith here. Inspection just came back on our Westfield listing at 741 Briar Ridge Court. Buyer's agent sent over $24,000 in repair requests. Seller is furious. What do I do?
```

**Orchestrator behavior:**
1. Loads config
2. Identifies: seller-side negotiation scenario, inspection response
3. Routes to re-negotiation-advisor with context:
   - Seller side
   - $24K repair request
   - Emotional seller (motivations and framing section relevant)
4. Produces: itemized response strategy — what to concede, what to push back on, credit vs repair framework, talking points for the emotional seller conversation

---

## Scenario 7: Multiple Active Transactions

Agent is juggling several deals at once; orchestrator summarizes state across all of them.

```
Jane Smith. I've got three deals going right now — 8812 Maple Ridge (under contract, closing May 15), 4521 Oak Creek (active listing, no offers yet), and the Johnson buyer is about to make an offer on a Carmel property. What should I be focused on right now?
```

**Orchestrator behavior:**
1. Loads config
2. Assesses each transaction:
   - 8812 Maple Ridge: calculate days to close from May 15 → flag nearest deadline
   - 4521 Oak Creek: active listing, no offers → recommend marketing/showing review
   - Johnson buyer: offer-ready → queue up re-offer-writer
3. Returns prioritized action list:
   - Priority 1: 8812 Maple Ridge — [specific deadline today/this week]
   - Priority 2: Johnson offer — run re-offer-writer
   - Priority 3: 4521 Oak Creek — review showing feedback with re-showing-coordinator

---

## Scenario 8: Switching Between Buyer and Seller Transactions

Agent needs to context-switch mid-session from a seller task to a buyer task.

```
Working as Mike Davis. I just finished updating the showing feedback for 2245 Windermere (our listing). Now I need to shift gears — the Hendersons want to make an offer on a property in Geist. What do we need?
```

**Orchestrator behavior:**
1. Retains Windermere listing context in session memory
2. Switches to Henderson buyer context:
   - Loads buyer profile if available from prior session
   - Routes to re-offer-writer for Geist property
   - Confirms: "Ready to run re-offer-writer for the Hendersons' offer?"
3. Notes: Geist is in Marion/Hamilton County overlap — pulls relevant market context from market-areas.yaml
