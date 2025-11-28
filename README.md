# BuildMyAiAgent

> A production-ready visual platform for designing, testing, and deploying custom AI agents with zero-code workflow automation

<div align="center">

![Next.js](https://img.shields.io/badge/Next.js%2015-black?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React%2019-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Convex](https://img.shields.io/badge/Convex-FF4785?style=for-the-badge)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)

[Live Demo](#) · [Report Bug](https://github.com/abhishekboadgurjar/BuildMyAiAgent/issues) · [Request Feature](https://github.com/abhishekboadgurjar/BuildMyAiAgent/issues)

</div>

---

## 🎯 Project Overview

BuildMyAiAgent empowers users to create sophisticated AI-powered automation workflows through an intuitive visual interface. Built with modern full-stack architecture, it demonstrates enterprise-level patterns for realtime collaboration, serverless computing, and intelligent agent orchestration.

**Author:** Abhishek Gurjar — [GitHub Profile](https://github.com/abhishekboadgurjar)

---

## ✨ Core Features

### Visual Workflow Engine
- **Drag-and-drop node editor** powered by @xyflow/react for intuitive agent design
- **Custom node library** including API calls, conditional logic, loops, and approval gates
- **Real-time canvas** with auto-save and collaborative editing capabilities
- **Visual debugging** with execution path highlighting and error tracking

### Intelligent Agent System
- **LLM Integration** with OpenAI for natural language processing
- **Multi-step workflows** supporting complex business logic
- **API orchestration** with built-in HTTP client and response handling
- **State management** across workflow execution with context preservation

### Production Infrastructure
- **Secure authentication** via Clerk with SSO and MFA support
- **Serverless backend** using Convex for automatic scaling
- **Real-time sync** enabling instant updates across users
- **Type-safe API layer** with end-to-end TypeScript coverage

### Developer Experience
- **Interactive testing** environment with live agent preview
- **Comprehensive logging** for debugging workflow execution
- **Export/import** workflows as JSON for version control
- **Responsive UI** built with Tailwind CSS utility classes

---

## 🛠️ Technical Architecture

### Frontend Stack
```
Next.js 15 (App Router)     → SSR/SSG hybrid rendering
React 19                    → Modern concurrent features
TypeScript                  → Type safety across codebase
Tailwind CSS                → Utility-first styling
@xyflow/react               → Flow-based visual editor
Lucide React                → Consistent icon system
Recharts                    → Data visualization
```

### Backend & Services
```
Convex                      → Realtime serverless functions
Clerk                       → Authentication & user management
OpenAI API                  → LLM-powered intelligence
Arcjet                      → Security & rate limiting
```

### Key Architectural Decisions

**Why Next.js App Router?**  
Leverages React Server Components for optimal performance, streaming SSR for faster TTFB, and simplified data fetching patterns that reduce client-side JavaScript.

**Why Convex?**  
Provides automatic real-time subscriptions, optimistic updates out-of-the-box, and eliminates the need for separate REST/GraphQL API layer with fully typed client-server communication.

**Why Clerk?**  
Production-ready auth with zero backend code, built-in UI components, and seamless JWT integration with our serverless architecture.

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        Client Layer                          │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │ Agent Builder│  │ Dashboard UI │  │  Auth Pages  │      │
│  │  (@xyflow)   │  │   (Recharts) │  │   (Clerk)    │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
└─────────────────────────────────────────────────────────────┘
                            │
                            │ HTTP/WebSocket
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                     Next.js API Layer                        │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │ Agent Chat   │  │ Config Gen   │  │ Webhook API  │      │
│  │   Routes     │  │   Routes     │  │   Routes     │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
└─────────────────────────────────────────────────────────────┘
                            │
                ┌───────────┴───────────┐
                ▼                       ▼
┌──────────────────────┐    ┌──────────────────────┐
│   Convex Backend     │    │   External APIs      │
│  ┌────────────────┐  │    │  ┌────────────────┐  │
│  │ Agents Schema  │  │    │  │  OpenAI API    │  │
│  │ Users Schema   │  │    │  │  Custom APIs   │  │
│  │ Workflows DB   │  │    │  └────────────────┘  │
│  └────────────────┘  │    └──────────────────────┘
└──────────────────────┘
```

---

## 🚀 Full-Stack Skills Demonstrated

### Frontend Engineering
- ✅ **Modern React Patterns**: Hooks, Context API, Server/Client Components
- ✅ **Complex State Management**: Multi-step form flows, canvas state synchronization
- ✅ **Performance Optimization**: Code splitting, lazy loading, memoization strategies
- ✅ **Responsive Design**: Mobile-first approach with Tailwind breakpoints
- ✅ **Advanced UI/UX**: Custom drag-and-drop, keyboard shortcuts, visual feedback

### Backend Development
- ✅ **Serverless Architecture**: Function-as-a-Service patterns with Convex
- ✅ **API Design**: RESTful endpoints, WebSocket connections, error handling
- ✅ **Database Modeling**: Relational schema design with Convex types
- ✅ **Real-time Features**: Live updates, optimistic UI, conflict resolution
- ✅ **External Integrations**: OpenAI SDK, HTTP clients, webhook handling

### DevOps & Infrastructure
- ✅ **Environment Management**: Multi-stage configuration (.env patterns)
- ✅ **Type Safety**: End-to-end TypeScript with Convex generated types
- ✅ **Security**: Authentication flows, API key management, rate limiting
- ✅ **Deployment**: Vercel integration, CI/CD ready structure
- ✅ **Monitoring**: Error boundaries, logging strategies, debugging tools

### Software Engineering Practices
- ✅ **Clean Architecture**: Separation of concerns, modular component design
- ✅ **Code Quality**: ESLint configuration, TypeScript strict mode
- ✅ **Documentation**: Inline comments, README, architecture diagrams
- ✅ **Version Control**: Git workflow, semantic commits, branching strategy
- ✅ **Scalability**: Stateless design, horizontal scaling considerations

---

## 📂 Project Structure

```
ai-agent-builder/
├── app/
│   ├── (auth)/                    # Authentication routes
│   │   ├── sign-in/              # Clerk sign-in page
│   │   └── sign-up/              # Clerk sign-up page
│   ├── agent-builder/            # Visual workflow editor
│   │   ├── _customNodes/         # Custom node components
│   │   └── [id]/                 # Dynamic agent routes
│   ├── api/                      # API route handlers
│   │   ├── agent-chat/           # LLM chat integration
│   │   └── config-gen/           # Configuration endpoints
│   ├── dashboard/                # User dashboard
│   ├── provider.tsx              # Context providers (Clerk + Convex)
│   └── layout.tsx                # Root layout with providers
├── convex/
│   ├── schema.ts                 # Database schema definitions
│   ├── agents.ts                 # Agent CRUD operations
│   ├── users.ts                  # User management functions
│   └── http.ts                   # HTTP actions
├── components/
│   ├── ui/                       # Reusable UI components
│   └── features/                 # Feature-specific components
├── lib/
│   └── utils.ts                  # Utility functions
├── public/                       # Static assets
└── types/                        # TypeScript type definitions
```

---

## 🔧 Local Development Setup

### Prerequisites
- Node.js 18+ and pnpm (or npm/yarn)
- Clerk account for authentication
- Convex account for backend
- OpenAI API key

### Installation Steps

1. **Clone the repository**
```bash
git clone https://github.com/abhishekboadgurjar/ai-agent-builder.git
cd ai-agent-builder
```

2. **Install dependencies**
```bash
pnpm install
```

3. **Configure environment variables**

Create `.env.local` in the project root:

```env
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxx
CLERK_SECRET_KEY=sk_test_xxxxxxxxxxxxx

# Convex Backend
NEXT_PUBLIC_CONVEX_URL=https://your-project.convex.cloud
CONVEX_DEPLOY_KEY=prod:your-project|xxxxxxxx

# OpenAI Integration
OPENAI_API_KEY=sk-xxxxxxxxxxxxx

# Optional: Arcjet Security
ARCJET_KEY=ajkey_xxxxxxxxxxxxx
```

4. **Initialize Convex backend**
```bash
npx convex dev
```

5. **Start development server**
```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) to see the application.

---

## 🌐 Deployment Guide

### Vercel Deployment (Recommended)

1. **Connect your repository** to Vercel
2. **Configure environment variables** in Vercel dashboard
3. **Deploy** from main branch

```bash
vercel --prod
```

### Convex Production Deployment

```bash
npx convex deploy --prod
```

Update your `NEXT_PUBLIC_CONVEX_URL` to the production URL.



## 🤝 Contributing

Contributions are highly appreciated! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Contribution Guidelines
- Follow existing code style and TypeScript patterns
- Add comments for complex logic
- Update documentation for new features
- Test your changes locally before submitting

---

## 📝 License

This project is available under the MIT License. See `LICENSE` file for details.

---

## 🙏 Acknowledgments

- **Next.js Team** for the incredible App Router architecture
- **Convex** for simplifying real-time backend development
- **Clerk** for seamless authentication
- **xyflow** for the powerful node-based editor

---

## 📬 Contact & Support

**Abhishek Gurjar**
- GitHub: [@abhishekboadgurjar](https://github.com/abhishekboadgurjar)
- Portfolio: [Link](https://abhishekboadgurjar.vercel.app/)

**Project Link:** [https://github.com/abhishekboadgurjar/BuildMyAiAgent](https://github.com/abhishekboadgurjar/BuildMyAiAgent)

---

<div align="center">

**⭐ Star this repo if you find it useful!**

Made with ❤️ by Abhishek Gurjar

</div>
