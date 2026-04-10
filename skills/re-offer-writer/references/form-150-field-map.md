# IAR Form 150 — Purchase Agreement (2026) Field Map

This reference maps every fillable field in the IAR Form 150 (Purchase Agreement, Improved Property, Copyright IAR 2026) to the offer data collected during the re-offer-writer workflow. Use this when filling the blank template at `templates/iar-form-150-purchase-agreement-2026.pdf`.

The form is 9 pages. Fields are identified by section letter, line number, and description.

---

## Template PDF Info

- **File:** `templates/iar-form-150-purchase-agreement-2026.pdf`
- **Pages:** 9
- **PDF dimensions:** 612 × 792 points per page
- **Form type:** Non-fillable (image-based) — use the `pdf` skill's visual estimation approach (Approach B in FORMS.md)

---

## Page 1 — Header, Buyer, Property, Inclusions/Exclusions, Price, Earnest Money

### Header (above line 1)

| Field | Location | Data Source |
|---|---|---|
| Listing Broker (Co.) | Top line, after label | Agent config → listing brokerage name (seller side) or obtained from listing agent |
| Office code (listing) | After broker name, in parentheses | Listing office MLS code |
| By (listing) | After "By" | Listing agent name |
| Individual code (listing) | End of line | Listing agent MLS ID |
| Selling Broker (Co.) | Second line, after label | Agent config → `agent-profile.yaml` → brokerage name (buyer side) |
| Office code (selling) | After broker name | Agent config → office code from `agent-profile.yaml` |
| By (selling) | After "By" | Agent config → agent full name |
| Individual code (selling) | End of line | Agent config → MLS ID from `agent-profile.yaml` |

### Section A — Date and Buyer (Lines 1–5)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Date | 1 | After "Date:" | Offer date (from agent input) |
| Buyer name(s) | 3 | After "A. BUYER:" through "("Buyer")" | Full legal name(s) of buyer(s) — from buyer consultation or agent input |

### Section B — Property (Lines 7–9)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Property address / known as | 7 | After "is known as" to end of line | Street address of subject property |
| City / location | 8 | After "in" to "Township," | City name |
| Township | 8 | After "Township," to "County," | Township name |
| County | 8 | After "County," to end of line | County name |
| Zip code | 9 | After "Indiana," to "(zip code)" | ZIP code |
| Legal description | 9 | After "legally described as" to end | Legal description (from tax records or title) — can write "See attached" |

### Inclusions/Exclusions (Lines 10–21)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Smart home devices | 17–18 | After "addressed in this paragraph.)" through line 18 | List of smart home devices included, if any, or "None" |
| Additional inclusions | 18–19 | Blank lines after smart home | Any additional personal property included |
| Excluded items | 20–21 | After "EXCLUDES THE FOLLOWING (include leased items):" through line 21 | Items excluded from sale (e.g., "Ring doorbell - leased", "Water softener - leased") |

### Section C — Price (Lines 31–36)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Purchase price (numeric) | 31 | After "purchase price of ($" before ")" | Offer price as number (e.g., "338,000.00") |
| Purchase price (words) | 32 | Before "U.S. Dollars" | Offer price in words (e.g., "Three Hundred Thirty-Eight Thousand and 00/100") |

### Section D — Earnest Money (Lines 38–55)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Earnest money amount | 39 | After "Buyer submits $" | Earnest money amount (e.g., "5,000.00") |
| Earnest money (words) | 39 | Before "U.S. Dollars as earnest money" | Amount in words |
| Delivery hours | 41 | In box before "hours" | Hours for earnest money delivery (e.g., "48") |
| Delivery days | 41 | In box before "days after acceptance" | Days for delivery (alternative to hours) |
| Escrow: Listing Broker | 42 | Checkbox after "Escrow Agent to be:" | Check if listing broker holds escrow |
| Escrow: Selling Broker | 42 | Checkbox after "Listing Broker" | Check if selling broker holds escrow |
| Escrow: Other | 42 | Checkbox after "Selling Broker" | Check if other party holds escrow |
| Escrow agent name | 42 | After "Other" to end of line | Name of escrow agent if "Other" selected (e.g., title company name) |

---

## Page 2 — Payment Method, Financing, Seller Contributions, Closing

### Section E — Method of Payment (Lines 60–76)

