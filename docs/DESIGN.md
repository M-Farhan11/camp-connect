# CampusConnect — DESIGN.md

> **Design system and UI specification for AI-generated screens**
>
> **Project:** CampusConnect — A Mini University Web Portal  
> **Scope:** UI/UX design only  
> **Implementation:** HTML5 + CSS3 + Vanilla JavaScript  
> **Status:** Design baseline — pending visual approval  
> **Primary use:** Claude / Google Stitch / other UI-generation tools  
>
> **Important:** This document defines the visual language and screen requirements. It does not expand the product scope defined in `IDEA.md`.

---

## 1. Purpose

`DESIGN.md` is the single source of truth for the visual design of CampusConnect.

The purpose is to ensure that every AI-generated screen looks like it belongs to the same product instead of allowing each page to invent a different:

- color palette
- typography system
- navigation
- spacing system
- card style
- button style
- border radius
- shadow treatment
- responsive behavior
- interaction language

The design should feel like a **modern university portal**, not a generic template and not an over-designed SaaS dashboard.

The UI should be:

- Clean
- Modern
- Professional
- Academic
- Calm
- Student-friendly
- Highly readable
- Responsive
- Consistent
- Slightly premium without becoming flashy

---

# 2. Design Principles

## 2.1 Information First

CampusConnect exists to help students find information quickly.

The UI must prioritize:

1. Page title
2. Important information
3. Primary actions
4. Supporting information
5. Secondary actions

Do not sacrifice clarity for decoration.

---

## 2.2 One Product, One Visual Language

Every screen must look like part of the same website.

Do not independently redesign:

- Header
- Navigation
- Buttons
- Cards
- Forms
- Footer
- Typography
- Page containers

for individual pages.

---

## 2.3 Modern, Not Trendy

Use contemporary UI patterns, but avoid:

- excessive gradients
- glassmorphism everywhere
- huge decorative blobs
- excessive rounded pills
- excessive animations
- neon colors
- dashboard-like visual density
- unnecessary illustrations
- overly large typography
- excessive shadows

The visual direction should remain appropriate for a university website.

---

## 2.4 Strong Visual Hierarchy

Every screen should have an obvious hierarchy:

```text
Brand / Navigation
        ↓
Page Purpose
        ↓
Primary Content
        ↓
Supporting Content
        ↓
Primary Action
        ↓
Footer
```

---

## 2.5 Generous Whitespace

Use whitespace deliberately.

The UI should never feel cramped.

Cards, sections, headings, and controls should have breathing room.

---

# 3. Color System

## 3.1 Palette Direction

The chosen direction is a **cool navy + blue + soft neutral** university palette.

Coolors is being used as the palette reference source because it provides palette generation, visualization, and accessibility/contrast checking tools.

Reference:

https://coolors.co/

A Coolors-style palette direction for CampusConnect:

```text
Primary Navy       #0F172A
Primary Blue       #2563EB
Soft Blue          #EFF6FF
Page Background    #F8FAFC
Surface            #FFFFFF
Text Primary       #0F172A
Text Secondary     #475569
Text Muted         #64748B
Border             #E2E8F0
Success            #16A34A
Success Soft       #F0FDF4
Warning            #D97706
Warning Soft       #FFFBEB
Error              #DC2626
Error Soft         #FEF2F2
```

### Palette roles

| Token | Value | Purpose |
|---|---|---|
| `--color-primary` | `#0F172A` | Brand/navy, major headings, footer |
| `--color-primary-soft` | `#E2E8F0` | Soft navy/neutral backgrounds |
| `--color-accent` | `#2563EB` | Primary CTA and active states |
| `--color-accent-hover` | `#1D4ED8` | CTA hover |
| `--color-accent-soft` | `#EFF6FF` | Soft blue surfaces |
| `--color-background` | `#F8FAFC` | Main page background |
| `--color-surface` | `#FFFFFF` | Cards, header, form surfaces |
| `--color-text` | `#0F172A` | Main text |
| `--color-text-secondary` | `#475569` | Secondary text |
| `--color-text-muted` | `#64748B` | Supporting/meta text |
| `--color-border` | `#E2E8F0` | Borders/dividers |
| `--color-success` | `#16A34A` | Success states |
| `--color-warning` | `#D97706` | Warning states |
| `--color-error` | `#DC2626` | Error states |

