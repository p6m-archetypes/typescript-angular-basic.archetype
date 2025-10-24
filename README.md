# TypeScript Angular Application Archetype

![Latest Release](https://img.shields.io/github/v/release/p6m-archetypes/typescript-angular-basic.archetype?style=flat-square&label=Latest%20Release&color=blue)

Modern Angular application archetype with TypeScript, standalone components, and Kubernetes deployment configuration.

## 🎯 What This Generates

This archetype creates an Angular application with:

- **⚡ Angular 17+**: Modern Angular with standalone components and signals
- **🎨 TypeScript**: Full type safety across the application
- **🔧 Angular CLI**: Official tooling for development and builds
- **🧪 Testing Setup**: Jasmine and Karma configured for unit testing
- **🐳 Container-Ready**: Docker and Kubernetes deployment manifests
- **📦 Modern Tooling**: ESLint, Prettier, and Angular DevTools support

## 📦 Generated Project Structure

```
my-customer-frontend/
├── src/
│   ├── app/                # Application components and modules
│   ├── assets/             # Static assets (images, styles)
│   ├── environments/       # Environment configurations
│   └── index.html
├── k8s/                     # Kubernetes manifests
├── Dockerfile
├── angular.json             # Angular CLI configuration
└── package.json
```

## 🚀 Quick Start

### Prerequisites

- [Archetect](https://archetect.github.io/) CLI tool
- Node.js 18+ and npm
- Docker (optional, for containerized deployment)

### Generate a New Application

```bash
archetect render https://github.com/p6m-archetypes/typescript-angular-basic.archetype.git#v1

# Example prompt answers:
# org-name: acme-inc
# project-title: Customer Portal
# project-prefix: customer
# Result: customer-frontend/
```

### Development Workflow

```bash
cd customer-frontend

# 1. Install dependencies
npm install

# 2. Run development server
npm start

# 3. Run tests
npm test

# 4. Build for production
npm run build

# 5. Access application
# - Development: http://localhost:4200
```

## 📋 Configuration Prompts

| Property | Description | Example |
|----------|-------------|---------|
| `org-name` | GitHub organization or username | acme-inc |
| `project-title` | Display name for the application | Customer Portal |
| `project-prefix` | Project identifier (suffix '-frontend' added automatically) | customer |

## ✨ Key Features

### 🏛️ Angular Features

- **Standalone Components**: Modern component architecture without NgModules
- **Angular Router**: Client-side routing with lazy loading support
- **RxJS**: Reactive programming for async operations
- **Signals**: New reactive primitives for state management
- **Dependency Injection**: Powerful DI system for service architecture

### 🎨 Developer Experience

- **TypeScript**: Full type safety with strict mode
- **Hot Reload**: Instant updates during development with Angular CLI
- **ESLint**: Code quality with Angular-specific rules
- **Prettier**: Consistent code formatting
- **Angular DevTools**: Browser extension for debugging

### 🧪 Testing

- **Jasmine**: BDD-style unit testing framework
- **Karma**: Test runner with browser automation
- **Component Testing**: TestBed for Angular component testing
- **E2E Ready**: Can integrate Cypress or Playwright

### 🚢 Deployment

- **Docker**: Production-ready Nginx-based container
- **Kubernetes**: Deployment and Service manifests
- **Environment Configuration**: Build-time environment switching
- **Optimized Builds**: AOT compilation and tree-shaking

## 🎯 Use Cases

This archetype is ideal for:

1. **Enterprise Applications**: Large-scale applications with complex state management
2. **Admin Dashboards**: Internal tools with rich data visualization
3. **Progressive Web Apps**: Applications requiring offline support and native features
4. **Customer Portals**: Client-facing applications with authentication and authorization

## 🔌 Backend Integration Patterns

This frontend application typically consumes:

1. **GraphQL Gateways**: Primary recommended pattern
   - Unified GraphQL API aggregating multiple backend services
   - Client-driven queries reduce over-fetching
   - Single endpoint simplifies frontend architecture
   - Real-time updates via GraphQL subscriptions

2. **REST APIs**: Traditional HTTP/JSON services
   - Public REST APIs with OpenAPI documentation
   - Direct service-to-frontend communication
   - Standard HTTP verbs (GET, POST, PUT, DELETE)
   - Works well for simple CRUD operations

3. **Backend-for-Frontend (BFF)**: Dedicated backend for this frontend
   - Custom API tailored to this application's needs
   - Can be GraphQL or REST
   - Aggregates multiple services on the backend
   - Optimizes payload size and query patterns

**Architecture Examples**:

**Option 1: GraphQL Gateway (Recommended)**
```
Angular App → GraphQL Gateway → gRPC/REST Services
```

**Option 2: Direct REST API**
```
Angular App → REST Services → Database
```

**Option 3: BFF Pattern**
```
Angular App → Dedicated BFF (GraphQL/REST) → Multiple Services
```

## 🔗 Related Archetypes

- **[TypeScript Next.js](../typescript-nextjs-basic.archetype)** - React with SSR for SEO-focused apps
- **[TypeScript Vue.js](../typescript-vuejs-basic.archetype)** - Lightweight alternative with progressive adoption
- **[TypeScript Svelte](../typescript-svelte-basic.archetype)** - Compiled framework with minimal runtime

## 📄 License

MIT License

---

**Build powerful enterprise applications with Angular!** 🚀
