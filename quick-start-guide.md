---
title: "Data Skills for Psychology — Quick-Start Guide"
---

# Quick-Start Catch-Up Guide

Falling behind? No problem. This guide walks through the minimum steps needed to get caught up to where the class is right now (Week 3: Data Summaries). Work through it in order — each step builds on the one before it. Plan on about 4–6 focused hours.

All links point to the course website at <https://ritcheym.github.io/dataskills>.

------------------------------------------------------------------------

## Step 1 — Get your software installed (30 min)

Before anything else, make sure R and RStudio are installed (or updated) on your laptop.

-   Follow the [RSetGo install guide](https://psyteachr.github.io/RSetGo/)
-   Open RStudio once to confirm it launches

Full Week 1 module page: [Introduction to R and RStudio](https://ritcheym.github.io/dataskills/modules/01_intro.html)

## Step 2 — Learn the RStudio interface and Quarto reports (1–1.5 hrs)

Start with the lecture slides — these cover what happened in class:

-   [Tuesday's slides — Intro to R and RStudio](https://ritcheym.github.io/dataskills/slides/01_intro.html)
-   [Thursday's slides — Reports](https://ritcheym.github.io/dataskills/slides/02_reports.html)
-   [Week 1 flashcards](https://ritcheym.github.io/dataskills/files/flashcards-ch1-2.html)

Need more detail? These chapters from *Applied Data Skills* are optional deeper reading:

-   [Chapter 1: Intro to R and RStudio](https://psyteachr.github.io/ads-v3/01-intro.html)
-   [Chapter 2: Reports with R Markdown](https://psyteachr.github.io/ads-v3/02-reports.html)

**Week 1 assignment to complete:** Build the `demo_report` project per [section 2.7 of Chapter 2](https://psyteachr.github.io/ads-v3/02-reports.html#sec-exercises-reports). Add (1) a sentence or two on how programming might help you in the future, and (2) an embedded data visualization you like. Zip the project folder and submit on BruinLearn. Full instructions on the [Week 1 module page](https://ritcheym.github.io/dataskills/modules/01_intro.html). See Step 6 below for a walkthrough of creating, rendering, and zipping your Quarto document.

## Step 3 — Programming foundations: variables, vectors, loops, branches (1.5–2 hrs)

Start with the class materials:

-   [Week 2 lecture slides](https://ritcheym.github.io/dataskills/slides/02_programming-foundations.html)
-   [Companion code](https://ritcheym.github.io/dataskills/_code/programming-foundations-code.html)
-   Module page: [Programming Foundations Part 1](https://ritcheym.github.io/dataskills/modules/02_programming-foundations-1.html)

For more depth, these short chapters from *R for Psychological Science* are optional reference reading:

-   [Variables](https://psyr.djnavarro.net/variables.html)
-   [Vectors](https://psyr.djnavarro.net/vectors.html)
-   [Loops](https://psyr.djnavarro.net/loops.html)
-   [Branches](https://psyr.djnavarro.net/branches.html)

**Week 2 Part 1 assignment:** Create an R project called `programming-foundations` with an Rmd called `part-1.Rmd`, and complete the four exercises listed on the module page (sum 1–100, count words, build 1–100 with a loop and `seq()`, and sum all multiples of 3 or 5 below 1000).

## Step 4 — Functions and algorithms (1 hr)

Work from the module page and its linked slides:

-   Module page: [Programming Foundations Part 2](https://ritcheym.github.io/dataskills/modules/03_programming-foundations-2.html)

Optional deeper reading from *R for Psychological Science* if concepts need more explanation:

-   [Functions](https://psyr.djnavarro.net/functions.html)
-   [Programming](https://psyr.djnavarro.net/programming.html)

**Week 2 Part 2 assignment:** In the same `programming-foundations` project, save a new `part-2.Rmd`. Write an `is_prime()` function and use it to list primes 1–1000, then write your own functions for mean, mode, median, range, and standard deviation.

## Step 5 — Catch up to where we are now: Data Summaries (1–1.5 hrs)

This is the current module. Start with the module page and in-class materials:

-   Module page: [Data Summaries](https://ritcheym.github.io/dataskills/modules/05_data-summaries.html)
-   [Lecture slides](https://ritcheym.github.io/dataskills/slides/05_data-summaries.html)
-   [Companion code](https://ritcheym.github.io/dataskills/_code/data-summaries-code.html)

Optional deeper reading from *Applied Data Skills* if a concept needs more explanation:

-   [Chapter 4: Data Summaries](https://psyteachr.github.io/ads-v3/04-summary.html)

**Current assignment preview:** Practice reading in a csv file and summarizing key variables using the `screentime` dataset. Download the [`screentime-summaries.qmd`](https://ritcheym.github.io/dataskills/_code/screentime-summaries.qmd) starter file, fill in the code and markdown, and submit. See the [screentime dataset page](https://ritcheym.github.io/dataskills/datasets/screentime.html) for background on the data.

------------------------------------------------------------------------

## Step 6 — How to create, render, and submit a Quarto document

Every assignment in this class gets turned in as a rendered Quarto report. Here's the full workflow, start to finish.

### Create an R Project (one time per assignment)

1.  In RStudio, go to **File → New Project → New Directory → New Project**.
2.  Name the directory (e.g., `demo_report`) and pick a location on your computer.
3.  Click **Create Project**. RStudio will open the new project — you'll see the project name in the top-right corner.

Using projects keeps everything for one assignment (data, code, output) in a single folder, which is also what you'll zip and submit.

### Create a new Quarto document

1.  **File → New File → Quarto Document...**
2.  Fill in a title and your name as author, choose **HTML** as the output format, and click **Create**.
3.  RStudio opens a template `.qmd` file. **Save it immediately** (File → Save) into your project folder — give it a descriptive name like `demo_report.qmd`.

The file has three parts to know:

-   **YAML header** at the top (between `---` lines): controls title, author, output format.
-   **Prose**: regular text written in Markdown — use `#` for headings, `**bold**`, `*italic*`, etc.
-   **Code chunks**: gray blocks that start with ```` ```{r} ```` and end with ```` ``` ````. Code inside these runs when the document is rendered.

Insert a new code chunk with the green **+C** button at the top of the editor, or the shortcut **Cmd/Ctrl + Alt + I**.

### Render the document to HTML

1.  Click the **Render** button at the top of the editor (blue arrow icon). Shortcut: **Cmd/Ctrl + Shift + K**.
2.  RStudio runs every code chunk top-to-bottom and produces an `.html` file in the same folder as your `.qmd`.
3.  A preview opens automatically. If it doesn't look right, fix the `.qmd` and render again.

If rendering fails, read the error message in the **Render** or **Background Jobs** pane — it usually points at the exact line that broke. Common culprits: an un-installed package (`install.packages("ggplot2")` in the console), a typo in a variable name, or a missing closing backtick on a code chunk.

### Zip your project and upload

Once the `.qmd` renders cleanly to `.html`:

1.  Close the RStudio project (optional, but ensures files are saved).
2.  Find the project folder in Finder (Mac) or File Explorer (Windows).
3.  Zip the **entire folder**:
    -   **Mac**: right-click the folder → **Compress "folder-name"**. A `.zip` file appears next to it.
    -   **Windows**: right-click the folder → **Send to → Compressed (zipped) folder**.
4.  Verify the zip contains the `.Rproj` file, the `.qmd` file, the rendered `.html` file, and any data files used.
5.  Upload the `.zip` via the assignment link on BruinLearn.

One sanity check before submitting: unzip the file somewhere else and open the `.html` — if it displays correctly in a browser, you're good to go.

------------------------------------------------------------------------

## Key reference pages

-   [Full course schedule](https://ritcheym.github.io/dataskills/schedule.html)
-   [All modules](https://ritcheym.github.io/dataskills/modules/)
-   [Syllabus](https://ritcheym.github.io/dataskills/syllabus.html)
-   [Exercises](https://ritcheym.github.io/dataskills/exercises.html)
-   [Resources](https://ritcheym.github.io/dataskills/resources.html)

## Tips for catching up efficiently

-   The slides are condensed versions of the readings, so refer to the readings if you need more information.
-   Type out the code examples yourself rather than copy-pasting. Muscle memory helps.
-   Submit assignments even if incomplete — partial credit beats zero, and feedback is more useful than a blank slate.
-   Come to office hours with a specific question and your `.qmd` file open. That's the fastest way to get unstuck.