### Color usage rule

The website should be approximately:

```text
70% — neutral/white surfaces
20% — navy/blue visual structure
10% — accent and status colors
```

Do not turn the whole website blue.

### Background rule

Use:

- `#F8FAFC` for the primary page background
- `#FFFFFF` for cards and major content surfaces
- `#EFF6FF` for selected soft-highlight sections
- `#0F172A` for strong dark sections such as footer or optional hero contrast areas

Avoid full-screen dark backgrounds except where explicitly requested.

---

# 4. Typography System

## 4.1 Direction

Use a clean modern sans-serif typeface.

Preferred direction:

```text
Primary font:
Inter / system sans-serif equivalent
```

If the design tool cannot guarantee Inter, use a visually similar modern sans-serif.

Do not mix multiple unrelated font families.

---

## 4.2 Type Scale

### Desktop

```text
Display:       52–64px
H1:            42–48px
H2:            32–36px
H3:            22–24px
H4:            18–20px
Body Large:    18px
Body:          16px
Body Small:    14px
Caption:       12–13px
Button:        14–16px
```

### Mobile

```text
Display:       38–44px
H1:            32–36px
H2:            26–30px
H3:            20–22px
Body:          15–16px
Small:         13–14px
```

Do not use huge 80–100px hero headings.

---

## 4.3 Typography Rules

Headings:

- strong
- concise
- high contrast
- slightly tight line-height

Body:

- readable
- relaxed line-height
- muted where appropriate

Recommended approximate line heights:

```text
Headings: 1.1–1.2
Body:     1.5–1.7
```

---

# 5. Layout System

## 5.1 Global Container

Desktop content should use a centered container:

```text
max-width: 1200px
```

Allow approximately:

```text
24px mobile side padding
32px tablet side padding
40–48px desktop side padding
```

Do not allow content to touch viewport edges.

---

## 5.2 Page Structure

Every page follows:

```text
┌────────────────────────────────────────────┐
│ Header / Navigation                        │
├────────────────────────────────────────────┤
│                                            │
│ Page-specific content                      │
│                                            │
├────────────────────────────────────────────┤
│ Footer                                     │
└────────────────────────────────────────────┘
```

---

## 5.3 Section Spacing

Desktop:

```text
Small section gap:     48px
Standard section gap:  72px
Major section gap:     96px
```

Mobile:

```text
Small section gap:     32px
Standard section gap:  48px
Major section gap:     64px
```

Avoid arbitrary spacing values throughout the UI.

---

# 6. Border Radius System

Use moderate, consistent rounding.

```text
Small controls:     8px
Buttons:            8px
Inputs:             8px
Cards:              14px
Large feature card: 18px
```

Do not make every component pill-shaped.

Pill shapes are reserved for:

- status badges
- small category tags
- compact filters where appropriate

---

# 7. Shadow System

Use subtle shadows only.

### Shadow Small

```text
0 1px 3px rgba(15, 23, 42, 0.06)
```

### Shadow Medium

```text
0 8px 24px rgba(15, 23, 42, 0.08)
```

### Shadow Large

```text
0 16px 40px rgba(15, 23, 42, 0.10)
```

Default cards should generally use:

- subtle border
- very light shadow

Avoid heavy floating-card effects.

---

# 8. Buttons

Buttons must be visually consistent throughout the entire website.

## 8.1 Primary Button

Purpose:

- Main CTA
- Important navigation action
- Form submission

Appearance:

```text
Background: #2563EB
Text:       #FFFFFF
Radius:     8px
Height:     44–48px
Padding:    0 18–22px
Font:       14–16px / semibold
```

Hover:

```text
Background → #1D4ED8
Slight upward movement: 1–2px
Subtle shadow increase
```

Do not use dramatic scaling.

---

## 8.2 Secondary Button

Purpose:

- Supporting CTA
- Alternative action

Appearance:

```text
Background: #FFFFFF
Text:       #0F172A
Border:     #E2E8F0
Radius:     8px
```

Hover:

```text
Background → #F8FAFC
Border → slightly darker
```

---

## 8.3 Ghost Button

Purpose:

