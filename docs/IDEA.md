# CampusConnect — IDEA.md

> **Project:** CampusConnect — A Mini University Web Portal  
> **Project Type:** Front-end academic lab project  
> **Primary Technologies:** HTML5, CSS3, Vanilla JavaScript  
> **Development Environment:** VS Code + modern web browser  
> **Optional Environment:** WampServer for localhost demonstration  
> **Status:** Baseline / Locked Product Specification

---

## 1. Project Overview

CampusConnect is a small, modern, responsive university web portal designed to help students quickly find information about academic departments, courses, student services, and contact details.

The project is intentionally implemented using only standard HTML, CSS, and JavaScript. It is a front-end prototype rather than a full production university information system. No framework, database, PHP application, or external backend is required for the basic implementation.

The project serves two purposes:

1. **Practical web development:** demonstrate the creation of a complete multi-page website using HTML, CSS, and JavaScript.
2. **Lab concepts:** provide one project through which one-tier, two-tier, and N-tier web architecture, development environments, HTTP, client/server concepts, navigation, sitemap planning, responsiveness, and web-design constraints can be discussed.

The supplied lab manual identifies CampusConnect as a "Mini University Web Portal" whose purpose is to help students find information about departments, courses, student services, and contact details.

---

## 2. Source Requirements

The lab manual requires the following minimum pages:

- Home
- Departments
- Courses
- Student Services
- Contact

It also identifies a **Student Enquiry form with a JavaScript validation message** as an optional feature.

The manual requires:

- Standard HTML structure and meaningful elements
- Separate CSS where practical
- Clear and consistent navigation
- Consideration of different browsers and screen sizes
- Avoidance of unnecessarily large images/files
- Information that is easy to find
- A simple and user-friendly interface
- A sitemap
- A rough Home-page wireframe
- A working HTML/CSS/JavaScript website
- One-tier, two-tier, and N-tier architecture diagrams
- A short development-environment explanation
- Browser testing and navigation testing

These source requirements are the non-negotiable academic baseline for this project.

---

## 3. Project Goals

### 3.1 Primary Goals

CampusConnect should:

1. Provide a complete five-page university portal.
2. Make important student information easy to discover.
3. Maintain consistent navigation across every page.
4. Use semantic and readable HTML.
5. Use one shared CSS file across the website.
6. Use one shared JavaScript file for client-side interactions.
7. Be fully responsive on desktop, tablet, and mobile screen sizes.
8. Include meaningful JavaScript interaction.
9. Include a validated Student Enquiry form.
10. Demonstrate good basic web-design practices.
11. Be simple enough to explain confidently during the lab demonstration.
12. Remain within the HTML/CSS/JavaScript scope of the assignment.

### 3.2 Secondary Goals

The website should also feel polished rather than like a collection of plain HTML pages.

The visual target is:

- Modern
- Clean
- Professional
- Academic
- Minimal
- Accessible
- Consistent
- Responsive
- Easy to navigate

---

## 4. Scope

### 4.1 In Scope

The project includes:

- Multi-page static website
- Shared header/navigation
- Responsive mobile navigation
- Shared footer
- Home page
- Departments page
- Courses page
- Student Services page
- Contact page
- Student Enquiry form
- Client-side form validation
- Course search/filter interaction
- Responsive layouts
- Cards and structured content sections
- Internal page navigation
- Basic visual interaction/feedback
- Browser-based testing
- Optional localhost testing through WampServer
- Sitemap
- Home-page wireframe
- Architecture diagrams

### 4.2 Out of Scope

The basic project does **not** include:

- User accounts
- Login/authentication
- Registration system
- Real student records
- Database storage
- PHP backend
- MySQL database
- REST API
- Node.js
- React/Vue/Angular
- Bootstrap/Tailwind
- Server-side form submission
- Real email delivery
- Real-time notifications
- Payment functionality
- Administrative dashboard
- CMS
- Cloud deployment as a requirement

If any of these are introduced later, that is an explicit scope change and must not silently alter the baseline specification.

---

# 5. Technology Decisions

## 5.1 HTML5

HTML is responsible for:

- Page structure
- Content
- Semantic sections
- Navigation
- Headings
- Links
- Forms
- Accessible labels
- Content hierarchy

Meaningful semantic elements should be preferred where appropriate, including:

