# {PROJECT_NAME} -- AI Context

> This file gives AI coding assistants full context about this project.
> Drop it in your repo root. Reference it from your Cursor rules or paste it into conversations.

## What Is This Project?

{1-3 sentences describing what the app/service does, who it's for, and what makes it different.}

**Example:** *Ironclub is an AI-first fitness app where an AI trainer coaches users through every aspect of their workout journey -- from building plans to teaching form to tracking progress. The trainer persona is the primary interface, not a feature bolted onto a traditional app.*

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | {e.g., React Native + Expo} |
| Backend | {e.g., Node.js + Serverless} |
| Database | {e.g., WatermelonDB (local), DynamoDB (cloud)} |
| Auth | {e.g., Cognito + Google/Apple SSO} |
| AI | {e.g., OpenAI GPT-4o via custom service} |
| Payments | {e.g., RevenueCat} |

## Architecture

```
{Brief ASCII or mermaid diagram of how the pieces connect}
```

## Core Entities

| Entity | Description | Key Fields |
|--------|-------------|------------|
| {User} | {What it represents} | {id, email, trainerId, ...} |
| {Workout} | {What it represents} | {id, name, days, status, ...} |
| ... | ... | ... |

## Navigation / Routes

{Describe the main user flows and how screens/pages connect}

```
{Route tree or flow diagram}
```

## Design System

| Token | Value | Usage |
|-------|-------|-------|
| Primary Color | {#hex} | {Main actions, links} |
| Background | {#hex} | {Screen backgrounds} |
| Text | {#hex} | {Body text} |
| Accent | {#hex} | {Highlights, badges} |
| Font | {Name} | {All text} |
| Spacing unit | {8px} | {All spacing is multiples of this} |

## Key Patterns

### {Pattern 1: e.g., "AI Persona System"}
{How it works, where the config lives, how to add to it}

### {Pattern 2: e.g., "Offline-First Data"}
{How sync works, conflict resolution, data flow}

### {Pattern 3: e.g., "Component Library"}
{Where components live, naming conventions, how to create new ones}

## Services & APIs

| Service | Purpose | Base URL |
|---------|---------|----------|
| {ai-service} | {Chat, workout generation} | {/v1/chat, /v1/analyze} |
| {ironclub-backend} | {CRUD, sync} | {/api/v1/...} |

## File Structure

```
src/
├── screens/          # One file per screen
├── components/       # Reusable UI components
│   ├── ui/           # Design system primitives
│   └── {domain}/     # Domain-specific components
├── hooks/            # Custom React hooks
├── services/         # API clients, business logic
├── config/           # App configuration, constants
├── context/          # React Context providers
├── navigation/       # Route definitions
└── assets/           # Images, fonts
```

## DDD Rules for This Project

1. {Project-specific DDD rule, e.g., "The AI trainer speaks on every screen via CoachBubble"}
2. {Project-specific DDD rule, e.g., "No empty states without a coach CTA"}
3. {Project-specific DDD rule, e.g., "All user-facing text must be <15 words"}

## Current State & Known Issues

{What's working, what's not, what's being actively developed. Update this as the project evolves.}

## How to Run

```bash
{Commands to install, configure, and run the project}
```
