# Electrical Invoice Generator

A browser-based invoice builder for Shanjana Electricals. It uses Next.js + React + TypeScript and creates PDFs locally with jsPDF. There is no API server, database, account login, or paid service requirement.

## Features

- Editable company header, bank details, IFSC, and UPI details.
- Customer name, address, phone, invoice number, and date.
- Add or remove product rows dynamically.
- Automatic line amounts, subtotal, fixed/percentage discount, gross amount, and amount-in-words.
- Download the active invoice as a PDF.
- Select multiple invoices and combine them into one PDF. Every invoice starts on a new page; long product tables continue onto additional pages.
- Automatic local browser saving through `localStorage`.
- JSON backup and restore so data can be moved to another browser or computer.
- A4 portrait PDF layout inspired by the supplied Shanjana Electricals reference image.

## Requirements

- Node.js 20.9 or later.
- npm.

## Run locally

Open a terminal in this project folder and run:

```bash
npm install
npm run dev
```

Open <http://localhost:3000>.

For a production build:

```bash
npm run typecheck
npm run build
npm start
```

## Deploy to Vercel

1. Create a GitHub repository and push this project.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Keep the detected framework as **Next.js** and the default build command (`npm run build`).
4. Deploy. No environment variables are required.

## Data and privacy notes

- Invoice data and settings are saved only in the browser's `localStorage` on the device and browser where they were entered.
- Data is not synchronized between devices or users.
- Clearing browser site data can remove saved invoices. Use **Backup data** regularly and before switching browsers/devices.
- PDF creation runs in the browser. No invoice/customer content is sent to an application database or PDF API.

## PDF layout notes

The PDF is A4 portrait with a black outer border, centered red company name, blue address and phone, customer/invoice metadata, green table headings, serial number/description/quantity/rate/amount columns, subtotal/discount/gross amount summary, amount in words, and bank/UPI footer. The web preview is a compact visual guide; the downloaded PDF is the print layout.

The sample company and bank values are prefilled from the reference image. Update them under **Company settings** before issuing invoices. Review account number, IFSC, UPI number, customer data, and totals before printing or sending any bill.
# Electrical-Invoice-Generator
