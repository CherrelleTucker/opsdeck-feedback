# OpsDeck

**OpsDeck** is the operations dashboard for small craft and service businesses
— a single place to run a microbusiness's day. Industry-configurable,
mobile-friendly, Google-Sheets backed. A [ForkAround](https://forkaround.io)
product.

## This repo

Public-facing companion to the (private) OpsDeck product repo. Two roles:

1. **Brand assets** — favicons, logo variants. Used by the platform itself
   (`setFaviconUrl`) and anywhere the OpsDeck mark needs a stable hosted URL.
2. **Feedback intake** *(coming)* — bug reports and feature requests from
   operators. Issue templates will land here once the product is broadly
   available.

## Brand assets

Hosted under [`assets/`](./assets):

| File | Use |
|---|---|
| `favicon.svg` | Simplified mark (ring + disc + D, no chevrons or shadows). Source for the PNGs below. |
| `favicon-32.png` | Browser tab favicon (used by `setFaviconUrl` in the platform). Rendered from `favicon.svg`. |
| `favicon-192.png` | High-DPI / PWA icon. Rendered from `favicon.svg`. |
| `opsdeck-logo.svg` | Full logo mark with chevrons + drop shadow, light backgrounds. |
| `opsdeck-logo-dark.svg` | Full logo mark, dark backgrounds (cream variant). |

**Favicon vs logo.** The favicon drops the chevrons and shadows because they
turn into noise at 16–32px tab sizes. The full mark is used for in-product
chrome, marketing imagery, and anywhere there's room for the chevron rank
detail to read.

Stable raw URLs:

```
https://raw.githubusercontent.com/CherrelleTucker/opsdeck-feedback/main/assets/favicon-32.png
https://raw.githubusercontent.com/CherrelleTucker/opsdeck-feedback/main/assets/favicon-192.png
https://raw.githubusercontent.com/CherrelleTucker/opsdeck-feedback/main/assets/favicon.svg
https://raw.githubusercontent.com/CherrelleTucker/opsdeck-feedback/main/assets/opsdeck-logo.svg
https://raw.githubusercontent.com/CherrelleTucker/opsdeck-feedback/main/assets/opsdeck-logo-dark.svg
```

**Regenerating the favicon PNGs** (when the mark changes):

```sh
qlmanage -t -s 256 -o /tmp assets/favicon.svg
sips -Z 32  /tmp/favicon.svg.png --out assets/favicon-32.png
sips -Z 192 /tmp/favicon.svg.png --out assets/favicon-192.png
```

## About OpsDeck

Learn more at [opsdeckondeck.com](https://opsdeckondeck.com).

---

© Cherrelle Tucker. OpsDeck is a ForkAround product. Brand assets in this
repo are made public for hosting and integration purposes; trademark and
copyright are reserved.
