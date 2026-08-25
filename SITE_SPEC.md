# Video Site Specification

Please build a video streaming website using the eporner.com public API.

## 1. API (public, no API key required)

```
Search:  https://www.eporner.com/api/v2/video/search/?query=KEYWORD&per_page=16&page=PAGE&thumbsize=big
Detail:  https://www.eporner.com/api/v2/video/id/?id=VIDEO_ID
```

Response fields: `id`, `title`, `embed`, `default_thumb.src`, `length_min`, `length_sec`, `views`, `keywords`

Notes:
- `query` must be URL-encoded
- `per_page` = number of results per request (use 16)
- `page` = page number (used for infinite scroll)
- `thumbsize=big` for larger thumbnails
- `embed` is the iframe player URL for playing a video

## 2. Categories

- Asian
- Japanese
- Korean
- Myanmar
- HD

## 3. Features

- Category buttons (filter videos by query)
- Search box (search by keyword)
- Video card grid: thumbnail, duration, views count, title
- Infinite scroll (load next page when scrolled to bottom)
- Detail page with iframe embed player
- Favorites (saved to localStorage)
- Share video link (URL with `#video/ID` hash)
- 18+ age verification overlay (gate on entry)
- Bottom navigation: Discover, Favorites

## 4. Design

- Mobile-first responsive layout
- Dark theme, accent color: #ff2a5f
- Video grid: 2 columns on mobile, 4 columns on desktop
- Sticky header with logo + search box

## 5. Ad Integration (optional)

Adsterra ad codes will be provided separately. Include slots for:
- Leaderboard banner (728x90 desktop / 320x50 mobile) below header
- 300x250 in detail page below player
- Native banner below video grid on home page
- Popunder (load after age verification)
- SocialBar (sticky bottom bar)
- Smartlink button in bottom nav
