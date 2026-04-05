# DDD Screen Checklist

Run this checklist before shipping any new or modified screen.

## The 2-Second Test

- [ ] A new user can understand what to do within 2 seconds
- [ ] There is exactly ONE primary action that is visually dominant
- [ ] The primary action can be reached with one thumb (bottom 60% of screen)

## Text

- [ ] No user-facing text block is longer than 15 words
- [ ] Labels are 1-3 words max
- [ ] No paragraph-length descriptions (use AI coach instead)
- [ ] Button text is a verb: "Start", "Save", "Send" -- not "Submit" or "OK"

## States

- [ ] Empty state has a clear CTA (never just "No items found")
- [ ] Loading state shows contextual progress (not a blank screen)
- [ ] Error state tells the user what to do, not what went wrong
- [ ] First-visit state teaches in context (no tutorial modals)
- [ ] Returning-visit state skips teaching, shows relevant content

## AI Presence (AI-first apps only)

- [ ] Screen has a coach/AI presence point
- [ ] AI message is contextual to current data state
- [ ] AI message is 1-2 sentences max
- [ ] AI avatar + name + color are visible
- [ ] First-visit message is different from return-visit message
- [ ] Message uses trainer persona voice, not generic text

## Layout

- [ ] Maximum 3 colors on screen (background, text, accent)
- [ ] No competing CTAs at the same visual weight
- [ ] Touch targets are at least 44x44pt
- [ ] Content scrolls; navigation doesn't
- [ ] Back button or clear exit path exists

## Performance

- [ ] Screen renders within 300ms (no white flash)
- [ ] Lists use virtualization (FlatList, not ScrollView + map)
- [ ] Images have explicit dimensions (no layout shift)
- [ ] No unnecessary re-renders (check with React DevTools)

## The Final Test

Ask yourself: could I use this screen at 2 AM, tired, one eye open, after a long day?

If the answer is "probably, but I'd have to think about it" -- simplify.
