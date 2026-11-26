# Brief to Board

A design-research tool for performance ads, published as a claude.ai Artifact:
https://claude.ai/artifact/BngoWsHz2gLs79eYZUewZj

Flow: brand guideline → growth brief → Claude research (3 art directions + Pinterest / Meta Ad Library / Instagram searches) → references (paste screenshots, palette-fit + Claude review against the guideline) → mood board (art-direction note, PNG export).

`index.html` is the published page source. Republish it through Claude Code's Artifact tool to the URL above to keep the same link and data.

## Reference boards and taste learning

- Figma reference boards live in https://www.figma.com/design/4AJk3cDY1Kh9e1GDZ9CTSK/References (page per month, e.g. `DEC`).
- Each card is named `<board>-<brief>-<nn> · <tag>` (e.g. `dec-tshirt-07 · RTB close-up`) and holds an instance of the `Rating` component (`Rating=None | Like | Dislike`).
- The same keys exist as documents in the dashboard database collection `figmaRefs` (brief, tag, note, search query, image URL, `rating`).
- **Sync ratings:** read every card's `Rating` instance via the Figma plugin API, write `rating` back to `figmaRefs/<key>`, then rewrite `brand/taste` (`summary`, `likes`, `dislikes`, `rated`, `updatedAt`). The dashboard appends `brand/taste.summary` to every Claude research, review and art-direction prompt.
- Before building new boards, read `brand/taste` and the liked/passed `figmaRefs` and bias searches and picks toward liked patterns.