- `header`
- `nav`
- `main`
- `section`
- `article`
- `footer`
- `form`
- `label`
- `button`

## 5.2 CSS3

CSS is responsible for:

- Layout
- Typography
- Colors
- Spacing
- Cards
- Buttons
- Navigation appearance
- Responsive behavior
- Hover/focus states
- Transitions
- Visual consistency

A single shared stylesheet will be used.

## 5.3 Vanilla JavaScript

JavaScript is responsible for client-side interaction, including:

- Mobile navigation
- Course filtering/search
- Student enquiry validation
- User feedback messages
- Small interface interactions where useful

JavaScript should remain understandable and proportional to the lab's scope.

## 5.4 Browser

The website will be tested in a modern browser such as:

- Chrome
- Edge
- Firefox

The lab manual specifically requires browser testing and recommends Developer Tools for inspecting HTML/CSS, console messages, and network requests.

## 5.5 VS Code

VS Code is the primary development environment.

The project should remain easy to open, understand, edit, and run directly from the project folder.

## 5.6 WampServer

WampServer is optional for the lab's localhost/server demonstration.

The website itself does not require PHP or MySQL for the basic implementation.

---

# 6. Project Structure

The project follows the structure specified by the lab manual:

```text
CampusConnect/
│
├── index.html
├── departments.html
├── courses.html
├── services.html
├── contact.html
│
├── css/
│   └── style.css
│
├── js/
│   └── script.js
│
└── assets/
```

## File Responsibilities

### `index.html`

The Home page and primary entry point.

### `departments.html`

Displays academic departments.

### `courses.html`

Displays courses/programs and provides course search/filter functionality.

### `services.html`

Displays available student services.

### `contact.html`

Displays contact information and contains the Student Enquiry form.

### `css/style.css`

Contains the shared visual design and responsive layout rules for all pages.

### `js/script.js`

Contains all shared client-side JavaScript behavior.

### `assets/`

Contains any local visual assets required by the website.

Images and other files should be appropriately sized because the lab manual explicitly identifies unnecessarily large files as a web-design/loading constraint.

---

# 7. Information Architecture

CampusConnect uses a simple flat structure so that major information is reachable directly from the main navigation.

```text
CampusConnect
│
├── Home
│
├── Departments
│
├── Courses
│
├── Student Services
│
└── Contact
    └── Student Enquiry
```

The Home page acts as the central entry point.

---

# 8. Sitemap

```text
                              CAMPUSCONNECT
                                    │
          ┌─────────────────────────┼─────────────────────────┐
          │                         │                         │
        HOME                 DEPARTMENTS                  COURSES
          │
          │
          ├────────────────── STUDENT SERVICES
          │
          └────────────────── CONTACT
                                  │
                                  └── Student Enquiry
```

A more detailed conceptual sitemap:

```text
Home
│
├── Departments
│   ├── Computer Science
│   ├── Software Engineering
│   ├── Information Technology
│   ├── Electrical Engineering
│   └── Business Administration
│
├── Courses
│   └── Search / Filter Programs
│
├── Student Services
│   ├── Academic Advising
│   ├── Library
│   ├── Career Services
│   ├── Student Affairs
│   └── IT Support
│
└── Contact
    └── Student Enquiry Form
```

The detailed department/service names above are **project content decisions for the prototype**, not additional requirements stated by the lab manual.

---

# 9. Global Design System

## 9.1 Design Philosophy

The design should communicate:

- Trust
- Academic professionalism
- Simplicity
- Accessibility
- Organization
- Student friendliness

The UI should avoid excessive decoration.

## 9.2 Color Direction

The baseline visual direction uses a university-style palette:

- Deep navy as the primary brand color
- Blue as an interactive/accent color
- White for primary surfaces
- Light neutral backgrounds
- Dark neutral text
- Subtle borders and shadows

Exact color values should be defined centrally in CSS variables so the entire site can be changed consistently.

Example conceptual variables:

```css
:root {
    --primary: ...;
    --primary-dark: ...;
    --accent: ...;
    --background: ...;
    --surface: ...;
    --text: ...;
    --text-muted: ...;
    --border: ...;
}
```

The exact palette can be finalized during implementation without changing the product scope.

## 9.3 Typography

Typography should prioritize:

- Readability
- Clear hierarchy
- Appropriate line height
- Strong headings
- Comfortable body text
- Responsive sizing

