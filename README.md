# DDD -- Drunk Driven Development

> If someone who's half asleep, distracted, or three beers deep can't figure out what to do on your screen within 2 seconds -- the design has failed.

DDD is a development philosophy disguised as a joke. It's a framework for building software that **respects the user's brain** by refusing to waste it. It's also a reminder that the best ideas don't come from grinding -- they come from letting go.

This repo contains the manifesto, practical Cursor rules you can drop into any project, AI context templates, and bootstrapping guides.

---

## The Origin Story

3 AM. College. Exam at 5 AM in a different city. Can't memorize a single algorithm. Staring at the textbook like it's written in a dead language.

Then a spark. Something completely unrelated -- a SQL report for a sales app. A real problem. Something that actually mattered. Been stuck on it for two years. Suddenly, at 3 AM, with zero sleep and an exam in two hours -- the solution is obvious.

Fuck the exam. Implement it. It works.

Show up late. Barely pass. Can't even pronounce my own name. But the SQL works.

That night, pour a glass of Ballantine's -- the finest cheap whiskey money can buy. Another problem, one that's been hanging around for months. Morning comes. It just works.

**That's the moment.** The best code doesn't come from discipline. It comes from giving a shit about the right problem at the right time, and being relaxed enough to let your brain do its thing.

DDD is the formalization of that 3 AM spark.

---

## The Ritual

Before you write a single line of code, follow the ritual.

### Step 1: Pour

Pour yourself a big glass of what you love. Czech beer is the best. Single malt is recommended. Ballantine's if you're feeling nostalgic on a budget.

### Step 2: The German Beer Mug Rule

When you clink glasses -- with a friend, a coworker, or your own reflection -- you **look them in the eye**. This is the German/Czech tradition: maintain eye contact during the toast, or it's 7 years of bad luck.

This isn't about beer. It's about **presence**. Be here. Look at what you're building. Don't multitask. Don't check Slack. Don't scroll Twitter. Look the problem in the eye like you're clinking glasses with it.

### Step 3: Burger the Facts

**Bun. Patty. Bun.**

In DDD terms: **Beer. Single malt. Beer.**

Start light (the first beer -- get loose). Go deep (the single malt -- the real thinking). Come back light (the second beer -- review with fresh eyes).

This is also how you structure work:
1. **Light pass** -- sketch it, rough draft, no polish
2. **Deep pass** -- the real implementation, the hard decisions
3. **Light pass** -- step back, simplify, cut what doesn't belong

### Step 4: Now the Ideas Come

You can't force a spark. You can only create the conditions for one. The ritual isn't about alcohol -- it's about **permission to stop trying so hard**. The more you grind, the more you drown. Don't code too hard.

The solution to a problem you've been stuck on for months is often one relaxed evening away.

### Step 5: Make Money (Why Not?)

DDD isn't art for art's sake. Ship it. Charge for it. If you built something that works at 3 AM with a glass of whiskey, it's probably good enough for people to pay for.

---

## The Manifesto

### You are not building software. You are building a decision eliminator.

Every screen, every flow, every interaction should answer one question: **"What do I do right now?"** If the user has to think, you've failed. If they have to read instructions, you've really failed. If they need a tutorial, burn it down and start over.

The best software feels like talking to a smart friend who already knows what you need.

### The Five Laws

#### 1. One Screen, One Action

If there are 5 equally-weighted buttons, you have 0 buttons. Every screen has a **primary action** -- the thing 80% of users came here to do. Make it obvious. Make it big. Make everything else secondary.

```
Bad:  [Edit] [Share] [Delete] [Archive] [Export]
Good: [Start Workout]  ...  [more options]
```

#### 2. Zero Reading Required

Nobody reads. Not your labels, not your tooltips, not your onboarding carousel. The interface must communicate through **hierarchy, color, and position** -- not paragraphs.

If you must use text, keep it under the length of a text message. If a coach tip is longer than what fits on a phone screen without scrolling, cut it in half. Then cut it again.

```
Bad:  "Welcome to the exercise library. Here you can browse through our 
       collection of over 800 exercises, filter by muscle group, equipment 
       type, or difficulty level. Tap on any exercise to see detailed 
       instructions and form tips."

Good: "800+ exercises. Search or filter by muscle."
```

#### 3. The Thumb Test

Can you do everything with one thumb while holding a coffee in the other hand? No precise tapping on tiny targets. No hidden swipe gestures. No hamburger menus hiding critical features.

The bottom 60% of the screen is prime real estate. The top-left corner is a graveyard. Design accordingly.

#### 4. State-Aware Defaults

The app should already know what you want. Don't ask questions you can answer with data.

- Got a workout today? Show the play button.
- Finished? Show "done."
- No plan? Show "let's build one."
- Returning user? Skip the tutorial.
- First time on this screen? Teach by doing, not by telling.

Never present an empty state without a clear next step.

```
Bad:  "No workouts found."
Good: "No workouts yet. Want me to build one for you?" [Yes]
```

#### 5. The AI Is the UI

In AI-first apps, the AI isn't a feature -- it's the interface. Instead of labels, headers, section titles, and instructions, the AI persona *is* all of those things.

The user doesn't navigate menus. The AI guides them. The user doesn't read documentation. The AI teaches them. The user doesn't configure settings. The AI asks what they prefer.

```
Bad:  Section header: "Exercise Description"  
      Body: "Stand with feet shoulder-width apart..."

Good: [Coach avatar] Maya: "Plant your feet shoulder-width apart and 
       keep your core tight throughout the movement."
```

