# Grading Contract Template

This repository is a template for generating a personalized grading contract using R Markdown. Students and instructors can use it to create a semester-long schedule of assignments and deliverables based on a chosen grade contract.

## What Is a Grading Contract?

A grading contract is an agreement between a student and instructor that specifies the work a student will complete in order to earn a particular grade (A, B, or Pass). This template auto-generates a dated schedule of lab assignments and portfolio pieces based on the parameters you provide.

## Prerequisites

- [R](https://cran.r-project.org/) and [RStudio](https://posit.co/download/rstudio-desktop/)
- The `tidyverse` R package (`install.packages("tidyverse")`)
- The `rmarkdown` R package (`install.packages("rmarkdown")`)

## How to Use This Template

### 1. Use this template

Click the green **"Use this template"** button at the top of this GitHub page to create your own copy of this repository, or fork/clone it directly.

### 2. Open the project

Open `grade_contract.Rproj` in RStudio to load the project.

### 3. Edit the parameters in `contract.Rmd`

At the top of `contract.Rmd`, update the `params` section in the YAML front matter to match your course details:

```yaml
params:
  semester: Spring 2026          # Semester name shown in the contract
  semester_half:
    label: Half Semester Contract
    value: TRUE                  # TRUE = 8-week contract; FALSE = full 15-week contract
  weekonemonday: "2026-01-13"    # Date of the Monday of the first week (YYYY-MM-DD)
  thesisdeadline: "2023-01-10"   # (if applicable) thesis deadline date
  springbreak: "2023-01-10"      # (if applicable) spring break Monday date
  name: Tukey Cat                # Student's full name
  labs: 11                       # Number of lab assignments required
  portfolios: 10                 # Number of portfolio pieces required
  grade:
    value: A                     # Contracted grade: A, B, or Pass
  startweek:
    value: Friday                # Day of the week assignments are due
```

**Parameter descriptions:**

| Parameter | Description |
|---|---|
| `semester` | The semester label displayed in the contract (e.g., `Spring 2026`) |
| `semester_half` | Set to `TRUE` for a half-semester (8-week) contract; `FALSE` for a full-semester contract |
| `weekonemonday` | The Monday of Week 1 in `YYYY-MM-DD` format |
| `name` | The student's name as it will appear in the contract |
| `labs` | Total number of lab assignments the student agrees to complete |
| `portfolios` | Total number of portfolio pieces the student agrees to complete |
| `grade` | The grade the student is contracting for (`A`, `B`, or `Pass`) |
| `startweek` | The day of the week on which weekly deliverables are due (e.g., `Friday` means all that week's work is due by Friday) |

### 4. Knit the document

Click **Knit** in RStudio (or press `Ctrl+Shift+K` / `Cmd+Shift+K`) to render `contract.Rmd` into `contract.md`. The output is a GitHub-flavored Markdown document with a full dated schedule.

You can also render from the R console:

```r
rmarkdown::render("contract.Rmd")
```

### 5. Review and adjust the schedule

The generated schedule in `contract.md` is a *suggested* schedule. Students are encouraged to rearrange labs and portfolio pieces to fit their own needs—just keep the overall deadlines in mind.

### 6. Submit your contract

Once the contract looks correct, share `contract.md` (or a rendered copy) with your instructor for approval.

## Repository Structure

| File | Description |
|---|---|
| `contract.Rmd` | Source R Markdown file — edit this to customize the contract |
| `contract.md` | Rendered output — the final grading contract document |
| `grade_contract.Rproj` | RStudio project file |

## Credits

This contract template is adapted from [Annie Somerville's contract](https://github.com/anniehsom).
