![Corven](./assets/logo.png)

**[English](./README.md) · [Português](./README.pt.md)**

# Corven

### The CSS compiler that treats every byte as a decision.

Corven is an interface compiler. It generates the minimum CSS necessary to build fast, accessible, and efficient applications, and nothing more. Not a component library. Not a theme. A compiler, with CSS as its output.

---

## Why Corven exists

Most CSS frameworks solve "how do I style things quickly." Very few solve "how do I make sure the CSS I ship five months from now is still lean, still consistent, and still explainable." Corven is built around the second question.

- **Utility-first, but disciplined.** Every utility class does exactly one thing (one class, one CSS property). No hidden side effects, no mystery classes that secretly set six properties.
- **Familiar on day one.** If you know Tailwind, you already know most of Corven's naming and scale, copied deliberately, not reinvented for the sake of being different. The learning curve is a design constraint, not an afterthought.
- **Documentation that can't lie.** Reference docs are generated directly from the compiled CSS output, not hand-written. If a class exists in the build, it's documented. If it doesn't, it isn't. There's no drift between what's shipped and what's written down.
- **Predictable cascade, no specificity wars.** Components and custom overrides use native CSS Cascade Layers instead of `!important`. The layer that should win, wins, always, without guesswork.
- **Components built from tokens, never arbitrary CSS.** Every component is composed from the same design tokens the utilities use. There's no back door where a hardcoded hex color or a random pixel value sneaks into the system.
- **Engineering discipline you can verify yourself.** Every layer of the Core ships with automated compilation tests, structural checks, and visual regression tests. Not because it looks good in a README, but because a real bug (a duplicate detector that didn't understand `@media`) was actually caught by this exact setup during development. See [UPDATES.md](./UPDATES.md).

## What makes it different in the market

Utility-first CSS solved a real problem, but it created a new one: frameworks that grow forever, HTML that gets verbose, and documentation that quietly falls out of sync with the code. Corven's answer isn't "add more features." It's:

1. **A compiler mindset from day one.** CSS is Corven's output, not its identity. That's what opens the door to a real JIT compiler, build-time waste detection, and performance budgets later, without retrofitting them onto a static framework that was never designed to be compiled.
2. **HTML that's allowed to get simpler over time.** The plan isn't "utilities forever." As patterns repeat, Corven is designed to help you compose them into real components, without you ever hand-writing arbitrary CSS to do it.
3. **Sustainability as a measurable side effect, not a slogan.** Less CSS, fewer duplicate rules, and a predictable cascade all reduce bytes transferred and work the browser has to do. Corven's roadmap includes reporting this with an actual methodology (the Sustainable Web Design model), not an invented score.

## Where it stands today

Layers 1 through 4 of the Core (Tokens, Utilities, Components, Layouts) are closed: each compiles clean, is covered by automated tests, and has a working example. There is **no installable package yet**. This is early. See [UPDATES.md](./UPDATES.md) for the development log and [ROADMAP.md](./ROADMAP.md) for what's ahead (JIT compiler, CLI, runtime, DevTools).

If you want to watch this happen rather than take a snapshot's word for it, star the repo. Updates land here as real milestones close, not as marketing beats.

## License

MIT. See [LICENSE](./LICENSE).

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md). The project isn't accepting external code contributions yet, since there's no stable public API to contribute against, but issues and discussion are welcome.

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

## Security

See [SECURITY.md](./SECURITY.md) for how to report vulnerabilities.