- Low-emphasis actions
- Header utility actions

Appearance:

```text
Transparent background
No strong border
Text: #475569
```

Hover:

```text
Background: #F8FAFC
Text: #0F172A
```

---

## 8.4 Text Link

Use for:

- card actions
- inline navigation
- secondary navigation

Style:

```text
Accent blue
Semibold
Optional arrow →
```

Hover:

```text
Color darkens
Arrow moves 2–3px
```

---

## 8.5 Button States

Every button should conceptually support:

```text
Default
Hover
Focus
Active
Disabled
```

Disabled:

```text
Reduced contrast
No hover animation
Cursor indicates unavailable state
```

---

# 9. Header & Navigation

## 9.1 Desktop Header

The header should be:

- white
- clean
- compact
- sticky or visually persistent if appropriate
- separated from content by a subtle border

Layout:

```text
[CampusConnect]              Home Departments Courses Services Contact
```

Brand on left.

Navigation on right.

---

## 9.2 Active Navigation

Current page:

- accent blue text
- subtle background or underline
- clearly visible

Do not use an oversized active tab.

---

## 9.3 Mobile Header

Layout:

```text
[CampusConnect]                       [☰]
```

On menu open:

```text
┌──────────────────────────────┐
│ Home                         │
│ Departments                  │
│ Courses                      │
│ Student Services             │
│ Contact                      │
└──────────────────────────────┘
```

The mobile menu should animate softly.

---

# 10. Hero Design

The Home hero is the strongest visual section.

## Required content

Headline:

> Your Campus. Your Opportunities.

Supporting text:

> Explore departments, discover courses, access student services, and stay connected with your university.

Primary CTA:

> Explore Departments

Secondary CTA:

> View Courses

## Visual direction

Use:

- strong typography
- generous whitespace
- subtle blue visual accents
- optional abstract academic/geometric visual treatment

Do not use:

- stock-photo-heavy hero
- huge illustration taking most of the viewport
- complicated animation
- excessive gradient

The hero should feel polished but fast-loading.

---

# 11. Cards

Cards are a major component across CampusConnect.

## 11.1 Standard Card

Structure:

```text
┌──────────────────────────────┐
│ Icon / visual                │
│                              │
│ Card Title                   │
│ Short supporting description │
│                              │
│ Explore →                    │
└──────────────────────────────┘
```

Properties:

```text
Background: white
Border: 1px solid #E2E8F0
Radius: 14px
Padding: 24px
Shadow: subtle
```

Hover:

```text
translateY(-3px)
shadow increases slightly
border/accent becomes subtly stronger
```

Animation should be around 180–220ms.

---

# 12. Quick Access Cards

Home page:

```text
Departments
Courses
Student Services
Contact
```

These should be visually prominent but not oversized.

Desktop:

```text
[ Departments ] [ Courses ] [ Services ] [ Contact ]
```

Tablet:

```text
[ Departments ] [ Courses ]
[ Services   ] [ Contact ]
```

Mobile:

```text
[ Departments ]
[ Courses ]
[ Services ]
[ Contact ]
```

---

# 13. Department Cards

Each department card should contain:

- subtle icon
- department name
- short description
- action

Suggested departments:

- Computer Science
- Software Engineering
- Information Technology
- Electrical Engineering
- Business Administration
- Mathematics

Do not add unrelated departments beyond this project content unless explicitly requested.

---

# 14. Course Cards

Course cards should prioritize scanability.

Suggested structure:

```text
┌──────────────────────────────┐
│ BS Computer Science          │
│ Computing                    │
│                              │
│ 4 Years                      │
│                              │
│ Explore →                    │
└──────────────────────────────┘
```

Use small metadata text for:

- department
- duration

---

# 15. Course Search & Filter UI

The Courses page should contain a clean filter row.

Desktop:

```text
┌──────────────────────────────┐ ┌─────────────────┐
│ Search courses...            │ │ All Departments │
└──────────────────────────────┘ └─────────────────┘
```

Mobile:

```text
┌──────────────────────────────┐
│ Search courses...            │
└──────────────────────────────┘

┌──────────────────────────────┐
│ All Departments              │
└──────────────────────────────┘
```

Inputs should use the same form-control language as the Contact page.

