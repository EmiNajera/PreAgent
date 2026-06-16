# 🎨 UI Specifications Template

*Duplicate this page and customize for your project*

---

## 🎯 Project Details

**Project Name:** [Your App Name]

**Version:** 1.0

**Last Updated:** [Today's Date]

---

## 🎨 Design System

### Color Palette

**Primary Colors:**

- Primary 50: #[hex]
- Primary 500: #[hex] (main)
- Primary 900: #[hex]

**Secondary Colors:**

- Secondary 50: #[hex]
- Secondary 500: #[hex]
- Secondary 900: #[hex]

**Semantic Colors:**

- Success: #10b981
- Warning: #f59e0b
- Error: #ef4444
- Info: #3b82f6

### Typography

**Font Families:**

- Primary: [Font name] (body text)
- Secondary: [Font name] (headings)

**Scale:**

- xs: 12px
- sm: 14px
- base: 16px
- lg: 18px
- xl: 20px
- 2xl: 24px
- 3xl: 30px
- 4xl: 36px

### Spacing

**Base unit:** 4px

**Scale:** 4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px

---

## 🧩 Components

### Atoms (Basic Elements)

**Button:**

- Variants: primary, secondary, outline, ghost
- Sizes: sm, md, lg
- States: default, hover, active, disabled, loading

**Input:**

- Types: text, email, password, number
- States: default, focus, error, disabled
- Variants: default, error, success

**Avatar:**

- Sizes: xs, sm, md, lg, xl
- Variants: circle, rounded, square
- Fallback: initials or icon

### Molecules (Component Groups)

**[Your Key Component 1]:**

- Purpose: [What it does]
- Composition: [Which atoms it contains]
- Variants: [Different versions]
- States: [Different states]

**[Your Key Component 2]:**

- Purpose: [What it does]
- Composition: [Which atoms it contains]
- Interactions: [How users interact with it]

### Organisms (Complex Sections)

**[Main Feature Component]:**

- Purpose: [Primary functionality]
- Sections: [Different parts]
- Behaviors: [How it behaves]

---

## 📱 Screen Flows

### Onboarding Flow

1. Welcome Screen
2. Sign Up / Login
3. Profile Setup
4. [Your specific onboarding steps]
5. Main App

### Main App Flow

1. [Primary screen]
2. [Secondary screens]
3. [Feature screens]

### User Actions

**Primary Actions:**

- [Main user action] → [Result]
- [Secondary action] → [Result]

**Gestures:** (for mobile)

- Swipe: [Action]
- Tap: [Action]
- Long press: [Action]
- Pull to refresh: [Action]

---

## 🧭 Navigation

### Structure

**Type:** [Tab Navigation / Drawer / Stack]

**Main Tabs:**

- [Tab 1]: [Icon] - [Purpose]
- [Tab 2]: [Icon] - [Purpose]
- [Tab 3]: [Icon] - [Purpose]

### Transitions

- Tab to tab: fade
- List to detail: slide left
- Modal: slide up
- Back navigation: slide right

---

## 💻 Responsive Design

### Mobile (< 768px)

- Navigation: bottom tabs
- Layout: single column
- Gestures: enabled
- Touch targets: 44px minimum

### Tablet (768px - 1024px)

- Navigation: side rail
- Layout: split view
- Gestures: limited

### Desktop (> 1024px)

- Navigation: top bar + sidebar
- Layout: multi-column
- Interactions: hover states

---

## ♿ Accessibility

### Standards

- WCAG 2.1 AA compliance
- Screen reader support
- Keyboard navigation
- High contrast mode

### Implementation

- Semantic HTML elements
- ARIA labels and descriptions
- Focus management
- Color contrast ratios (4.5:1 minimum)
- Alternative text for images

---

## 🎨 Interactions

### Animations

- Duration: 200ms (fast), 300ms (standard), 500ms (slow)
- Easing: ease-out for entrances, ease-in for exits
- Loading states: skeleton screens or spinners

### Feedback

- Haptic feedback on mobile
- Visual feedback for all interactions
- Success/error messages
- Progress indicators

---

## ✅ Component Checklist

For each component, ensure:

- [ ]  Follows design system tokens
- [ ]  All variants implemented
- [ ]  All states defined
- [ ]  Responsive behavior
- [ ]  Accessibility compliant
- [ ]  Interactive feedback
- [ ]  Error states handled
- [ ]  Loading states included

---

*Export this as ui-specifications.json for Cursor*