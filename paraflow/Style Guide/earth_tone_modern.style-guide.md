# Earth Tone Modern Style Guide

**Style Overview**:
A warm flat design centered on deep forest green, using subtle surface color differences instead of shadows to create unified minimalist layers, complemented by a low-saturation Morandi palette and natural textures for an organic, trustworthy, and intellectually calm atmosphere.

## Colors
### Primary Colors
  - **primary-base**: `text-[#3D5E47]` or `bg-[#3D5E47]`
  - **primary-lighter**: `bg-[#5A7A5E]`
  - **primary-darker**: `text-[#2A4332]` or `bg-[#2A4332]`

### Background Colors

#### Structural Backgrounds

Choose based on layout type:

**For Vertical Layout** (Top Header + Optional Side Panels):
- **bg-nav-primary**: `bg-[hsla(28, 18%, 94%, 1)]` - Top header
- **bg-nav-secondary**: `bg-[hsla(28, 20%, 96%, 1)]` - Inner Left sidebar (if present)
- **bg-page**: `bg-[hsla(28, 15%, 98%, 1)]` - Page background (bg of Main Content area)

**For Horizontal Layout** (Side Navigation + Optional Top Bar):
- **bg-nav-primary**: `bg-[hsla(28, 18%, 94%, 1)]` - Left main sidebar
- **bg-nav-secondary**: `bg-[hsla(28, 20%, 96%, 1)]` - Inner Top header (if present)
- **bg-page**: `bg-[hsla(28, 15%, 98%, 1)]` - Page background (bg of Main Content area)

#### Container Backgrounds
For main content area. Adjust values when used on navigation backgrounds to ensure sufficient contrast.
- **bg-container-primary**: `bg-white/85`
- **bg-container-secondary**: `bg-white/65`
- **bg-container-inset**: `bg-[#3D5E47]/8`
- **bg-container-inset-strong**: `bg-[#3D5E47]/15`

### Text Colors
- **color-text-primary**: `text-[#2C2C2C]`
- **color-text-secondary**: `text-[#5A5A5A]`
- **color-text-tertiary**: `text-[#8A8A8A]`
- **color-text-quaternary**: `text-[#B5B5B5]`
- **color-text-on-dark-primary**: `text-white/85` - Text on dark backgrounds and primary-base color surfaces
- **color-text-on-dark-secondary**: `text-white/65` - Text on dark backgrounds and primary-base color surfaces
- **color-text-link**: `text-[#3D5E47]` - Links, text-only buttons without backgrounds, and clickable text in tables

### Functional Colors
Use **sparingly** to maintain a minimalist and neutral overall style. Used for the surfaces of text-only cards, simple cards, buttons, and tags.
  - **color-success-default**: #B8D4B8
  - **color-success-light**: #E3F0E3 - tag/label bg
  - **color-error-default**: #D8B5AB - alert banner bg
  - **color-error-light**: #F5E5E0 - tag/label bg
  - **color-warning-default**: #E8D5B8 - tag/label bg
  - **color-warning-light**: #F5EBDA - tag/label bg, alert banner bg
  - **color-function-default**: #5A7A8E
  - **color-function-light**: #D4E3EB - tag/label bg

### Accent Colors
  - A secondary palette for occasional highlights and categorization. **Avoid overuse** to protect brand identity. Use **sparingly**.
  - **accent-olive**: `text-[#8B9A7E]` or `bg-[#8B9A7E]`
  - **accent-taupe**: `text-[#A89B8E]` or `bg-[#A89B8E]`
  - **accent-sage**: `text-[#9AAA97]` or `bg-[#9AAA97]`

### Data Visualization Charts
For data visualization charts only.
  - Standard data colors: #8B9A7E, #A89B8E, #9AAA97, #7A8E7A, #9B8E7E, #8A9B8A
  - Important data can use small amounts of: #3D5E47, #5A7A5E, #2A4332

## Typography
- **Font Stack**:
  - **font-family-base**: `-apple-system, BlinkMacSystemFont, "Segoe UI"` — For regular UI copy

- **Font Size & Weight**:

  - **Caption**: `text-base font-normal`
  - **Body**: `text-lg font-normal`
  - **Body Emphasized**: `text-lg font-semibold`
  - **Card Title / Subtitle**: `text-xl font-semibold`
  - **Page Title**: `text-2xl font-semibold`
  - **Headline**: `text-4xl font-semibold`

- **Line Height**: 1.5

## Border Radius
  - **Small**: 8px — Elements inside cards (e.g., photos)
  - **Medium**: 12px
  - **Large**: 16px — Cards
  - **Full**: full — Toggles, avatars, small tags, inputs, etc.