---

# 16. Forms

## 16.1 Input

Default:

```text
Background: #FFFFFF
Border: #CBD5E1
Radius: 8px
Height: 44–48px
Padding: 12–14px
```

Focus:

```text
Border: #2563EB
Visible focus ring
```

Example:

```text
0 0 0 3px rgba(37, 99, 235, 0.12)
```

---

## 16.2 Labels

Labels should:

- appear above fields
- be clearly associated with inputs
- use medium/semi-bold text
- remain visible rather than relying on placeholders

---

## 16.3 Placeholder

Use muted gray.

Do not use placeholder text as the only field label.

---

# 17. Validation & Error Design

Error states must be calm, clear, and aligned with the design system.

## Invalid field

```text
Label

[ invalid input................ ]

Please enter a valid email address.
```

Error color:

```text
#DC2626
```

Input border:

```text
#DC2626
```

Soft background only when useful.

---

## Form-level error

Use a compact alert near the form:

```text
┌─────────────────────────────────────────┐
│ Please correct the highlighted fields.  │
└─────────────────────────────────────────┘
```

Do not use browser-default alert popups.

---

# 18. Success Message

After valid Student Enquiry submission:

```text
┌─────────────────────────────────────────┐
│ ✓ Your enquiry has been submitted       │
│   successfully.                         │
└─────────────────────────────────────────┘
```

Use:

```text
Success: #16A34A
Soft background: #F0FDF4
```

The message should appear inline within the form context.

---

# 19. Warning & Informational States

### Warning

Use sparingly.

```text
Color: #D97706
Background: #FFFBEB
```

### Information

Use:

```text
Blue accent
Very soft blue background
```

Avoid creating alerts for ordinary content.

---

# 20. Icons

Icons should be:

- simple
- line-based
- consistent
- restrained

Use icons primarily for:

- departments
- courses
- student services
- contact
- navigation
- validation states

Do not mix multiple icon styles.

If an icon library is not available in the final HTML/CSS/JS implementation, use simple inline SVG or CSS-friendly alternatives rather than adding a large dependency.

---

# 21. Footer

The footer should be visually distinct but simple.

Suggested structure:

```text
┌──────────────────────────────────────────────────┐
│ CampusConnect                                    │
│ Connecting students with campus information.     │
│                                                  │
│ Quick Links       Contact                        │
│ Home              Email                          │
│ Departments       Phone                          │
│ Courses           Address                        │
│ Services                                           │
│                                                  │
│ ──────────────────────────────────────────────── │
│ © CampusConnect. All rights reserved.            │
└──────────────────────────────────────────────────┘
```

Use the primary navy background.

Keep the footer compact.

---

# 22. Animation System

Animations should improve perceived quality without distracting users.

## 22.1 General Duration

```text
Fast:       120–160ms
Standard:   180–220ms
Emphasis:   250–350ms
```

---

## 22.2 Hover Animation

Cards:

```text
translateY(-2px to -3px)
```

Buttons:

```text
small shadow increase
subtle background transition
```

Links:

```text
arrow shifts slightly
```

---

## 22.3 Page Entrance

Use subtle fade/translate transitions where appropriate:

```text
opacity: 0 → 1
translateY: 8px → 0
```

Avoid making every element animate independently.

---

## 22.4 Mobile Menu

Use:

```text
opacity
transform
height/visibility
```

with a short transition.

---

## 22.5 Accessibility

Respect:

```text
prefers-reduced-motion
```

When reduced motion is requested:

- minimize transitions
- disable decorative entrance animations
- keep functional state changes understandable

---

# 23. Responsive Breakpoints

Use a simple breakpoint system.

```text
Mobile:      < 640px
Tablet:      640px–1023px
Desktop:     1024px+
Large:       1280px+
```

The exact CSS implementation can use a small number of media queries.

Do not create a different design for every device width.

---

# 24. Responsive Component Rules

## Header

Desktop:

```text
Horizontal navigation
```

Mobile:

```text
Hamburger navigation
```

## Card grids

Desktop:

```text
3–4 columns
```

Tablet:

```text
2 columns
```

Mobile:

```text
1 column
```

## Buttons

Desktop:

```text
inline
```

Mobile:

```text
stack when necessary
full-width when appropriate
```

## Forms

Desktop:

```text
Two-column where appropriate
```

Mobile:

```text
Single-column
```

---

# 25. Page-Specific UI Direction

## Home

Visual priority:

```text
Hero
↓
Quick Access
↓
Popular Departments
↓
Student Services Preview
↓
Contact CTA
↓
Footer
```

The Home page should be the most visually expressive screen.

---

## Departments

Visual priority:

```text
Page Hero
↓
Department Grid
↓
Footer
```

Avoid unnecessary filters or dashboards.

---

## Courses

Visual priority:

```text
Page Hero
↓
Search + Filter
↓
Course Grid
↓
Footer
```

The search/filter area is the key interactive component.

---

## Student Services

Visual priority:

```text
Page Hero
↓
Service Grid
↓
Footer
```

Use clear service categories and concise descriptions.

---

## Contact

Visual priority:

```text
Page Hero
↓
Contact Information + Enquiry Form
↓
Footer
```

The form should be the main interactive focus.

---

# 26. Content Density

CampusConnect should feel spacious.

Avoid:

- giant tables
- dense dashboard layouts
- long paragraphs
- excessive badges
- excessive metadata
- unnecessary filters
- sidebar navigation
- charts
- statistics dashboards

This is a university information portal, not an admin dashboard.

---

# 27. Things AI Must NOT Add

This section is critical.

Do **NOT** introduce:

- Login
- Signup
- User profiles
- Student dashboard
- Admin dashboard
- Notifications center
- Chat system
- Calendar
- Events page
- News page
- Blog
- Admissions portal
- Fee payment
- Attendance
- Results
- GPA calculator
- Real-time messaging
- Database UI
- Dark mode
- Language selector
- Social feed
- AI chatbot
- Maps section
- Extra navigation pages
- Extra major sections not specified in `IDEA.md`

unless explicitly approved later.

---

# 28. AI Generation Rules

## 28.1 Preserve the Design System

Every generated screen must reuse:

- same header
- same navigation
- same typography
- same container width
- same buttons
- same card style
- same border radius
- same shadows
- same color roles
- same spacing system
- same footer

---

## 28.2 Do Not Reinvent Existing Components

If the Home page establishes a button style, every other page must use that exact visual language.

If the Departments page establishes the card style, Courses and Services must use the same base card language.

---

## 28.3 No Scope Expansion

AI must not invent additional product features.

If a design idea is not explicitly required by `IDEA.md` or `DESIGN.md`, do not add it.

---

## 28.4 Realistic Content

Use realistic prototype university content.

Avoid:

```text
Lorem ipsum
Test Test Test
Random Company
Generic SaaS copy
```

Use CampusConnect-specific content.

---

# 29. Screen Generation Order

To maximize consistency, screens should be generated in this order:

### 1. Home

Establish:

- header
- navigation
- hero
- buttons
- cards
- spacing
- footer

### 2. Departments

Reuse the established design system.

### 3. Courses

Reuse the same system and add search/filter.

### 4. Student Services

Reuse the card system.

### 5. Contact

Reuse forms/buttons and establish validation states.

### 6. Mobile variants

Validate responsive versions after desktop direction is approved.

---

# 30. MASTER CLAUDE / STITCH PROMPT

Use the following as the primary design-generation prompt.

