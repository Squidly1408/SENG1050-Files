# AI Guide – SENG1050 course files

Your job is to **sort, rename, and document** the course files following the rules below, then keep the READMEs accurate.

Read [README.md](README.md) first for the course overview and dates.

---

## 1. Ground rules

1. **Never delete files.** Move or rename only. If two files look like duplicates, keep both and tell the user.
2. **Never overwrite** an existing file. If the target name exists, stop and ask, or add a suffix such as `_V2`.
3. **Don't edit the content of course files** (PDFs, HTML, XLSX, ZIPs). The exception is the user's own work, if they ask.
4. **Ask before renaming anything whose meaning you're unsure of** (e.g. `1.txt`, `Untitled.pdf`). Open it, identify it, then propose a name.
5. After any move or rename, **update every README** that links to the file. Broken links are the most common failure.
6. Report what you moved as a short `old → new` list at the end.
7. Weeks are by teaching week, not calendar date. If a file says "Week 8", it goes in `Week08`. Lecture N and Lab N belong in `WeekNN`.

---

## 2. Folder structure

```
SENG1050-Files/
├── README.md              index for humans
├── CLAUDE.MD              this guide
├── Course_Outline.pdf
├── Assessment1/           Mid-semester quiz (20%)             [create when files arrive]
├── Assessment2/           Web-Based Assignment 1 (15%)        A2_...
├── Assessment3/           Web-Based Assignment 2 (25%)        A3_...
├── Assessment4/           Final exam (40%)                    Exam_...
├── Week01/ … Week12/      weekly teaching material
├── Resources/             non-weekly help: guides, cheat sheets, course intro
├── Notes/                 the user's own notes                [create if needed]
└── Submissions/           the user's own submitted work       [create if needed]
```

- Week folders are always **two digits**: `Week01`, not `Week1`.
- Assessment folders match the numbering in [Course_Outline.pdf](Course_Outline.pdf) and the specification files (1 quiz, 2 and 3 web assignments, 4 exam).
- Only create a folder when there is a file to put in it.
- No nested folders inside a week unless it has 6+ files of one kind. Then use `Labs/` or `Code/`.

### Where things go

| If the file is…                                        | Put it in                     |
| ------------------------------------------------------ | ----------------------------- |
| Lecture slides                                         | `WeekNN/`                     |
| Lab sheet (PDF/HTML)                                   | `WeekNN/`                     |
| Lab sample solution                                    | `WeekNN/`                     |
| Starter/sample files a lab tells you to download       | `WeekNN/` of that lab         |
| Assessment brief, marking scheme/rubric, starter code  | `AssessmentN/`                |
| Practice exam, exam review/info                        | `Assessment4/`                |
| Software guides, cheat sheets, course intro text       | `Resources/`                  |
| The user's completed work                              | `Submissions/AssessmentN/`    |
| Course outline                                         | root                          |

If a file spans several weeks, put it in the **first** week and mention it in the later weeks' READMEs.

---

## 3. File naming conventions

**General:** English, no spaces, `Words_Separated_By_Underscores`, first letter of each word capitalised, ASCII only, no `(1)`/`Copy of` suffixes, no parentheses. Keep the original extension.

### Week folder files

| Type                 | Name                                                         |
| -------------------- | ------------------------------------------------------------ |
| Lecture slides       | `Lecture.pdf` (several: `Lecture_<Topic>.pdf`)               |
| Lab sheet            | `Lab_Notes.pdf` and `Lab_Notes.html` (per OS: `Lab_Notes_Windows.pdf`) |
| Lab solution         | `Lab_Solutions.<zip/pdf/xlsx>`                               |
| Lab code/downloads   | `Lab_Code_<Name>.<ext>` (e.g. `Lab_Code_Calculator.html`)    |
| Extra material       | `Extra_<Topic>.<ext>`                                        |

### Assessment folder files

`A<N>_Specification.<pdf/html>`, `A<N>_Marking_Scheme.<ext>`, `A<N>_Starter_Code.zip`, `A<N>_Clarifications.<ext>`, using the assessment number (`A2`, `A3`). For the exam use `Exam_...` (`Exam_Review.pdf`, `Exam_Practice_Exam.pdf`).

