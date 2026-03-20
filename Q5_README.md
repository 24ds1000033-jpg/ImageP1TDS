# Question 5 — Image: The Affective Chart

## What you turn in (exam box)

One line in the **Submission URLs** field, **two URLs separated by a space** (image **first**, JSON **second**):

```text
https://raw.githubusercontent.com/YOUR_USER/YOUR_REPO/main/tds-p1/q5_affective_chart.png https://raw.githubusercontent.com/YOUR_USER/YOUR_REPO/main/tds-p1/q5_submission.json
```

Replace `YOUR_USER`, `YOUR_REPO`, and paths with yours. **No** line breaks in the middle (one line is safest).

---

## Automatic checks (from the assignment)

1. Exactly **two** public URLs; **image first**, **JSON second**.
2. **Image**: ends in `.png`, `.jpg`, `.webp`, or `.avif`; loads with **CORS**; decodes; **short side ≥ 1024 px**.
3. **JSON**: loads with **CORS**; matches the required keys (see below).

---

## Files in this folder (ready to upload)

| File | Role |
|------|------|
| `q5_affective_chart.png` | Your image (here: **1834×1024**, short side **1024**). |
| `q5_submission.json` | Metadata + prompt for the instructor; **evaluator mainly sees the image**. |

### Required JSON shape (do not rename keys)

```json
{
  "prompt": "...",
  "model": "...",
  "dataset_name": "...",
  "dataset_url": "...",
  "insight": "..."
}
```

Optional: `"publish_email": true` if you want your email shown on a public exhibition.

---

## Step-by-step: host on GitHub (beginner)

### 1. Create a repository

1. Log in at [github.com](https://github.com).
2. **New repository** (e.g. name `tds-jan-2026-assets`).
3. Public, no README required (you can add one later).
4. Create repository.

### 2. Upload the two files

**Option A — in the browser**

1. Open the repo → **Add file** → **Upload files**.
2. Drag in `q5_affective_chart.png` and `q5_submission.json`.
3. Put them in a folder if you like, e.g. `tds-p1/` (create by typing `tds-p1/filename` when uploading).
4. **Commit** to **`main`** (or remember your branch name).

**Option B — Git on your PC**

```powershell
cd "d:\path\to\your\empty\repo"
mkdir tds-p1
copy "d:\RKD\DATA SCI\DIPLOMA\TDS\TDS PROJECT 1\tds-work\images\q5_affective_chart.png" tds-p1\
copy "d:\RKD\DATA SCI\DIPLOMA\TDS\TDS PROJECT 1\tds-work\images\q5_submission.json" tds-p1\
git add tds-p1
git commit -m "Add Q5 affective chart assets"
git push origin main
```

### 3. Build the two **raw** URLs

Pattern:

```text
https://raw.githubusercontent.com/<USER>/<REPO>/<BRANCH>/<path-to-file>
```

Example if user `janedoe`, repo `tds-jan-2026-assets`, branch `main`, files under `tds-p1/`:

- `https://raw.githubusercontent.com/janedoe/tds-jan-2026-assets/main/tds-p1/q5_affective_chart.png`
- `https://raw.githubusercontent.com/janedoe/tds-jan-2026-assets/main/tds-p1/q5_submission.json`

**Tip:** On GitHub, open each file → **Raw** → copy the address bar URL.

### 4. Test before the exam

1. Open an **Incognito / private** window.
2. Paste each URL in the address bar — you should see the image or JSON text.
3. If either **404**s or asks for login, fix the path or make the repo **public**.

### 5. Paste on the exam

Paste **both** URLs on **one line**, **image URL first**, space, **JSON URL**. **Check** → **Save**.

---

## Brief reminder (what “good” looks like)

- Real, citable **dataset** (named in JSON).
- **Not** a plain bar/line/pie/scatter chart “with a style slapped on”—use metaphor, scene, or strong visual transformation.
- **No** reliance on axis labels, legends, or on-image text to carry the meaning (viewer should *feel* the insight).
- **Single** frame (not a comic strip of panels).

If **Check** passes but grades feel low later, that’s often the **AI exhibition** scoring—iterate on the image and prompts; use the exam’s **Discuss** link and the self-eval instructions (e.g. Gemini in AI Studio) from the assignment page.

---

## If you want to replace the image

Regenerate with any tool (Midjourney, DALL·E, etc.), export **≥1024 px** on the short side, update **`q5_submission.json`** (`prompt`, `model`, `dataset_*`, `insight`) to match, re-upload, same URL pattern (or new commit).