```text
PROJECT: CampusConnect — A Mini University Web Portal

ROLE:
Act as a senior product designer and UI/UX designer creating a polished, modern university web portal. Design the interface for a real student-facing university information website, not a SaaS dashboard.

SOURCE OF TRUTH:
Use the provided IDEA.md and DESIGN.md as the authoritative product and visual specifications.

IMPORTANT:
Do not invent new product features.
Do not expand the information architecture.
Do not add pages that are not specified.
Do not add login, signup, dashboard, chatbot, events, news, payments, student records, admin tools, or other unrelated functionality.

TECHNOLOGY TARGET:
The final implementation will use only:
- HTML5
- CSS3
- Vanilla JavaScript

DESIGN GOAL:
Create a clean, modern, professional, student-friendly university website with excellent visual hierarchy, generous whitespace, strong typography, subtle interactions, and highly consistent components.

PRODUCT:
CampusConnect helps students quickly find:
- Academic departments
- Courses/programs
- Student services
- Contact information

REQUIRED SCREENS:
1. Home
2. Departments
3. Courses
4. Student Services
5. Contact

GLOBAL NAVIGATION:
CampusConnect | Home | Departments | Courses | Student Services | Contact

DESIGN LANGUAGE:
- Modern university portal
- Professional
- Minimal
- Calm
- Premium but not flashy
- Information-first
- Spacious
- Highly readable
- Responsive

COLOR SYSTEM:
Use the exact color roles defined in DESIGN.md.
Do not invent a new palette for individual screens.

TYPOGRAPHY:
Use one clean modern sans-serif family consistently.
Follow the typography scale defined in DESIGN.md.
Do not change typography between screens.

LAYOUT:
Use a centered max-width content container around 1200px.
Use generous horizontal padding.
Maintain consistent vertical rhythm and section spacing.
Use responsive grids that transition from desktop to tablet to mobile.

COMPONENT CONSISTENCY:
Reuse the exact same:
- Header
- Navigation
- Buttons
- Cards
- Inputs
- Form controls
- Footer
- Spacing
- Border radii
- Shadows
- Icon treatment

HEADER:
White, clean, compact navigation bar.
Brand on the left.
Navigation on the right on desktop.
Hamburger menu on mobile.
Clearly indicate the active page.
Use a subtle border/divider.

BUTTONS:
Use the DESIGN.md button system.
Primary CTA uses the primary blue.
Secondary CTA is white with a subtle border.
Use subtle hover transitions only.
Do not use oversized pill buttons.

CARDS:
White surfaces, subtle border, moderate corner radius, restrained shadow.
Use consistent padding and typography.
On hover, cards may rise 2–3px with a subtle shadow increase.

ANIMATION:
Use light 120–350ms transitions.
Use subtle hover states.
Use restrained page entrance transitions.
Respect prefers-reduced-motion.
No flashy animations.

ACCESSIBILITY:
Use semantic structure.
Maintain readable contrast.
Provide visible focus states.
Use proper labels.
Do not rely on color alone for validation.

HOME SCREEN:
Create:
- Global header
- Hero section
- Headline: "Your Campus. Your Opportunities."
- Supporting text explaining CampusConnect
- Primary CTA: "Explore Departments"
- Secondary CTA: "View Courses"
- Quick Access cards for Departments, Courses, Student Services, Contact
- Popular Departments section
- Student Services preview
- Contact CTA
- Footer

DEPARTMENTS SCREEN:
Create:
- Same global header
- Page hero titled "Academic Departments"
- Concise supporting description
- Responsive department card grid
- Departments:
  Computer Science
  Software Engineering
  Information Technology
  Electrical Engineering
  Business Administration
  Mathematics
- Same global footer

COURSES SCREEN:
Create:
- Same global header
- Page hero titled "Courses & Programs"
- Search input
- Department/category filter
- Responsive course card grid
- Example programs:
  BS Computer Science
  BS Software Engineering
  BS Information Technology
  BBA
- Same footer

STUDENT SERVICES SCREEN:
Create:
- Same global header
- Page hero titled "Student Services"
- Responsive service card grid
- Academic Advising
- Library
- Career Services
- Student Affairs
- IT Support
- Admissions
- Same footer

CONTACT SCREEN:
Create:
- Same global header
- Page hero titled "Contact CampusConnect"
- Contact information area
- Student Enquiry form
- Fields:
  Full Name
  Email
  Subject
  Message
- Send Enquiry primary button
- Inline validation/error states
- Inline success message
- Same footer

VALIDATION STATES:
Design:
- Default input
- Focused input
- Invalid input
- Valid/success state
- Form-level error
- Successful submission message

ERROR COPY:
"Please enter your name."
"Please enter a valid email address."
"Please enter a subject."
"Please enter your message."
"Please correct the highlighted fields."

SUCCESS COPY:
"Your enquiry has been submitted successfully."

RESPONSIVE BEHAVIOR:
Desktop:
- Horizontal navigation
- Multi-column grids
- Spacious layouts

Tablet:
- Reduced columns
- Adjusted spacing

Mobile:
- Hamburger navigation
- Single-column cards
- Stacked forms
- Full-width controls where appropriate
- No horizontal overflow

IMPORTANT VISUAL CONSTRAINT:
Do not turn CampusConnect into an admin dashboard.
Do not add sidebars.
Do not create a dark theme.
Do not use excessive gradients.
Do not use oversized illustrations.
Do not add unnecessary statistics or charts.
Do not add unrequested features.

OUTPUT:
Generate a high-fidelity desktop-first web UI that can later be implemented faithfully using HTML, CSS, and Vanilla JavaScript.
Prioritize exact component consistency and realistic university content.
```

