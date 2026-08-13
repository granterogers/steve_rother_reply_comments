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

Replies are generated via the Google Gemini API using a key embedded directly in
`index.html`, so anyone with the link can use it without any per-person setup.

**Note:** because this is a plain static page, that API key is visible to anyone
who views the page source — there's no way to hide a secret in client-side-only
code. It's a free-tier key with no billing attached, so the worst case of misuse
is quota exhaustion, not a bill. If it ever gets abused, generate a new key at
[aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) and swap
the `API_KEY` constant near the top of the `<script>` block in `index.html`.