## Layout & Spacing
  - **Tight**: 12px - For closely related small internal elements, such as icons and text within buttons
  - **Compact**: 16px - For small gaps between small containers, such as a line of tags
  - **Standard**: 24px - For gaps between medium containers like list items
  - **Relaxed**: 32px - For gaps between large containers and sections
  - **Section**: 40px - For major section divisions


## Create Boundaries (contrast of surface color, borders, shadows)
Primarily relying on subtle surface color contrast with weak contrast to create unified minimalist layers, maintaining a natural and organic aesthetic throughout.

### Borders
  - **Case 1**: No Borders for most elements to maintain flat aesthetic.
  - **Case 2**: If needed for inputs or specific emphasis
    - **Default**: 1px solid #E5DDD5. Used for inputs when necessary. `border border-[#E5DDD5]`
    - **Stronger**: 1px solid #D4C9BD. Used for active or focused states. `border border-[#D4C9BD]`

### Dividers
  - **Case 1**: Prefer using background color differences over dividers.
  - **Case 2**: If needed for clear separation, `border-t` or `border-b` `border-[#E5DDD5]`.

### Shadows & Effects
  - **Case 1**: No shadow - maintain pure flat design aesthetic.

## Visual Emphasis for Containers
When containers (tags, cards, list items, rows) need visual emphasis to indicate priority, status, or category, use the following techniques:

| Technique | Implementation Notes | Best For | Avoid |
|-----------|---------------------|----------|-------|
| Background Tint | Slightly darker/lighter color or reduce transparency of backgrounds | Gentle, common approach for moderate emphasis needs | Heavy colors on large areas (e.g., red background for entire large cards) |
| Border Highlight | Use thin border with opacity for subtlety | Active/selected states, form validation | - |
| Status Tag/Label | Add colored tag/label inside container | Larger containers | - |

## Assets
### Image

- For normal `<img>`: object-cover
- For `<img>` with:
  - Slight overlay: object-cover brightness-85
  - Heavy overlay: object-cover brightness-50

### Icon

- Use Lucide icons from Iconify.
- To ensure an aesthetic layout, each icon should be centered in a square container, typically without a background, matching the icon's size.
- Use Tailwind font size to control icon size
- Example:
  ```html
  <div class="flex items-center justify-center bg-transparent w-5 h-5">
  <iconify-icon icon="lucide:flag" class="text-base"></iconify-icon>
  </div>
  ```

### Third-Party Brand Logos:
   - Use Brand Icons from Iconify.
   - Logo Example:
     Monochrome Logo: `<iconify-icon icon="simple-icons:x"></iconify-icon>`
     Colored Logo: `<iconify-icon icon="logos:google-icon"></iconify-icon>`

### User's Own Logo:
- To protect copyright, do **NOT** use real product logos as a logo for a new product, individual user, or other company products.
- **Icon-based**:
  - **Graphic**: Use a simple, relevant icon (e.g., a `calendar` icon for a scheduling app, a `heart` icon for a dating app).

## Page Layout - Web (*EXTREMELY* important)
### Determine Layout Type
- Choose between Vertical or Horizontal layout based on whether the primary navigation is a full-width top header or a full-height sidebar (left/right).
- User requirements typically indicate the layout preference. If unclear, consider:
  - Marketing/content sites typically use Vertical Layout.
  - Functional/dashboard sites can use either, depending on visual style. Sidebars accommodate more complex navigation than top bars. For complex navigation needs with a preference for minimal chrome (Vertical Layout adds an extra fixed header), choose Horizontal Layout (omits the fixed top header).
