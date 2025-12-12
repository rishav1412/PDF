# UI Prompt Template

Use this template to create comprehensive, actionable UI prompts from design screenshots. Copy the template below and fill in each section with details from your design.

---

## 📋 Template Structure

```markdown
# UI Component/Screen Name: [Name Here]

## 1. Overview
**Purpose:** [What this UI component/screen does]
**Type:** [e.g., Login Screen, Dashboard, Navigation Menu, Form, Card Component]
**Platform/Framework:** [e.g., Web, iOS, Android, React, Vue, etc.]

## 2. Layout & Structure

### Overall Layout
- **Container:** [Describe outer container - full width, centered, max-width, etc.]
- **Layout Type:** [Flexbox, Grid, Stack, etc.]
- **Orientation:** [Vertical, Horizontal, Mixed]
- **Alignment:** [Center, Left, Right, Space-between, etc.]
- **Dimensions:** [Width, Height - use specific values or relative units]

### Visual Hierarchy
- **Primary Focus:** [Main element that draws attention]
- **Secondary Elements:** [Supporting elements]
- **Spacing/Padding:**
  - Container padding: [e.g., 24px all sides]
  - Element spacing: [e.g., 16px gap between items]
  - Section margins: [e.g., 48px between sections]

### Grid/Layout System
- **Columns:** [Number of columns, if applicable]
- **Rows:** [Number of rows, if applicable]
- **Gaps:** [Gutter sizes between grid items]
- **Breakpoints:** [Responsive breakpoints if applicable]

## 3. Colors & Styling

### Color Palette
- **Primary Color:** [Hex/RGB value and usage - e.g., #3B82F6 for buttons]
- **Secondary Color:** [Hex/RGB value and usage]
- **Background:** [Color and gradient details]
- **Text Colors:**
  - Primary text: [e.g., #1F2937 - dark gray]
  - Secondary text: [e.g., #6B7280 - medium gray]
  - Accent/Link text: [e.g., #3B82F6 - blue]
- **Border Colors:** [Colors used for borders, dividers]
- **Status Colors:**
  - Success: [e.g., #10B981 - green]
  - Error: [e.g., #EF4444 - red]
  - Warning: [e.g., #F59E0B - yellow]
  - Info: [e.g., #3B82F6 - blue]

### Visual Effects
- **Shadows:** [Box shadows, text shadows - e.g., "subtle shadow: 0 1px 3px rgba(0,0,0,0.1)"]
- **Borders:** [Border width, style, radius - e.g., "1px solid #E5E7EB, 8px radius"]
- **Opacity:** [Any transparency effects]
- **Gradients:** [Gradient definitions if used]
- **Backdrop Effects:** [Blur, overlays, etc.]

## 4. Typography

### Font Families
- **Primary Font:** [e.g., Inter, Roboto, San Francisco]
- **Secondary Font:** [If applicable - monospace, serif, etc.]
- **Fallbacks:** [System font fallbacks]

### Text Styles

**Headings:**
- H1: [Font size, weight, line height, color - e.g., "32px, 700 weight, 1.2 line-height, #1F2937"]
- H2: [e.g., "24px, 600 weight, 1.3 line-height, #1F2937"]
- H3: [e.g., "20px, 600 weight, 1.4 line-height, #374151"]

**Body Text:**
- Regular: [e.g., "16px, 400 weight, 1.5 line-height, #4B5563"]
- Small: [e.g., "14px, 400 weight, 1.5 line-height, #6B7280"]
- Caption: [e.g., "12px, 400 weight, 1.4 line-height, #9CA3AF"]

**Special Text:**
- Links: [e.g., "16px, 500 weight, #3B82F6, underline on hover"]
- Labels: [e.g., "14px, 500 weight, #374151, uppercase"]
- Buttons: [e.g., "16px, 600 weight, white, centered"]

### Text Formatting
- **Letter Spacing:** [If applicable]
- **Text Transform:** [Uppercase, lowercase, capitalize]
- **Text Decoration:** [Underline, strikethrough]
- **Text Alignment:** [Left, center, right, justify]

## 5. Components & Elements

### [Component Name 1] (e.g., Input Fields)
- **Type:** [Text input, number input, email, password, etc.]
- **Size:** [Width, height - e.g., "full width, 44px height"]
- **Styling:**
  - Border: [e.g., "1px solid #D1D5DB, 6px border-radius"]
  - Background: [e.g., "white (#FFFFFF)"]
  - Padding: [e.g., "12px horizontal, 10px vertical"]
  - Font: [e.g., "16px, #1F2937"]
- **Placeholder:** [Placeholder text style and color]
- **Icon:** [If includes icon - position, size, color]
- **Label:** [Associated label styling and position]

### [Component Name 2] (e.g., Buttons)
- **Type:** [Primary, secondary, tertiary, icon button, etc.]
- **Size:** [Width, height, padding]
- **Styling:**
  - Background: [Color]
  - Text: [Color, size, weight]
  - Border: [If applicable]
  - Border-radius: [Corner rounding]
  - Shadow: [If applicable]
- **States:** [See Interactive States section]

### [Component Name 3] (e.g., Cards)
- **Dimensions:** [Width, height, or aspect ratio]
- **Layout:** [Internal layout structure]
- **Background:** [Color or image]
- **Border/Shadow:** [Edge styling]
- **Content Structure:** [How content is arranged inside]
- **Padding:** [Internal spacing]

### [Additional Components]
[Repeat pattern above for each unique component type]

## 6. Interactions & States

### Interactive Elements

**Buttons:**
- **Default:** [Background, text, border colors]
- **Hover:** [Changes on mouse hover - e.g., "background darkens to #2563EB"]
- **Active/Pressed:** [Changes when clicking - e.g., "background darkens further, slight scale down"]
- **Focus:** [Keyboard focus state - e.g., "2px blue ring around button"]
- **Disabled:** [Non-interactive state - e.g., "gray background, 50% opacity"]

**Input Fields:**
- **Default:** [Normal appearance]
- **Focus:** [When clicked/selected - e.g., "blue border, subtle shadow"]
- **Filled:** [With content entered]
- **Error:** [Invalid input - e.g., "red border, error message below"]
- **Disabled:** [Non-editable state]

**Links:**
- **Default:** [Standard appearance]
- **Hover:** [Mouse over - e.g., "underline appears"]
- **Visited:** [Already clicked - if applicable]
- **Active:** [While clicking]

### Animations & Transitions
- **Hover Transitions:** [e.g., "all properties 200ms ease-in-out"]
- **Page Transitions:** [Fade, slide, etc.]
- **Loading States:** [Spinners, skeletons, progress bars]
- **Micro-interactions:** [Button ripples, checkbox checks, etc.]

### User Feedback
- **Success Messages:** [Appearance and position]
- **Error Messages:** [Appearance and position]
- **Validation:** [When and how validation occurs]
- **Loading Indicators:** [Spinners, progress bars, skeletons]
- **Tooltips:** [Hover information, styling]

## 7. Responsive Behavior

### Breakpoints
- **Mobile:** [< 640px - describe layout changes]
- **Tablet:** [640px - 1024px - describe layout changes]
- **Desktop:** [> 1024px - describe layout changes]
- **Large Desktop:** [> 1440px - if applicable]

### Layout Adaptations
- **Mobile Changes:**
  - [Stack columns vertically]
  - [Reduce padding/margins]
  - [Adjust font sizes]
  - [Hide/show specific elements]
  - [Navigation changes - hamburger menu, etc.]

- **Tablet Changes:**
  - [Adjust grid columns]
  - [Moderate spacing]
  - [Component size adjustments]

- **Desktop Changes:**
  - [Multi-column layouts]
  - [Larger spacing]
  - [Show all navigation]
  - [Enhanced hover states]

### Touch vs. Mouse Considerations
- **Touch Targets:** [Minimum 44px x 44px for mobile]
- **Hover States:** [Desktop only or touch alternatives]
- **Gestures:** [Swipe, pinch, etc. for mobile]

## 8. Accessibility Considerations

- **Semantic HTML:** [Use of proper tags - button, nav, main, etc.]
- **ARIA Labels:** [Screen reader descriptions]
- **Keyboard Navigation:** [Tab order, keyboard shortcuts]
- **Focus Indicators:** [Visible focus states]
- **Color Contrast:** [WCAG compliance level]
- **Alternative Text:** [Image alt text]
- **Form Labels:** [Proper input associations]

## 9. Additional Details

### Icons
- **Icon Library:** [e.g., Heroicons, Font Awesome, Material Icons]
- **Icon Style:** [Outline, solid, two-tone]
- **Icon Sizes:** [Consistent sizing - e.g., 20px, 24px]
- **Icon Colors:** [Match text or custom colors]

### Images/Media
- **Image Types:** [Photos, illustrations, avatars]
- **Aspect Ratios:** [16:9, 1:1, 4:3, etc.]
- **Object Fit:** [Cover, contain, fill]
- **Placeholders:** [Loading state for images]

### Special Features
- **Modals/Dialogs:** [Overlay, centered, backdrop]
- **Dropdowns:** [Menu styling, positioning]
- **Tabs:** [Active/inactive states]
- **Accordions:** [Expand/collapse behavior]
- **Date Pickers:** [Calendar styling]
- **File Uploads:** [Drag-and-drop areas]

## 10. Implementation Notes

### Technical Considerations
- **CSS Framework:** [If recommending - Tailwind, Bootstrap, etc.]
- **Component Library:** [If using - Material-UI, Chakra, etc.]
- **Browser Support:** [Compatibility requirements]
- **Performance:** [Optimization notes]

### Edge Cases
- **Empty States:** [What shows when no data]
- **Long Content:** [Text overflow, truncation]
- **Loading States:** [Initial load appearance]
- **Error States:** [Failed data loading]
- **Offline:** [Behavior without connection]

### Dependencies
- **Required Assets:** [Fonts, icons, images]
- **External Libraries:** [Third-party tools needed]
- **API Integration:** [Data requirements]

---

## ✅ Completion Checklist

Before finalizing your prompt, verify you've covered:

- [ ] Overall layout and structure clearly described
- [ ] All colors specified with exact values
- [ ] Typography fully detailed (sizes, weights, heights)
- [ ] All UI components documented
- [ ] Interactive states described for all clickable elements
- [ ] Responsive behavior explained for all breakpoints
- [ ] Accessibility considerations included
- [ ] Edge cases and special states addressed
- [ ] Clear, specific language used throughout
- [ ] No ambiguous or subjective terms
```