| Field | Line | Location | Data Source |
|---|---|---|---|
| E.1 CASH checkbox | 61 | Checkbox before "CASH:" | Check if cash purchase |
| Cash proof of funds: with offer | 62 | Checkbox after "submitted" | Check if proof of funds submitted with offer |
| Cash proof of funds: within days | 62 | Checkbox + blank after "within" | Days to submit proof of funds |
| Cash: will/will not have appraisal | 65 | Checkboxes "will" / "will not" | Whether cash buyer will get appraisal |
| E.2 NEW MORTGAGE checkbox | 66 | Checkbox before "NEW MORTGAGE" | Check if financed purchase |
| Loan type: Conventional | 67 | Checkbox | Check if conventional loan |
| Loan type: Insured Conventional | 67 | Checkbox | Check if insured conventional |
| Loan type: FHA | 67 | Checkbox | Check if FHA loan |
| Loan type: VA | 67 | Checkbox | Check if VA loan |
| Loan type: USDA | 67 | Checkbox | Check if USDA loan |
| Loan type: Other | 67 | Checkbox + fill | Check if other; specify type |
| Loan type description | 67 | After "Other:" to "first" | Loan type if other |
| Mortgage percentage | 68 | After "mortgage loan for" before "%" | LTV percentage (e.g., "95") |
| Loan term (years) | 68 | After "payable in not less than" before "years" | Loan term (e.g., "30") |
| Interest rate cap | 69 | After "not to exceed" before "%" | Max interest rate (e.g., "7.5") |
| Points cap | 69 | After "not to exceed" before "points" | Max points (e.g., "2") |
| E.3 ASSUMPTION checkbox | 74 | Checkbox | Check if assumption |
| E.4 CONDITIONAL SALES CONTRACT | 75 | Checkbox | Check if conditional sale |
| E.5 OTHER METHOD | 76 | Checkbox | Check if other payment method |

### Section F — Time for Obtaining Financing (Lines 78–86)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Application days | 79 | After "Within" before "days" | Days to apply for financing (e.g., "5") |
| Approval days | 83 | After "No more than" before "days" | Days for loan approval (e.g., "21") |

### Section G — Seller Contributions (Lines 88–93)

| Field | Line | Location | Data Source |
|---|---|---|---|
| G.1 Seller concessions checkbox | 89 | Checkbox before "SELLER CONCESSIONS" | Check if requesting seller concessions |
| Concessions amount ($) | 89 | After "up to $" | Dollar amount of concessions |
| Concessions percentage | 89 | After "or" before "% of purchase price" | Percentage alternative |
| G.2 Buyer broker compensation checkbox | 91 | Checkbox before "BUYER BROKER COMPENSATION" | Check if seller pays buyer broker |
| Buyer broker comp amount ($) | 91 | After "amount of $" | Dollar amount |
| Buyer broker comp percentage | 92 | Before "% of purchase price" | Percentage alternative |

### Section H — Closing (Lines 94–114)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Closing date | 94 | After "on or before" | Target closing date |
| Closing days after | 95 | After "within" + "days after" | Days after [event] to close |
| Closing days after event | 95 | After "days after" | The event (e.g., "acceptance") |
| Closing fee: Buyer | 99 | Checkbox "Buyer" | Check if buyer pays closing fee |
| Closing fee: Seller | 99 | Checkbox "Seller" | Check if seller pays |
| Closing fee: Shared equally | 99 | Checkbox "Shared equally" | Check if shared |
| H.3 Not contingent | 100–101 | Checkbox "is not contingent" | Check if no home sale contingency |
| H.3 Contingent on closing | 102 | Checkbox "is contingent upon the closing" | Check if contingent on buyer's home closing |
| Contingent property address | 102 | After "located at" | Address of buyer's property |
| Contingent close date | 103 | After "scheduled to close by" | Expected close date of buyer's property |
| H.3 Contingent on acceptance | 106 | Checkbox "is contingent upon the acceptance" | Check if contingent on buyer's home sale |
| First Right addendum | 107 | Checkbox | First right contingency addendum |
| Limited Purchase addendum | 108 | Checkbox | Limited purchase contingency addendum |

---

## Page 3 — Possession, Survey, Flood, Building Use, Insurance

### Section I — Possession (Lines 121–132)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Possession: at closing | 122–123 | Checkbox "at closing" | Check if possession at closing |
| Possession: Pre-Closing Agreement | 124 | Checkbox "Pre-Closing Possession" | Check if pre-closing possession |
| Possession: Post-Closing Agreement | 124 | Checkbox "Post-Closing Possession" | Check if post-closing possession |
| Possession: Leased Property | 124 | Checkbox "Leased Property Addendum" | Check if leased |
| Non-delivery penalty per day | 127 | After "$" before "U.S. Dollars per day" | Daily penalty amount |

