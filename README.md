# VHT.ai translations

User-interface text of the [VHT.ai](https://vht.ai) app and public website in seven
languages: English (`en`), French (`fr`), Japanese (`ja`), Simplified Chinese (`zh-CN`),
Spanish (`es`), German (`de`) and Brazilian Portuguese (`pt`).

This repo exists so native speakers can read the strings in context and tell the VHT team
what sounds wrong. Every fix helps members read their health app in their own language.

## How this repo works

- **One-way export.** The files under `translations/` are generated from the private app
  repo by an automated export. Nothing here flows back on its own: the VHT team reads each
  accepted proposal and applies it by hand in the app, then the next export refreshes the
  copy here. Do not expect edits in this repo to survive the next export.
- **Layout.** `translations/<lang>/public.json` holds the public website and marketing pages
  (dotted keys such as `nav.pricing` or `pages.contact.title`). `translations/<lang>/<area>.json`
  holds one area of the member app each; the key is the exact English string and the value is
  the translation, so `en/` is simply the identity map. `translations/manifest.json` lists
  counts, the source commit and the export date.
- **Placeholders.** Keep `{0}`, `{name}`, `%s`, HTML tags, URLs, prices and brand names
  (VHT, VHT.ai, ECHNA, Health Index, Digital Twin, plan names) exactly as in English.

## Propose a fix

**Open an issue** (preferred for one or a few strings) using the
[Translation fix](../../issues/new?template=translation-fix.yml) template. It asks for:

1. the language,
2. the key (or the screen where you saw the text),
3. the current text,
4. your suggested text and, if useful, why.

**Or open a pull request** editing the JSON under `translations/`. Keep the keys unchanged
and edit only the values. A PR is a proposal, not the final change; it is applied in the app
repo by hand and then closed with a note.

Larger questions (tone, terminology, a language we do not have yet) are welcome in the
[VHT.ai community](https://github.com/virtual-healthcare-technologies/community) or by email
to <echna@vht.ai>.

## No personal health information

This is a public repository. Never paste member data, screenshots that show a real person's
details, or any health information into an issue or pull request. Describe the screen in
words instead. Issues containing personal health information are closed and the content
removed.

## Licence

The strings in `translations/` are licensed under
[Creative Commons Attribution 4.0 International](LICENSE) (CC BY 4.0). Product and brand
names (VHT, VHT.ai, ECHNA and others) remain trademarks of Virtual Healthcare Technologies
and are not covered by the licence.
