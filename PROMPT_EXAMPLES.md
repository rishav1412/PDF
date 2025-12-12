# UI Prompt Examples

This document provides detailed examples of UI prompts for common interface patterns. Use these as references when creating your own prompts.

---

## Table of Contents

1. [Login/Authentication Screen](#1-loginauthentication-screen)
2. [Dashboard/Analytics Interface](#2-dashboardanalytics-interface)
3. [Contact Form](#3-contact-form)
4. [Navigation Menu (Sidebar)](#4-navigation-menu-sidebar)
5. [Card-Based Product Grid](#5-card-based-product-grid)

---

## 1. Login/Authentication Screen

### Example: Modern Minimal Login

```markdown
Create a centered login form with a clean, modern aesthetic.

**Layout:**
- Center the form card both vertically and horizontally on the page
- Card container: 400px width, white background, rounded corners (12px radius)
- Elevated appearance with shadow: 0 8px 16px rgba(0,0,0,0.1)
- Page background: light gradient from #F0F4F8 (top) to #D9E2EC (bottom)
- Internal padding: 48px all sides

**Header:**
- Logo: 48px x 48px, centered, 24px margin below
- Title: "Welcome Back" - 32px, 700 weight, #1A202C, centered
- Subtitle: "Sign in to continue" - 16px, 400 weight, #718096, centered, 8px margin top

**Form Elements:**
- Two input fields stacked vertically with 20px gap

Email Input:
- Label: "Email Address" - 14px, 500 weight, #2D3748, positioned above with 8px gap
- Input field: full width, 48px height
- Border: 1px solid #CBD5E0, 8px border-radius
- Background: #FFFFFF
- Font: 16px, #1A202C
- Placeholder: "you@example.com" - #A0AEC0
- Padding: 12px 16px

Password Input:
- Same styling as email input
- Label: "Password"
- Placeholder: "Enter your password"
- Eye icon on the right side (20px, #718096) to toggle visibility
- Icon positioned 16px from right edge

**Additional Links:**
- "Forgot password?" link
- Position: right-aligned, 12px below password field
- Style: 14px, 500 weight, #3182CE (blue), no underline by default
- Hover: underline appears

**Submit Button:**
- Full width, 48px height, 16px margin top
- Background: linear gradient from #3182CE to #2C5282 (left to right)
- Text: "Sign In" - 16px, 600 weight, white (#FFFFFF), centered
- Border-radius: 8px
- Shadow on hover: 0 4px 12px rgba(49,130,206,0.3)
- Transition: all 200ms ease

**Footer:**
- Centered text below button, 24px margin top
- "Don't have an account?" - 14px, #718096
- "Sign up" link - 14px, 600 weight, #3182CE, inline

**Interactive States:**
- Input Focus: Border changes to 2px solid #3182CE, subtle blue glow shadow
- Button Hover: Slight brightness increase, shadow appears, scale: 1.02
- Button Active: Scale: 0.98, shadow reduces
- Button Loading: Show spinner, text changes to "Signing in...", button disabled

**Accessibility:**
- All inputs have associated labels with htmlFor
- Form has proper semantic HTML structure
- Tab order: email → password → forgot link → submit button
- Focus visible with 2px blue outline offset by 2px
- ARIA labels for screen readers
```

---

## 2. Dashboard/Analytics Interface

### Example: Sales Analytics Dashboard

```markdown
Create a comprehensive analytics dashboard with multiple data visualization sections.

**Overall Layout:**
- Full-width layout with sidebar navigation on left (260px fixed width)
- Main content area with light gray background (#F7FAFC)
- Top navigation bar: 64px height, white background, bottom border 1px solid #E2E8F0

**Top Navigation:**
- Left side: Dashboard title "Analytics Dashboard" - 20px, 600 weight, #1A202C
- Right side: User profile section
  - Notifications icon (bell) - 24px, #718096, with red dot badge if unread
  - User avatar - 40px circle, 12px margin left
  - Dropdown trigger on click

**Main Content Grid:**
- Container padding: 24px
- CSS Grid layout: 4 columns with 24px gaps
- Responsive: 2 columns on tablet, 1 column on mobile

**Stat Cards (4 cards in top row):**
Each card:
- Background: white (#FFFFFF)
- Border-radius: 12px
- Padding: 24px
- Shadow: 0 1px 3px rgba(0,0,0,0.1)
- Hover: shadow increases to 0 4px 6px rgba(0,0,0,0.1)

Card Structure:
- Icon: Top left, 48px x 48px, rounded background with 12px padding
  - Revenue card: Green background (#D4EDDA), dollar icon (#28A745)
  - Users card: Blue background (#CCE5FF), users icon (#007BFF)
  - Orders card: Purple background (#E7D4F5), shopping icon (#6F42C1)
  - Growth card: Orange background (#FFE5CC), trend icon (#FD7E14)
- Label: Below icon, 14px, 500 weight, #718096, 8px margin top
- Value: 32px, 700 weight, #1A202C, 4px margin top
- Change indicator: 12px, 500 weight, with up/down arrow
  - Positive: #28A745 with ↑ arrow
  - Negative: #DC3545 with ↓ arrow
- Percentage: e.g., "+12.5% from last month"

**Chart Section (spans 3 columns):**
- White background card, 16px padding
- Header: "Revenue Over Time" - 18px, 600 weight, #1A202C
- Dropdown filter on right: "Last 30 Days", "Last 90 Days", "Last Year"
- Line chart below header with 16px margin top
- Chart height: 300px
- Grid lines: light gray (#E2E8F0)
- Line color: #3182CE (blue), 2px thickness
- Data points: 6px circles on line with hover tooltip
- Axes labels: 12px, #718096
- Tooltip on hover: white background, shadow, shows date and value

**Recent Activity Section (spans 1 column, right side):**
- White background card, same styling as stat cards
- Header: "Recent Activity" - 16px, 600 weight, #1A202C
- Scrollable list (max-height: 300px, overflow-y: auto)
- Activity items:
  - Avatar: 32px circle on left
  - Text: 14px, #2D3748
  - Timestamp: 12px, #A0AEC0, right-aligned
  - Divider: 1px solid #E2E8F0 between items (except last)
  - Padding: 12px per item

**Table Section (spans full width below):**
- White background card, 16px padding, 24px margin top
- Header: "Recent Orders" - 18px, 600 weight, #1A202C
- Search input on right of header: 240px width, 36px height
- Table:
  - Header row: #F7FAFC background, 14px, 600 weight, #2D3748
  - Data rows: 14px, 400 weight, #1A202C
  - Row hover: #F7FAFC background
  - Borders: 1px solid #E2E8F0 between rows
  - Padding: 12px per cell
  - Columns: Order ID, Customer, Date, Amount, Status
  - Status badges:
    - Completed: #D4EDDA background, #28A745 text, 6px border-radius
    - Pending: #FFF3CD background, #FFC107 text
    - Cancelled: #F8D7DA background, #DC3545 text
  - Pagination at bottom: centered, 36px height buttons

**Responsive Behavior:**
- Desktop (>1024px): 4-column grid as described
- Tablet (768-1024px): 2-column grid, chart and activity stack
- Mobile (<768px): Single column, sidebar becomes hamburger menu

**Interactions:**
- Chart tooltips appear on hover with 150ms fade-in
- Stat cards have subtle lift on hover (translateY: -2px)
- Table rows highlight on hover
- All transitions: 200ms ease-in-out
```

---

## 3. Contact Form

### Example: Multi-Step Contact Form

```markdown
Create a clean, user-friendly contact form with progress indicator and validation.

**Container:**
- Centered on page, max-width: 600px
- White background, 16px border-radius
- Padding: 40px
- Shadow: 0 4px 12px rgba(0,0,0,0.08)
- Page background: #F5F7FA

**Progress Indicator (Top):**
- Horizontal stepper showing 3 steps
- Steps: "Personal Info" → "Message" → "Review"
- Layout: Flexbox, space-between, 32px margin bottom

Each step indicator:
- Number circle: 36px diameter
- Active step: #3B82F6 background, white text
- Completed step: #10B981 background, white checkmark icon
- Inactive step: #E5E7EB background, #9CA3AF text
- Line between steps: 2px height, #E5E7EB, grows to #3B82F6 as complete
- Label below circle: 12px, 500 weight, color matches step state

**Form Header:**
- Title: "Get in Touch" - 28px, 700 weight, #111827, 16px margin bottom
- Description: "Fill out the form below and we'll get back to you soon" - 14px, 400 weight, #6B7280

**Form Fields (Step 1 - Personal Info):**

Name Fields (side by side on desktop, stacked on mobile):
- First Name and Last Name
- Each: 50% width minus 8px gap on desktop, full width on mobile
- Label: 14px, 500 weight, #374151, 8px margin bottom
- Input: Full width, 44px height, 12px padding horizontal
- Border: 1px solid #D1D5DB, 8px border-radius
- Background: white
- Font: 16px, #1F2937
- Placeholder: "John" / "Doe" - #9CA3AF
- 20px margin bottom

Email Field:
- Same styling as name fields
- Full width
- Type: email
- Placeholder: "john.doe@example.com"
- Email icon on left inside input (20px, #9CA3AF, 12px from left)
- Text padding-left: 40px to accommodate icon

Phone Field (optional):
- Same styling as email
- Type: tel
- Placeholder: "+1 (555) 000-0000"
- Phone icon on left inside input
- Small "optional" badge in label - 12px, #9CA3AF, italic

**Form Fields (Step 2 - Message):**

Subject Dropdown:
- Label: "Subject" - 14px, 500 weight, #374151
- Select input: Full width, 44px height
- Border: 1px solid #D1D5DB, 8px border-radius
- Chevron down icon on right
- Options: "General Inquiry", "Support", "Sales", "Partnership"
- 20px margin bottom

Message Textarea:
- Label: "Your Message" - 14px, 500 weight, #374151
- Textarea: Full width, 120px height (expandable)
- Border: 1px solid #D1D5DB, 8px border-radius
- Padding: 12px
- Font: 16px, #1F2937, 1.5 line-height
- Placeholder: "Tell us what you need help with..."
- Character counter bottom-right: "0/500" - 12px, #9CA3AF
- Resize: vertical only

File Attachment (optional):
- Dashed border drag-and-drop area
- 120px height, 12px border-radius
- Border: 2px dashed #D1D5DB
- Background: #F9FAFB
- Center-aligned content:
  - Upload icon: 32px, #9CA3AF
  - Text: "Drag and drop or click to browse" - 14px, #6B7280
  - Subtext: "PDF, DOC, or images up to 10MB" - 12px, #9CA3AF
- Hover: Border color changes to #3B82F6
- On file select: Show file name, size, remove button

**Form Fields (Step 3 - Review):**
- Summary of entered information
- Each field displayed in read-only format
- Label: 12px, 500 weight, #6B7280, uppercase
- Value: 16px, 400 weight, #1F2937
- 16px margin between fields
- Edit buttons next to each section: "Edit" - 14px, #3B82F6, goes back to specific step

**Validation:**
- Real-time validation on blur
- Invalid field: Border changes to 2px solid #EF4444
- Error message below field: 14px, #EF4444, with error icon (16px)
- Required fields marked with red asterisk in label
- Valid field: Subtle green checkmark appears on right side of input

**Navigation Buttons:**
- Fixed to bottom of form container, 24px margin top
- Layout: Flexbox, space-between

Back Button (not on first step):
- Text button: "Back" - 16px, 500 weight, #6B7280
- No background, no border
- Hover: #374151 color

Next/Submit Button:
- Primary button: 140px width, 44px height
- Background: #3B82F6
- Text: "Next Step" or "Submit" on last step - 16px, 600 weight, white
- Border-radius: 8px
- Shadow: 0 2px 4px rgba(59,130,246,0.2)
- Hover: Background #2563EB, shadow increases
- Disabled: Background #9CA3AF, cursor not-allowed
- Loading state: Shows spinner, text "Submitting..."

**Success State (After Submission):**
- Replace form with success message
- Large checkmark icon: 64px, #10B981, centered
- Heading: "Thank You!" - 32px, 700 weight, #111827, centered, 16px margin top
- Message: "We've received your message and will respond within 24 hours." - 16px, #6B7280, centered
- Button: "Send Another Message" - resets form

**Interactive Behaviors:**
- Smooth step transitions with fade effect (300ms)
- Input focus: Border changes to #3B82F6, subtle blue shadow
- Prevent next step if current step has validation errors
- Auto-save to localStorage on field change
- Show warning if user tries to leave with unsaved changes

**Responsive:**
- Desktop: Form fields side-by-side where applicable
- Mobile (<640px): All fields full width, stacked
- Progress indicator: Smaller circles (28px) on mobile
- Padding reduces to 24px on mobile
```

---

## 4. Navigation Menu (Sidebar)

### Example: App Sidebar Navigation

```markdown
Create a modern sidebar navigation for a web application with collapsible sections and active states.

**Sidebar Container:**
- Fixed position on left side of screen
- Width: 260px (expanded), 72px (collapsed)
- Height: 100vh (full viewport height)
- Background: #1F2937 (dark gray)
- Border-right: 1px solid #374151
- Box-shadow: 2px 0 8px rgba(0,0,0,0.1)
- Transition: width 300ms ease-in-out

**Header Section:**
- Height: 64px
- Border-bottom: 1px solid #374151
- Padding: 16px

Logo Area (expanded state):
- Logo icon: 32px x 32px on left
- Company name: "AppName" - 18px, 600 weight, white, 12px margin left
- Layout: Flexbox, align-items center

Logo Area (collapsed state):
- Only show logo icon centered

Toggle Button:
- Position: Top-right of sidebar header
- Icon: Hamburger/close icon - 24px, #9CA3AF
- Hover: #E5E7EB
- Click: Toggles sidebar collapsed state

**Navigation Sections:**
- Scrollable area (overflow-y: auto)
- Padding: 16px 12px

Section Structure:
Multiple sections with headers: "Main", "Analytics", "Settings"

Section Header (expanded state):
- Text: 11px, 700 weight, #9CA3AF, uppercase, 0.05em letter-spacing
- Padding: 16px 12px 8px 12px
- First section: no top padding

Section Header (collapsed state):
- Hidden, replaced with subtle divider line

**Navigation Items:**

Individual Item:
- Height: 44px
- Padding: 12px
- Border-radius: 8px
- Margin-bottom: 4px
- Layout: Flexbox, align-items center
- Transition: all 200ms ease

Item Structure (expanded):
- Icon: 20px, left-aligned, 12px margin right
- Label: 14px, 500 weight
- Badge (optional): Right-aligned, shows count
- Chevron (for expandable): Right-aligned

Item Colors:
- Default: Icon #9CA3AF, text #D1D5DB, no background
- Hover: Icon #E5E7EB, text #F3F4F6, background #374151
- Active: Icon #3B82F6, text white, background #1E40AF
- Focus: 2px outline #3B82F6

Item Structure (collapsed):
- Only show centered icon
- Label appears in tooltip on hover
- Tooltip: Dark background #1F2937, white text, 8px padding, 6px border-radius, positioned to right of sidebar

**Expandable Sections:**
Example: "Projects" section with sub-items

Parent Item:
- Same structure as regular item
- Chevron icon on right: Rotates 90° when expanded (180deg when collapsed)
- Click anywhere on item to expand/collapse

Expanded Sub-items:
- Indented 32px from left (8px in collapsed state - shown in tooltip)
- Slightly smaller: 40px height
- Font-size: 13px
- Background on hover: #374151 with 50% opacity
- Active sub-item: Left border 3px solid #3B82F6

**Special Items:**

Search Item (at top):
- Input field: Full width when expanded
- Background: #374151
- Border: 1px solid #4B5563
- Border-radius: 8px
- Height: 40px
- Padding: 8px 12px
- Icon: Search icon on left inside input (18px, #9CA3AF)
- Placeholder: "Search..." - #6B7280
- Text: white, 14px
- Focus: Border #3B82F6
- Collapsed state: Just shows search icon button, click opens search modal

Profile Item (at bottom):
- Fixed to bottom of sidebar
- Border-top: 1px solid #374151
- Padding: 16px 12px
- Layout: Flexbox

Profile Content (expanded):
- Avatar: 36px circle, left-aligned
- Info section: 12px margin left
  - Name: 14px, 600 weight, white
  - Email: 12px, #9CA3AF
- Logout icon: 20px, #9CA3AF, right-aligned
- Hover: Background #374151, cursor pointer

Profile Content (collapsed):
- Only show avatar centered
- Hover: Shows tooltip with name and logout option

**Notification Badge:**
- Positioned top-right of nav items with notifications
- Circle: 18px diameter (or auto-width for 2+ digits)
- Background: #EF4444 (red)
- Text: white, 11px, 600 weight, centered
- Border: 2px solid #1F2937 (matches sidebar background)

**Hover Tooltip (Collapsed State):**
- Appears 8px to the right of sidebar
- Background: #1F2937
- Border: 1px solid #374151
- Padding: 8px 12px
- Border-radius: 6px
- Text: white, 14px
- Shadow: 0 4px 8px rgba(0,0,0,0.2)
- Arrow pointing to sidebar (8px triangle)
- Delay: 200ms before appearing

**Responsive Behavior:**
- Desktop (>1024px): Expanded by default, can collapse
- Tablet (768-1024px): Collapsed by default
- Mobile (<768px): Hidden by default, opens as overlay when triggered
  - Overlay: Covers full screen with semi-transparent backdrop (#00000080)
  - Sidebar slides in from left
  - Close button visible in header
  - Click outside sidebar to close

**Interactive States:**
- Smooth transitions for all state changes (200-300ms)
- Active state persists based on current route
- Expand/collapse animations use CSS transforms for performance
- Sub-menu expansion: Max-height animation with ease timing
- Icons can rotate or change on state changes (e.g., folder open/closed)

**Accessibility:**
- Semantic nav element with aria-label="Main navigation"
- Active item has aria-current="page"
- Expandable sections have aria-expanded attribute
- Keyboard navigation: Tab through items, Enter to activate, Space to expand
- Focus visible with outline
- Screen reader announcements for state changes
```

---

## 5. Card-Based Product Grid

### Example: E-commerce Product Listing

```markdown
Create a responsive product grid with card components, filters, and sorting.

**Page Layout:**
- Container: max-width 1280px, centered, 24px padding on sides
- Background: #FFFFFF
- Header at top, filter sidebar on left, product grid on right

**Page Header:**
- Height: auto, padding 24px 0
- Border-bottom: 1px solid #E5E7EB
- Breadcrumb navigation:
  - 14px, #6B7280
  - Links separated by chevron icon (16px)
  - Active page: #111827, not linked
  - Hover: #3B82F6
- Page title below breadcrumb:
  - "All Products" - 32px, 700 weight, #111827, 12px margin top
- Result count:
  - "Showing 24 of 156 products" - 14px, #6B7280, 8px margin top

**Filter Sidebar:**
- Width: 240px (fixed on desktop)
- Padding: 24px 0
- Border-right: 1px solid #E5E7EB (desktop only)
- Background: #F9FAFB (mobile overlay)

Mobile Filter:
- Hidden by default on mobile
- Opens as sliding overlay from left
- Full height, 280px width
- Backdrop: rgba(0,0,0,0.5)
- Close button top-right

Filter Sections:
Multiple collapsible sections

Section Header:
- Text: 16px, 600 weight, #111827
- Chevron icon on right: rotates on expand
- Padding: 12px 0
- Border-bottom: 1px solid #E5E7EB
- Cursor: pointer

Filter Options (per section):
- Checkboxes for multi-select
- Radio buttons for single-select
- Padding: 12px 0 per option

Checkbox Styling:
- Custom checkbox: 18px square
- Border: 2px solid #D1D5DB
- Border-radius: 4px
- Checked: Background #3B82F6, white checkmark
- Label: 14px, #374151, 8px margin left
- Hover: Border #3B82F6
- Count in gray on right: (24)

Filter Categories:
1. **Price Range:**
   - Dual-thumb range slider
   - Min/max inputs below slider
   - Slider track: #E5E7EB, 4px height
   - Active range: #3B82F6
   - Thumbs: 16px circle, white, border 2px solid #3B82F6

2. **Category:**
   - Checkboxes: Electronics, Fashion, Home, Sports, Books
   - Each with product count

3. **Brand:**
   - Checkboxes: Top 8 brands
   - "Show more" link to expand full list

4. **Rating:**
   - Star rating options: 4★ & up, 3★ & up, etc.
   - Gold stars (#F59E0B), gray empty stars (#D1D5DB)

5. **Color:**
   - Color swatches: 24px circles with actual color
   - Border: 2px solid transparent
   - Selected: 3px solid #3B82F6 border
   - Grid: 3 columns, 8px gap

Clear Filters Button:
- Bottom of sidebar
- Text button: "Clear all filters" - 14px, #3B82F6
- Hover: #2563EB, underline

**Toolbar (above grid):**
- Flexbox: space-between, align-items center
- Padding: 16px 0
- Border-bottom: 1px solid #E5E7EB

Left side:
- Filter toggle button (mobile): "Filters" text with icon
- Active filter tags:
  - Pill-shaped: 8px padding horizontal, 4px vertical
  - Background: #EEF2FF
  - Text: 14px, #3B82F6
  - X button to remove: 16px, hover #2563EB

Right side:
- View toggle: Grid/List view icons (24px, #6B7280)
- Selected view: #3B82F6
- Sort dropdown:
  - "Sort by: Featured" - 14px
  - Chevron down icon
  - Dropdown menu on click:
    - White background, shadow, border-radius 8px
    - Options: Featured, Price: Low to High, Price: High to Low, Newest, Best Rating
    - Hover: #F3F4F6 background
    - Selected: Checkmark icon, #3B82F6 text

**Product Grid:**
- CSS Grid layout
- Desktop: 4 columns
- Tablet: 3 columns
- Mobile: 2 columns (1 column on very small)
- Gap: 24px between cards
- Padding: 24px

**Product Card:**
- Background: white
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Overflow: hidden
- Transition: all 300ms ease
- Hover: Shadow 0 8px 16px rgba(0,0,0,0.1), translateY(-4px)

Card Structure:

1. **Image Container:**
   - Aspect ratio: 1:1 (square)
   - Background: #F3F4F6
   - Position: relative
   - Overflow: hidden

Product Image:
- Object-fit: cover
- Width: 100%
- Height: 100%
- Transition: transform 300ms
- Hover: scale(1.05)

Badges (top-left overlay):
- "Sale" badge: #EF4444 background, white text, 8px padding, 6px border-radius top-left
- "New" badge: #10B981 background
- Position: 12px from top and left

Wishlist Button (top-right overlay):
- Heart icon: 20px, white color
- Background: rgba(0,0,0,0.4)
- Padding: 8px
- Border-radius: 50%
- Position: 12px from top and right
- Hover: Background rgba(0,0,0,0.6)
- Filled heart when favorited: #EF4444

Quick View Button (center, appears on hover):
- "Quick View" text - 14px, 600 weight, white
- Background: rgba(0,0,0,0.7)
- Padding: 10px 20px
- Border-radius: 6px
- Fade in on card hover
- Click: Opens modal

2. **Content Section:**
   - Padding: 16px
   - Background: white

Brand/Category:
- Text: 12px, 500 weight, #6B7280, uppercase, 0.05em letter-spacing
- Margin-bottom: 4px

Product Name:
- Text: 16px, 600 weight, #111827
- Line-height: 1.3
- Margin-bottom: 8px
- Max 2 lines with ellipsis overflow
- Hover: #3B82F6 color, cursor pointer

Rating Section:
- Margin-bottom: 8px
- Star icons: 14px each, gold (#F59E0B) if filled, gray (#D1D5DB) if empty
- Rating text: "(4.5)" - 12px, #6B7280, 4px margin left
- Review count: "128 reviews" - 12px, #9CA3AF, 4px margin left

Price Section:
- Margin-bottom: 12px

Current Price:
- Text: 20px, 700 weight, #111827
- If on sale: #EF4444 color

Original Price (if on sale):
- Text: 16px, 400 weight, #9CA3AF
- Text decoration: line-through
- 8px margin left

Discount Badge (if on sale):
- Text: "-20%" - 12px, 600 weight, #EF4444
- Background: #FEE2E2
- Padding: 2px 6px
- Border-radius: 4px
- 8px margin left

3. **Action Section:**
   - Border-top: 1px solid #F3F4F6
   - Padding-top: 12px

Add to Cart Button:
- Full width
- Height: 40px
- Background: #3B82F6
- Text: "Add to Cart" - 14px, 600 weight, white
- Border-radius: 8px
- Icon: Shopping cart (16px) on left, 8px margin right
- Hover: Background #2563EB
- Active: Scale 0.98
- Loading: Shows spinner, text "Adding..."

**Load More Section:**
- Centered below grid
- 32px margin top
- Button: "Load More Products" or "Show More"
  - Width: 200px, height: 44px
  - Border: 2px solid #3B82F6
  - Background: transparent
  - Text: #3B82F6, 16px, 600 weight
  - Border-radius: 8px
  - Hover: Background #3B82F6, text white
- Pagination alternative:
  - Page numbers: 36px square buttons
  - Active page: #3B82F6 background, white text
  - Other pages: Transparent, #6B7280 text
  - Arrows: Previous/Next - same styling
  - 8px gap between buttons

**Empty State:**
- Shown when no products match filters
- Centered content:
  - Icon: Empty box or search (64px, #9CA3AF)
  - Heading: "No products found" - 24px, 600 weight, #111827
  - Description: "Try adjusting your filters" - 16px, #6B7280
  - Button: "Clear all filters" - primary button style

**Loading State:**
- Skeleton cards in grid
- Animated shimmer effect
- Gray blocks for image, title, price
- Pulsing animation (1.5s duration)

**Responsive Behavior:**
- Desktop (>1024px): 4-column grid, sidebar visible
- Tablet (768-1024px): 3-column grid, sidebar collapsible
- Mobile (640-768px): 2-column grid, overlay sidebar
- Small mobile (<640px): 1-column grid, larger cards

**Accessibility:**
- Product cards are semantic article elements
- Links have descriptive text
- Images have alt text with product name
- Buttons have aria-labels
- Filter controls are keyboard accessible
- Focus visible with blue outline
- Screen reader announcements for filter changes and product count
```

---

## 📝 Tips for Using These Examples

### How to Apply These Examples

1. **Find Similar Patterns**: Look for examples that match your design type
2. **Copy and Modify**: Use the structure but adjust colors, sizes, spacing
3. **Combine Elements**: Mix components from different examples
4. **Be Specific**: Replace placeholder values with exact measurements from your design
5. **Add Context**: Include any unique features not covered in examples

### Common Patterns Across Examples

- **Consistent spacing**: 4px, 8px, 12px, 16px, 24px, 32px, 48px
- **Border radius**: 4px (subtle), 8px (moderate), 12px (rounded), 50% (circles)
- **Shadows**: Layered from subtle to prominent
- **Transitions**: 150-300ms for smooth interactions
- **Colors**: Specific hex values, not generic names
- **Typography**: Clear hierarchy with size, weight, and color

### Adapting Examples to Your Design

When your design differs from these examples:

- **Layout Changes**: Describe the actual grid/flex structure you see
- **Color Scheme**: Replace all color values with your brand colors
- **Typography**: Update font families, sizes, and weights
- **Components**: Add or remove sections as needed
- **Interactions**: Describe your specific hover, active, and loading states

### Testing Your Prompts

After creating a prompt based on these examples:

1. Read it to someone unfamiliar with the design
2. Can they visualize it without seeing the screenshot?
3. Are all measurements specific, not vague?
4. Have you covered all interactive states?
5. Is responsive behavior clearly described?

---

## 🎯 Next Steps

- Review [UI_PROMPT_TEMPLATE.md](UI_PROMPT_TEMPLATE.md) for the complete template structure
- Check [README.md](README.md) for best practices and guidelines
- Start creating your own prompts using these examples as reference
- Iterate and refine based on implementation feedback

**Remember**: Good prompts are detailed, specific, and leave no room for ambiguity!