- Vertical Layout Diagram:
┌──────────────────────────────────────────────────────┐
│  Header (Primary Nav)                                │
├──────────┬──────────────────────────────┬────────────┤
│Left      │ Sub-header (Tertiary Nav)    │ Right      │
│Sidebar   │ (optional)                   │ Sidebar    │
│(Secondary├──────────────────────────────┤ (Utility   │
│Nav)      │ Main Content                 │ Panel)     │
│(optional)│                              │ (optional) │
│          │                              │            │
└──────────┴──────────────────────────────┴────────────┘
- Horizontal Layout Diagram:
┌──────────┬──────────────────────────────┬───────────┐
│          │ Header (Secondary Nav)       │           │
│ Left     │ (optional)                   │ Right     │
│ Sidebar  ├──────────────────────────────┤ Sidebar   │
│ (Primary │ Main Content                 │ (Utility  │
│ Nav)     │                              │ Panel)    │
│          │                              │ (optional)│
│          │                              │           │
└──────────┴──────────────────────────────┴───────────┘
### Detailed Layout Code
**Vertical Layout**
```html
<!-- Body: Adjust width (w-[1440px]) based on target screen size -->
<body class="w-[1440px] min-h-[700px] font-[-apple-system,BlinkMacSystemFont,'Segoe UI'] leading-[1.5]">

  <!-- Header (Primary Nav): Fixed height -->
  <header class="w-full">
    <!-- Header content -->
  </header>

  <!-- Content Container: Must include 'flex' class -->
  <div class="w-full flex min-h-[700px]">
    <!-- Left Sidebar (Secondary Nav) (Optional): Remove if not needed. If Left Sidebar exists, use its ml to control left page margin -->
    <aside class="flex-shrink-0 min-w-fit">

    </aside>

    <!-- Main Content Area:
     Use Main Content Area's horizontal padding (px) to control distance from main content to sidebars or page edges.
     For pages without sidebars (like Marketing Pages, simple content pages such as help centers, privacy policies) use larger values (px-30 to px-80), for pages with sidebars (Functional/Dashboard Pages, complex content pages with multi-level navigation like knowledge base articles) use moderate values (px-8 to px-16) -->
    <main class="flex-1 overflow-x-hidden flex flex-col">
    <!--  Main Content -->

    </main>

    <!-- Right Sidebar (Utility Panel) (Optional): Remove if not needed. If Right Sidebar exists, use its mr to control right page margin -->
    <aside class="flex-shrink-0 min-w-fit">
    </aside>

  </div>
</body>
```

**Horizontal Layout**

```html
<!-- Body: Adjust width (w-[1440px]) based on target screen size. Must include 'flex' class -->
<body class="w-[1440px] min-h-[700px] flex font-[-apple-system,BlinkMacSystemFont,'Segoe UI'] leading-[1.5]">

<!-- Left Sidebar (Primary Nav): Use its ml to control left page margin -->
  <aside class="flex-shrink-0 min-w-fit">
  </aside>

  <!-- Content Container-->
  <div class="flex-1 overflow-x-hidden flex flex-col min-h-[700px]">

    <!-- Header (Secondary Nav) (Optional): Remove if not needed. If Header exists, use its mx to control distance to left/right sidebars or page margins -->
    <header class="w-full">
    </header>

    <!-- Main Content Area: Use Main Content Area's pl to control distance from main content to left sidebar. Use pr to control distance to right sidebar/right page edge -->
    <main class="w-full">
    </main>


  </div>

  <!-- Right Sidebar (Utility Panel) (Optional): Remove if not needed. If Right Sidebar exists, use its mr to control right page margin -->
  <aside class="flex-shrink-0 min-w-fit">
  </aside>

</body>
```

## Tailwind Component Examples (Key attributes)
**Important Note**: Use utility classes directly. Do NOT create custom CSS classes or add styles in <style> tags for the following components
### Basic

