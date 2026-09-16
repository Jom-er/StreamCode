# StreamCode

**StreamCode** is a simple, fast code-sharing and preview platform inspired by the clean, instant-sharing experience of Streamable. Instead of sharing videos, StreamCode allows users to paste or upload code and instantly create a shareable page that displays the **entire code file without artificial truncation, pagination, or preview limits**.

## Problem

Many code-sharing and preview services limit how much code can be displayed, require users to open separate files, truncate long content, or provide an editor that becomes difficult to navigate for large files.

StreamCode focuses on one core idea:

> **Share code once and let anyone view the entire file in a clean, readable preview.**

## Core Functionality

### 1. Code Input

Users can:

* Paste code directly into the editor.
* Upload a code file.
* Drag and drop a file into the interface.
* Open previously shared StreamCode pages.

The application should preserve the original code exactly, including:

* Indentation
* Line breaks
* Spaces
* Tabs
* Special characters
* Comments
* Long lines

### 2. Full Code Preview

The preview is the primary feature.

StreamCode should display the **complete code**, regardless of how long the file is.

The viewer should provide:

* Syntax highlighting
* Line numbers
* Horizontal scrolling
* Vertical scrolling
* Monospace typography
* Code folding
* Search within code
* Copy entire code
* Copy selected code
* Download original file
* Full-screen viewer

There should be no visual truncation such as:

```text
...
```

simply because the file is large.

Large files should remain continuously scrollable.

### 3. Supported Languages

StreamCode should automatically detect common programming and markup languages, including:

* HTML
* CSS
* JavaScript
* TypeScript
* JSON
* XML
* Python
* Java
* C
* C++
* C#
* Rust
* Go
* PHP
* Ruby
* Swift
* Kotlin
* Lua
* SQL
* Shell
* YAML
* Markdown
* GDScript
* Minecraft `.mcfunction`
* Minecraft JSON files

Users should also be able to manually select the language.

### 4. Shareable Links

After uploading or pasting code, the user can create a StreamCode page.

Example:

```text
streamcode.example/code/abc123
```

The shared page should immediately open the complete code preview.

The user can copy the URL and share it through:

* Discord
* Reddit
* GitHub
* Social media
* Websites
* Messaging applications
* Forums

### 5. Embed Support

StreamCode should provide an optional embed mode.

Example:

```html
<iframe
    src="https://streamcode.example/embed/abc123"
    width="100%"
    height="600">
</iframe>
```

The embedded viewer should display the complete code while remaining independently scrollable.

## User Experience

### Step 1 — Open StreamCode

The homepage should immediately present a clean interface.

```text
┌──────────────────────────────────────────────┐
│ StreamCode                         Share     │
├──────────────────────────────────────────────┤
│                                              │
│  Paste your code here...                     │
│                                              │
│                                              │
│                                              │
├──────────────────────────────────────────────┤
│ JavaScript                         Upload     │
│                                              │
│                         [ Preview Code ]      │
└──────────────────────────────────────────────┘
```

### Step 2 — Add Code

The user pastes code or uploads a file.

StreamCode detects the language automatically.

### Step 3 — Preview

The application immediately displays the complete code.

```text
┌──────────────────────────────────────────────┐
│ StreamCode          JavaScript    Copy ↓     │
├──────┬───────────────────────────────────────┤
│  1   │ const app = {};                       │
│  2   │                                       │
│  3   │ function start() {                     │
│  4   │     console.log("Hello");              │
│  5   │ }                                     │
│  6   │                                       │
│ ...  │                                       │
│ 9999 │ // entire file remains accessible    │
└──────┴───────────────────────────────────────┘
```

The user can scroll from the first line to the final line without the service intentionally cutting off the preview.

### Step 4 — Share

The user selects:

**Share Code**

StreamCode generates a unique URL.

### Step 5 — Recipient Opens Link

The recipient does not need to install anything.

They see:

* File name
* Language
* Complete code
* Line numbers
* Search
* Copy button
* Download button
* Full-screen button

## StreamCode Design Philosophy

StreamCode should follow a **minimal, content-first interface**.

### Visual Style

* Clean
* Modern
* Minimal
* Dark code viewer
* Simple navigation
* Rounded controls
* Subtle borders
* Minimal animations
* Large readable code area
* Responsive layout

The interface should feel similar in simplicity to Streamable, but the primary content is **code instead of video**.

## Key Difference

The defining feature of StreamCode is:

### **Full Code, No Preview Truncation**

StreamCode should not intentionally shorten the displayed code because it is long.

A file containing:

```text
100 lines
1,000 lines
10,000 lines
100,000 lines
```

should use the same basic viewing model: a continuously scrollable code viewer.

The actual technical infrastructure may impose practical limits related to browser memory, storage, upload size, or server resources, but StreamCode should not impose an arbitrary **"only show the first X lines"** limitation on the user interface.

## Sharing Features

Each shared code page can provide:

* Copy link
* Copy code
* Download file
* Open raw code
* Embed
* QR code
* Social sharing
* Report page
* Optional expiration
* Optional private/unlisted sharing

## Code Viewer

The viewer should support:

* Line numbers
* Syntax highlighting
* Code folding
* Find/search
* Jump to line
* Word wrapping toggle
* Horizontal scrolling
* Vertical scrolling
* Full-screen mode
* Copy selection
* Copy entire file
* Download original file

## File Handling

When a file is uploaded, StreamCode should preserve the original file contents.

For example:

```text
example.js
example.py
index.html
style.css
main.cpp
script.mcfunction
manifest.json
```

The original filename should be displayed on the shared page.

## Responsive Design

StreamCode should work on:

* Desktop
* Laptop
* Tablet
* Mobile

On smaller screens, the code viewer should remain horizontally scrollable rather than forcing long code lines into an unreadable layout.

## Core Product Statement

**StreamCode is an instant code-sharing platform for sharing and previewing complete code files in a clean, scrollable viewer—with the entire file available to read, copy, download, and share.**