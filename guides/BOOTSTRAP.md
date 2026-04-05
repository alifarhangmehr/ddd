# Bootstrapping a DDD Project

How to start a new project with Drunk Driven Development from day one.

## Step 1: Define Your One Thing

Before writing any code, answer in one sentence:

> **What is the ONE thing a user comes to this app to do?**

Not three things. Not "it depends." One thing.

- Fitness app: **Start today's workout**
- Note app: **Write a note**
- Finance app: **See how much money I have**
- Chat app: **Send a message**

This becomes your default screen. Everything else orbits around it.

## Step 2: Map the Minimum Screens

You need fewer screens than you think. Start with the absolute minimum:

| Screen | Purpose | Primary Action |
|--------|---------|----------------|
| Home / Landing | The ONE thing | [Do the thing] |
| Create / Add | Make new content | [Save] |
| Detail / View | See one item deeply | [Act on it] |
| Settings | Account & preferences | [Back] |

That's 4 screens. If your app needs more than 8 screens at launch, you're building too much.

## Step 3: Set Up AI Context

1. Copy `templates/AI_CONTEXT_TEMPLATE.md` to your project root as `AI_CONTEXT.md`
2. Fill in every section -- this is how your AI assistant understands your project
3. Keep it updated as the project evolves

## Step 4: Install Cursor Rules

Copy the rules that apply to your project into `.cursor/rules/`:

```bash
# All projects
cp ddd/cursor-rules/ddd-core.mdc your-project/.cursor/rules/

# Projects with UI
cp ddd/cursor-rules/ddd-ux.mdc your-project/.cursor/rules/

# AI-first apps
cp ddd/cursor-rules/ddd-ai-first.mdc your-project/.cursor/rules/
```

## Step 5: Build the Landing Screen First

Don't build the auth flow. Don't build settings. Don't build onboarding.

Build the landing screen -- the ONE thing. Make it work. Make it feel right. Use it yourself 50 times. Then build the next most important screen.

### DDD Build Order

1. **Landing screen** -- the core experience
2. **Create flow** -- how users add content
3. **Detail view** -- how users consume content
4. **Auth** -- only now, and only what you need (guest mode first)
5. **Settings** -- last, minimal, sane defaults for everything

## Step 6: The DDD Review Loop

After building each screen, run the checklist from `templates/SCREEN_CHECKLIST.md`.

Then do the actual test: put down your phone, pick it up again, and try to do the thing on that screen in under 2 seconds. If you hesitate -- even for a moment -- something is wrong.

---

## AI-First Bootstrap: Extra Steps

If your app has an AI persona (coach, assistant, tutor):

### Define the persona early

Before building any screens, define:

| Attribute | Example |
|-----------|---------|
| Name | Maya |
| Role | Fitness coach |
| Tone | Warm, encouraging, concise |
| Avatar | 512x512 portrait |
| Color | #E8A838 (warm gold) |
| Emoji | ✨ |

### Create the config first

```
src/config/personas.ts    # All persona definitions
src/hooks/usePersona.ts   # Hook to load current persona
src/components/PersonaBubble.tsx  # Reusable presence component
```

This infrastructure goes in before any screens. Every screen will use it.

### The persona test

On every screen, ask: **"What would {persona name} say here?"**

If the answer is "nothing useful" -- the screen might not need AI presence. That's fine. Not every screen needs a coach bubble. But if the AI COULD say something helpful and you're showing a static label instead -- replace it.

---

## Common Mistakes in DDD Projects

### Starting with auth
Auth is boring. It's friction. Build the core experience first, let users try it as guests, then add auth when they have a reason to create an account (save data, sync across devices).

### Building a design system before building screens
You'll over-engineer components you don't need. Build 3 screens first, then extract the patterns into components. Design systems emerge from usage, not from planning.

### Adding features before polishing the core
If your landing screen isn't perfect, nothing else matters. Users won't discover your clever settings page if the first screen confused them.

### Over-planning
DDD is build-use-fix, not plan-plan-plan-build. A 20-page spec is the antithesis of DDD. Write 5 bullet points, build the thing, use it, iterate.
