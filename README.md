# UI Prompt Generator from Design Slides

This repository provides comprehensive documentation, templates, and examples to help you create effective UI prompts from design slides and screenshots. Whether you're working with Figma exports, design PDFs, or UI mockups, this guide will help you translate visual designs into actionable prompts for UI implementation.

## 📋 Overview

Creating accurate UI from design screenshots requires detailed, structured prompts. This repository helps you:

- Extract images from PDF design documents
- Write clear, comprehensive UI prompts
- Follow best practices for describing visual designs
- Use proven templates for consistent results

## 🎯 Purpose

This toolkit enables developers, designers, and AI prompt engineers to:

1. **Extract visual assets** from PDF design documents systematically
2. **Generate precise prompts** that capture all aspects of UI design
3. **Communicate design intent** effectively to implementation teams or AI assistants
4. **Maintain consistency** across multiple UI components and screens

## 📦 Repository Contents

- **README.md** (this file) - Overview and instructions
- **UI_PROMPT_TEMPLATE.md** - Reusable template for creating UI prompts
- **PROMPT_EXAMPLES.md** - Real-world examples for common UI patterns
- **.gitignore** - Configured for extracted images and artifacts

## 🖼️ How to Extract Images from PDF

### Method 1: Using PDF Viewer Tools (macOS Preview, Adobe Acrobat)

**macOS Preview:**
1. Open the PDF file in Preview
2. Click on a page/image you want to extract
3. Go to `File > Export...`
4. Choose your desired format (PNG, JPEG)
5. Save to your `extracted_images/` folder

**Adobe Acrobat:**
1. Open PDF in Adobe Acrobat
2. Go to `Tools > Export PDF`
3. Select `Image` and choose format (PNG/JPEG)
4. Click `Export All Images`
5. Save to your designated folder

### Method 2: Using Command Line Tools

**Using `pdfimages` (Linux/macOS):**
```bash
# Install poppler-utils (if not already installed)
# Ubuntu/Debian: sudo apt-get install poppler-utils
# macOS: brew install poppler

# Extract all images
pdfimages -png "PDFGallery_20251207_131647 (1).pdf" extracted_images/page

# This creates files like: page-000.png, page-001.png, etc.
```

**Using `pdftoppm` (Linux/macOS):**
```bash
# Convert each page to a high-quality PNG image
pdftoppm -png -r 300 "PDFGallery_20251207_131647 (1).pdf" extracted_images/page

# -r 300 sets DPI to 300 for high quality
# Creates: page-1.png, page-2.png, etc.
```

**Using Python with pdf2image:**
```bash
# Install required packages
pip install pdf2image pillow

# Run conversion script
python extract_images.py
```

```python
# extract_images.py
from pdf2image import convert_from_path
import os

# Create output directory
os.makedirs('extracted_images', exist_ok=True)

# Convert PDF to images
images = convert_from_path('PDFGallery_20251207_131647 (1).pdf', dpi=300)

# Save each page as PNG
for i, image in enumerate(images):
    image.save(f'extracted_images/page_{i+1}.png', 'PNG')
    print(f'Saved page {i+1}')
```

### Method 3: Online Tools

For quick extraction without installing software:
- **PDF2PNG.com** - Simple drag-and-drop conversion
- **ILovePDF** - Batch PDF to image conversion
- **Smallpdf** - PDF to PNG/JPEG converter

> **Note:** For sensitive designs, prefer local tools over online services.

## 📝 Best Practices for Creating UI Prompts

### 1. **Be Specific and Detailed**

❌ **Bad:** "Create a login form"
✅ **Good:** "Create a login form with email and password fields, both using rounded rectangular inputs with light gray borders, a primary blue submit button with white text, and a 'Forgot Password?' link in small gray text below"

### 2. **Follow a Consistent Structure**

Always describe UI elements in this order:
1. Overall layout and positioning
2. Visual hierarchy and spacing
3. Color scheme and styling
4. Typography and text content
5. Interactive elements and states
6. Responsive behavior

### 3. **Use Precise Measurements**

Instead of "small" or "large", use:
- Relative units: "2rem padding", "16px font size"
- Percentages: "spans 60% of container width"
- Specific values from design: "24px gap between elements"

### 4. **Describe Colors Accurately**

Provide exact color values when possible:
- Hex codes: `#3B82F6` (blue)
- RGB: `rgb(59, 130, 246)`
- Named colors: "slate-700" (if using design system)
- Descriptions: "primary brand blue" with context

### 5. **Include All Interactive States**

Don't forget to describe:
- Default/normal state
- Hover state
- Active/pressed state
- Focused state
- Disabled state
- Error/validation states

### 6. **Specify Component Relationships**

Explain how elements relate:
- "The search icon is positioned inside the left edge of the input"
- "Card components are arranged in a 3-column grid with 24px gaps"
- "The dropdown menu appears below the button, aligned to the left edge"

### 7. **Reference Design Systems**

When applicable, reference existing patterns:
- "Uses Material Design elevated button style"
- "Follows iOS native input field appearance"
- "Implements Tailwind CSS card component pattern"

### 8. **Break Complex UIs into Sections**

For complex screens:
1. Describe the overall layout first
2. Break into logical sections (header, sidebar, main content, footer)
3. Detail each section independently
4. Explain how sections connect

### 9. **Include Accessibility Considerations**

Mention important a11y features:
- "Input has associated label for screen readers"
- "Interactive elements have minimum 44px touch target"
- "Color contrast meets WCAG AA standards"

### 10. **Provide Context for Interactions**

Describe expected behavior:
- "Clicking the hamburger icon slides in the navigation drawer from the left"
- "Form validates on submit and displays inline error messages"
- "Infinite scroll loads more items when user reaches bottom"

## 🎨 Quick Start Guide

1. **Extract your design images** using one of the methods above
2. **Open UI_PROMPT_TEMPLATE.md** and copy the template
3. **Fill in each section** while viewing your design screenshot
4. **Review PROMPT_EXAMPLES.md** for inspiration and patterns
5. **Refine your prompt** using the best practices above
6. **Test your prompt** by implementing or sharing with your team

## 📚 Additional Resources

### Design Tools
- [Figma](https://www.figma.com/) - Collaborative design tool
- [Sketch](https://www.sketch.com/) - macOS design tool
- [Adobe XD](https://www.adobe.com/products/xd.html) - UI/UX design platform

### Prompt Engineering
- Focus on observable, visual characteristics
- Avoid subjective terms like "nice" or "elegant"
- Use consistent terminology throughout
- Include measurements and spacing details

### Component Libraries Reference
- [Material-UI](https://mui.com/) - React component library
- [Tailwind UI](https://tailwindui.com/) - Pre-built Tailwind components
- [shadcn/ui](https://ui.shadcn.com/) - Re-usable component collection
- [Chakra UI](https://chakra-ui.com/) - Modular component library

## 💡 Tips for Success

- **Start simple**: Begin with basic elements before tackling complex interactions
- **Use screenshots**: Reference specific visual examples when describing
- **Be consistent**: Use the same terms for the same concepts
- **Review examples**: Check PROMPT_EXAMPLES.md for similar patterns
- **Iterate**: Refine prompts based on implementation results
- **Collaborate**: Share prompts with team members for feedback

## 🤝 Contributing

Feel free to:
- Add more prompt examples
- Suggest template improvements
- Share best practices you've discovered
- Report issues or unclear documentation

## 📄 License

This documentation is provided as-is for educational and practical use.

---

**Ready to get started?** Open [UI_PROMPT_TEMPLATE.md](UI_PROMPT_TEMPLATE.md) to begin creating your first UI prompt!