The page should visually distinguish:

- Main page headings
- Section headings
- Card titles
- Body text
- Supporting text
- Buttons/links

## 9.4 Spacing

The design should use a consistent spacing system rather than arbitrary margins throughout the stylesheet.

## 9.5 Cards

Cards will be used for:

- Quick-access links
- Departments
- Courses/programs
- Student services

Cards should have:

- Clear title
- Short description
- Optional icon
- Clear action/link
- Subtle hover state

---

# 10. Global Components

Every page should share the same major components.

## 10.1 Header

The header contains:

- CampusConnect branding
- University/project identity
- Main navigation

Desktop:

```text
CampusConnect        Home  Departments  Courses  Services  Contact
```

Mobile:

```text
CampusConnect                                      ☰
```

## 10.2 Navigation

Navigation must:

- Appear consistently on every page
- Link to every required page
- Clearly identify the current page
- Work on mobile
- Remain easy to understand

## 10.3 Mobile Navigation

On smaller screens:

- Desktop navigation is replaced by a menu button.
- JavaScript controls opening/closing.
- Menu items remain accessible.
- The page should not overflow horizontally.

## 10.4 Footer

The footer should appear consistently across pages.

It can contain:

- CampusConnect branding
- Short description
- Navigation links
- Contact information
- Copyright notice

The footer should remain visually simple.

---

# 11. Page Specifications

# 11.1 Home Page — `index.html`

## Purpose

Introduce CampusConnect and provide immediate access to major areas of the portal.

## Section Structure

### A. Header

Shared global header/navigation.

### B. Hero

Primary message:

> Your Campus. Your Opportunities.

Supporting message should explain that CampusConnect helps students explore university information and services.

Primary actions:

- Explore Departments
- View Courses

### C. Quick Access

Four major cards:

1. Departments
2. Courses
3. Student Services
4. Contact

Each card links to the corresponding page.

### D. Why CampusConnect?

A small feature section highlighting qualities such as:

- Easy to Navigate
- Student Focused
- Accessible Information
- Connected Campus

This section is presentation content rather than a separate backend feature.

### E. Popular Departments

Display selected department cards.

Initial prototype content may include:

- Computer Science
- Software Engineering
- Information Technology
- Electrical Engineering

### F. Student Services Preview

Display selected services such as:

- Academic Advising
- Library
- Career Services
- IT Support

Include a link to the complete Student Services page.

### G. Contact Call-to-Action

A final section encouraging students to contact CampusConnect for questions.

### H. Footer

Shared footer.

---

# 11.2 Departments Page — `departments.html`

## Purpose

Provide an easy-to-scan overview of academic departments.

## Page Structure

### A. Page Hero

Title:

> Academic Departments

Supporting text explains that students can explore the university's academic areas.

### B. Department Grid

Prototype department cards:

1. Computer Science
2. Software Engineering
3. Information Technology
4. Electrical Engineering
5. Business Administration
6. Mathematics

Each card contains:

- Department name
- Short description
- Optional icon
- Explore link/action

### C. Footer

Shared footer.

---

# 11.3 Courses Page — `courses.html`

## Purpose

Help students discover available academic programs.

## Page Structure

### A. Page Hero

Title:

> Courses & Programs

### B. Search/Filter Area

Provide:

- Course search field
- Department/category filter

Example:

```text
[ Search courses... ] [ All Departments ▼ ]
```

### C. Course Grid

Prototype programs may include:

- BS Computer Science
- BS Software Engineering
- BS Information Technology
- BBA

Each course card may display:

- Program name
- Department
- Duration
- Short description
- View/Explore action

### D. JavaScript Filtering

The user can:

- Type a search term
- Select a department/category
- See matching course cards
- See a useful empty-state message when no match exists

The filtering is client-side and does not require a backend.

### E. Footer

Shared footer.

---

# 11.4 Student Services Page — `services.html`

## Purpose

Give students a central location for common university support services.

## Page Structure

### A. Page Hero

Title:

> Student Services

### B. Services Grid

Prototype services:

#### Academic Advising

Academic planning and guidance.

#### Library

Learning resources and study facilities.

#### Career Services

Career guidance, internships, and employment resources.

#### Student Affairs

Support for student activities and campus life.

#### IT Support

Technical assistance for university systems.

