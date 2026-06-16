# 🎨 UI Specifications

*Core document for screen flows, components, and behaviors*

---

## 🌿 JSON Structure for Cursor

```json
{
  "uiSpecifications": {
    "projectName": "",
    "version": "1.0",
    "lastUpdated": "",
    "designSystem": {
      "colorPalette": {},
      "typography": {},
      "spacing": {},
      "iconography": {},
      "breakpoints": {}
    },
    "components": {
      "atoms": [],
      "molecules": [],
      "organisms": [],
      "templates": []
    },
    "screens": {
      "flows": [],
      "wireframes": [],
      "interactions": [],
      "states": []
    },
    "navigation": {
      "structure": {},
      "transitions": [],
      "gestures": []
    },
    "responsive": {
      "mobile": {},
      "tablet": {},
      "desktop": {}
    },
    "accessibility": {
      "standards": [],
      "screenReader": [],
      "keyboardNav": [],
      "colorContrast": {}
    }
  }
}
```

---

## 📋 Template Instructions

### 🎨 Design System

**Establish visual consistency:**

- Color palette and themes
- Typography scale and fonts
- Spacing and layout grids
- Icon sets and imagery
- Responsive breakpoints

### 🧩 Component Library

**Atomic design methodology:**

- **Atoms:** Basic UI elements (buttons, inputs)
- **Molecules:** Simple component groups
- **Organisms:** Complex component sections
- **Templates:** Page layout structures

### 📱 Screen Flows

**User journey mapping:**

- Wireframes for each screen
- User flow connections
- Interaction behaviors
- State variations (loading, error, empty)

### 🧭 Navigation

**Movement between screens:**

- Information architecture
- Transition animations
- Gesture controls
- Deep linking structure

### 💻 Responsive Design

**Multi-device experience:**

- Mobile-first approach
- Tablet adaptations
- Desktop considerations
- Progressive enhancement

### ♿ Accessibility

**Inclusive design:**

- WCAG compliance
- Screen reader support
- Keyboard navigation
- Color contrast ratios

---

## 🏷️ Example: Dating App UI Specs