### Section J — Survey (Lines 143–150)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Survey: Surveyor Location Report | 143 | Checkbox "SURVEYOR LOCATION REPORT" | Check for location report |
| Survey: Boundary Survey | 144 | Checkbox "BOUNDARY SURVEY" | Check for boundary survey |
| Survey: Waived | 145 | Checkbox "WAIVED" | Check if survey waived |
| Survey cost: Buyer's expense | 145 | Checkbox "Buyer's expense" | Check if buyer pays |
| Survey cost: included in allowance | 146 | Checkbox "included in allowance" | Check if in allowance |
| Survey cost: Seller's expense | 146 | Checkbox "Seller's expense" | Check if seller pays |
| Survey cost: Shared equally | 146 | Checkbox "Shared equally" | Check if shared |

### Section K — Flood Area (Lines 151–155)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Flood: may terminate | 155 | Checkbox "may" | Check if buyer may terminate for flood |
| Flood: may not terminate | 155 | Checkbox "may not" | Check if buyer may not terminate |

### Section L — Building Use Limitations (Lines 156–168)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Intended use: single-family | 156 | Checkbox "single-family" | Check if single-family use |
| Intended use: owner occupied | 156 | Checkbox "owner occupied use" | Check if owner occupied |
| Intended use: rental | 156 | Checkbox "rental" | Check if rental/investment |
| Intended use: other | 157 | After "other" | Other intended use description |
| Diligence period days | 158 | After "have" before "days" | Days for building use diligence |
| NOT contingent on building use | 160 | Checkbox | Check if NOT contingent |
| IS contingent on building use | 161 | Checkbox | Check if IS contingent |
| Building use limitation detail | 161 | After "limitation(s):" | Specific limitation |

### Section M — Homeowner's Insurance (Lines 170–172)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Insurance commitment days | 171 | After "within" before "days" | Days to obtain insurance commitment |

---

## Page 4 — Environmental, Inspections

### Section N — Environmental Contaminants (Lines 173–188)

No fillable fields — boilerplate advisory and release language.

### Section O — Inspections (Lines 190–211)

| Field | Line | Location | Data Source |
|---|---|---|---|
| O.1 Buyer WAIVES inspections | 195 | Checkbox before "BUYER WAIVES" | Check if buyer waives inspection |
| O.2 Buyer RESERVES right to inspect | 202 | Checkbox before "BUYER RESERVES" | Check if buyer reserves inspection right |
| O.3 Property sold AS IS | 211 | Checkbox before "PROPERTY IS SOLD 'AS IS'" | Check if sold as-is |

### Section P — Inspection/Response Period (Lines 213–236)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Initial inspection days | 215 | After "have" before "days" | Days for initial inspection (e.g., "10") |
| Scope of inspection additions | 221 | After "and/or the following:" to end of line | Additional inspection scope items |
| Additional inspection days | 225 | After "have" before "additional days" | Additional days for lead paint/radon/mold testing |

---

## Page 5 — Home Warranty, Disclosures, Title, Taxes

### Section Q — Limited Home Warranty (Lines 254–260)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Warranty: will / will not be provided | 256 | Checkboxes "will" / "will not" | Whether warranty is provided |
| Warranty cost cap | 256 | After "not to exceed $" | Maximum warranty cost |
| Warranty charged to: Seller | 257 | Checkbox "Seller" | Check if seller pays warranty |
| Warranty charged to: Buyer | 257 | Checkbox "Buyer" | Check if buyer pays warranty |
| Warranty ordered by: Seller | 257 | Checkbox "Seller" | Check if seller orders |
| Warranty ordered by: Buyer | 257 | Checkbox "Buyer" | Check if buyer orders |

### Section R — Disclosures (Lines 265–269)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Seller disclosure: has received | 266 | Checkbox "has" | Check if buyer has received seller disclosure |
| Seller disclosure: has not received | 266 | Checkbox "has not" | Check if not yet received |
| Seller disclosure: not applicable | 266 | Checkbox "not applicable" | Check if N/A |
| Lead paint: has received | 268 | Checkbox "has" | Check if lead paint cert received |
| Lead paint: has not received | 268 | Checkbox "has not" | Check if not received |
| Lead paint: not applicable | 268 | Checkbox "not applicable" | Check if N/A (post-1978 construction) |

