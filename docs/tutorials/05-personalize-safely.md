# Tutorial 05: Personalize Safely

## Goal

Add persona and self-context without making the system hard to reuse.

## Steps

1. Install Core.
2. Copy everything inside `templates/packs/personalization/` into the vault root.
3. Edit:

```txt
99_System/Prompts/Personas/default.md
index/02_Areas/self_context.md
index/02_Areas/observer_profile.md
```

4. Keep private facts out of public templates.
5. Use `crystallize` before adding durable personal context to memory.

## Expected Result

Your assistant can adapt to your working style while the reusable system remains
portable.