#### Admissions

Application and enrollment information.

### C. Footer

Shared footer.

The service names and descriptions are prototype content decisions used to make the required Student Services page meaningful.

---

# 11.5 Contact Page — `contact.html`

## Purpose

Provide contact information and allow students to submit a basic enquiry.

## Page Structure

### A. Page Hero

Title:

> Contact CampusConnect

### B. Contact Information

Include placeholder/prototype information for:

- Campus address
- Phone
- Email
- Office hours

Any real university identity or contact information should only be inserted if provided by the project team/instructor.

### C. Student Enquiry Form

Fields:

1. Full Name
2. Email
3. Subject
4. Message

Submit button:

> Send Enquiry

### D. Client-Side Validation

JavaScript should check:

- Name is not empty
- Email is present and follows a reasonable email pattern
- Subject is not empty
- Message is not empty

Validation messages should be clear and understandable.

Examples:

```text
Please enter your name.
Please enter a valid email address.
Please enter a subject.
Please enter your message.
```

On valid submission, show a success message such as:

```text
Your enquiry has been submitted successfully.
```

Because this is a static HTML/CSS/JS prototype, the form does **not** actually send an email or save information to a database.

### E. Footer

Shared footer.

---

# 12. JavaScript Specification

All JavaScript should be placed in:

```text
js/script.js
```

## 12.1 Mobile Menu

Required behavior:

1. User clicks menu button.
2. Navigation becomes visible.
3. User clicks again/close control.
4. Navigation closes.
5. Menu remains usable on small screens.

## 12.2 Active Navigation

The current page should receive an active visual state.

This can be implemented using the current document path or explicit page classes.

## 12.3 Course Search

The course page should support client-side searching.

Example:

```text
Input: "software"

Result:
BS Software Engineering
```

The search should be case-insensitive.

## 12.4 Course Category Filter

The department/category selector should filter available courses.

The search and category filter should work together.

## 12.5 Empty Search State

If no course matches, display a clear message such as:

```text
No courses found.
Try a different search term or category.
```

## 12.6 Enquiry Form Validation

The form should prevent invalid submission and display appropriate feedback.

No backend submission is required.

---

# 13. Responsive Design Specification

Responsiveness is a core requirement.

## 13.1 Desktop

At large widths:

- Full navigation visible
- Multi-column card grids
- Wide hero layout
- Comfortable whitespace

## 13.2 Tablet

At medium widths:

- Reduced column count
- Adjusted spacing
- Navigation remains usable
- Cards resize naturally

## 13.3 Mobile

At small widths:

- Hamburger navigation
- Single-column or compact layouts
- Full-width buttons where appropriate
- Form fields stacked vertically
- No horizontal overflow
- Readable text
- Comfortable touch targets

## 13.4 Responsive Rules

The implementation should be tested by manually resizing the browser.

Testing should confirm:

- No content is cut off
- No horizontal scrollbar caused by layout mistakes
- Navigation works
- Cards fit correctly
- Images remain within their containers
- Forms remain usable
- Text remains readable

---

# 14. Accessibility & Usability Baseline

The project should follow basic accessibility practices even though this is a lab prototype.

## Requirements

- Use semantic HTML
- Use labels for form controls
- Provide meaningful link text
- Maintain sufficient text/background contrast
- Keep keyboard focus visible
- Avoid relying only on color to communicate information
- Use buttons for button actions
- Use links for navigation
- Provide `alt` text for meaningful images
- Maintain logical heading hierarchy

The website should prioritize user-centered design and make information easy to find.

---

# 15. Navigation Rules

Every page must have working navigation to:

```text
Home
Departments
Courses
Student Services
Contact
```

Navigation should use relative links appropriate for the folder structure.

Example:

```html
<a href="index.html">Home</a>
<a href="departments.html">Departments</a>
<a href="courses.html">Courses</a>
<a href="services.html">Services</a>
<a href="contact.html">Contact</a>
```

No navigation link should lead to a missing page.

---

# 16. Content Strategy

The content should be:

- Concise
- Professional
- Student-focused
- Easy to scan
- Consistent in tone

Avoid large blocks of unnecessary text.

Use:

- Headings
- Short paragraphs
- Lists
- Cards
- Clear calls to action

The portal's primary goal is quick information discovery.

---

# 17. Asset Strategy

