# isa198x.github.io

The ISA198x site. A skeleton: a wordmark, a sentence, and the shared kit
wired up — so the name has somewhere to point and the identity is applied from
the start rather than retrofitted.

A layer inside Asm198x today. This site exists so it has somewhere to surface when it stands alone.

## Running it

```sh
npm install
npm run dev
```

`predev` and `prebuild` fetch [198x-ui](https://github.com/stevehill1981/198x-ui)
into a gitignored `_198x-ui/`, at the tag pinned in `scripts/fetch-ui.sh`, and
copy the kit's `fonts/` into `public/fonts/` because `fonts.css` serves them
from the site root. Neither is vendored here.

To move the pin, edit `REF` in that script. To try a different tag once:

```sh
UI_REF=v0.4.0 npm run build
```

## What is deliberately missing

No accessibility sweep in CI. The four established sites run one over every
route in both themes before publishing, and this should too **once it has more
than one route**. Adding it means copying `scripts/a11y-sweep.mjs` and its
Playwright step from any of them.
