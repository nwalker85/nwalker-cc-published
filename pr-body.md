## Summary
- Remove `example-essay.md` from the essays corpus: the Bragi Phase 1B promotion-path test seed (`status: candidate`, `canonical: false`, `publish_eligible: true`).
- It is currently rendered live at nwalker.cc/writing/example-essay because the site build consumes this corpus (RAV-1318) and gates only on `publish_eligible`.
- README now states the render rule (`status: published` or absent; never `canonical: false`).

This is cleanup. The durable fix is the site-side canonical/status filter in nwalker85/nwalker.cc (RAV-1894); the seed was promoted twice already (#1, #3), so without that filter the next promotion test lands in production again.

Linear: RAV-1895

## Test plan
- [ ] Editorial gates CI green on this PR
- [ ] After merge and the next nwalker.cc build: `/writing` lists no "Example Essay"

🤖 Generated with [Claude Code](https://claude.com/claude-code)

https://claude.ai/code/session_017YAwTFdTPU4mM6XBJbfJG6
