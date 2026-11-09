# Embogo Motel-LUGALA

A one-page website for Embogo Motel- LUGALA, Bar and Massage. Guests can browse the rooms, look through the photos and send a booking request to reception on WhatsApp.

WhatsApp: 256779904035
Email: bwikizoc@gmail.com

## Features

- Hero section with quick check-in, check-out and guest selection
- Five room cards with photos, features and nightly rates
- Facilities list: hot showers, mosquito nets, bar, pool table, lounge and TV, parking, reception, massage
- Photo gallery with a full-screen viewer (arrow keys and Escape work)
- Three-step booking form: stay, guest details, payment
- Payment choices: MTN Mobile Money, Airtel Money, cash at reception, bank transfer
- Live booking summary with the total calculated from nights and rooms
- Booking message sent to reception through WhatsApp, with a Copy button as a backup
- Works on phones and desktops, in light and dark mode

No money is taken on the website. Reception confirms each booking and shares payment details on WhatsApp.

## Project structure

```
embogo/
├── index.html     the whole site (HTML, CSS and JavaScript)
├── README.md      this file
└── img/           photos of the rooms, bar, lounge, reception and compound
```

There is nothing to install or build. Open `index.html` in a browser to run it.

## Editing the site

All the details you are likely to change are in the `CONFIG` block near the top of the `<script>` section in `index.html`.

### Room prices

Each room has a `rate` value. Replace `null` with the price per night in UGX, as a plain number with no commas or quotes:

```js
{ id: 'plum', name: 'Plum Room', ..., rate: 60000, ... }
```

Rooms with `rate: null` show "Ask for tonight's rate". Rooms with a price show it, and the booking summary works out the total.

### Payment details

Each payment method has a `detail` value. Replace `null` with text in quotes to show it under that method:

```js
{ id: 'mtn', tag: 'MTN MoMo', name: 'MTN Mobile Money', text: '...', detail: 'Send to 0779 904 035' },
```

### WhatsApp number

Change `whatsapp` in `CONFIG` to the number in international format with no plus sign or spaces, for example `256779904035`. Update `phoneDisplay` to match. The phone number is also written in the contact section and the hero caption in the HTML.

### Photos

Replace files in `img/` with your own, keeping the same file names, or change the paths in the `CONFIG.rooms` and `GALLERY` lists.

## Deploying on GitHub Pages

1. Create a new repository on GitHub and upload the contents of this folder.
2. Go to Settings → Pages.
3. Under Build and deployment, choose Deploy from a branch, select the `main` branch and the `/ (root)` folder, then save.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Notes

- Fonts (Bricolage Grotesque, Instrument Sans, DM Mono) load from Google Fonts. The site falls back to system fonts if they cannot load.
- Bookings are not stored anywhere. They exist only as the WhatsApp message the guest sends.
- Availability is not checked automatically. Reception confirms every request.

## Contact

Embogo Motel-LUGALA
WhatsApp: 0779 904 035
Email: bwikizoc@gmail.com
