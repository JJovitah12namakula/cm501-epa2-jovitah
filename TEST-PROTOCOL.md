 Accessibility Test Protocol — Campus Café (EPA 2)

Student:Jovitah ronah namakula  
Course: CM-501 Frontend Web Development  
Pages: index.html and contact.html  
Target: WCAG 2.2 Level AA

> Complete the result fields only after performing each test. This is a protocol template, not evidence that tests have passed.
 C1 — Identified issues and repairs
| Missing document language | Added lang="en"
 No skip navigation | Added skip link to main content | 2.4.1 Bypass Blocks
> Generic divs used for page regions Added header, nav, main and footer landmarks | 1.3.1 Info and Relationships |
| Navigation uses clickable divs | Replaced with keyboard-operable links | 2.1.1 Keyboard |
| Weak heading hierarchy | Added h1, section h2 and item h3 headings | 1.3.1 Info and Relationships |
| Menu items lack list semantics | Grouped category items in unordered lists | 1.3.1 Info and Relationships |
| Today's special is only in image | Added product, price and availability as HTML text | 1.1.1 Non-text Content |
| Latte image lacks alternative text | Added concise description | 1.1.1 Non-text Content |
| Contact image file is missing | Removed broken image reference | 1.1.1 Non-text Content |
| Focus outline removed globally | Added visible :focus-visible style | 2.4.7 Focus Visible |
| Pale text has weak contrast | Replaced with darker text; verify colour pairs | 1.4.3 Contrast (Minimum) |
| Fixed width overflows on small screens | Added fluid layout and responsive grid | 1.4.10 Reflow |
| Form controls have no labels | Added explicit label/input associations | 1.3.1; 3.3.2 |
| Email/date/phone use generic text inputs | Used email/date/tel types and autocomplete | 1.3.5 Identify Input Purpose |
| Required fields not marked | Marked name and email required | 3.3.2 Labels or Instructions |
| Submit is a clickable div | Replaced with native submit button | 2.1.1; 4.1.2 |

## C2 — Automated checks

| Tool | Page | Actual result | Evidence |
|---|---|---|---|
| W3C Nu HTML Checker | index.html | [Fill after running] | [Screenshot/URL] |
| W3C Nu HTML Checker | contact.html | [Fill after running] | [Screenshot/URL] |
| Lighthouse Accessibility | index.html | [Fill score and findings] | [Screenshot] |
| Lighthouse Accessibility | contact.html | [Fill score and findings] | [Screenshot] |
| WAVE or axe | Both | [Fill errors, alerts and review items] | [Screenshot] |

Tools: https://validator.w3.org/nu/ and Chrome DevTools Lighthouse; WAVE: https://wave.webaim.org/

## C3 — Manual checks

### Keyboard
1. Reload the menu and press Tab. The skip link should receive focus first.
2. Press Enter on the skip link and confirm navigation to main content.
3. Use Tab and Shift+Tab through navigation links.
4. Open Contact and tab through each field and the submit button.
5. Submit with required fields empty; browser validation should identify a missing value.
6. Confirm focus is visible and no keyboard trap occurs.

**Browser / OS:** [Enter]  
**Result:** [Pass/fail and observations]

### Screen reader
**Screen reader / browser:** [e.g. NVDA + Firefox]  
- Confirm page title and landmarks are announced.
- Navigate by headings and confirm a logical hierarchy.
- Confirm menu names, descriptions and prices are understandable.
- Confirm each form field is announced with its label and required status.

**Result:** [Record actual observations]

### 200% zoom
Set browser zoom to 200% on both pages. Confirm text and controls remain usable and content reflows without unnecessary horizontal scrolling.

**Browser:** [Enter]  
**Result:** [Pass/fail and observations]

## C4 — Peer test
**Peer tester:** [Name/initials, if permitted]  
**Date:** [Date]  
**Tasks:** [What the peer attempted]  
**Findings:** [What the peer reported]  
**Changes made:** [Changes made after feedback]

## C5 — Limits of automated testing
Automated tools can detect many technical problems, such as missing alternative text, some colour-contrast failures and missing form labels. They cannot fully decide whether alternative text is meaningful, whether content is understandable, or whether a keyboard and screen-reader journey works for a real person. A checker may confirm that an image has alt text, but a person must judge whether the description communicates the image's purpose. Automated checks must therefore be combined with keyboard, screen-reader, zoom and peer testing.

## AI use disclosure
ChatGPT was used to help identify issues in the supplied starter code and propose accessible HTML/CSS repairs. I reviewed the changes and must be able to explain them. Automated, manual and peer test outcomes are to be completed by me after carrying out those tests.
