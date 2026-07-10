<p align="center">
  <img src="./assets/logo.png" alt="Corven" width="364">
</p>

<p align="center">
  <strong>English</strong> · <a href="./README.pt.md">Português</a>
</p>

# Corven

### CSS that ships only what your project actually uses.

Corven is an interface compiler: it generates the minimum CSS necessary to build fast, accessible, and efficient applications, then strips out everything your project doesn't touch. Not a component library. Not a theme. A compiler, with CSS as its output.

---

## The pitch, in one number

Corven's own JIT engine was pointed at a real example page and told to keep only what that page uses. The result: **173,576 bytes of CSS down to 16,243 bytes. A 90.6% reduction, verified by an automated test, not a marketing estimate.** No configuration, no manual purge setup, no separate tool to wire up. You write HTML with utility classes; Corven figures out what's actually needed.

That number is the whole thesis of the project: a framework should get *smaller* as your build tooling gets smarter, not bigger.

## Why Corven exists

Most CSS frameworks solve "how do I style things quickly." Very few solve "how do I make sure the CSS I ship five months from now is still lean, still consistent, and still explainable." Corven is built around the second question.

- **Utility-first, but disciplined.** Every utility class does exactly one thing (one class, one CSS property). No hidden side effects, no mystery classes that secretly set six properties.
- **Familiar on day one.** If you know Tailwind, you already know most of Corven's naming and scale, copied deliberately, not reinvented for the sake of being different. The learning curve is a design constraint, not an afterthought.
- **A real JIT compiler, built in-house.** Corven scans your templates and ships only the CSS you actually use, the same idea Tailwind popularized, implemented as Corven's own compiler rather than a bolted-on third-party tool.
- **Documentation that can't lie.** Reference docs are generated directly from the compiled CSS output, not hand-written. If a class exists in the build, it's documented. If it doesn't, it isn't.
- **Predictable cascade, no specificity wars.** Components and custom overrides use native CSS Cascade Layers instead of `!important`. The layer that should win, wins, always, without guesswork.
- **Components built from tokens, never arbitrary CSS.** Every component is composed from the same design tokens the utilities use. There's no back door where a hardcoded hex color or a random pixel value sneaks into the system.
- **Engineering discipline you can verify yourself.** Every layer ships with automated compilation tests, structural checks, and visual regression tests, not because it looks good in a README, but because real bugs (a duplicate detector that didn't understand `@media`, a purge rule that treated comma-separated selectors as AND instead of OR) were actually caught by this exact setup during development. See [UPDATES.md](./UPDATES.md).

## What makes it different in the market

Utility-first CSS solved a real problem, but it created a new one: frameworks that grow forever, HTML that gets verbose, and documentation that quietly falls out of sync with the code. Corven's answer isn't "add more features." It's:

1. **A compiler mindset from day one.** CSS is Corven's output, not its identity. The scanner and purge engine already exist and already measure real results against a real page, not a hypothetical roadmap item.
2. **HTML that's allowed to get simpler over time.** The plan isn't "utilities forever." As patterns repeat, Corven is designed to help you compose them into real components, without you ever hand-writing arbitrary CSS to do it.
3. **Sustainability as a measurable side effect, not a slogan.** Less CSS, fewer duplicate rules, and a predictable cascade all reduce bytes transferred and work the browser has to do. Corven's roadmap includes reporting this with an actual methodology (the Sustainable Web Design model), not an invented score.

## Where it stands today

All five layers of the Core (Tokens, Utilities, Components, Layouts, Pages) are closed: each compiles clean, is covered by automated tests, and has a working example. The JIT compiler is in active development: the scanner and the purge engine both exist and both have real, measured results (see above). There is **no installable package yet**. This is early. See [UPDATES.md](./UPDATES.md) for the development log and [ROADMAP.md](./ROADMAP.md) for what's ahead.

If you want to watch this happen rather than take a snapshot's word for it, star the repo. Updates land here as real milestones close, not as marketing beats.

## License

MIT. See [LICENSE](./LICENSE).

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md). The project isn't accepting external code contributions yet, since there's no stable public API to contribute against, but issues and discussion are welcome.

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

## Security

See [SECURITY.md](./SECURITY.md) for how to report vulnerabilities.
