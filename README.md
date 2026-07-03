# Blue Bill

**1st Place — HackMT 2024**

Hospitals charge insurers negotiated rates while uninsured patients get billed list price for the same procedure. Blue Bill helps uninsured patients fight back: photograph your itemized hospital bill, and it tells you which line items are overcharged and hands you a negotiation script to take back to the billing office.

## How it works

1. **Upload** a photo of an itemized hospital bill.
2. **OCR** — Azure Document Intelligence (Form Recognizer) extracts the line items.
3. **Price check** — each procedure is compared against an open dataset of typical costs to flag overcharges.
4. **Negotiation script** — OpenAI generates a personalized script citing the fair-price data, ready to use on a call with the hospital's billing department.

## Stack

- **Next.js** (App Router) + TypeScript
- **Azure Document Intelligence / Form Recognizer** — bill OCR
- **OpenAI** — negotiation script generation
- **Prisma** — procedure cost data
- **Jotai** — client state
- **Tailwind CSS**

## Running locally

```bash
npm install
npm run dev
```

Requires Azure Document Intelligence and OpenAI credentials in environment variables. Sample bills for testing live in `TestData/`.

Built by a student team in one weekend at [HackMT 2024](https://www.hackmt.com/) (project also known as BlueAid). Won 1st place overall.