The `assets/` directory should only contain assets that genuinely improve the interface.

Rules:

- Avoid unnecessarily large images.
- Prefer appropriately sized assets.
- Do not add dozens of decorative files.
- Keep filenames descriptive.
- Use optimized images when images are included.
- Do not make the website dependent on large external assets.

If no image is necessary for a section, a clean CSS-based design should be preferred.

---

# 18. Error & Empty States

The website should provide useful feedback.

Examples:

### No courses found

```text
No courses found.
Try a different search term or department.
```

### Invalid enquiry

```text
Please enter a valid email address.
```

### Successful enquiry

```text
Your enquiry has been submitted successfully.
```

Messages should be visually noticeable without being disruptive.

---

# 19. Architecture Representation

The website itself is a front-end prototype, but the lab requires understanding and diagrams for three architectures.

## 19.1 One-Tier

For this lab, the simple self-contained prototype is treated as one tier.

```text
Browser
   │
   ├── HTML
   ├── CSS
   └── JavaScript
```

The browser handles presentation and client-side logic.

## 19.2 Two-Tier

The browser communicates with a web server.

```text
Browser / Client
       │
       │ HTTP
       ▼
   Web Server
       │
       ▼
    Response
```

## 19.3 N-Tier

Responsibilities are separated into logical layers.

```text
Presentation
     │
     ▼
Application / Business Logic
     │
     ▼
Data Access
     │
     ▼
Database
```

The N-tier diagram is conceptual for this lab; the actual CampusConnect prototype does not implement these backend layers.

---

# 20. Development Workflow

The project should be developed incrementally.

## Phase 1 — Planning

- Understand requirements
- Finalize sitemap
- Finalize wireframe
- Lock page responsibilities
- Lock design direction

## Phase 2 — Project Setup

Create the required folders and files.

## Phase 3 — Global Foundation

Build:

- HTML base structure
- Shared header
- Navigation
- Footer
- CSS variables
- Typography
- Buttons
- Responsive foundation

## Phase 4 — Home Page

Implement the complete Home page.

## Phase 5 — Departments

Implement department content and cards.

## Phase 6 — Courses

Implement course cards and JavaScript filtering/search.

## Phase 7 — Student Services

Implement service cards and supporting content.

## Phase 8 — Contact

Implement contact information and enquiry form validation.

## Phase 9 — Responsive Polish

Test and refine desktop, tablet, and mobile layouts.

## Phase 10 — Testing

Test:

- Navigation
- Forms
- JavaScript
- Browser console
- Responsiveness
- Typography
- Layout
- Links
- Assets

## Phase 11 — WampServer

If WampServer is available:

1. Start WampServer.
2. Ensure Apache is running.
3. Place CampusConnect inside the WampServer web directory.
4. Open the project through localhost.
5. Test all pages and navigation.

## Phase 12 — Architecture Deliverables

Prepare:

- One-tier diagram
- Two-tier diagram
- N-tier diagram

## Phase 13 — Final Demonstration

Prepare a short walkthrough demonstrating:

1. Home page
2. Navigation
3. Departments
4. Courses
5. Course filtering
6. Student Services
7. Contact page
8. Enquiry validation
9. Responsive behavior
10. Architecture concepts

---

# 21. Testing Checklist

## Functional Testing

- [ ] Home page loads
- [ ] Departments page loads
- [ ] Courses page loads
- [ ] Services page loads
- [ ] Contact page loads
- [ ] All navigation links work
- [ ] Home CTA links work
- [ ] Course search works
- [ ] Course category filter works
- [ ] Empty course state works
- [ ] Mobile menu opens
- [ ] Mobile menu closes
- [ ] Form rejects empty fields
- [ ] Form rejects invalid email
- [ ] Form accepts valid input
- [ ] Success message appears

## Responsive Testing

- [ ] Desktop layout works
- [ ] Tablet layout works
- [ ] Mobile layout works
- [ ] No unintended horizontal overflow
- [ ] Navigation remains usable
- [ ] Cards resize/stack correctly
- [ ] Forms remain usable
- [ ] Buttons remain accessible

## Visual Testing

- [ ] Consistent header
- [ ] Consistent footer
- [ ] Consistent typography
- [ ] Consistent spacing
- [ ] Consistent buttons
- [ ] Consistent cards
- [ ] Active navigation state works
- [ ] Hover/focus states work
- [ ] Text is readable
- [ ] Sections are visually distinct

