# fiction-retail-dbt

The fictional retail team's dbt project — and a real, independent consumer
of the [Downstream Impact Guardian](https://github.com/jwlai-cloud/downstream-impact-guardian)
GitHub Action. Total integration surface: the one `uses:` block in
[`.github/workflows/guardian.yml`](.github/workflows/guardian.yml).

Open a PR that touches `dbt/**` and the guardian analyzes it: schema
breaks, metric drift, semantic drift, cross-system blast radius from
DataHub, a proposed Data Contract, and mergeable compatibility code —
posted as a PR comment.

## Try it (3 clicks, no setup)

1. Open the [rename scenario compare view](../../compare/main...demo/rename-order-total?expand=1)
   — or the [delete-a-model scenario](../../compare/main...demo/delete-revenue-daily?expand=1)
2. Click **Create pull request**
3. Wait ~60s — the guardian's report appears as a comment

No DataHub credentials are configured here yet, so runs use the guardian's
offline fixture mode (full report, clearly labeled). Same code runs live
when secrets exist.

Apache 2.0.