---

# 31. STITCH-SPECIFIC GENERATION STRATEGY

Stitch should be used incrementally rather than asking it to invent the entire project in one generation.

The current Stitch guidance recommends starting with a clear high-level concept and then refining screen-by-screen; specific incremental prompts generally provide better control than combining many unrelated changes. citeturn0search2turn0search4

Stitch also now supports `DESIGN.md` as an agent-friendly design-system format for carrying design rules between design and coding tools. citeturn0search1

Therefore:

### Step 1

Create the project/design system first.

### Step 2

Generate Home.

### Step 3

Approve Home.

### Step 4

Use the approved Home as the visual reference for the other pages.

### Step 5

Generate Departments.

### Step 6

Generate Courses.

### Step 7

Generate Student Services.

### Step 8

Generate Contact.

### Step 9

Generate responsive variants.

### Step 10

Polish one issue at a time.

Do not ask Stitch to redesign the entire website repeatedly.

---

# 32. SCREEN-SPECIFIC STITCH PROMPTS

## Home Prompt

```text
Design the CampusConnect Home page using the existing CampusConnect design system.

PLATFORM:
Responsive web, desktop-first with tablet and mobile behavior.

PAGE STRUCTURE:
1. Header:
   Use the exact CampusConnect global header and navigation from the design system.

2. Hero:
   Large but controlled headline:
   "Your Campus. Your Opportunities."
   Supporting text explaining that CampusConnect helps students explore departments, courses, student services, and contact information.
   Primary CTA: "Explore Departments"
   Secondary CTA: "View Courses"

3. Quick Access:
   Four consistent cards:
   Departments
   Courses
   Student Services
   Contact

4. Popular Departments:
   Display a clean responsive card grid for:
   Computer Science
   Software Engineering
   Information Technology
   Electrical Engineering

5. Student Services Preview:
   Display concise cards for:
   Academic Advising
   Library
   Career Services
   IT Support

6. Contact CTA:
   A restrained final call-to-action encouraging students to contact CampusConnect.

7. Footer:
   Use the exact global footer.

VISUAL:
Clean, modern, academic, spacious, information-first.
Use the existing CampusConnect design system without inventing new colors, typography, card styles, or button styles.

DO NOT:
Add statistics, charts, login, dashboard, events, news, chatbot, or additional pages.
```

---

## Departments Prompt

```text
Create the CampusConnect Departments page.

Reuse the exact visual system, header, navigation, container, typography, buttons, card styling, spacing, icons, and footer from the approved CampusConnect Home screen.

STRUCTURE:
1. Global header
2. Page hero:
   Title: "Academic Departments"
   Short supporting description.
3. Responsive department card grid:
   - Computer Science
   - Software Engineering
   - Information Technology
   - Electrical Engineering
   - Business Administration
   - Mathematics
4. Global footer

The department cards should use the same base card component established on the Home page.

Do not introduce filters, sidebars, dashboards, statistics, or unrelated sections.
```

---

## Courses Prompt

```text
Create the CampusConnect Courses & Programs page.

Reuse the exact approved CampusConnect design system and global components.

STRUCTURE:
1. Global header
2. Page hero:
   Title: "Courses & Programs"
3. Search/filter controls:
   - Search courses input
   - Department/category selector
4. Course grid:
   - BS Computer Science
   - BS Software Engineering
   - BS Information Technology
   - BBA
5. Each course card should show:
   Program name
   Department
   Duration
   Short description
   Explore action
6. Empty search state
7. Global footer

The search/filter controls should visually match the Contact form controls.

Do not add enrollment, fees, GPA, student dashboard, or registration functionality.
```

---

