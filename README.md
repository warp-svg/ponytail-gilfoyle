<p align="center">
  <img src="assets/gilfoyle.svg" width="640" alt="Gilfoyle, the senior systems engineer who replaces your fifty lines with one">
</p>

<h1 align="center">gilfoyle</h1>

<p align="center">
  <em>He says nothing. He deletes your class. It still works. He does not explain why.</em>
</p>

<p align="center">
  <strong>80–94% less code &middot; 3–6&times; faster &middot; 47–77% cheaper</strong><br>
  <sub>Reported by the original <a href="https://github.com/DietrichGebert/ponytail">ponytail</a> benchmarks (median of 10 runs across Haiku, Sonnet, and Opus).</sub>
</p>

---

## What this is

This is a **Gilfoyle-voiced reskin** of [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) — the agent skill that forces the laziest solution that actually works.

The logic is untouched. The decision ladder, the intensity levels, the safety carve-outs, the test discipline — all identical and fully functional. The only thing that changed is the prose, which now carries the deadpan, sardonic, contemptuous-of-busywork energy of Bertram Gilfoyle from HBO's *Silicon Valley*. The YAGNI ladder was always his worldview. We just gave it his voice.

All credit for the actual skill — the ladder, the benchmarks, the cross-agent plumbing — belongs to [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail). Go star the original.

## How it works

Before writing code, the agent stops at the first rung that holds:

```
1. Does this need to exist?   → no: skip it (YAGNI)
2. Stdlib does it?            → use it
3. Native platform feature?   → use it
4. Installed dependency?      → use it
5. One line?                  → one line
6. Only then: the minimum that works
```

Lazy, not negligent: **trust-boundary validation, data-loss handling, security, and accessibility are never on the chopping block.** Contempt for busywork does not extend to the things that page you at 3am.

## Before / after

You ask for a date picker. Your agent installs flatpickr, writes a wrapper component, adds a stylesheet, and opens a discussion about timezones.

With gilfoyle:

```html
<!-- gilfoyle: the browser already has one. you knew that. -->
<input type="date">
```

## Install

This repo ships the skill at [`skills/gilfoyle/SKILL.md`](skills/gilfoyle/SKILL.md).

### Claude Code

Drop the skill into your skills directory:

```bash
git clone https://github.com/warp-svg/ponytail-gilfoyle
cp -r ponytail-gilfoyle/skills/gilfoyle ~/.claude/skills/gilfoyle
```

It activates on the same intents as ponytail — say "gilfoyle", "be lazy", "lazy mode", "simplest solution", "yagni", "do less", "shortest path", or just complain about over-engineering, bloat, boilerplate, or unnecessary dependencies.

### Levels

```
/gilfoyle lite     # name the lazier path, let the user pick
/gilfoyle full     # the ladder enforced (default)
/gilfoyle ultra    # for when the codebase has wronged you personally
```

For the full multi-agent install matrix (Codex, Copilot CLI, Gemini, OpenCode, Cursor, Windsurf, etc.), see the [upstream ponytail README](https://github.com/DietrichGebert/ponytail#install) — the mechanics are identical, only the skill name and voice differ.

## Credits

- **Original skill:** [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) — MIT.
- **Reskin:** voice, framing, and avatar swapped to Bertram Gilfoyle. Logic preserved verbatim.
- **Character:** Bertram Gilfoyle is a character from HBO's *Silicon Valley*. This is an unofficial fan reskin, not affiliated with HBO.

## License

[MIT](https://github.com/DietrichGebert/ponytail/blob/main/LICENSE), inherited from the original. The shortest license that works.
