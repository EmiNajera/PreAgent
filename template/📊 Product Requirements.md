# 📊 Product Requirements

*Core document for defining users, problems, features, and exclusions*

---

## 🌿 JSON Structure for Cursor

```json
{
  "productRequirements": {
    "projectName": "",
    "version": "1.0",
    "lastUpdated": "",
    "targetUsers": {
      "primaryPersona": {
        "name": "",
        "demographics": "",
        "painPoints": [],
        "goals": [],
        "techSavviness": ""
      },
      "secondaryPersonas": []
    },
    "problemStatement": {
      "primaryProblem": "",
      "problemContext": "",
      "currentSolutions": [],
      "limitations": []
    },
    "coreFeatures": {
      "mustHave": [
        {
          "feature": "",
          "description": "",
          "userStory": "",
          "acceptanceCriteria": [],
          "priority": "P0"
        }
      ],
      "shouldHave": [],
      "couldHave": []
    },
    "exclusions": {
      "outOfScope": [],
      "futureVersions": [],
      "deliberatelyExcluded": []
    },
    "successMetrics": {
      "userAcquisition": [],
      "engagement": [],
      "retention": [],
      "revenue": []
    }
  }
}
```

---

## 📋 Template Instructions

### 🎯 Target Users

**Define who you're building for:**

- Primary persona (80% of users)
- Demographics, pain points, goals
- Technical proficiency level
- Secondary personas (edge cases)

### 🔄 Problem Statement

**Clearly articulate the problem:**

- What specific problem does this solve?
- When/where do users experience this?
- What do they currently do instead?
- Why are current solutions inadequate?

### ✨ Core Features

**Prioritized feature breakdown:**

- **Must Have (P0):** Core value proposition
- **Should Have (P1):** Important but not MVP
- **Could Have (P2):** Nice to have

### ❌ Exclusions

**Be explicit about what you're NOT building:**

- Out of scope for this version
- Planned for future versions
- Deliberately excluded features

### 📈 Success Metrics

**How will you measure success:**

- User acquisition targets
- Engagement benchmarks
- Retention goals
- Revenue objectives

---

## 🏷️ Example: Clinic Management App

```json
{
  "productRequirements": {
    "projectName": "ClinicPro",
    "version": "1.0",
    "lastUpdated": "2026-06-15",
    "targetUsers": {
      "primaryPersona": {
        "name": "Dr. Sarah Chen, Clinic Owner",
        "demographics": "35-45 years, MD, runs a private practice with 8 staff, medium-sized city.",
        "painPoints": [
          "Patient records are scattered across paper files and spreadsheets.",
          "Appointment scheduling causes frequent double-booking and no-shows.",
          "Inventory management is manual — running out of supplies unexpectedly."
        ],
        "goals": [
          "Centralize all patient data in one digital system.",
          "Automate appointment reminders to reduce no-shows by 50%.",
          "Track inventory in real-time with low-stock alerts."
        ],
        "techSavviness": "Medium"
      },
      "secondaryPersonas": [
        {
          "name": "Maria, Front Desk Receptionist",
          "description": "25-35 years, high school diploma, comfortable with basic computer use. Needs an intuitive interface."
        },
        {
          "name": "Dr. James Park, Part-time Physician",
          "description": "40-55 years, specialist, works at the clinic 3 days a week. Needs quick access to patient histories."
        }
      ]
    },
    "problemStatement": {
      "primaryProblem": "Clinic operations rely on disconnected manual processes, causing administrative overhead, data loss, and patient dissatisfaction.",
      "problemContext": "Staff spend 30% of their time on paperwork. Patients wait longer because information isn't readily available.",
      "currentSolutions": [
        "Paper charts and forms",
        "Google Sheets for scheduling",
        "Physical logbook for inventory"
      ],
      "limitations": [
        "No centralized patient history",
        "Frequent scheduling conflicts",
        "No inventory visibility until stock runs out",
        "No automated patient communication"
      ]
    },
    "coreFeatures": {
      "mustHave": [
        {
          "feature": "Patient Profiles",
          "description": "Digital medical records with complete visit history.",
          "userStory": "As a receptionist, I want to create a patient profile in under 2 minutes to streamline check-in.",
          "acceptanceCriteria": [
            "Register name, age, phone, reason for visit, medical history.",
            "Attach documents (PDFs, images) to patient records.",
            "Search patients by name, phone, or ID."
          ],
          "priority": "P0"
        },
        {
          "feature": "Appointment Scheduling",
          "description": "Visual calendar for managing appointments by doctor and room.",
          "userStory": "As a receptionist, I want to see real-time availability to book appointments without conflicts.",
          "acceptanceCriteria": [
            "Day, week, and month views.",
            "Automated SMS/email reminders.",
            "Appointments linked to patient profiles."
          ],
          "priority": "P0"
        },
        {
          "feature": "Inventory Management",
          "description": "Track medical supplies and medications with low-stock alerts.",
          "userStory": "As a clinic manager, I want low-stock alerts so I never run out of critical supplies.",
          "acceptanceCriteria": [
            "Record SKU, description, quantity, and reorder threshold.",
            "Automatic alerts when stock falls below threshold.",
            "Inventory usage reports."
          ],
          "priority": "P0"
        }
      ],
      "shouldHave": [
        {
          "feature": "Billing & Invoices",
          "description": "Generate invoices and track payments.",
          "priority": "P1"
        },
        {
          "feature": "Reporting Dashboard",
          "description": "Key metrics: appointments per day, revenue, patient volume.",
          "priority": "P1"
        }
      ],
      "couldHave": [
        {
          "feature": "Patient Portal",
          "description": "Patients can view their history and upcoming appointments online.",
          "priority": "P2"
        },
        {
          "feature": "Telemedicine Integration",
          "description": "Video call scheduling and integration.",
          "priority": "P2"
        }
      ]
    },
    "exclusions": {
      "outOfScope": [
        "Insurance claim processing (MVP)",
        "HR/Payroll management"
      ],
      "futureVersions": [
        "Patient self-check-in kiosk",
        "Integration with insurance APIs",
        "Mobile app for patients"
      ],
      "deliberatelyExcluded": [
        "Full EHR compliance — this is a clinic management tool, not a hospital system"
      ]
    },
    "successMetrics": {
      "userAcquisition": [
        "100% staff adoption within first month"
      ],
      "efficiency": [
        "50% reduction in patient check-in time",
        "30% reduction in no-shows through automated reminders"
      ],
      "accuracy": [
        "Zero scheduling conflicts after first week",
        "99% inventory accuracy"
      ]
    }
  }
}
```

---
---

## ⚙️ Instructions for Cursor

**When working on features, always reference this document to ensure:**

- Features align with target user needs
- Implementation serves the core problem
- Nothing conflicts with explicit exclusions
- Success metrics can be tracked

---

*📄 Export this as `product-requirements.json` for Cursor ingestion*