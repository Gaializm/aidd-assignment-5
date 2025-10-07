# AI Development Notes

## Prompt Log Entries

### Entry 1: Initial Website Structure Creation
**Prompt**: I knew I would have to personalize the website and likely debug and tweak the code with more prompts, so I set out to try to build a comprehensive prompt that would build the base for all my pages fairly close to final specifications in one attempt based on my prior web development experience. The lengthy prompt I built for this and that I started my session with was the following:

*******************************************************************************
ROLE
You are a senior front-end dev. Generate a COMPLETE, STATIC multi-page personal website repo (no frameworks; optional Bootstrap via CDN). Keep code simple and class-friendly.

SCOPE (STRICT)
- Pure HTML5 + CSS3 + tiny JS for form validation hints + thank-you redirect.
- Optional: Bootstrap 5 from CDN for grid/utilities only.
- No React, no build tools, no SPA/routers, no backend.

DESIGN GUIDELINES
- Color theme: blue primary with tasteful white and brown accents (define CSS vars).
- Non-default font: import one Google Font (e.g., "Inter" or "Poppins").
- “Feels like a React site” visually (cards, spacing, chips, sticky header), but implemented with plain HTML/CSS.
- Minimize scrolling: tight sections, above-the-fold summaries, compact cards; enable smooth scrolling.
- Responsive: mobile-first, fluid grid; max-width container ~72rem.
- Accessibility: semantic landmarks, visible focus, labels tied to inputs, alt text on images.

FILES / STRUCTURE
/
├─ index.html
├─ about.html
├─ resume.html
├─ projects.html
├─ contact.html
├─ thankyou.html
├─ styles.css
├─ script.js
├─ README.md
├─ .gitignore
├─ .prompt/
│  └─ dev_notes.md
└─ images/
  

NAV & LAYOUT (CONSISTENT)
- Sticky header with brand “Gaializ Mejias Gonzalez” and compact nav (Home, About, Resume, Projects, Contact).
- Active link highlighting based on current page.
- Footer: © {currentYear} • Built with HTML & CSS • GitHub link.

PAGE CONTENT (USE THESE LINKS & COPY PLACEHOLDERS)
1) index.html
   - Hero (name + short tagline: “Web Programming & MSIS — Portfolio”), two CTAs: View Projects, Contact.
   - Three compact cards linking to About, Resume, Projects (minimize scroll).
2) about.html
   - Headshot: images/gaia-headshot.jpg (alt: “Gaia Mejias professional headshot”).
   - Short bio paragraph, skill chips (HTML, CSS, JS, Python, SQL, Tableau, etc.).
   - Link out to LinkedIn: https://www.linkedin.com/in/gaializm/
3) resume.html
   - Clean HTML resume sections (Summary, Education, Experience, Skills, Awards).
   - Button: “Open PDF Resume” → ./docs/MejiasGonzalez_Gaializ_Resume_MSIS.pdf (create docs/ folder and link; include a short note that this is a copy of the PDF.)
4) projects.html
   - Two+ project cards, each with title, role, tech tags, 2–3 bullets, thumbnail, and buttons:
     • “Puerto Rican Diaspora — Tableau” → https://public.tableau.com/app/profile/gaializ.mejias.gonzalez/viz/AnExaminationofthePuertoRicanDiasporabyEducationalAttainmentOverview/StatesOverviewDashboard
     • “Portfolio Project — Case Study” → https://gaializm.github.io/PortfolioProject/#/projects/1
     • “Past Work (Weebly)” → https://gaializm.weebly.com/past-work.html
   - Keep cards compact; use grid; avoid long scroll by collapsing descriptions to 2–3 lines max.
5) contact.html
   - Contact info block (email, LinkedIn, GitHub placeholder).
   - REQUIRED FORM (meets assignment spec):
     * firstName (required)
     * lastName (required)
     * email (type=email, required)
     * password (required, minlength=8)
     * confirmPassword (required; must match)
   - All inputs have <label for="..."> and helper text regions (aria-live="polite").
   - On valid submit, preventDefault and redirect to thankyou.html.
