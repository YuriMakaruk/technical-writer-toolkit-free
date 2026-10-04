# Getting started guide template

| | |
|---|---|
| **Use for** | Taking a new user from zero to one meaningful result as fast as possible. |
| **Not for** | Covering every option. Link to the user guide, how-to guides, and reference for that. |
| **Reader** | Someone evaluating or just starting to use the product. |
| **Typical size** | 1–3 pages. Target: finished in 10–20 minutes. |

## Section guide

| Section | What belongs here | Required |
|---|---|---|
| Introduction | What the reader will have at the end and how long it takes. | Yes |
| Before you begin | The shortest possible list of prerequisites, with links to get each one. | Yes |
| Steps | 3–7 numbered steps, each with a heading and a visible result. | Yes |
| Verify | How the reader knows it worked. | Yes |
| Next steps | 2–4 links to what most readers do next. | Yes |
| Clean up | How to delete test resources, if the guide created any that cost money or clutter an account. | If applicable |

**Design rule:** one path, no choices. If you must support alternatives (for example, two programming languages), use tabs rather than "if/else" instructions in the text.

---

## Template

````markdown
# Get started with [Product name]

In this guide, you [what the reader does]. At the end, you have [concrete
result]. It takes about [number] minutes.

## Before you begin

You need:

- [Account], which you can [create for free at Link]
- [Tool with minimum version], for example "Node.js 20 or later"

## Step 1: [Set up or install something]

[One sentence on why this step is needed, if not obvious.]

```bash
[command]
```

## Step 2: [Configure or connect]

[Instructions.]

## Step 3: [Do the core action]

[Instructions.]

The output is similar to the following:

```text
[expected output]
```

## Verify the result

[Where to look and what the reader should see.]

## Clean up

To avoid [charges/clutter], delete [resources]:

```bash
[command]
```

## Next steps

- [Link]: [What the reader learns or does there.]
- [Link]: [What the reader learns or does there.]
````

> **Guidance:**
> - Choose the result that best shows the product's value, not the simplest possible task.
> - Use sandbox or test credentials so the reader cannot cause real-world effects.
> - Every step must produce something the reader can see. If a step has no visible result, merge it with another step.
> - Remove optional configuration. Mention it in *Next steps* instead.
> - Time the guide with someone who has never used the product, and update the time estimate.

---

## Example

> The following excerpt uses the fictional Parcelwise API.

# Get started with the Parcelwise API

In this guide, you create a test shipment and download its shipping label. It takes about 10 minutes.

## Before you begin

You need:

- A Parcelwise account. You can create a free sandbox account at `dashboard.parcelwise.example/signup`.
- `curl` 7.68 or later

## Step 1: Get a sandbox API key

1. In the Parcelwise Dashboard, go to **Developers** > **API keys**.
2. Click **Create key**, select **Sandbox**, and then copy the key. Sandbox keys start with `pw_test_`.

## Step 2: Create a shipment

Replace `<your-api-key>` with your key, and then run:

```bash
curl https://api.parcelwise.example/v1/shipments \
  -H "Authorization: Bearer <your-api-key>" \
  -H "Content-Type: application/json" \
  -d '{"to_address": {"name": "Ana Silva", "line1": "Rua Augusta 100", "city": "Lisboa", "postal_code": "1100-053", "country": "PT"}, "parcel": {"weight_kg": 1.2}, "service": "standard"}'
```

The response contains the shipment ID and a label URL:

```json
{
  "id": "shp_8Kd2LmQ4",
  "status": "label_created",
  "label_url": "https://files.parcelwise.example/labels/shp_8Kd2LmQ4.pdf"
}
```

## Verify the result

Open the `label_url` in a browser. The label shows the recipient address and a barcode marked **SANDBOX – NOT FOR SHIPPING**.

## Next steps

- Handle webhooks: receive status updates when a shipment moves.
- API reference: see all shipment options.
