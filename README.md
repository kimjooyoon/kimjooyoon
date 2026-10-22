# asketeddy

I build [Gooo](https://github.com/kimjooyoon/meta-ontology-go), an experimental programming language, and practical examples that compile its rules into ordinary Go.

A current focus is **automatic service-policy changes**: explain which requests a rule admits, find a concrete request that gains access, and apply constrained changes with current authority and revision checks in an in-memory reference host.

- **Try Gooo without installing anything:** [interactive tutorial](https://kimjooyoon.github.io/gooo-go-ports/tutorial.html) — edit the inputs and inspect the Gooo source.
- **Explore a policy change in your browser:** [service-grant refinement demo](https://go.dev/play/p/50KaIY6GTHg) — both patterns allow one familiar request, but the program finds a new request admitted by only one.
- **Use the generated code from Go:** [small service-policy consumer](https://gist.github.com/kimjooyoon/af3d75e04ac625e0e08652b8b6a07726) — includes the pinned dependency, required Go version, and expected output.

- **Highlight Gooo sources locally:** [highlight-gooo v0.1.1](https://github.com/kimjooyoon/gooo-language-bridge/releases/tag/examples/highlight-gooo/v0.1.1) — create self-contained HTML or source-preserving JSON with published Chroma.

Development lives in [meta-ontology-go](https://github.com/kimjooyoon/meta-ontology-go) (the language) and [gooo-go-ports](https://github.com/kimjooyoon/gooo-go-ports) (ports, original policy examples, and reproducible checks). Reproducible bug reports and examples from real workflows help shape the work.

The [language-bridge workbench](https://github.com/kimjooyoon/gooo-language-bridge) keeps native language comparisons, reproducible examples, and upstream contribution evidence together.

Start with a concrete comparison: [string-length units across Go, Python and JavaScript](https://github.com/kimjooyoon/gooo-language-bridge/blob/main/docs/string-length-units.md), or [execution versus completion input intent](https://github.com/kimjooyoon/gooo-language-bridge/blob/main/docs/completion-input-intent.md).

Compare Goja or Sobek with Node.js using [source-pinned JavaScript snapshots](https://github.com/kimjooyoon/gooo-language-bridge/blob/main/examples/js-differential/README.md). Supply a small script and retain exact source revisions, original outputs and per-case differences; the guide includes a 54-observation Sobek example. No model or API key is required.

## Selected OSS work

- **urfave/cli:** [submitted fix](https://github.com/urfave/cli/pull/2485) retains unfinished short-flag groups for shell completion callbacks. [Six platform/version CI jobs passed](https://github.com/urfave/cli/actions/runs/39697751487); the [native/Gooo guide](https://github.com/kimjooyoon/gooo-language-bridge/blob/main/docs/completion-input-intent.md) explains the intent boundary.
- **pflag:** [run a type-identity counterexample in your browser](https://go.dev/play/p/GsveDskxbgt) — two distinct Go types share a display label. The [submitted fix](https://github.com/spf13/pflag/pull/529) checks actual native type identity. The browser example runs the pinned original.
- **Goja:** [reported normalization bug](https://github.com/dop251/goja/issues/820) replaces lone UTF-16 surrogates with U+FFFD. The [24-case Goja/Node comparison](https://gist.github.com/kimjooyoon/cdc0106aefec97d80b8fbd75ac6ff5aa/5d39c4a5e3871541a0372e9b57424ed32444628e) includes a pinned reproducer, regression tests and raw results.
- **Bubbles:** [submitted fix](https://github.com/charmbracelet/bubbles/pull/1072) preserves the newline when Delete removes a line's final character. [Native/Gooo reproduction](https://github.com/kimjooyoon/gooo-language-bridge/blob/main/docs/delete-forward-newline.md).
- **Chroma:** [submitted fix](https://github.com/alecthomas/chroma/pull/1411) recognizes Go imaginary literals such as `0b10i` and `0x1p-2i`, checked against native Go.
- **Caddy:** [reproduced PR review](https://github.com/caddyserver/caddy/pull/8248#discussion_r4342769424) shows how a value-only cache turns unknown placeholders into known empty values.
