# 🏗️ Technical Architecture

*Core document for tech stack, database schema, API structure, and file organization*

---

## 🌿 JSON Structure

```json
{
  "technicalArchitecture": {
    "projectDetails": {
      "projectName": "[Your App Name]",
      "version": "1.0",
      "lastUpdated": "[YYYY-MM-DD]"
    },
    "techStack": {
      "frontend": {
        "framework": "[React / Next.js / Vue / etc.]",
        "language": "[TypeScript / JavaScript]",
        "styling": "[Tailwind CSS / Styled Components / etc.]",
        "stateManagement": "[Zustand / Redux / Context API]",
        "buildTool": "[Vite / Webpack / Turbopack]"
      },
      "backend": {
        "runtime": "[Node.js / Python / Go / etc.]",
        "framework": "[Express / FastAPI / Next.js API routes / etc.]",
        "language": "[TypeScript / Python / Go]",
        "orm": "[Prisma / Drizzle / SQLAlchemy / etc.]",
        "authentication": "[NextAuth / Clerk / Supabase Auth / Auth0]",
        "apiStyle": "[REST / GraphQL / tRPC]"
      },
      "database": {
        "primary": "[PostgreSQL / MongoDB / MySQL]",
        "cache": "[Redis / none]",
        "fileStorage": "[Cloudinary / AWS S3 / Supabase Storage / local]"
      },
      "deployment": {
        "hosting": "[Vercel / Railway / AWS / Supabase]",
        "ciCd": "[GitHub Actions / GitLab CI]",
        "monitoring": "[Sentry / LogRocket / none]"
      }
    },
    "databaseSchema": {
      "tables": [
        {
          "name": "[EntityName]",
          "columns": [
            {"name": "id", "type": "UUID", "constraints": "PRIMARY KEY DEFAULT gen_random_uuid()"},
            {"name": "[field]", "type": "[DATA_TYPE]", "constraints": "[NOT NULL / UNIQUE / etc.]"},
            {"name": "created_at", "type": "TIMESTAMP", "constraints": "DEFAULT NOW()"},
            {"name": "updated_at", "type": "TIMESTAMP", "constraints": "DEFAULT NOW()"}
          ]
        }
      ],
      "relationships": [
        "[EntityA] has many [EntityB]",
        "[EntityB] belongs to [EntityA]"
      ]
    },
    "apiStructure": {
      "baseUrl": "https://api.[yourapp].com/v1",
      "authentication": {
        "type": "Bearer Token / Session Cookie",
        "provider": "[NextAuth / Clerk / Supabase Auth]"
      },
      "endpoints": {
        "[resource]": [
          "GET    /api/[resource]        — List all",
          "GET    /api/[resource]/:id    — Get by ID",
          "POST   /api/[resource]        — Create",
          "PUT    /api/[resource]/:id    — Update",
          "DELETE /api/[resource]/:id    — Delete"
        ]
      },
      "errorFormat": {
        "error": "string",
        "message": "string",
        "code": "integer",
        "details": {}
      }
    },
    "fileStructure": {
      "app": ["(routes)", "api/", "layout.tsx", "globals.css"],
      "components": ["ui/", "forms/", "layout/", "[feature]/"],
      "lib": ["db.ts", "auth.ts", "utils.ts", "validators.ts"],
      "types": ["index.ts"],
      "conventions": {
        "components": "PascalCase (Button.tsx)",
        "utilities": "camelCase (formatDate.ts)",
        "constants": "UPPER_CASE (API_BASE_URL)",
        "routes": "kebab-case (/patient-profile)"
      }
    }
  }
}
```

---

## 📋 Template Instructions

### 🏗️ Tech Stack
Define every tool and library. Be specific — the agent will enforce these boundaries.

### 📦 Database Schema
List every table with columns, types, and constraints. Include relationships. This is the single source of truth for data.

### 🔌 API Structure
Define endpoints, auth method, and error format. Consistency here prevents chaos later.

### 📁 File Structure
Where does each type of code live? Naming conventions? The agent will follow this exactly.

---

*📄 Export as `technical-architecture.json` — place in project root alongside `product-requirements.json` and `tasks.md`*
