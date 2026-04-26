# AGENTS.md

## Purpose

Defines how to add a new recipe post.

---

## File Location

Create a new file in:

```
/_posts/
```

---

## File Naming

```
YYYY-MM-DD-title.md
```

Example:

```
2026-04-25-jablecznik-joanny.md
```

Rules:

* lowercase only
* hyphens instead of spaces
* no Polish characters

---

## Frontmatter (Required)

```yaml
---
layout: post
title: "Polish title"
subtitle: "Optional polish subtitle"
cover-img: /assets/img/YYYY-MM-DD-name-01.jpg
thumbnail-img: /assets/img/YYYY-MM-DD-name-02.jpg
share-img: /assets/img/YYYY-MM-DD-name-01.jpg
tags: [tag1, tag2]
comments: true
---
```

---

## Images

* Store in:

```
/assets/img/
```

* Naming:

```
YYYY-MM-DD-name-01.jpg
YYYY-MM-DD-name-02.jpg
```

---

## Content Structure (Required)

```md
## Składniki

| składnik | ilość |

## Przepis
```

If recipe contains separate list of ingredients:

```md
## Składniki

### Sekcja (ex. Ciasto|Krem|Polewa)

| składnik | ilość |

## Przepis
```

---

## Formatting Rules

* Markdown only
* Tables for ingredients
* Use `##`, `###`
* Highlight key values (e.g. **160℃**)

---

## Special Blocks

```md
{: .box-note}
```

```md
{: .box-warning}
```

```md
{: .box-error}
```

---

## Validation Checklist

* [ ] filename correct
* [ ] frontmatter valid
* [ ] images exist
* [ ] renders correctly
* [ ] no typos

---

## Writing Style Guidelines

* Write in Polish
* Keep sentences short and clear
* Use simple, everyday language (no overcomplication)
* Prefer imperative form (e.g. "Dodaj", "Wymieszaj", "Piecz")
* Avoid unnecessary filler text
* Keep a consistent tone across posts
* Use emojis sparingly (or not at all)
* Be practical — focus on steps, not storytelling

Formatting:

* Use bold for key values (e.g. **160℃**, **10 min**)
* Keep sections structured and predictable
* Ingredients → clean table format
* Instructions → step-by-step

Goal:
Clear, readable, and easy-to-follow recipe.

---

## Git Workflow (Fork + PR)

1. Create a branch:

```bash
git checkout -b post/<slug>
```

2. Commit changes:

```bash
git add . -- ':!AGENTS.md'
git commit -m "Add post: <slug>"
```

3. Push to your fork:

```bash
git push origin post/<slug>
```

4. Create Pull Request to:

```
jkotarska/przepysznik
```

Done.
