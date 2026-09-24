# Assessment 2 - Web-Based Assignment 1

**Weight:** 15% | **Due:** 11:59 pm Fri 05 Sep 2025 (Week 6) | **Submission:** Canvas, one zip named `A2_cXXXXXXX.zip` (student ID) containing a `fevergamez` directory.

## Files

| File | Contents |
| ---- | -------- |
| [A2_Specification.pdf](A2_Specification.pdf) | Assignment brief |
| [A2_Specification.html](A2_Specification.html) | Same brief, HTML version |
| [A2_Marking_Scheme.xlsx](A2_Marking_Scheme.xlsx) | Rubric spreadsheet |

## The task

Prototype website for FeverGamez (Nintendo Switch games store) showing **two genres with three games each**.

- **HTML:** `index.html`, `about.html`, `contact.html`. Full document structure, relative-URL navigation bar on every page, footer with name, student number, email and degree. Homepage: welcome note (h1, paragraphs, blockquote), three featured products with images, one absolute external link, EM/STRONG/ABBR. About: history, privacy policy, terms and conditions. Contact: POST form to `https://jkorpela.fi/cgi-bin/echo.cgi` with name, email, subject, message, two urgent/not-urgent radios, submit and clear buttons, all inputs required.
- **XML:** `xmltemplate.xml` with an internal DTD (name, description, pricing, search tags 0+, reviews 0+ with a 0-5 score attribute, one or more image filenames, one URL; at least two `<!ENTITY>`), plus `xmldata1.xml` and `xmldata2.xml` (three games each, same DTD).
- **CSS:** `style.css` (body side margins at least 1 cm, readable background, distinct link states with hover enlargement, an id and a class selector, styled `div` and `span`), plus a document-level style and an inline style on the homepage.
- **Coding style:** valid HTML/XML/CSS, indented, file header comments (file name, author, date), `README.txt` with all references.

## Marking breakdown (100 marks)

General requirements 2 | HTML 47 | XML 18.5 | CSS 11.5 | Coding style 21 | up to -10 for poor aesthetics, untidiness, spelling/grammar or not following instructions.

## Format checklist

- [ ] All files in `fevergamez/`, images in `fevergamez/images/`
- [ ] index.html, about.html, contact.html, xmltemplate.xml, xmldata1.xml, xmldata2.xml, style.css, README.txt
- [ ] Zip named `A2_cXXXXXXX.zip`, submitted via Canvas

## Pitfalls

- Code-generation tools and GenAI for code are forbidden (zero mark). GenAI is allowed only for creative text and images, and must be referenced in `README.txt`.
- Late penalty 10% of the maximum per day (including weekends). Extensions need an approved Adverse Circumstances application, lodged at least a day before the due date.

## Flags

- The outline's assessment table is garbled: it seems to list a Week 7 (12 Sep, 20%) date next to Assessment 2, whereas the specification says 15%, Week 6 (05 Sep). This README follows the specification.

## Related material

[Week 2](../Week02/README.md) (HTML), [Week 3](../Week03/README.md) (XML/DTD), [Week 4](../Week04/README.md) (CSS), [Week 5](../Week05/README.md). Continued in [Assessment 3](../Assessment3/README.md).
