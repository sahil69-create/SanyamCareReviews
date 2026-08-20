# WhatsApp Review Request

<img src="message-thumbnail.jpeg" alt="message thumbnail" srcset="">

A lightweight, mobile-first customer feedback page for sending a personalized Google Review request through WhatsApp.

## Features

- Customer name and WhatsApp number form
- Indian mobile validation: exactly 10 digits, starting with 6, 7, 8, or 9
- Automatic removal of non-numeric phone characters
- Live personalized WhatsApp message preview
- Redirects directly to the entered customer's pre-filled WhatsApp chat
- No backend, database, API, form submission, logging, or browser storage
- Responsive desktop, tablet, and mobile layout
- Accessible labels, focus states, validation messages, and reduced-motion support
- Local customer-support image: `message-thumbnail.jpeg`

## Run Locally

No build step is required.

1. Open `index.html` directly in a browser, or
2. Run a local static server from the `Google Review` folder:

```powershell
python -m http.server 8080
```

Then open <http://localhost:8080>.

## How It Works

1. Enter the customer name.
2. Enter a valid 10-digit Indian WhatsApp number.
3. Review the personalized message.
4. Click **Send on WhatsApp**.
5. The browser redirects directly to that customer's pre-filled WhatsApp chat.

The direct `wa.me` URL supports text only. WhatsApp does not allow a webpage to attach an image automatically to a specific chat through that URL. The page therefore prioritizes direct number redirection and pre-filled text.

The direct chat URL format is:

```text
https://wa.me/91XXXXXXXXXX?text=ENCODED_MESSAGE
```

The number is used only at click time to create the WhatsApp URL. It is never saved or sent to this project or any server.

## Project Files

```text
Google Review/
├── index.html
├── message-thumbnail.jpeg
└── README.md
```

## Deployment

This is a static HTML project and can be deployed to GitHub Pages, Vercel, Netlify, or any static hosting provider. Upload the complete `Google Review` folder and use `index.html` as the entry page.

## Technology

- HTML5
- Tailwind CSS via CDN
- Custom CSS
- Vanilla JavaScript

No React, Vue, Angular, Bootstrap, backend, database, or WhatsApp Business API is required.
