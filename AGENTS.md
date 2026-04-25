# AGENTS.md - Instructions for Adding Recipes to Przepysznik

## Where Recipes Are Located
All recipes are stored in the `_posts` directory as individual markdown files.
Each recipe follows the Jekyll blog post format with YAML frontmatter.

## How to Add a New Recipe

### 1. Create a New File
Create a new markdown file in the `_posts` directory with the naming convention:
```
YYYY-MM-DD-title-of-recipe.md
```
Where:
- YYYY-MM-DD is the current date (or desired publish date)
- title-of-recipe is a lowercase, hyphen-separated version of the recipe title
- Example: `2026-04-25-szarlotka-jabłkowa.md`

### 2. Required Frontmatter
Each recipe file must begin with YAML frontmatter enclosed in `---` lines:

```markdown
---
layout: post
title: "Recipe Title in Polish"
subtitle: "Optional English title or description"
cover-img: "/path/to/image.jpg" # Optional: large background image
thumbnail-img: "/path/to/image.jpg" # Optional: small image for homepage
share-img: "/path/to/image.jpg" # Optional: image for social sharing
tags: [tag1, tag2, tag3] # Optional: relevant tags (e.g., [deser, ciasto, owoce])
author: "Author Name" # Optional: defaults to site author
comments: true # Optional: enable/disable comments
---
```

### 3. Recipe Content
After the frontmatter, add the recipe content in markdown format:

#### Suggested Structure:
- Brief introduction about the recipe
- **Składniki** (Ingredients) section - can use a table or list
- **Przepis** (Instructions) section with numbered steps
- Optional tips or notes using Jekyll callout boxes:
  - `{: .box-warning}` for warnings
  - `{: .box-note}` for notes
  - `{: .box-error}` for errors

### 4. Example Recipe Format
See existing recipes in `_posts/` for examples:
- `2022-01-13-chocolate-chip-cookies.md` - shows ingredient table and warnings
- `2024-12-22-Jablecznik-Joanny.md` - another recipe example

### 5. Important Notes
- All images should be placed in the `assets/img/` directory or use external URLs
- The site uses kramdown markdown processor
- Recipes are automatically added to the site feed and tag pages
- After adding a file, commit and push to GitHub to trigger site rebuild
- The site is built with Jekyll using the Beautiful Jekyll theme

### 6. Tagging Guidelines
Use relevant Polish tags such as:
- deser, obiad, śniadanie, kolacja
- ciasto, ciasteczka, chleb, zupa
- mięso, ryby, wegetariańskie, wegańskie
- sezonowe (wiosna, lato, jesień, zima)
- specjalne okazje (święta, urodziny, itp.)

## Workflow Summary
1. Create file: `_posts/YYYY-MM-DD-title.md`
2. Add proper YAML frontmatter
3. Write recipe content in markdown
4. Commit and push to your fork of the repository
5. Create a Pull Request (PR) to the main repository (jkotarska/przepysznik)
6. After PR is merged, site will automatically update