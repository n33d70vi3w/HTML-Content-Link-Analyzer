# 🔍 HTML Content & Link Analyzer

## Project Overview

The **HTML Content & Link Analyzer** is a lightweight, client-side tool designed to quickly dissect and extract critical data from raw HTML content, such as email body renders, newsletter templates, or webpage snippets.

This tool acts as a digital detective, instantly providing three crucial pieces of information for Quality Assurance (QA), email marketing verification, and security review.

**Key Features:**

* **Zero Dependencies:** This tool uses only pure HTML, CSS, and "Vanilla" JavaScript. It requires no external libraries, dependencies, or server-side setup.
* **Actionable Output:** Provides numbered, copyable results for immediate use.


## 🔎 Analysis Breakdown (The Three Detective Jobs)

The analyzer performs three core functions using highly specialized search criteria called **Regular Expressions (Regex)**.

### 1. Extracted Raw HTTP/HTTPS Links

**What it finds:** Every single URL in the input text that begins with `http://` or `https://`.

* **Why it's useful:** Quickly verify the existence and destination of all links, including broken or unintended development links.
* **Format:** A numbered list of unique links, each with a copy button.

### 2. Button Parameter Analysis (Raw Inline Styles)

**What it finds:** The raw `style="..."` attribute from *every* `<button>` tag found in the input.

* **Why it's useful:** Essential for designers and QA teams to verify that button colors, padding, and borders match the specification exactly, especially in emails where styling is often complex and inline.
* **Format:** Each button's style is listed separately (Button 1, Button 2, etc.) with its full style string and a dedicated copy button.

### 3. Hyperlink Anchor Text (Keywords)

**What it finds:** The actual clickable text (the "keyword") used inside any link (`<a href="...">...</a>`) that points to an external site.

* **Why it's useful:** Helps identify and verify the Call-to-Action (CTA) phrases used by the sender, such as "Click Here," "Download Now," or "Read More."
* **Format:** A numbered list of unique anchor texts.

## ⚙️ Technical Deep Dive


### Core Extraction Logic (Regular Expressions)

The analytical power comes from three core Regex patterns executed by the browser's built-in engine:

| Data Extracted | Regex Pattern Concept |
| :--- | :--- |
| **Raw Links** | Find a phrase starting with `http` or `https`, followed by `://`, and continue until a space or end-of-link punctuation is hit. |
| **Button Styles** | Find the literal string `<button`, look for the `style=` attribute, and capture everything inside its quotation marks. |
| **Anchor Text** | Find a link tag (`<a href=...`), ignore the tag, and capture all the text up until the closing tag (`</a>`). |

## 🤝 Contribution

This tool is designed to be simple and highly functional. Feedback, bug reports, and suggestions for new extraction features are welcome! Please open an issue on the repository page.

## 📝 License

Free from such things 