### Section S — Title Approval (Lines 271–288)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Title: insurance commitment | 271 | Checkbox "a title insurance commitment" | Check for title insurance commitment |
| Title: abstract | 273 | Checkbox "an abstract of title" | Check for abstract |
| Owner's title premium: Buyer | 279 | Checkbox "Buyer" | Check if buyer pays owner's policy |
| Owner's title premium: included in allowance | 280 | Checkbox "included in allowance" | Check if in allowance |
| Owner's title premium: Seller | 280 | Checkbox "Seller" | Check if seller pays |
| Owner's title premium: Shared | 280 | Checkbox "Shared equally" | Check if shared |
| Lender's title premium: Buyer | 283 | Checkbox "Buyer" | Check if buyer pays lender's policy |
| Lender's title premium: included in allowance | 284 | Checkbox "included in allowance" | Check if in allowance |
| Lender's title premium: Seller | 284 | Checkbox "Seller" | Check if seller pays |
| Lender's title premium: Shared | 284 | Checkbox "Shared equally" | Check if shared |
| Lender's title: Other | 284 | After "Other" | Other arrangement |
| Title company selected by: Seller | 287 | Checkbox "Seller" | Check if seller selects |
| Title company selected by: Buyer | 287 | Checkbox "Buyer" | Check if buyer selects |
| Order commitment: immediately | 288 | Checkbox "immediately" | Check if order immediately |
| Order commitment: other | 288 | Checkbox "other:" + fill | Other timing |

### Section T — Taxes (Lines 297–301)

| Field | Line | Location | Data Source |
|---|---|---|---|
| T.1 Buyer assumes taxes | 298 | Checkbox "1." | Check if buyer assumes taxes from date |
| Tax assumption date | 299 | After "payable on" | Date buyer assumes taxes |
| T.2 Seller pays prior year | 301 | Checkbox "2." | Check if seller pays prior accrued taxes |
| T.3 Tax credit amount | 303 | After "credit of $" | Tax credit dollar amount |

---

## Page 6 — Prorations, Time, HOA

### Section U — Prorations (Lines 318–326)

No fillable fields — standard proration language.

### Section V — Time (Lines 328–333)

No fillable fields — time is of the essence boilerplate.

### Section W — HOA (Lines 335–356)

| Field | Line | Location | Data Source |
|---|---|---|---|
| HOA document delivery days | 337 | After "within" before "days" | Days for HOA documents (default: 10) |
| HOA response days | 346 | After "within" before "days" | Days for buyer response to HOA docs |
| HOA approval days | 350 | After "within" before "days" | Days for HOA approval of sale |

---

## Page 7 — Additional Provisions, Attorney's Fees, Fair Housing

### Section Z — Additional Provisions (Lines 368–424)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Z.5 Conveyance: or by | 382 | After "Warranty Deed, or by" | Alternative conveyance method (if any) |
| Z.16 Buyer RE license # | 421 | After "License #" | Buyer's RE license number if applicable |

No other fillable fields on this page — all boilerplate.

---

## Page 8 — Further Conditions, Acknowledgements, Expiration, Buyer Signatures

### Section AA — Further Conditions (Lines 426–440)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Further conditions line 1 | 427 | Full line after "addenda):" | Additional conditions text — line 1 |
| Further conditions line 2 | 428 | Full line | Line 2 |
| Further conditions line 3 | 429 | Full line | Line 3 |
| Further conditions line 4 | 430 | Full line | Line 4 |
| Further conditions line 5 | 431 | Full line | Line 5 |
| Further conditions line 6 | 432 | Full line | Line 6 |
| Further conditions line 7 | 433 | Full line | Line 7 |
| Further conditions line 8 | 434 | Full line | Line 8 |
| Further conditions line 9 | 435 | Full line | Line 9 |
| Further conditions line 10 | 436 | Full line | Line 10 |
| Further conditions line 11 | 437 | Full line | Line 11 |
| Further conditions line 12 | 438 | Full line | Line 12 |
| Further conditions line 13 | 439 | Full line | Line 13 |
| Further conditions line 14 | 440 | Full line | Line 14 |

**Common further conditions to include:**
- Escalation clause language (from Step 7B)
- Appraisal gap coverage language
- Personal property inclusions not covered in Section B
- Addenda references (inspection addendum, financing addendum, etc.)
- Any non-standard terms the agent has drafted

### Section CC — Acknowledgements (Line 447)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Limited agency: is | 447 | Checkbox "is" | Check if limited agency transaction |
| Limited agency: is not | 447 | Checkbox "is not" | Check if NOT limited agency |

### Expiration of Offer (Lines 451–452)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Expiration: AM | 452 | Checkbox "AM" | Check if AM |
| Expiration: PM | 452 | Checkbox "PM" | Check if PM |
| Expiration: Noon | 452 | Checkbox "Noon" | Check if Noon |
| Expiration date/time | 451 | After "by" to end of line | Expiration date (e.g., "April 10, 2026") |
| Expiration on line | 452 | After "on" to before AM/PM | Expiration time if not noon |