## Developer Tools

- [ ] Console has no avoidable JavaScript errors
- [ ] HTML structure inspected
- [ ] CSS inspected
- [ ] Network/resources checked where appropriate

## Browser Testing

Where available:

- [ ] Chrome
- [ ] Edge
- [ ] Firefox

---

# 22. Performance Baseline

For a small static website, performance should remain simple.

Rules:

- Keep CSS organized.
- Keep JavaScript lightweight.
- Avoid unnecessary libraries.
- Avoid unnecessarily large images.
- Avoid duplicated CSS across HTML files.
- Avoid duplicated JavaScript across pages.
- Use one shared stylesheet and one shared script.

---

# 23. Code Quality Rules

## HTML

- Use valid document structure.
- Use semantic elements.
- Use meaningful class names.
- Keep indentation consistent.
- Avoid unnecessary inline styles.

## CSS

- Keep styling in `css/style.css`.
- Use CSS variables for repeated design values.
- Group related rules.
- Keep responsive rules organized.
- Avoid excessive specificity.
- Avoid duplicated styles.

## JavaScript

- Keep logic in `js/script.js`.
- Use descriptive variable/function names.
- Avoid unnecessary global variables.
- Add event listeners cleanly.
- Validate DOM elements before operating on optional page-specific components.
- Keep page-specific functionality from breaking other pages.

---

# 24. Page Independence Requirement

Because the same `script.js` is loaded on every page, JavaScript must be written so that a feature existing on one page does not cause errors on pages where its related HTML does not exist.

For example:

```text
Courses page → course search exists
Contact page → course search does not exist
```

The script should safely detect whether the relevant elements exist before attaching behavior.

This is an important implementation rule for a shared multi-page JavaScript file.

---

# 25. Visual Consistency Rules

The following must remain consistent throughout the website:

- Header height/style
- Navigation
- Active navigation state
- Button styles
- Card radius
- Card shadows/borders
- Typography hierarchy
- Page container width
- Section spacing
- Footer
- Responsive breakpoints

A user should immediately recognize that all five pages belong to the same website.

---

# 26. Home Page Wireframe

Conceptual wireframe:

```text
┌─────────────────────────────────────────────────────┐
│ CAMPUSCONNECT              Home Departments Courses │
│                            Services Contact      ☰ │
├─────────────────────────────────────────────────────┤
│                                                     │
│              YOUR CAMPUS.                           │
│              YOUR OPPORTUNITIES.                    │
│                                                     │
│      Explore university information and services.   │
│                                                     │
│      [ Explore Departments ] [ View Courses ]       │
│                                                     │
├─────────────────────────────────────────────────────┤
│                  QUICK ACCESS                       │
│                                                     │
│   [ Departments ] [ Courses ] [ Services ] [Contact]│
│                                                     │
├─────────────────────────────────────────────────────┤
│              POPULAR DEPARTMENTS                    │
│                                                     │
│       [ Card ]      [ Card ]      [ Card ]           │
│                                                     │
├─────────────────────────────────────────────────────┤
│              STUDENT SERVICES                       │
│                                                     │
│       [ Service ]    [ Service ]    [ Service ]     │
│                                                     │
├─────────────────────────────────────────────────────┤
│                    NEED HELP?                       │
│                  [ Contact Us ]                     │
├─────────────────────────────────────────────────────┤
│ Footer                                              │
└─────────────────────────────────────────────────────┘
```

This satisfies the lab's requested rough Home-page wireframe components:

- Header/university name
- Navigation
- Main content
- Important links/services
- Footer

---

# 27. Academic Demonstration Mapping

The website should make it easy to demonstrate the concepts in the lab.

| Lab Concept | CampusConnect Demonstration |
|---|---|
| HTML | Page structure and semantic elements |
| CSS | Layout, colors, typography, responsive design |
| JavaScript | Menu, course filtering, form validation |
| Browser | Running and viewing the website |
| HTTP | Browser/server request concept |
| Client | Browser |
| Server | WampServer/Apache concept |
| One-tier | Browser + HTML/CSS/JS |
| Two-tier | Browser → Web Server |
| N-tier | Presentation → Logic → Data Access → Database |
| Sitemap | CampusConnect navigation structure |
| Wireframe | Home-page planning |
| Responsive design | Browser resizing |
| Developer Tools | Inspect HTML/CSS/Console |
| Web constraints | Readability, bandwidth, screen sizes, navigation |

