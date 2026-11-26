# Brief to Board

A design-research tool for performance ads, published as a claude.ai Artifact:
https://claude.ai/artifact/BngoWsHz2gLs79eYZUewZj

Flow: brand guideline → growth brief → Claude research (3 art directions + Pinterest / Meta Ad Library / Instagram searches) → references (paste screenshots, palette-fit + Claude review against the guideline) → mood board (art-direction note, PNG export).

`index.html` is the published page source. Republish it through Claude Code's Artifact tool to the URL above to keep the same link and data.

## References, ratings and taste

- Claude's curated references live in the `curated` collection (one doc per image: `briefId`, `label`, `note`, `query`, `source`, original `imageUrl`, and the stored copy `assetId` / `url` = `/_blob/<id>`). Images are uploaded to the artifact's asset store because the page cannot load third-party image hosts.
- Team uploads stay in `refs`.
- Ratings are private per person: `data/users/<uid>/r_<key>` with `rating` = `like` | `pass` (`<key>` is the curated doc id, or `u_<refId>` for uploads). Liked curated images appear on the brief's mood board.
- `data/users/<uid>/taste` holds the learned taste profile (`summary`, `lookFor`, `avoid`, `searchTerms`). The page appends it to every Claude prompt. Claude sessions read it via `data/users/me`.
- To add references for more briefs: search, pick, upload images as assets, then write `curated` docs with the next `order` values. Read `data/users/me/taste` and liked/passed items first and bias picks accordingly.