### Buyer Signatures (Lines 472–477)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Buyer 1 printed name | 477 | Under "PRINTED" (left) | Buyer 1 full legal name |
| Buyer 2 printed name | 477 | Under "PRINTED" (right) | Buyer 2 full legal name (if applicable) |

**Note:** Signature lines (472–474) and DATE fields are left blank — these are signed by the parties, not pre-filled.

---

## Page 9 — Seller's Response, Seller Signatures

### Seller's Response (Lines 478–487)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Response date | 480 | After "On" | Date of seller response |
| Response time: AM | 480 | Checkbox "AM" | Check if AM |
| Response time: PM | 480 | Checkbox "PM" | Check if PM |
| Response time: Noon | 480 | Checkbox "Noon" | Check if Noon |
| Response: Accepted | 482 | Checkbox "1." | Check if accepted |
| Response: Rejected | 484 | Checkbox "2." | Check if rejected |
| Response: Countered | 486 | Checkbox "3." | Check if countered |

### Seller Signatures (Lines 492–497)

| Field | Line | Location | Data Source |
|---|---|---|---|
| Seller 1 printed name | 497 | Under "PRINTED" (left) | Seller 1 full legal name |
| Seller 2 printed name | 497 | Under "PRINTED" (right) | Seller 2 full legal name (if applicable) |

**Note:** Signature lines and DATE fields are left blank — signed by parties.

---

## Property Address Footer

Every page has a "(Property Address)" footer line at the bottom. This should be filled with the property address on every page for identification.

| Field | Page | Location | Data Source |
|---|---|---|---|
| Property Address footer | 1–9 | Bottom of each page, centered | Property street address |

---

## Data Collection Summary

To fill IAR Form 150, the following data points are needed from the offer workflow:

### Required (Every Offer)
1. **Date** — offer date
2. **Buyer name(s)** — full legal name(s)
3. **Property address** — street, city, township, county, ZIP
4. **Legal description** — from tax records or "See attached"
5. **Purchase price** — numeric and written
6. **Earnest money amount** — numeric and written
7. **Earnest money delivery timeline** — hours or days
8. **Escrow agent** — who holds earnest money
9. **Payment method** — cash or financing type
10. **Closing date** — target date
11. **Possession** — at closing or other arrangement
12. **Inspection election** — waive, reserve, or as-is
13. **Inspection days** — if reserving (e.g., 10)
14. **Offer expiration** — date and time
15. **Agency type** — limited or not limited

### Required (Financed Purchases)
16. **Loan type** — conventional, FHA, VA, USDA, other
17. **LTV percentage** — loan-to-value ratio
18. **Loan term** — years
19. **Interest rate cap** — maximum rate
20. **Points cap** — maximum points
21. **Application days** — days to apply for financing
22. **Approval days** — days for loan approval

### Optional / Situational
23. **Seller concessions** — amount or percentage
24. **Buyer broker compensation** — if seller pays
25. **Appraisal gap coverage language** — in further conditions
26. **Escalation clause language** — in further conditions
27. **Home sale contingency details** — address, close date
28. **Smart home devices** — inclusions
29. **Excluded items** — leased items, etc.
30. **Survey election** — type, who pays
31. **Flood termination right** — may/may not terminate
32. **Building use** — intended use, diligence period
33. **Insurance days** — days for homeowner's insurance commitment
34. **Home warranty** — will/will not, cost, who pays/orders
35. **Disclosure receipt status** — seller disclosure, lead paint
36. **Title insurance elections** — who pays owner's/lender's policies, who selects company
37. **Tax handling** — which paragraph applies
38. **HOA timelines** — if applicable
39. **Further conditions** — escalation, appraisal gap, addenda, etc.
40. **Broker info** — listing and selling broker/agent names, office codes, MLS IDs

---

## Fill Process

1. Copy the blank template to a working file
2. Use the `pdf` skill's FORMS.md → Approach B (Visual Estimation) workflow:
   a. Convert PDF to images
   b. For each page with fields to fill, crop relevant areas to get precise coordinates
   c. Build `fields.json` with entry positions and values
   d. Run `fill_pdf_form_with_annotations.py`
   e. Verify output with `convert_pdf_to_images.py`
3. The filled PDF should be saved as `[buyer-last-name]-offer-[property-address]-[date].pdf`

**Important:** Signature lines and DATE fields next to signatures are NEVER pre-filled. These are completed by the signing parties through their contract platform (Dotloop, ZipForms, etc.).