---

## 📝 Example: Filled Template

Here's an example of how to use this template for a simple login screen:

```markdown
# UI Component/Screen Name: Login Screen

## 1. Overview
**Purpose:** User authentication screen for email/password login
**Type:** Login Screen / Authentication Form
**Platform/Framework:** Web (React with Tailwind CSS)

## 2. Layout & Structure

### Overall Layout
- **Container:** Centered card on page, max-width 400px
- **Layout Type:** Flexbox, vertical stack
- **Orientation:** Vertical
- **Alignment:** Center-aligned content
- **Dimensions:** 400px width, auto height, positioned vertically and horizontally center of viewport

### Visual Hierarchy
- **Primary Focus:** Login form card with white background
- **Secondary Elements:** "Forgot Password?" link and Sign Up CTA at bottom
- **Spacing/Padding:**
  - Container padding: 40px all sides
  - Element spacing: 20px gap between form elements
  - Section margins: 32px between form and footer links

### Grid/Layout System
- **Columns:** Single column layout
- **Rows:** Auto-flowing rows for form elements
- **Gaps:** 20px vertical gap between elements

## 3. Colors & Styling

### Color Palette
- **Primary Color:** #3B82F6 (blue) - used for primary button and links
- **Secondary Color:** #6B7280 (gray) - used for secondary text
- **Background:** #F9FAFB (light gray) - page background; #FFFFFF (white) - card background
- **Text Colors:**
  - Primary text: #111827 (almost black)
  - Secondary text: #6B7280 (medium gray)
  - Accent/Link text: #3B82F6 (blue)
- **Border Colors:** #E5E7EB (light gray)
- **Status Colors:**
  - Error: #EF4444 (red)

### Visual Effects
- **Shadows:** Card shadow: 0 4px 6px rgba(0,0,0,0.1)
- **Borders:** Input fields: 1px solid #E5E7EB, 6px border-radius
- **Opacity:** N/A
- **Gradients:** N/A

## 4. Typography

### Font Families
- **Primary Font:** Inter
- **Fallbacks:** system-ui, -apple-system, sans-serif

### Text Styles

**Headings:**
- H1: 28px, 700 weight, 1.2 line-height, #111827 - "Welcome Back"

**Body Text:**
- Regular: 16px, 400 weight, 1.5 line-height, #374151
- Small: 14px, 400 weight, 1.5 line-height, #6B7280

**Special Text:**
- Links: 14px, 500 weight, #3B82F6, underline on hover
- Labels: 14px, 500 weight, #374151
- Buttons: 16px, 600 weight, white

## 5. Components & Elements

### Input Fields
- **Type:** Email input (type="email"), Password input (type="password")
- **Size:** Full width (100%), 44px height
- **Styling:**
  - Border: 1px solid #E5E7EB, 6px border-radius
  - Background: #FFFFFF
  - Padding: 12px horizontal, 10px vertical
  - Font: 16px, #111827
- **Placeholder:** "Enter your email" / "Enter your password" - #9CA3AF color
- **Label:** Positioned above input, 14px, 500 weight, #374151, 8px margin-bottom

### Primary Button (Login Button)
- **Type:** Primary action button
- **Size:** Full width, 44px height
- **Styling:**
  - Background: #3B82F6 (blue)
  - Text: white, 16px, 600 weight
  - Border: none
  - Border-radius: 6px
  - Shadow: subtle - 0 1px 2px rgba(0,0,0,0.05)

### Link (Forgot Password)
- **Type:** Text link
- **Styling:** 14px, 500 weight, #3B82F6
- **Position:** Right-aligned, 12px below password field

## 6. Interactions & States

### Interactive Elements

**Buttons:**
- **Default:** Background #3B82F6, white text
- **Hover:** Background darkens to #2563EB, subtle scale (1.01)
- **Active/Pressed:** Background darkens to #1D4ED8
- **Focus:** 2px blue ring (#3B82F6) with 2px offset
- **Disabled:** Background #9CA3AF, cursor not-allowed

**Input Fields:**
- **Default:** 1px solid #E5E7EB border
- **Focus:** 2px solid #3B82F6 border, subtle blue shadow
- **Filled:** Maintains focus border while typing
- **Error:** 2px solid #EF4444 border, error message in red below
- **Disabled:** Background #F3F4F6, cursor not-allowed

**Links:**
- **Default:** #3B82F6, no underline
- **Hover:** #2563EB, underline appears
- **Active:** #1D4ED8

### Animations & Transitions
- **Hover Transitions:** All interactive elements - 150ms ease-in-out
- **Focus Transitions:** Border and shadow - 100ms ease
- **Button Press:** Slight scale animation - 100ms

### User Feedback
- **Error Messages:** Red text (#EF4444), 14px, appears below field with slide-down animation
- **Validation:** On blur for individual fields, on submit for form
- **Loading State:** Button shows spinner, text changes to "Logging in..."

## 7. Responsive Behavior

### Breakpoints
- **Mobile:** < 640px - 
  - Container padding reduces to 24px
  - Card width becomes 100% with 16px margin on sides
  - Font sizes reduce slightly (H1: 24px)

- **Desktop:** > 640px - 
  - Fixed 400px card width
  - 40px container padding
  - Full typography scale

### Touch vs. Mouse Considerations
- **Touch Targets:** All inputs and buttons are minimum 44px height
- **Hover States:** Desktop only - touch shows active states on tap

## 8. Accessibility Considerations

- **Semantic HTML:** <form>, <label>, <input>, <button> elements
- **ARIA Labels:** Form has aria-label="Login form"
- **Keyboard Navigation:** Tab order: email → password → forgot link → button
- **Focus Indicators:** Clear 2px blue ring on all focusable elements
- **Color Contrast:** All text meets WCAG AA (4.5:1 minimum)
- **Form Labels:** Each input has associated <label> with htmlFor

## 9. Additional Details

### Icons
- **Icon Library:** Heroicons (outline style)
- **Usage:** Optional email/password icons inside inputs on left side
- **Icon Sizes:** 20px
- **Icon Colors:** #9CA3AF

### Special Features
- **Password Toggle:** Eye icon on right of password field to show/hide password
- **Remember Me:** Optional checkbox below password field

## 10. Implementation Notes

### Technical Considerations
- **CSS Framework:** Tailwind CSS recommended
- **Component Library:** Headless UI for form elements
- **Browser Support:** Modern browsers (Chrome, Firefox, Safari, Edge)
- **Performance:** Minimal dependencies, fast load time

### Edge Cases
- **Empty States:** Show validation errors on submit if fields empty
- **Long Email:** Text truncates with ellipsis if too long
- **Loading States:** Disable form during API call
- **Error States:** Show generic error message below form for auth failures
```

---

## 💡 Tips for Using This Template

1. **Don't skip sections** - Even if brief, every section provides important context
2. **Be specific** - "16px" is better than "medium", "#3B82F6" better than "blue"
3. **Use consistent units** - Stick to px, rem, or % throughout
4. **Reference actual designs** - Have the screenshot visible while filling template
5. **Start broad, then detail** - Overall structure first, then dive into specifics
6. **Copy & customize** - Start with this template and adjust sections as needed
7. **Keep it updated** - Revise prompt as designs evolve

---

Ready to create your prompt? Copy the template above and start filling in your design details!
