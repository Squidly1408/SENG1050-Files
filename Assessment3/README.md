# Assessment 3 - Web-Based Assignment 2

**Weight:** 25% | **Due:** 11:59 pm Fri 24 Oct 2025 (Week 12) | **Milestone 1:** checked from Week 8 labs (15-19 Sep) | **Milestone 2:** checked from Week 10 labs (6-10 Oct) | **Submission:** Canvas.

## Files

| File | Contents |
| ---- | -------- |
| [A3_Specification.pdf](A3_Specification.pdf) | Assignment brief |
| [A3_Specification.html](A3_Specification.html) | Same brief, HTML version |
| [A3_Marking_Scheme.xlsx](A3_Marking_Scheme.xlsx) | Grading rubric spreadsheet |

## The task

Extend the FeverGamez site from [Assessment 2](../Assessment2/README.md) to sell second-hand products.

- Runs on Apache + PHP at `http://fevergamez.com`. Directory `fevergamez` with images in `data/images`, XML in `data/xml`, templates in `themes`.
- Import the A2 site and generate HTML pages with PHP.
- **Genre pages:** rename the XML data files, use a PHP template to read XML and render pages, and a PHP file to access each genre page.
- **Data collection page:** a form for people listing a second-hand product (submitter information, all product fields from the XML template, submit and clear buttons).
- **Responsive web design.**
- **Bonus:** form submission script that writes the submission into the correct genre XML file and redirects.

## Marking breakdown (92 marks)

General requirements 12 | Web server setup and website import 6.5 | Genre pages 13.5 | Data collection page 22 | Responsive web design 6 | Coding style 32 | bonus form script [5] | up to -10 for poor aesthetics and not following instructions.

## Pitfalls

- The specification's code-generation and GenAI restrictions are expected to match Assessment 2; check the A3 specification for the exact wording.
- Late penalty 10% of the maximum per day.

## Flags

- The specification's contents list says 'Genre Pages' while the body uses 'Category Pages' in places; they appear to be the same section.

## Related material

[Week 6](../Week06/README.md) (Apache/PHP), [Week 7](../Week07/README.md) (PHP templates, XML), [Week 8](../Week08/README.md) and [Week 9](../Week09/README.md) (JavaScript, milestones).
