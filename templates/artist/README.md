# Artist Memecoin Site Template

This is a generic, parameterizable HTML template for creating artist memecoin websites. It's designed to be used with a template engine or script that can replace placeholders with actual content.

## Template Variables

The template uses `{{VARIABLE_NAME}}` syntax for simple replacements and `{{#SECTION}}...{{/SECTION}}` for conditional/repeating blocks (Mustache-style syntax).

### Core Information

- `{{TOKEN_NAME}}` - Full name of the token (e.g., "SmoovCoin")
- `{{TICKER_SYMBOL}}` - Ticker symbol (e.g., "SMV")
- `{{ARTIST_NAME}}` - Artist's name (e.g., "JP Cali Smoov")
- `{{ASSETS_PATH}}` - Path to assets folder (e.g., "assets")

### Hero Section

- `{{HERO_BADGE}}` - Badge text (e.g., "LIVE")
- `{{HERO_SUBTITLE}}` - Main hero subtitle
- `{{HERO_DESCRIPTION}}` - Hero paragraph description
- `{{TOKEN_TAGLINE}}` - Short tagline below hero stats
- `{{HERO_IMAGE}}` - Hero image filename
- `{{HERO_VIDEO}}` - (Optional) Hero video filename (if provided, video will be used instead of image)
- `{{HERO_BADGE_TEXT}}` - Text in the floating badge (e.g., "🎤 BATTLE TESTED")
- `{{HERO_BADGE_DESCRIPTION}}` - Description in the floating badge

### Scrolling Banner

- `{{SCROLLING_BANNER_TEXT}}` - Text to repeat in scrolling banner

### Artist Section

- `{{ARTIST_DESCRIPTION}}` - Main artist description paragraph
- `{{ARTIST_PROFILE_TAGLINE}}` - Tagline shown next to profile image
- `{{PROFILE_IMAGE}}` - Profile image filename

#### Artist Features (Array)

```
{{#ARTIST_FEATURES}}
  - {{ICON}} - Emoji or icon
  - {{TITLE}} - Feature title
  - {{DESCRIPTION}} - Feature description
{{/ARTIST_FEATURES}}
```

### Quick Facts

- `{{TOTAL_SUPPLY}}` - Total token supply (e.g., "10,000,000")
- `{{SUPPLY_TYPE}}` - Supply type (e.g., "Fixed, non-inflationary")
- `{{BLOCKCHAIN}}` - Blockchain name (e.g., "TBD – designed for GALA Music integration")
- `{{PRIMARY_UTILITY}}` - Primary utility description
- `{{UTILITY_DISCLAIMER}}` - Disclaimer about utility

### Concept Section

- `{{CONCEPT_DESCRIPTION}}` - Main concept description
- `{{CONCEPT_IDEAS}}` - Array of idea bullet points
- `{{CONCEPT_VIBES}}` - Array of vibe bullet points

### Reason Section

- `{{REASON_DESCRIPTION}}` - Main reason description

#### Reason Points (Array)

```
{{#REASON_POINTS}}
  - {{ICON}} - Emoji
  - {{TITLE}} - Point title
  - {{DESCRIPTION}} - OR paragraph description
  - {{BULLET_POINTS}} - OR array of bullet points
{{/REASON_POINTS}}
```

### Tokenomics

- `{{TOKENOMICS_DESCRIPTION}}` - Tokenomics section description
- `{{TOKENOMICS_BADGES}}` - Array of badge texts (e.g., ["Fair Launch", "No Presale"])
- `{{SUPPLY_DESCRIPTION}}` - Description for total supply card
- `{{CREATOR_BUY_IN_PERCENTAGE}}` - Percentage (e.g., "50")
- `{{CREATOR_BUY_IN_AMOUNT}}` - Amount (e.g., "5,000,000")
- `{{CREATOR_BUY_IN_DESCRIPTION}}` - Creator buy-in description
- `{{PUBLIC_PERCENTAGE}}` - Public allocation percentage
- `{{PUBLIC_DESCRIPTION}}` - Public allocation description
- `{{CREATOR_ALLOCATION_BENEFITS}}` - Array of benefit bullet points
- `{{CREATOR_VESTING_NOTE}}` - Note about vesting

#### Public Allocations (Array)

```
{{#PUBLIC_ALLOCATIONS}}
  - {{LABEL}} - Allocation label
  - {{PERCENTAGE}} - Percentage (number)
  - {{AMOUNT}} - Amount (e.g., "2,000,000")
  - {{COLOR_CLASS}} - Tailwind color class (e.g., "bg-emerald-400")
  - {{DESCRIPTION}} - Allocation description
{{/PUBLIC_ALLOCATIONS}}
```

#### Market Dynamics (Array)

```
{{#MARKET_DYNAMICS}}
  - {{TITLE}} - Section title
  - {{DESCRIPTION}} - OR paragraph description
  - {{BULLET_POINTS}} - OR array of bullet points
{{/MARKET_DYNAMICS}}
```

### Roadmap

- `{{ROADMAP_DESCRIPTION}}` - Roadmap intro description

#### Roadmap Phases (Array)

```
{{#ROADMAP_PHASES}}
  - {{PHASE_LABEL}} - Phase label (e.g., "Phase 1")
  - {{TITLE}} - Phase title
  - {{DESCRIPTION}} - Phase description
  - {{COLOR}} - Tailwind color name (e.g., "emerald", "amber", "sky")
{{/ROADMAP_PHASES}}
```

