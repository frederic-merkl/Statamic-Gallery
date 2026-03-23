# Image Grid with CSS Spotlight

Minimalistic Statamic image grid using pure CSS for interaction.

## Features
- **Spotlight Effect**: Darkens siblings when a specific image is hovered.
- **Pure CSS**: No JavaScript. Powered by `group-has` and `:not` (Tailwind CSS 3.4+).
- **Gap-Safe**: Effect only triggers on actual images, not on grid gaps.
- **Antlers Integration**: Handles dynamic looping via Statamic Assets.

## Core Logic
The interaction relies on the combination of `:has()` and `:not()`:
`group-has-[img:hover]:not-[&:hover]:brightness-10`

1. **`group-has-[img:hover]`**: Checks if any image within the group is currently hovered.
2. **`not-[&:hover]`**: Excludes the currently hovered image from the brightness reduction.
3. **`brightness-10`**: Applies heavy darkening to all non-hovered siblings.

## Development Mockups
Currently using Picsum for testing:
`src="https://picsum.photos/800/800?{{ index }}"`