```json
{
  "uiSpecifications": {
    "projectName": "DateDeck - Meaningful Dating App",
    "version": "1.0",
    "lastUpdated": "2025-08-12",
    "designSystem": {
      "colorPalette": {
        "primary": {
          "50": "#fef7ee",
          "500": "#f97316",
          "900": "#9a3412"
        },
        "secondary": {
          "50": "#f8fafc", 
          "500": "#64748b",
          "900": "#0f172a"
        },
        "accent": {
          "pink": "#ec4899",
          "purple": "#8b5cf6"
        },
        "semantic": {
          "success": "#10b981",
          "warning": "#f59e0b",
          "error": "#ef4444",
          "info": "#3b82f6"
        }
      },
      "typography": {
        "fontFamilies": {
          "primary": "Inter",
          "secondary": "Playfair Display"
        },
        "scale": {
          "xs": "12px",
          "sm": "14px",
          "base": "16px",
          "lg": "18px",
          "xl": "20px",
          "2xl": "24px",
          "3xl": "30px",
          "4xl": "36px"
        }
      },
      "spacing": {
        "unit": "4px",
        "scale": ["4px", "8px", "12px", "16px", "24px", "32px", "48px", "64px"]
      }
    },
    "components": {
      "atoms": [
        {
          "name": "Button",
          "variants": ["primary", "secondary", "outline", "ghost"],
          "sizes": ["sm", "md", "lg"],
          "states": ["default", "hover", "active", "disabled"],
          "props": [
            {"name": "variant", "type": "string", "default": "primary"},
            {"name": "size", "type": "string", "default": "md"},
            {"name": "disabled", "type": "boolean", "default": false},
            {"name": "loading", "type": "boolean", "default": false}
          ]
        },
        {
          "name": "Input",
          "variants": ["default", "error", "success"],
          "types": ["text", "email", "password", "number"],
          "states": ["default", "focus", "error", "disabled"]
        },
        {
          "name": "Avatar",
          "sizes": ["xs", "sm", "md", "lg", "xl"],
          "variants": ["circle", "rounded", "square"],
          "fallback": "initials"
        }
      ],
      "molecules": [
        {
          "name": "ConversationCard",
          "composition": ["Card", "Text", "Button", "Icon"],
          "variants": ["question", "prompt", "icebreaker"],
          "interactions": ["flip", "save", "share"]
        },
        {
          "name": "UserProfileCard",
          "composition": ["Avatar", "Text", "Badge", "Button"],
          "states": ["minimal", "detailed", "preview"]
        }
      ],
      "organisms": [
        {
          "name": "ProfileEditor",
          "composition": ["Form", "ImageUpload", "TextArea", "TagSelector"],
          "sections": ["photos", "basic-info", "preferences", "bio"]
        },
        {
          "name": "MatchesList",
          "composition": ["List", "UserProfileCard", "EmptyState"],
          "behaviors": ["infinite-scroll", "pull-to-refresh"]
        }
      ]
    },
    "screens": {
      "flows": [
        {
          "name": "Onboarding Flow",
          "screens": ["Welcome", "SignUp", "ProfileSetup", "PhotoUpload", "Preferences"],
          "transitions": "slide-right",
          "canSkip": ["PhotoUpload"],
          "validation": ["email", "age", "photos"]
        },
        {
          "name": "Matching Flow",
          "screens": ["Discovery", "ProfileView", "ConversationStarter", "Chat"],
          "gestures": ["swipe", "tap", "long-press"]
        }
      ],
      "wireframes": [
        {
          "screen": "Discovery",
          "layout": "stack",
          "sections": [
            {"component": "Header", "height": "60px"},
            {"component": "CardStack", "height": "flex-1"},
            {"component": "ActionButtons", "height": "80px"}
          ]
        }
      ],
      "interactions": [
        {
          "trigger": "swipe-right",
          "action": "like-user",
          "animation": "card-slide-out",
          "feedback": "haptic + heart-icon"
        },
        {
          "trigger": "double-tap",
          "action": "super-like",
          "animation": "star-burst",
          "feedback": "haptic + star-icon"
        }
      ]
    },
    "navigation": {
      "structure": {
        "type": "tab-navigation",
        "tabs": [
          {"name": "Discovery", "icon": "heart", "route": "/discover"},
          {"name": "Matches", "icon": "message-circle", "route": "/matches"},
          {"name": "Profile", "icon": "user", "route": "/profile"}
        ]
      },
      "transitions": [
        {"from": "any", "to": "modal", "animation": "slide-up"},
        {"from": "tab", "to": "tab", "animation": "fade"},
        {"from": "list", "to": "detail", "animation": "slide-left"}
      ]
    },
    "responsive": {
      "mobile": {
        "breakpoint": "<768px",
        "navigation": "bottom-tabs",
        "layout": "single-column",
        "gestures": "enabled"
      },
      "tablet": {
        "breakpoint": "768px-1024px",
        "navigation": "side-rail",
        "layout": "split-view",
        "gestures": "limited"
      }
    },
    "accessibility": {
      "standards": ["WCAG 2.1 AA"],
      "screenReader": [
        "Semantic HTML elements",
        "ARIA labels and descriptions",
        "Focus management",
        "Live regions for dynamic content"
      ],
      "keyboardNav": [
        "Tab order logical",
        "Skip links available",
        "All interactive elements focusable",
        "Custom keyboard shortcuts"
      ],
      "colorContrast": {
        "text": "4.5:1 minimum",
        "largeText": "3:1 minimum",
        "nonText": "3:1 minimum"
      }
    }
  }
}
```

---

## ⚙️ Instructions for Cursor

**When building UI components, always reference this document to ensure:**

- Components match design system specifications
- Interactions follow defined patterns
- Responsive behavior is implemented correctly
- Accessibility standards are met
- Navigation follows established structure

**Before implementing new UI elements:**

1. Check if component already exists in the system
2. Follow atomic design principles
3. Implement all required states and variants
4. Test across defined breakpoints
5. Validate accessibility compliance

**Component Development Checklist:**

- [ ]  Follows design system tokens
- [ ]  Implements all variants and states
- [ ]  Responsive across breakpoints
- [ ]  Accessible (ARIA, keyboard, contrast)
- [ ]  Proper TypeScript types
- [ ]  Interactive states (hover, focus, active)
- [ ]  Error and loading states
- [ ]  Performance optimized

---

*📄 Export this as `ui-specifications.json` for Cursor ingestion*