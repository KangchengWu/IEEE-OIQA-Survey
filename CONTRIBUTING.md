# Contributing

[← Back to the resource hub](README.md#maintenance)

For a new resource or correction, please provide:

1. The exact method or dataset name and its original paper.
2. An authoritative source: an author website, laboratory page, author repository, or publisher record.
3. The resource type: author implementation, third-party implementation, dataset, mirror, annotation, or model weights.
4. Any account, request form, access code, or archive password required.
5. The date checked and what was verified.

Keep the corresponding README entry, detail page in `docs/`, and `data/resources.json` consistent. Use the terminology and reference numbers in the survey. Include the full paper title in the method details; use an established model name or an author/reference label in summary tables.

Add code links when a corresponding implementation can be identified. For entries without a code link, omit that resource field. Label third-party implementations explicitly, and do not present paper search results, dataset pages, or empty project pages as implementations.

For benchmark corrections, update both `docs/benchmark.md` and `data/benchmark.json`. Identify the source table and evaluation protocol. Do not average correlations across different databases into an overall ranking. A repository being accessible does not establish that its results have been reproduced.
