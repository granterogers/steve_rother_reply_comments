# Comment Reply Assistant

A small single-page tool for replying to comments on Steve Rother's YouTube channel.

Paste in a viewer's comment (and optionally their name), and it proposes a few
reply options that acknowledge what they actually said and end with a question,
so the conversation keeps going. Click "Copy" to grab a reply and paste it into
YouTube.

## Usage

Just open `index.html` in a browser — no build step, no server, no setup needed.
It can also be hosted directly via GitHub Pages by pointing Pages at this repo's
root.

Replies are generated via the Google Gemini API. The first time someone opens
the page on a given device, it shows a one-time field asking for a free Gemini
API key (from [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey),
no credit card needed). Once entered, the key is saved in that browser's local
storage and the field disappears — they won't be asked again on that device.
