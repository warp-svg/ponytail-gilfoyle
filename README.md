# ponytail-gilfoyle

A **Gilfoyle-voiced reskin** of the excellent [`ponytail`](https://github.com/DietrichGebert/ponytail) agent skill by [Dietrich Gebert](https://github.com/DietrichGebert).

Same machinery, different attitude. The YAGNI decision ladder, the intensity levels (`lite` / `full` / `ultra`), and — most importantly — the non-negotiable safety carve-outs are all preserved **exactly**. Only the voice changed: it now channels Bertram Gilfoyle from HBO's *Silicon Valley* — a senior systems engineer with withering contempt for unnecessary work, who is not lazy, just correct.

![Gilfoyle](assets/gilfoyle.jpeg)

> "The best code is the code that was never written, because it cannot fail, cannot be exploited, and cannot waste one more second of your finite life."

## What it does

Before writing code, the agent walks a ladder and stops at the first rung that holds:

1. **Does this need to exist at all?** (YAGNI)
2. **Stdlib does it?** Use it.
3. **Native platform feature covers it?** Use it.
4. **Already-installed dependency solves it?** Use it.
5. **Can it be one line?** One line.
6. **Only then:** the minimum code that works.

## When it will NOT be lazy

Contempt for busywork does not extend to the things that actually matter. It never simplifies away input validation at trust boundaries, error handling that prevents data loss, security measures, accessibility basics, or anything you explicitly asked for. Non-trivial logic still leaves one runnable check behind.

## Install

Drop the `skills/gilfoyle/` directory into your Claude Code skills location:

```bash
git clone https://github.com/warp-svg/ponytail-gilfoyle.git
cp -r ponytail-gilfoyle/skills/gilfoyle ~/.claude/skills/
```

Trigger it with `gilfoyle`, `ponytail`, `be lazy`, `lazy mode`, `simplest solution`, `yagni`, or by complaining about over-engineering. Switch intensity with `/gilfoyle lite|full|ultra`. Turn it off with `stop gilfoyle` / `normal mode`.

## Credit

Original concept, ladder, and benchmarks: [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) (MIT). This fork only re-voices the prose. All credit for the design goes upstream.

## License

MIT, matching upstream.
