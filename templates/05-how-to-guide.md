# How-to guide template

| | |
|---|---|
| **Use for** | One specific task with one outcome, for a reader who already knows what they want to do. |
| **Not for** | Teaching concepts (use a concept document) or first-time onboarding (use the getting started guide). |
| **Reader** | Someone with a goal and basic familiarity with the product. |
| **Typical size** | Under 1 page. Up to 2 pages for complex tasks. |

This template follows the "how-to guide" type from the Diátaxis documentation framework: goal-oriented, practical, and free of explanation that the task does not need.

## Section guide

| Section | What belongs here | Required |
|---|---|---|
| Title | "[Verb] [object]", phrased the way a reader would search for it. | Yes |
| Introduction | One or two sentences: what the task achieves and when to do it. | Yes |
| Before you begin | Prerequisites for this task only: permissions, versions, and resources that must already exist. | If applicable |
| Steps | Numbered steps. One action per step. | Yes |
| Result | What the reader sees when the task succeeds. | Yes |
| Related | Links to the concept behind the task and to follow-up tasks. | Recommended |

---

## Template

````markdown
# [Verb] [object]

[What this task achieves.] [When or why a reader does it.]

## Before you begin

- [Permission or role]
- [Resource that must already exist]

## [Verb] [object]

1. [Action.]
2. [Action.]

   ```[language]
   [code or command, if needed]
   ```

3. [Action.]

**Result:** [What the reader sees.]

## Related

- [Link to concept]
- [Link to next task]
````

> **Guidance:**
> - Title the page with the words readers search for. "Cancel a shipment" beats "Shipment lifecycle management."
> - Start each step with the action. Put the location first if it helps: "In **Settings**, click **Webhooks**."
> - Put conditions before instructions: "If you use a proxy, set `PW_PROXY_URL`." The reader then knows whether to read the rest of the sentence.
> - If the task has two common variants, write two how-to guides or use tabs. Avoid long "if you use X, then … otherwise …" steps.
> - Leave out background. Link to the concept document instead.

---

## Example

> The following example uses the fictional Parcelwise API.

# Cancel a shipment

Cancel a shipment to void its label and get a refund of the label cost. You can cancel a shipment until the carrier scans the package.

## Before you begin

- You need an API key with the `shipments:write` scope.
- The shipment status must be `label_created`. Shipments with any other status cannot be canceled.

## Cancel the shipment

1. Get the shipment ID from the Parcelwise Dashboard or from the response to your create request. Shipment IDs start with `shp_`.
2. Send a `POST` request to the `cancel` endpoint:

   ```bash
   curl -X POST https://api.parcelwise.example/v1/shipments/shp_8Kd2LmQ4/cancel \
     -H "Authorization: Bearer $PW_API_KEY"
   ```

**Result:** The response contains `"status": "canceled"`. The refund appears on your next invoice.

## Related

- Shipment statuses
- Create a return label