### Tracks Section

- `{{TRACKS_DESCRIPTION}}` - Tracks section description
- `{{TRACK_IMAGES}}` - (Optional) Array of track objects with:
  - `{{IMAGE_URL}}` - Track image URL
  - `{{TRACK_NAME}}` - Track name

### CTA Section

- `{{CTA_TITLE}}` - CTA section title
- `{{CTA_DESCRIPTION}}` - CTA description
- `{{CTA_BUTTON_1_TEXT}}` - First button text
- `{{CTA_BUTTON_2_TEXT}}` - Second button text

### Social Links

- `{{SOCIALS_DESCRIPTION}}` - Social links intro
- `{{SOCIAL_IMAGE}}` - Image for GALA Music card
- `{{GALA_MUSIC_DESCRIPTION}}` - GALA Music card description
- `{{GALA_MUSIC_URL}}` - GALA Music artist URL

#### Social Links (Array)

```
{{#SOCIAL_LINKS}}
  - {{PLATFORM_NAME}} - Platform name (e.g., "X (Twitter)")
  - {{URL}} - Social media URL
  - {{DESCRIPTION}} - Card description
  - {{HANDLE}} - Social handle (e.g., "@username")
  - {{ICON_SVG}} - SVG path data for icon
{{/SOCIAL_LINKS}}
```

### Legal

- `{{LEGAL_NOTICE_1}}` - First legal notice paragraph
- `{{LEGAL_NOTICE_2}}` - Second legal notice paragraph

### Footer

- `{{FOOTER_IMAGE}}` - Footer logo image
- `{{FOOTER_TAGLINE}}` - Footer tagline
- `{{FOOTER_DESCRIPTION}}` - Footer description
- `{{FOOTER_DISCLAIMER}}` - Footer disclaimer

#### Footer Social Links (Array)

```
{{#FOOTER_SOCIAL_LINKS}}
  - {{URL}} - Link URL
  - {{LABEL}} - Link label
{{/FOOTER_SOCIAL_LINKS}}
```

## Usage Example

This template is designed to work with template engines like:
- Mustache
- Handlebars
- Jinja2
- Custom script

### Example Data Structure (JSON)

```json
{
  "TOKEN_NAME": "SmoovCoin",
  "TICKER_SYMBOL": "SMV",
  "ARTIST_NAME": "JP Cali Smoov",
  "ASSETS_PATH": "assets",
  "HERO_BADGE": "LIVE",
  "HERO_SUBTITLE": "The West Coast Memecoin Movement",
  "HERO_DESCRIPTION": "A fan-powered coin orbiting JP Cali Smoov's mission to change the world...",
  "TOKEN_TAGLINE": "SmoovCoin — On a mission to change the world, one bar at a time.",
  "HERO_IMAGE": "tokenlogo.jpg",
  "HERO_VIDEO": "rotating-coin.mp4",
  "HERO_BADGE_TEXT": "🎤 BATTLE TESTED",
  "HERO_BADGE_DESCRIPTION": "Real bars, real community, real utility.",
  "SCROLLING_BANNER_TEXT": "JP Cali Smoov • OnAMission2ChangeThe🌎 • SmoovCoin • Battle rap meets Web3",
  "ARTIST_DESCRIPTION": "A battle rap champion, community activist...",
  "ARTIST_PROFILE_TAGLINE": "JP Cali Smoov",
  "PROFILE_IMAGE": "tokenlogo.jpg",
  "ARTIST_FEATURES": [
    {
      "ICON": "🎤",
      "TITLE": "Battle-tested bars",
      "DESCRIPTION": "Winner of Hitman Holla's reality show..."
    }
  ],
  "TOTAL_SUPPLY": "10,000,000",
  "SUPPLY_TYPE": "Fixed, non-inflationary",
  "BLOCKCHAIN": "TBD – designed for GALA Music integration",
  "PRIMARY_UTILITY": "Purchasing tracks & drops via GALA Music",
  "UTILITY_DISCLAIMER": "Exact integration details and supported platforms will be announced at launch.",
  "GALA_MUSIC_URL": "https://music.gala.com/artists/jp-cali-smoov",
  "SOCIAL_LINKS": [
    {
      "PLATFORM_NAME": "X (Twitter)",
      "URL": "https://x.com/calismoov4life?s=21",
      "DESCRIPTION": "Get SmoovCoin updates...",
      "HANDLE": "@calismoov4life",
      "ICON_SVG": "<path d=\"M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z\"/>"
    }
  ]
}
```

## Notes

- The template uses Mustache-style syntax (`{{#}}` for sections, `{{^}}` for inverted sections)
- Arrays are used for repeating content (features, allocations, phases, etc.)
- Optional sections use `{{#VAR}}...{{/VAR}}` and `{{^VAR}}...{{/VAR}}` for conditional rendering
- Color classes should be Tailwind CSS color names (e.g., "emerald", "amber", "pink", "sky")
- All image paths are relative to the `{{ASSETS_PATH}}` variable
- The template is fully responsive and uses Tailwind CSS via CDN

## Customization

To customize colors, modify the gradient classes in:
- Hero badge: `from-amber-400 to-pink-500`
- Hero title gradient: `from-amber-400 via-pink-500 to-emerald-400`
- Various hover states and accent colors

To add more sections, follow the existing pattern of using section variables and arrays.

