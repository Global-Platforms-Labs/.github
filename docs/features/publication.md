---
type: documentation
entity: feature
feature: profile-publication
version: 1.0
---

# Feature: profile publication

> Part of [Global Platforms Labs public profile](../overview.md)

## Summary

- Visitors see the organization identity, affiliation and public navigation.

## How It Works

### User Flow

1. Open the organization page.
2. Read the public introduction and view the banner.
3. Follow a public navigation link.

### Technical Flow

1. GitHub locates this repository's `profile/README.md`.
2. It renders the Markdown and supported HTML.
3. The browser requests the public banner from the embedded URL.

## Implementation

| Module | Symbols | Role |
|---|---|---|
| [Public profile](../modules/profile.md) | Banner `img`, navigation `a` elements | Content and image references |

## Configuration

- Profile content is versioned in Git; organization description/avatar settings are separate.
- No runtime environment variables, application credentials or package manager are needed.

## Edge Cases & Limitations

- A renamed asset or incorrect branch in the raw URL breaks the image.
- A repository file preview is not a complete test of the organization-page layout.
- Caches can delay an appearance change; inspect the saved source and rendered asset separately.
- Root documentation changes do not change profile content.

## Related Features

- [Maintenance workflow](../maintenance.md)
