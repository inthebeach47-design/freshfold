# FreshFold Laundry Quotation System

A self-contained quotation builder for FreshFold Laundry. It runs in the browser and does not send quotation or customer information to an API or database. Quotes exist only in the current browser tab and are cleared when you start a new quote or close the tab.

## Run locally

Python 3 is required to serve the files on localhost, which enables offline caching:

```sh
npm run dev
```

Open <http://localhost:4173>. You can also deploy these static files to Vercel or another static web host.

## Offline use

Open the app once while online so the browser can cache the page, scripts, styles, service list, and logo. After that, the quotation builder and preview work offline. Service worker caching requires HTTPS or localhost; opening `index.html` directly from disk does not enable it.

## Create a PDF

Fill in the customer and service details, then use **Offline Preview** to review the live quotation. Return to the builder to edit any details. Choose **Save as PDF** and select **Save as PDF** in the browser's print dialog. No quotation is saved by the app; saving the PDF is handled by the browser and only happens when you choose a destination.