---

## The Anti-Patterns

### The Dashboard Trap
Building a dashboard with 12 metrics because "users might want to see them." They don't. They want to know one thing: **what should I do next?** Show that. Let them drill into data if they choose.

### The Settings Sprawl
56 settings because "power users need control." They don't. They need sane defaults. Every setting you add is an admission that you couldn't make the decision yourself.

### The Tutorial Carousel
5 screens explaining your app before letting users touch it. If your app needs a tutorial, fix the app. Teach in context, at the moment the user needs to know.

### The Feature Graveyard
Buttons that go to half-built features. Empty screens "coming soon." A navigation bar with 6 tabs. **If it's not ready, it doesn't exist.** Ship less, ship complete.

### The Confirmation Addiction
"Are you sure?" dialogs on every action. Undo is always better than confirm. Let users act, let them recover. Don't interrupt flow.

---

## DDD Applied: Decision Framework

When building any screen or feature, answer these in order:

| # | Question | If No... |
|---|----------|----------|
| 1 | Can a drunk person figure this out in 2 seconds? | Simplify |
| 2 | Is there exactly one obvious next action? | Remove or demote competing actions |
| 3 | Can I do this with one thumb? | Redesign the layout |
| 4 | Does the app already know the answer? | Use state-aware defaults |
| 5 | Can the AI say this instead of a UI element? | Replace with coach/AI persona |
| 6 | Is every word earning its place? | Cut text by 50% |
| 7 | Will this work on first use AND 100th use? | Balance teaching with efficiency |

---

## The Stack

DDD isn't about specific technologies. It's about **how you think**. But here's what makes it practical:

### For AI-First Apps
- **One AI persona, everywhere.** Not a chatbot on one screen. The AI is the voice of every screen.
- **Context over conversation.** The AI should know what screen you're on, what you just did, and what you probably want next.
- **Persona consistency.** The AI has a name, a voice, a visual identity. It's a character, not a feature.

### For Development Workflow
- **AI-assisted coding with context.** Your AI coding assistant should know your architecture, your patterns, your decisions. Feed it context files, not just code.
- **Ship fast, fix in context.** Don't plan for months. Build the screen, use it, feel what's wrong, fix it. DDD is iterative by nature.
- **Delete more than you add.** The best commit is the one that removes code. Every line is a liability.

---

## Project Structure

```
ddd/
├── README.md                          # This manifesto
├── cursor-rules/
│   ├── ddd-core.mdc                   # Core DDD principles for AI assistants
│   ├── ddd-ux.mdc                     # UX-specific rules
│   └── ddd-ai-first.mdc              # AI-first app development patterns
├── templates/
│   ├── AI_CONTEXT_TEMPLATE.md         # Template for project context files
│   └── SCREEN_CHECKLIST.md            # DDD checklist for new screens
├── guides/
│   └── BOOTSTRAP.md                   # How to start a DDD project
└── LICENSE
```

---

## Quick Start

1. **Read the Five Laws above.** Internalize them.
2. **Copy `cursor-rules/` into your project's `.cursor/rules/`** to have your AI assistant enforce DDD.
3. **Create an `AI_CONTEXT.md`** in your project root using the template. This gives your AI assistant the context it needs.
4. **Before every PR, run the DDD checklist** on each screen you touched.

---

## Philosophy

DDD comes from a simple truth: **the best work happens when you stop trying to be productive and start being honest.**

Honest about what problem actually matters. Honest about what's too complicated. Honest about what you'd actually use yourself at 2 AM.

The SQL report at 3 AM worked because it was a real problem that mattered. The algorithms for the exam didn't stick because they were someone else's problem. DDD is about building things that matter to you, in a way that matters to the person using them.

Fuck being normal. Fuck the rules. Be you.

Your grandma should be able to use your app. Your CEO should be able to use your app. Someone at 2 AM who just wants to log a workout should be able to use your app. Not because you removed features, but because you made the right feature obvious at the right time.

That's DDD. Pour yourself a glass, look the problem in the eye, and build something so simple that even you, three beers in at midnight, can ship a hotfix and not break production.

---

## The Zombie Test

The best currency in the universe is friendship. Not money. Not followers. Not connections. **True friendship.**

Here's the test: zombies are coming. Everyone for themselves. Your credit card won't help. Your yoga-good-morning guy won't show up. Your fake friend from the gaming lobby is gone.

Who saves you? Who saves your wife? Your kid?

That's your true friend. That's the person who shows up when everything else is stripped away.

**DDD is the zombie test for software.**

Strip away the dashboards, the settings pages, the onboarding carousels, the analytics, the A/B tests, the investor deck features. What's left?

If what's left is the ONE thing that actually helps someone -- that's your app. That's what survives. Everything else is decoration.

Build software like a true friend: it shows up when you need it, it doesn't waste your time, it has your back, and it doesn't pretend to be something it's not.

Fuck fake features. Fuck vanity metrics. Fuck building things to impress people who don't matter.

Build for the person at 2 AM who just needs the thing to work.

---

## License

MIT -- Take it, use it, make it yours.

## Contributing

Open an issue with a real example of DDD in action (or a DDD failure you fixed). PRs that add words get extra scrutiny. PRs that remove words get fast-tracked.

---

*"A spark. A reminder. Fuck being normal. Be you. Be you. Be you."*
