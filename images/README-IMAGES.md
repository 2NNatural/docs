# Images to export from GitBook

I could not download the 8 figures automatically — GitBook serves them from a CDN
behind tokenized URLs that are redacted for privacy, and direct binary downloads are
blocked in this environment. Export each one from GitBook (open the image in the
GitBook editor, or right-click → Save image on the live page) and drop it into this
`/images` folder using the exact filename below. The `.mdx` pages already reference
these paths, so once the files are here the figures render with no further edits.

| Save as (in /images) | Appears on page | GitBook file id | Context |
| --- | --- | --- | --- |
| overview-tranching.svg | overview.mdx | NZkgfPdP0bPuoibff0mD | Senior/Junior tranching diagram (top of Overview) |
| overview-utilization.svg | overview.mdx | rUg56j9ApZU8iULkRuIP | Utilization / yield distribution curve |
| yield-curve.svg | how-dawn-works.mdx | PK1WfGy8z6qkxo32sCCT | "The Yield Curve" figure |
| self-adapting-yield-curve.svg | how-dawn-works.mdx | P5q2JH9Ew2H51UMCqvIa | Self-adapting yield curve over time |
| flow-of-funds.svg | vault-products.mdx | PssFuuAOJMAzA4Ee33Xl | Flow of Funds (Makina / Concrete) |
| yield-share-fee.svg | yield-share-fees-explained.mdx | oQllUqLXOXYxXfSFmI9M | Yield Share Fee on the Risk Premium transfer |
| junior-performance-fee.svg | yield-share-fees-explained.mdx | 2AEil0jSh3Kx9quH8Yss | Junior performance fee on total position |
| yield-share-vs-performance.svg | yield-share-fees-explained.mdx | Xu8VQKeaZBwZKHIi4sNA | Yield Share vs Performance Fee comparison |

Note on file extensions: the two Overview diagrams were originally SVG. If any export
comes out as PNG instead, save it with the same base name but `.png` and update the
matching `src="/images/...."` line in the referenced `.mdx` page.
