# Seven deployment

This repository deploys [Seven](https://github.com/mikej340/seven) to
<https://playseven.uk/>. It intentionally contains no application source.

The **Deploy Seven** workflow checks out `mikej340/seven`, runs its root-domain
test/build target, and publishes the resulting `out/` directory with this
repository's `GITHUB_TOKEN`.

The workflow can be started manually with an optional full source commit SHA,
or by a `source-deployed` repository dispatch containing
`client_payload.source_sha`. An omitted SHA uses `mikej340/seven@main`.

Before the first run, select **GitHub Actions** under **Settings → Pages**.
Configure the `playseven.uk` custom domain only after a manual deployment has
completed successfully. The source repository's existing Pages custom domain
must remain unset.