- **Button**:
  - Example 1 (text button):
    - button: flex items-center gap-2 px-5 py-2.5 rounded-full bg-[#3D5E47] text-white/85 hover:bg-[#2A4332] transition
      - span(button copy): whitespace-nowrap text-base font-semibold
  - Example 2 (icon button):
    - button: flex items-center justify-center w-10 h-10 rounded-full bg-[#3D5E47] text-white/85 hover:bg-[#2A4332] transition
      - icon: text-lg

- **Tag Group (Filter Tags)**
  - container(scrollable): flex gap-3 overflow-x-auto [&::-webkit-scrollbar]:hidden
    - label (Tag item):
      - input: type="radio" name="tag1" class="sr-only peer" checked
      - div: px-4 py-2 rounded-full bg-white/65 text-[#5A5A5A] peer-checked:bg-[#3D5E47]/8 peer-checked:text-[#3D5E47] hover:bg-white/85 transition whitespace-nowrap text-base font-normal

### Data Entry
- **Progress bars/Slider**: h-3 bg-[#3D5E47]/8 rounded-full
  - filled portion: bg-[#3D5E47] h-full rounded-full

- **Checkbox**
  - label: flex items-center gap-2.5
    - input: type="checkbox" class="sr-only peer"
    - div: w-5 h-5 bg-white/65 rounded-md flex items-center justify-center peer-checked:bg-[#3D5E47] text-transparent peer-checked:text-white/85 transition
      - svg(Checkmark): stroke="currentColor" stroke-width="3"
    - span(text): text-base text-[#2C2C2C]

- **Radio button**
  - label: flex items-center gap-2.5
    - input: type="radio" name="option1" class="sr-only peer"
    - div: w-5 h-5 bg-white/65 rounded-full flex items-center justify-center peer-checked:bg-[#3D5E47] text-transparent peer-checked:text-white/85 transition
      - svg(dot indicator): fill="currentColor" class="w-2.5 h-2.5"
    - span(text): text-base text-[#2C2C2C]

- **Switch/Toggle**
  - label: flex items-center gap-2.5
    - div: relative
      - input: type="checkbox" class="sr-only peer"
      - div(Toggle track): w-14 h-7 bg-white/65 peer-checked:bg-[#3D5E47] transition rounded-full
      - div(Toggle thumb): absolute top-1 left-1 w-5 h-5 bg-white rounded-full peer-checked:translate-x-7 transition shadow-sm
    - span(text): text-base text-[#2C2C2C]

- **Select/Dropdown**
  - Select container: flex items-center justify-between gap-3 px-4 py-2.5 rounded-full bg-white/65 hover:bg-white/85 transition
    - text: text-base text-[#2C2C2C]
    - Dropdown icon(square container): flex items-center justify-center bg-transparent w-5 h-5
      - icon: text-base text-[#5A5A5A]


### Container
- **Navigation Menu - horizontal**
    - Navigation with sections/grouping:
        - Nav Container: flex items-center justify-between w-full px-8 py-4
        - Left Section: flex items-center gap-10
          - Menu Item: flex items-center gap-3 text-base text-[#2C2C2C] hover:text-[#3D5E47] transition
        - Right Section: flex items-center gap-4
          - Menu Item: flex items-center gap-3 text-base text-[#2C2C2C] hover:text-[#3D5E47] transition
          - Notification (if applicable): relative flex items-center justify-center w-12 h-12
            - notification-icon: w-6 h-6 text-[#5A5A5A]
            - badge (if has unread): absolute -top-1 -right-1 w-6 h-6 rounded-full bg-[#3D5E47] flex items-center justify-center
              - badge-count: text-xs text-white/85 font-semibold
          - Avatar(if applicable): flex items-center gap-2
            - avatar-image: w-10 h-10 rounded-full object-cover
            - dropdown-icon (if applicable): w-5 h-5 text-[#5A5A5A]

- **Card**
    - Example 1 (Vertical card with image and text):
        - Card: bg-white/85 rounded-2xl flex flex-col p-5 gap-4
        - Image: rounded-lg w-full object-cover
        - Text area: flex flex-col gap-3
          - card-title: text-xl font-semibold text-[#2C2C2C]
          - card-subtitle: text-base font-normal text-[#5A5A5A]
    - Example 2 (Horizontal card with image and text):
        - Card: bg-white/85 rounded-2xl flex gap-5 p-5
        - Image: rounded-lg h-full object-cover
        - Text area: flex flex-col gap-4 flex-1
          - card-title: text-xl font-semibold text-[#2C2C2C]
          - card-subtitle: text-base font-normal text-[#5A5A5A]
    - Example 3 (Image-focused card: no background or padding):
        - Card: flex flex-col gap-4
        - Image: rounded-2xl w-full object-cover
        - Text area: flex flex-col gap-3
          - card-title: text-xl font-semibold text-[#2C2C2C]
          - card-subtitle: text-base font-normal text-[#5A5A5A]
    - Example 4 (text-only cards, simple cards):
        - Card: bg-white/85 rounded-2xl flex flex-col p-6 gap-4

## Additional Notes
This style guide creates a warm, organic, and intellectually trustworthy atmosphere perfect for SOLVISTA's collaborative problem-solving environment. The deep forest green primary color combined with Morandi accent tones establishes natural calmness while maintaining professional credibility for B2B SaaS users.

The flat design approach with subtle surface color differences creates unified minimalist layers without shadows, emphasizing structured thinking and transparency. The warm off-white background with low-saturation palette reduces visual fatigue during extended research and collaboration sessions.

<colors_extraction>
#3D5E47
#5A7A5E
#2A4332
#EFE9E4
#F7F4F1
#FAFAF9
#FFFFFFD9
#FFFFFFA6
#3D5E4714
#3D5E4726
#2C2C2C
#5A5A5A
#8A8A8A
#B5B5B5
#FFFFFFD9
#FFFFFFA6
#B8D4B8
#E3F0E3
#D8B5AB
#F5E5E0
#E8D5B8
#F5EBDA
#5A7A8E
#D4E3EB
#8B9A7E
#A89B8E
#9AAA97
#7A8E7A
#9B8E7E
#8A9B8A
#E5DDD5
#D4C9BD
</colors_extraction>