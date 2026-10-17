# LGU Music Society - Three-Page Website

**Assignment #2: Design a Three-Page Website Using HTML and CSS**
**Course:** Web Technologies - BSCS, Semester 5

| Detail | Value |
|---|---|
| Name | Adeefah Ayaz |
| Roll Number | FA-24-BSCS-158 |
| Section | I |
| Department | Computer Science, Lahore Garrison University |
| Topic | University Society (Music Society) |
| GitHub Repository | `https://github.com/<your-username>/<repo-name>` *(add your URL)* |
| Live Website | `https://<your-username>.github.io/<repo-name>/` *(add your URL)* |

## Project Structure

| File | Purpose | CSS method |
|---|---|---|
| `index.html` | Home: introduction and activities | Inline CSS |
| `information.html` | Events and membership plans (table, audio, video) | Embedded CSS |
| `registration.html` | Membership registration form | External CSS (`style.css`) |
| `style.css` | Stylesheet for `registration.html` | - |
| `images/` | University logo and header illustration | - |
| `media/` | Audio (`.mp3`, `.ogg`) and video (`.mp4`) clips | - |
| `validation-screenshots/` | W3C validator screenshots | - |

**Design theme:** flat black, amber and cream colours with no gradients, inspired by the supplied music-studio reference.

## CSS Selectors Used

| Selector type | Example | Where |
|---|---|---|
| Element | `p`, `h2` | `information.html` (embedded), `style.css` |
| Class | `.notice` | `information.html` (aside), `registration.html` (info box) |
| ID | `#event-article`, `#registration-form` | `information.html`, `style.css` |
| Attribute | `a[href="information.html"]`, `input[type="email"]` | `information.html`, `style.css` |

Each selector carries a CSS comment naming its type.

## Testing

### Form validation (dummy data)
| Test | Expected result |
|---|---|
| Submit with empty Full Name, Email, Password, dropdown | Browser blocks submit and highlights the first empty required field |
| Email `bad` (no @) | "Please include an '@'" message appears |
| Password `short` (under 8 characters) | "Use at least 8 characters" message appears |
| Age below 16 or above 60 | Number-range message appears |
| Comments over 250 characters | Typing stops at 250 characters |

### Browser testing
| Browser | Result | Differences noticed |
|---|---|---|
| Google Chrome | All three pages, navigation, form validation, audio and video work | *(record yours)* |
| Mozilla Firefox | *(fill in after testing)* | *(e.g. date picker and validation message wording differ)* |

### W3C validation
Screenshots for all three pages are stored in `validation-screenshots/`.

---

## Short Explanation

**What is CSS?** Cascading Style Sheets (CSS) controls how HTML looks: colours, fonts, spacing and layout. Its benefits are a clean separation of content and design, consistent styling across pages, easier maintenance, and smaller, faster pages.

**Selector, property and value.** In `style.css` the rule `button:hover { background-color: #0b0b0b; }` has the selector `button:hover`, the property `background-color` and the value `#0b0b0b`.

**Inline, embedded and external CSS.** Inline CSS uses the `style` attribute on one element (used on `index.html`); it is quick but hard to reuse. Embedded CSS sits in a `<style>` element in the `<head>` and affects one page (`information.html`). External CSS lives in a separate `.css` file linked with `<link>` (`registration.html`); it can style many pages, is cached by the browser and is easiest to maintain.

**CSS versions.** CSS1 (1996) introduced basic fonts, colours and margins. CSS2/2.1 added positioning, media types, z-index and tables, and CSS 2.1 fixed errors. Modern CSS is split into modules (Selectors, Flexbox, Grid, Colors and more) that evolve separately, so new features such as `accent-color` arrive faster.

**Browser support.** Browsers may interpret CSS and form controls slightly differently, so a site must be tested to ensure every visitor sees the same layout and working features. I tested the site in Google Chrome and Mozilla Firefox.

**Semantic and non-semantic HTML.** Semantic: `<nav>` in every page describes a block of navigation links. Non-semantic: `<div class="choice">` in `registration.html` is only a generic container for grouping a radio button and its label.
