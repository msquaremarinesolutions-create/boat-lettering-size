# boat-lettering-size

**How big should your boat name be?** A free, dependency-free calculator for boat lettering: the letter height that suits the boat, the exact width the name needs in your chosen font, whether it fits the transom, and how far away it stays readable.

**Live:** https://size.msquaremarine.com

## What it does

- **Letter height** from boat length, with a sensible range rather than a single number.
- **Real name width** — measured from the actual letterforms of the selected font, not estimated. A script face runs far wider than a condensed one at the same height.
- **Transom fit** — enter the transom width and see whether the name is comfortable, tight or too wide, with the height that would fit.
- **Readable distance** — comfortable reading distance and the distance at which the name is still recognisable.
- **To-scale preview** against the transom, in eight open-licence fonts (SIL OFL, via Google Fonts).
- **Fabrication warnings** — e.g. script fonts with hairline strokes below ~6 in cap height, which get fragile in 3 mm steel.
- Imperial and metric throughout.

## Embed it on your own site

The calculator runs standalone in an iframe with `?embed=1` — page chrome hidden, credit link shown:

```html
<iframe src="https://size.msquaremarine.com/?embed=1" width="100%" height="900"
        style="border:1px solid #e6e1d6;border-radius:12px"
        title="Boat lettering size calculator" loading="lazy"></iframe>
<p>Calculator by <a href="https://www.msquaremarine.com">M.Square Marine</a></p>
```

No tracking and no scripts of ours run on your page. Free for any site, commercial or not — the credit link is the only ask.

## How the numbers are worked out

| Rule | Value |
| --- | --- |
| Letter height | ~1 in of cap height per 5 ft of boat length, clamped to 3–24 in |
| Sensible range | 80 %–125 % of that height |
| Transom fit | name should stay within ~70 % of transom width |
| Comfortable reading | ~10 ft per inch of cap height |
| Still recognisable | ~30 ft per inch of cap height |
| Name width | measured per font at cap height via canvas metrics |

These are the rules we apply to real orders in our own shop. US registration numbers follow a separate legal rule: plain block letters, at least 3 in high, contrasting colour — the vessel name and hailing port have no federal size requirement.

## Run locally

It is one static HTML file with no build step and no dependencies:

```bash
npx http-server docs -p 8125
```

## License

Code: [MIT](LICENSE). Fonts are loaded from Google Fonts under the SIL Open Font License and are not redistributed here.

---

Made by [M.Square Marine](https://www.msquaremarine.com) — laser-cut 316L stainless steel boat lettering. See also [boat-names-dataset](https://github.com/msquaremarinesolutions-create/boat-names-dataset) and [Boat Name Rank](https://names.msquaremarine.com).
