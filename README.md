# consult-next-steps

Static next-steps page for Lead From The Room consulting clients.
Hosted at `leadfromtheroom.svscreenings.com` via GitHub Pages.

---

## How to swap in the GHL scheduling form

When your GoHighLevel form is ready, follow these steps:

**1. Open `index.html`.**

**2. Find this block (around line 37):**

```html
<!-- GHL FORM EMBED START -->
<!--
  Paste the GHL iframe and its accompanying <script> tag here,
  exactly as GHL provides them. Do not remove the script tag;
  it is needed to resize the frame correctly.
-->
<!-- GHL FORM EMBED END -->
```

Paste the full GHL embed code (iframe + script tag) between the
`GHL FORM EMBED START` and `GHL FORM EMBED END` comments,
replacing the inner comment.

**3. Delete the placeholder card.**

Find and delete everything between (and including) these two comments:

```html
<!-- PLACEHOLDER: delete this block when the GHL embed is pasted in -->
...
<!-- end placeholder -->
```

**4. Update the two placeholders in the file:**

- `[CONTACT EMAIL]` appears twice (once in the placeholder card text, once in the after-form line). Update both.
- `[CONFIRMATION WINDOW]` appears once in the "What happens next" list. Replace it with your actual turnaround, for example: `one business day`.

**5. Commit and push:**

```bash
git add index.html
git commit -m "Add GHL scheduling embed"
git push
```

GitHub Pages will rebuild within a minute or two.

---

## Other placeholders

| Placeholder | Where | What to put |
|---|---|---|
| `[CONTACT EMAIL]` | index.html lines ~47 and ~53 | Your email address |
| `[CONFIRMATION WINDOW]` | index.html line ~28 | e.g. "one business day" |

---

## Local preview

No build step needed. Open `index.html` directly in a browser, or run any static server:

```bash
npx serve .
```
