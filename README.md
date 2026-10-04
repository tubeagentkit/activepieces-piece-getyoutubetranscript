# activepieces-piece-getyoutubetranscript

Release pipeline for [`@tubeagentkit/piece-getyoutubetranscript`](https://www.npmjs.com/package/@tubeagentkit/piece-getyoutubetranscript), the [GetYouTubeTranscript](https://getyoutubetranscript.com) piece for [Activepieces](https://www.activepieces.com).

The piece's source lives in our fork of the Activepieces monorepo: [tubeagentkit/activepieces](https://github.com/tubeagentkit/activepieces/tree/add-getyoutubetranscript/packages/pieces/community/getyoutubetranscript). This repo only builds and publishes it, so the fork does not need GitHub Actions.

## Install the piece

In Activepieces, go to **Settings > My Pieces > Install Piece** and enter `@tubeagentkit/piece-getyoutubetranscript`.

## Release

1. Commit piece changes to the fork, then put the new commit SHA in `PIECE_REF`.
2. Push a tag `vX.Y.Z`. The workflow builds the piece at that commit, bundles it with the Activepieces CLI, sets the npm name, version and README, smoke-tests the bundle, and publishes with npm trusted publishing (with provenance).

Run the workflow manually for a dry run that does everything except publish.