### Submissions

Follow the format in the assessment spec: a `fevergamez` directory zipped as `A2_cXXXXXXX.zip` (A2) or as the A3 spec says, via Canvas. Ask the user for their details before building a zip, and never invent a student number. Working drafts: `A2_Draft_v1/`.

### Files with no clear type

Keep the original name, list it in an "Unsorted" section of the nearest README, then ask the user.

---

## 4. README conventions

Every folder with content has a `README.md`.

### Week README template

```markdown
# Week N – <Topic>

<One line linking to the assessment it feeds, if any.>

## Files

| File | Contents |
| ---- | -------- |
| [Lecture.pdf](Lecture.pdf) | … |

(Say if a file is missing / not yet released / unreadable.)

## Lecture summary
## Lab summary
## Next

[Week N+1](../WeekNN/README.md)
```

### Assessment README template

Title, weight, due date, submission method → Files table → The task → Marking breakdown → Format checklist → Pitfalls → Related material.

### Rules

- **Link with relative paths**; avoid creating names with spaces.
- Summaries are **for studying**: definitions, rules, worked examples, and what the lab asks. Not slide-by-slide dumps.
- **Flag inconsistencies** in the source material instead of silently picking one.
- **Flag anything you couldn't read** rather than guessing its contents.
- When new material corrects an earlier README, update the earlier one and say so.
- Update the **root README** navigation table whenever a folder gains its first file.
- Deadlines: use the calendar dates from the outline/spec, and say which source you took them from.

---

## 5. Workflow for a batch of new files

1. **List** everything new (`Glob`), including loose files at the root.
2. **Identify** each file: open it and read the title and first page. Use `pdftotext -layout` for PDFs and `unzip -l` for zips. Save extracts to the scratchpad, not the project.
3. **Classify** using §2 and decide the new name using §3.
4. **Show the plan** as an `old → new` table and wait for the user's OK if more than ~5 files move, or anything is ambiguous.
5. **Move/rename** (`mv -n` in Git Bash; no overwriting).
6. **Write or update READMEs** (§4), including the root README.
7. **Verify links**: every relative link in the touched READMEs must point to an existing file.
8. **Report** the moves, anything unread, anything unsure.

Windows notes: the path contains `[2025] SEM 2`. Quote it in shell commands. Brackets are also glob characters, so prefer quoting over globbing.

---

## 6. Course facts

- **SENG1050: Web Technologies**, Semester 2 2025, Callaghan. Coordinator Dr Adrian Tan. Labs are 2 hours a week from Week 2 (attend 80%); lectures are 2 hours a week.
- **Topics by week:** 1 Internet concepts and communication, 2 HTML, 3 XML and DTD, 4 CSS, 5 Advanced HTML and CSS, 6 Client-server model (Apache/PHP), 7 Content management (PHP templates, XPath), 8 JavaScript, 9 Website design and HCI, 10 Encoding and compression, 11 Encryption, 12 Security, privacy and ethics.
- **Assessments:** 1 mid-semester quiz (20%, online), 2 Web-Based Assignment 1 (15%, 05 Sep, Week 6), 3 Web-Based Assignment 2 (25%, 24 Oct, Week 12; milestones checked in Week 8 and Week 10 labs), 4 final exam (40%, must score 40% to pass; 04 Nov 2025, 10:00). Late penalty: 10% of the maximum mark per day.
- **Academic integrity:** the user's assessment work must be their own. In A2/A3, code-generation tools and GenAI for code are forbidden (GenAI is allowed only for creative text such as descriptions, and must be referenced in README.txt). Don't write assessment code for the user; help with understanding and structure only.

---

## 7. Things not to do

- Don't rename files to include the student's name or ID unless building a submission zip.
- Don't move `Course_Outline.pdf` out of the root.
- Don't put personal notes into the course READMEs; use `Notes/WeekNN_Notes.md`.
- Don't invent content for weeks whose files haven't arrived.
- Don't leave temp files (text extracts, scripts) in the project; use the scratchpad.