## Student Services Prompt

```text
Create the CampusConnect Student Services page.

Reuse the exact approved CampusConnect global design system.

STRUCTURE:
1. Global header
2. Page hero:
   Title: "Student Services"
   Short supporting description.
3. Responsive service card grid:
   - Academic Advising
   - Library
   - Career Services
   - Student Affairs
   - IT Support
   - Admissions
4. Global footer

Use the same card component established on the Home and Departments screens.

Do not add appointment booking, chat, calendars, notifications, or student accounts.
```

---

## Contact Prompt

```text
Create the CampusConnect Contact page.

Reuse the exact approved CampusConnect design system, header, navigation, typography, buttons, cards, inputs, spacing, and footer.

STRUCTURE:
1. Global header
2. Page hero:
   Title: "Contact CampusConnect"
3. Contact information section:
   Campus address
   Phone
   Email
   Office hours
4. Student Enquiry form:
   Full Name
   Email
   Subject
   Message
   Send Enquiry button
5. Show the designed states for:
   Default input
   Focused input
   Invalid input
   Form-level error
   Successful submission
6. Global footer

VALIDATION MESSAGES:
"Please enter your name."
"Please enter a valid email address."
"Please enter a subject."
"Please enter your message."
"Please correct the highlighted fields."

SUCCESS:
"Your enquiry has been submitted successfully."

Do not add a backend, login, user account, map integration, chatbot, or extra contact functionality.
```

---

# 33. REFINEMENT PROMPT TEMPLATE

After generating a screen, use focused prompts rather than asking the AI to redesign everything.

```text
Keep the entire existing CampusConnect design unchanged.

Only modify:
[EXACT COMPONENT]

Change:
[EXACT CHANGE]

Do not change:
- Header
- Navigation
- Typography
- Color palette
- Container width
- Card styles
- Button styles
- Footer
- Other sections

Preserve all existing content and layout relationships.
```

---

# 34. CONSISTENCY AUDIT PROMPT

Use after all screens are generated:

```text
Audit the CampusConnect screens against DESIGN.md.

Do not redesign the product.

Check only for visual consistency across screens:

- Header height and structure
- Logo/brand position
- Navigation position
- Active navigation state
- Container width
- Horizontal padding
- Typography scale
- Heading weights
- Button height
- Button radius
- Card radius
- Card padding
- Border treatment
- Shadow intensity
- Input styling
- Section spacing
- Footer structure
- Responsive behavior

Identify inconsistencies first.

Do not introduce new components or features.
Do not change the established design direction.
```

---

# 35. FINAL DESIGN APPROVAL CHECKLIST

Before implementation begins, every screen must pass:

## Visual

- [ ] Looks like CampusConnect
- [ ] Consistent palette
- [ ] Consistent typography
- [ ] Consistent spacing
- [ ] Consistent cards
- [ ] Consistent buttons
- [ ] Consistent header
- [ ] Consistent footer

## UX

- [ ] Information is easy to find
- [ ] Primary action is obvious
- [ ] Navigation is clear
- [ ] Forms are understandable
- [ ] Error messages are clear
- [ ] Success feedback is clear

## Responsive

- [ ] Desktop approved
- [ ] Tablet approved
- [ ] Mobile approved
- [ ] No horizontal overflow
- [ ] Navigation works on mobile
- [ ] Cards stack correctly
- [ ] Forms stack correctly

## Scope

- [ ] No extra pages
- [ ] No extra product features
- [ ] No dashboard
- [ ] No authentication
- [ ] No backend UI
- [ ] No unnecessary visual complexity

---

# 36. Design Lock

Once the UI screens are approved, the following should be treated as locked:

- Color palette
- Typography
- Header
- Navigation
- Footer
- Container width
- Spacing scale
- Button styles
- Card styles
- Form styles
- Error/success states
- Animation behavior
- Responsive breakpoints
- Icon style

Any later visual change should be intentional and applied consistently across all affected screens.

---

# 37. Implementation Handoff

After visual approval, the approved UI should be translated into:

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

The implementation must reproduce the approved design using only:

```text
HTML5
CSS3
Vanilla JavaScript
```

No UI framework should be introduced unless the project specification is explicitly changed.

---

## End of DESIGN.md