6) thankyou.html
   - Friendly success message + “Back to Home” button.

TECHNICAL DETAILS
- styles.css:
  :root color vars (e.g., --blue-600, --brown-400, --bg, --text, --muted).
  System font fallback + Google Font import.
  Container, grid utilities, card, chip, button styles.
  Sticky header shadow; focus-visible outlines; reduced-motion respect.
- script.js:
  addActiveNav() based on location.pathname.
  Password/confirm live match message.
  Form submit handler: if valid & matching, redirect to thankyou.html.
- Optional Bootstrap:
  If used, limit to grid/utilities; do NOT rely on JS components. Keep classes readable.
- README.md:
  How to open locally, how to replace headshot & resume, how to validate HTML/CSS, and how to zip + submit.
- .gitignore:
  OS junk files, /docs/*.pdf (except the resume you include), zips.
- .prompt/dev_notes.md:
  Three prompt log entries (Prompt / AI Output Summary / Accepted-Modified-Rejected + Why) and a ~150-word reflection on AI help, mistakes, and your oversight.

CONTENT SEEDS (EDITABLE)
- Name: “Gaializ Mejias Gonzalez”
- Tagline: “Web Programming & MSIS — Portfolio”
- Bio snippet: short paragraph about Purdue BS in Web Programming & Design; IU Kelley MSIS; interests in enterprise systems, data viz, and accessible UX.
- Skills list: HTML, CSS, JavaScript, Python, SQL, Tableau, Bootstrap.
- External links:
  • Past Portfolio React Site Project (hosted on github): @https://gaializm.github.io/PortfolioProject/  
  • Tableau Dashboard Case Study Project: @https://public.tableau.com/app/profile/gaializ.mejias.gonzalez/viz/AnExaminationofthePuertoRicanDiasporabyEducationalAttainmentOverview/StatesOverviewDashboard 
  • Tableau viz: (link above)
  • Weebly past work: @https://gaializm.weebly.com/past-work.html 
  • LinkedIn: @https://www.linkedin.com/in/gaializm/ 

QUALITY / CHECKS (ALIGN TO ASSIGNMENT)
- Multi-page with consistent nav & semantic landmarks.
- Responsive layout; minimal scrolling; smooth scrolling behavior.
- Accessible labels, alt text, and visible focus states.
- Contact form fields & constraints exactly as specified; thank-you redirect works.
- Log AI prompts in .prompt/dev_notes.md.
*******************************************************************************

**AI Output Summary**: The AI created the complete HTML structure for all 6 pages (index, about, resume, projects, contact, thankyou) with proper semantic HTML, navigation, and content placeholders. Each page included proper meta tags, Google Fonts integration, and consistent structure. The AI also created a comprehensive CSS file with CSS custom properties for the blue/brown color theme, responsive grid layouts, modern typography using Inter font, accessibility features, and mobile-first responsive design. Included hover effects, transitions, and proper focus states.

**Accepted/Modified/Rejected**: **Accepted & Modified** - The HTML structure was exactly what was needed with proper semantic elements, accessibility features, and consistent navigation across all pages. The CSS implementation was excellent with proper color variables, responsive design, accessibility features, and modern styling that "feels like a React site" as requested. Still, stepping through the site the image imports were generic or placeholders and the AI originally went for validation by creating a javascript file. I went on to prompt it further to adjust this output as I will detail below. 


**Why**: The AI correctly implemented the multi-page structure with proper HTML5 semantic elements, included all required content sections, and maintained consistency across pages. The navigation structure was clean and the content placeholders were appropriate. The styling was in line with what I had in mind and any issues with the output code were easily fixable. For these reasons I kept most of the code, but I needed to modify it and remove the javascript file in order to ensure the validation remained HTML & CSS only as expected for class.


---

### Entry 2: JavaScript Removal and HTML5-Only Validation Part 1
**Prompt**: "Can you get rid of the javascript and just do basic client-side validation through the html & css? This assignment should essentially only be static html & CSS"

**AI Output Summary**: The AI removed the JavaScript file entirely and updated all HTML files to remove script references. Updated the contact form to use HTML5 validation attributes (required, minlength, type="email") and changed the form action to redirect to thankyou.html. Added CSS-only validation styling to show visual feedback for valid/invalid form states. Updated README to reflect the static nature of the website.

**Accepted/Modified/Rejected**: **Modified** - The Javascript file was removed and the HTML code was updated, but for some reason it would still allow submission of the form with invalid fields and would not display the validation messages. 

**Why**: The AI correctly deleted the file it was asked to and updated the code, but it did not take any further action to verify or resolve the issue with the HTML validation.

---

### Entry 3: JavaScript Removal and HTML5-Only Validation Part 2
**Prompt**: "The html validation still lets me submit without populating any error messages, help me fix that?"

**AI Output Summary**: The AI identified that the form validation wasn't working because the `novalidate` attribute was preventing browser validation, and the form was using `method="get"` which can bypass some validation. The AI removed the `novalidate` attribute, added `pattern` attributes for better validation (names must be letters only, passwords must be at least 8 characters), added descriptive `title` attributes for better error messages, and enhanced CSS validation styling to show visual feedback. The AI also added form-level validation styling to disable the submit button when the form is invalid.

**Accepted/Modified/Rejected**: **Accepted** - The AI correctly identified the root cause of the validation issue and implemented a comprehensive solution using pure HTML5 validation attributes and CSS styling. The form now properly validates all fields and shows browser-native error messages.

**Why**: The AI demonstrated good debugging skills by identifying that the `novalidate` attribute was the main issue preventing validation from working. The solution maintains the static HTML/CSS requirement while providing robust form validation through HTML5 attributes and visual feedback through CSS.

## Reflection on AI Assistance

### Where AI Helped Save Time
AI was incredibly helpful in scaffolding the entire website structure quickly and efficiently. The AI generated clean, semantic HTML for all 6 pages in minutes, created a comprehensive CSS system with proper color variables and responsive design, and initially implemented JavaScript functionality for form validation and navigation. When I requested to remove JavaScript for a truly static site, the AI quickly converted the form validation to use HTML5 attributes and CSS-only styling. This would have taken hours to code manually, especially the CSS custom properties system and responsive grid layouts.

### Where AI Made Mistakes
The AI initially had some issues with the write tool syntax, forgetting to include the file_path parameter in several calls. This required me to correct the tool calls and re-run them. Additionally, the AI created placeholder image files as HTML comments rather than actual image files. The initial JavaScript implementation was more complex than needed for the assignment requirements. Most significantly, when I first requested to remove JavaScript, the AI removed the file but didn't properly test or debug the resulting HTML5 validation, leaving the form non-functional until I prompted it again to fix the validation issues.


### Balancing AI Assistance with Personal Coding
I maintained critical oversight by reviewing all generated code for correctness, accessibility, and adherence to the assignment requirements. While the AI provided excellent scaffolding, I ensured that the content was personalized for myself, that all accessibility features were properly implemented, and that the form validation met the exact specifications. It was only able to make this scaffolding so close to the final specifications because I also had the language and terminology and gave it a specific enough starting prompt to achieve this output. When I realized the assignment should be purely static HTML/CSS, I requested the AI to remove JavaScript and convert to HTML5 validation, which it had some issues doing initially. The JavaScript removal process required multiple iterations. first the AI removed the file but left the form non-functional, then when I reported the validation wasn't working, it properly debugged the issue by identifying the `novalidate` attribute as the problem and implementing comprehensive HTML5 validation with pattern attributes and CSS styling. This iterative process highlighted the importance of testing AI-generated code and being specific about requirements. The AI's debugging skills improved with each prompt, showing it could learn from context and previous issues. In the end, this collaboration allowed me to create a professional-quality static website efficiently while maintaining full control over the final product.