---

# 28. Final Deliverables

The final submission should contain:

1. Working CampusConnect website
2. `index.html`
3. `departments.html`
4. `courses.html`
5. `services.html`
6. `contact.html`
7. `css/style.css`
8. `js/script.js`
9. `assets/` directory as needed
10. Sitemap
11. Home-page wireframe
12. One-tier architecture diagram
13. Two-tier architecture diagram
14. N-tier architecture diagram
15. Short development-environment explanation
16. Short demonstration

---

# 29. Exit-Question Preparation

The implementation should support explanations for the lab's exit questions.

The team should be able to explain:

### Internet vs WWW

The Internet is the global network infrastructure, while the WWW is a service that provides linked web pages and resources over the Internet.

### HTTP

HTTP is the protocol used for communication between web clients and web servers.

### Browser

A browser is client software that requests and displays web pages.

### Web Server

A web server receives web requests and sends responses.

### WampServer

WampServer provides a local Windows-based environment commonly involving Apache, PHP, and MySQL and can be used to demonstrate a local web server.

### Development Environment

A development environment is the collection of tools, software, and configuration used to create, test, and debug a website.

### One-Tier vs Two-Tier

One-tier keeps the relevant presentation/client-side logic together, while two-tier separates the client from a server.

### N-Tier

N-tier separates responsibilities into logical layers such as presentation, business logic, data access, and database.

### Sitemap

A sitemap represents the structure and navigation relationships between pages.

### Web Design Constraints

Examples include:

- Different screen sizes
- Browser differences
- Bandwidth/loading considerations
- Readability
- Navigation and information discoverability

---

# 30. Definition of Done

CampusConnect is considered complete when:

### Structure

- [ ] Required folder structure exists.
- [ ] All five required pages exist.
- [ ] Shared CSS is connected to every page.
- [ ] Shared JavaScript is connected to every page.

### Design

- [ ] Website has a coherent visual identity.
- [ ] Pages look like one unified product.
- [ ] Layout is clean and modern.
- [ ] Typography is readable.
- [ ] Spacing is consistent.
- [ ] Cards/buttons are consistent.

### Functionality

- [ ] Navigation works.
- [ ] Mobile menu works.
- [ ] Course search/filter works.
- [ ] Enquiry form validation works.
- [ ] User feedback messages work.

### Responsiveness

- [ ] Desktop works.
- [ ] Tablet works.
- [ ] Mobile works.
- [ ] No unintended horizontal scrolling.

### Quality

- [ ] No avoidable console errors.
- [ ] No broken internal links.
- [ ] No missing required pages.
- [ ] Assets are appropriately sized.
- [ ] HTML/CSS/JS are organized and understandable.

### Academic Requirements

- [ ] Sitemap completed.
- [ ] Home wireframe completed.
- [ ] One-tier diagram completed.
- [ ] Two-tier diagram completed.
- [ ] N-tier diagram completed.
- [ ] Development environment explanation prepared.
- [ ] Demo walkthrough prepared.

---

# 31. Change-Control Rule

This `IDEA.md` is the **baseline product specification** for CampusConnect.

Future implementation and planning should preserve:

- Required pages
- Folder structure
- HTML/CSS/JavaScript technology choice
- Core functionality
- Responsive requirement
- Navigation structure
- Student Enquiry validation
- Course filtering/search
- Design direction
- Architecture-learning purpose
- Academic deliverables
- Scope boundaries

A feature should not be added merely because it is technically possible.

Any change that affects the project's scope, architecture, required pages, core features, technology stack, or academic requirements must be explicitly approved before being treated as part of the project.

---

# 32. Implementation Principle

> **Build a polished website without overengineering the lab.**

CampusConnect should demonstrate strong fundamentals rather than unnecessary technical complexity.

The priority order is:

1. Correct requirements
2. Clean structure
3. Consistent design
4. Working navigation
5. Responsive behavior
6. Meaningful JavaScript interaction
7. Testing
8. Academic explanation

The final project should be simple enough to understand, polished enough to demonstrate confidently, and complete enough to satisfy every required component of the lab.

---

## End of IDEA.md
