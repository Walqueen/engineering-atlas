# Engineering ATLAS — the public record

The permanent home of one page: **[the-rail]** — the derived dynamic-range law,
the estimator-scoping result, and a ledger of every claim this project made and
then withdrew.

The page is at **https://walqueen.github.io/engineering-atlas/**

## What this repository is, and is not

This repository holds the **published page only**. The research code lives in a
separate private repository and is generated from there: `tools/site/build_site.py`
reads the commit, the module and test counts, the document list, and every point
on the ρ* curve out of the working tree at build time, then writes this
`index.html`. Nothing on the page is typed in by hand.

That is a deliberate constraint rather than a convenience. A hand-written "what
is not claimed" paragraph once sat on the project's dashboard for weeks after
the thing it disclaimed had been ingested. On a project about measurement
honesty, a stale disclaimer is the worst available bug, so the page is built in a
way that makes one impossible: if a number cannot be derived, it does not render.

**What is deliberately not here:** the source, the data, and the commit history.
The research repository is co-authored and its licence is held by a collaborator,
so it is not a single person's to publish. Publishing this page does not change
that.

## Updating it

From the research repository:

```
python -m tools.site.build_site --check --standalone ../engineering-atlas/index.html
cd ../engineering-atlas && git commit -am "rebuild" && git push
```

Pushing to `main` redeploys the page. There is nothing to keep awake and nothing
that expires: GitHub Pages serves a static file, so the page does not sleep from
inactivity the way a hosted application does.

## Credit

The statistical core this project extends — rolling peaks-over-threshold
estimation with a generalised Pareto tail, and the decision to make the Kupiec
and Christoffersen backtests first-class outputs rather than an afterthought —
originated with **Aarush Sharma**, in the ATLAS financial tail-risk model. This
project exists because of that one, and the direction of that dependency is
stated first for that reason.

The work described on this page — the battery Channel A/B measurement study, the
dynamic-range law and its derivation, the excitation and cohort decisions, and
the retraction ledger — originated in this project.

## Licence

The page and its text: [CC BY 4.0](LICENSE). Cite it with
[`CITATION.cff`](CITATION.cff), or by the DOI once one is minted.
