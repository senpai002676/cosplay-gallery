# Cosplay Gallery

A modern responsive static cosplay gallery using only HTML, CSS and JavaScript. It is Cloudflare Pages friendly and does not upload or store images.

## Files

- `index.html` — homepage + latest albums
- `cosplay.html` — all albums + sorting
- `cosers.html` — cosplayer list
- `search.html` — search
- `album.html` — reusable album page + lightbox
- `script.js` — gallery logic
- `style.css` — site styling
- `data/albums.json` — single source of album data
- `data/album-template.json` — new album template

## Add an album

Open `data/albums.json` and add an object before the final `]`:

```json
{
  "id": "marin-kitagawa",
  "title": "Marin Kitagawa",
  "coser": "Coser Name",
  "character": "Marin Kitagawa",
  "series": "My Dress-Up Darling",
  "description": "Full description of the photo set.",
  "photos": 2,
  "cover": "https://example.com/photo-1.jpg",
  "date": "2026-09-12",
  "images": [
    "https://example.com/photo-1.jpg",
    "https://example.com/photo-2.jpg"
  ]
}
```

Use a unique lowercase `id`. `images` contains direct external image URLs and `cover` is used on cards. The script derives the displayed photo count from `images.length`. Search covers title, coser, character, series and description. Keep the JSON valid, including commas between objects.

## Cloudflare Pages Direct Upload

Create a Cloudflare Pages project using Direct Upload and upload the contents of this repository. No framework, build command, backend or GitHub integration is required for Pages Direct Upload.

After editing `data/albums.json`, upload a new deployment in Cloudflare Pages.

## Images

Images stay externally hosted. Use a host that permits embedding/hotlinking and only display images you have permission to use.

## Advertisement slots

Empty `ADVERTISEMENT` slots are included at the top of every page, between album information and photos, and at the bottom of the album page. Replace the slot text with your ad provider code later.