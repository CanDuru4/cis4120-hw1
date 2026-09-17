# Course Picker Home

![HTML5](https://img.shields.io/badge/HTML5-vanilla-e34f26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-vanilla-1572b6?style=flat&logo=css3&logoColor=white)
[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-222222?style=flat&logo=github&logoColor=white)](https://canduru4.github.io/CIS-4120-HW1/)

A phone-sized, static HTML/CSS implementation of Screen 1 of a high-fidelity prototype:
Course Picker Home, a mock course-selection app for university students browsing and
shortlisting classes. It is a visual prototype for design review: there is no JavaScript, no
backend, and no interactive behaviour beyond the browser's own defaults.

> **Context:** CIS 4120 (Human-Computer Interaction) HW1, University of Pennsylvania, Spring 2026

Live page: [canduru4.github.io/CIS-4120-HW1](https://canduru4.github.io/CIS-4120-HW1/)

## Features

The prototype renders a single 390 × 844 phone frame containing:

- Status row and screen title
- Search field with placeholder text (visual only, no filtering)
- Filter chips: Requirement, Time, Workload, More Filters
- Tabs: "Suggested for You" and "All Courses"
- Three course cards (STAT 1020, CSCI 2470, PSYC 001) with rating, meeting time,
  requirement badge, and instructor
- "At a Glance: Fall 2024" weekly calendar built with CSS Grid
- Bottom navigation bar: Home, Builder, Plans, Cart

## Tech stack

- Vanilla HTML5: semantic sectioning elements, `aria-label` on the landmark regions
- Vanilla CSS3: custom properties for the colour palette, CSS Grid for the calendar,
  one `max-width: 420px` media query so the frame fits narrow screens
- No JavaScript, no frameworks, no build tooling, no dependencies

## Getting started

### Prerequisites

A modern web browser (Chrome, Safari, Firefox, or Edge). There is no build step, no package
manager, and no environment variables.

### Installation

Clone the repository, then open `index.html` in a browser by any of these methods:

1. Double-click `index.html` in Finder or your file manager.
2. From the terminal:

   ```bash
   open /path/to/CIS-4120-HW1/index.html      # macOS
   xdg-open /path/to/CIS-4120-HW1/index.html  # Linux
   start .\index.html                         # Windows (from the project folder)
   ```

3. Drag `index.html` into an open browser window.

## Project structure

```
CIS-4120-HW1/
├── index.html   # Screen 1 markup: header, search, chips, tabs, cards, calendar, nav
├── styles.css   # All styling: palette variables, phone frame, cards, CSS Grid calendar
└── README.md    # This file
```

## Testing

The layout targets a phone viewport, so review it in a device emulator:

1. Open the page in Chrome
2. `Cmd+Option+I` (macOS) or `F12` (Windows/Linux) to open DevTools
3. `Cmd+Shift+M` (macOS) or `Ctrl+Shift+M` (Windows/Linux) to toggle the device toolbar
4. Try iPhone 12, Pixel 5, or any ~390 px-wide preset

## Known limitations

- This is a static UI mock: buttons, tabs, and the search field are intentionally inert.
- Designed for phone-sized viewports (390 px frame width); below 420 px the frame scales to
  `95vw`.
- Course names, ratings, instructors, and schedule blocks are placeholder content for the
  prototype, not real course data.

## Acknowledgments

UI design and HTML/CSS layout assistance generated with AI (ChatGPT) and then manually edited
for the assignment.

## License

Coursework; no license granted. Please do not reuse this as your own assignment work.

## Author

Can Duru — [canduru.net](https://canduru.net)
