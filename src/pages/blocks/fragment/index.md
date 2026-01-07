---
title: Fragment Block
description: Include reusable content from other pages into your current page using the Fragment block.
---

# Fragment Block

Include reusable content from other markdown files.

## Syntax

```markdown
<Fragment src="path/to/your/fragment.md" />
```

## Parameters

- **src**: Path to the fragment file
  - Relative paths: `../shared/nav.md`, `./components/card.md`
  - Absolute paths: `/global/footer.md`


## Notes
- 
- Fragments are cached in sessionStorage for better performance
- Images and assets paths are automatically resolved
