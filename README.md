# asketeddy

I build [Gooo](https://github.com/kimjooyoon/meta-ontology-go), an experimental programming language, and practical examples that compile its rules into ordinary Go.

A current focus is **automatic service-policy changes**: explain which requests a rule admits, find a concrete request that gains access, and apply constrained changes with current authority and revision checks in an in-memory reference host.

- **Try Gooo without installing anything:** [interactive tutorial](https://kimjooyoon.github.io/gooo-go-ports/tutorial.html) — edit the inputs and inspect the Gooo source.
- **Explore a policy change in your browser:** [service-grant refinement demo](https://go.dev/play/p/50KaIY6GTHg) — both patterns allow one familiar request, but the program finds a new request admitted by only one.
- **Use the generated code from Go:** [small service-policy consumer](https://gist.github.com/kimjooyoon/af3d75e04ac625e0e08652b8b6a07726) — includes the pinned dependency, required Go version, and expected output.

Development lives in [meta-ontology-go](https://github.com/kimjooyoon/meta-ontology-go) (the language) and [gooo-go-ports](https://github.com/kimjooyoon/gooo-go-ports) (ports, original policy examples, and reproducible checks). Reproducible bug reports and examples from real workflows help shape the work.
