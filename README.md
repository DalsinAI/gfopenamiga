# GFOpenAmiga

An index of the GFOpenAmiga family: free software for AmigaOS 3.2 (m68k) from
the AmiCradle Team, made for AmiCradle and usable on real Amigas and PiStorm.
Each project lives in its own repository with its own README and licence.

## Programs and system parts

| Repository | What it is | State, 4 October 2026 |
| --- | --- | --- |
| [gfopensocket](https://github.com/DalsinAI/gfopensocket) | GFOpenSocket: `bsdsocket.library`, its driver, a Commodity and network tools | Working in AmiCradle |
| [gfopenmail](https://github.com/DalsinAI/gfopenmail) | GFOpenMail: IMAP/SMTP email client with TLS and OAuth sign-in | In progress |
| [gfopenprint](https://github.com/DalsinAI/gfopenprint) | GFOpenPrint: printing stack from `printer.device` to PDF and IPP printers | In progress |
| [gfopenbrowser](https://github.com/DalsinAI/gfopenbrowser) | GFOpenBrowser: WebKit-based web browser (68040 with FPU) | In progress |
| [gfoffice](https://github.com/DalsinAI/gfoffice) | The GFOffice Suite: OpenWrite, the word processor that opens and saves DOCX and ODT and opens the Amiga word processors' documents; `C:OWConvert` converts on any Amiga | In progress |
| [gfopenrtg](https://github.com/DalsinAI/gfopenrtg) | GFOpenRTG: RTG graphics system with `gfopenrtg.library`, GFOpenGPU and Warp3D | In progress |
| [gfopenmedia](https://github.com/DalsinAI/gfopenmedia) | GFOpenMedia: `gfopenmedia.library` for hardware video decode and encode | Designed |
| [gfopenvlc](https://github.com/DalsinAI/gfopenvlc) | Unofficial VLC media player port | Planned |
| [gfopenprefs](https://github.com/DalsinAI/gfopenprefs) | GFOpenPrefs: GadTools preferences editors | Designed |
| [gfopenmulticore](https://github.com/DalsinAI/gfopenmulticore) | GFOpenMulticore: spec and library for running jobs on extra cores | Specified |

## Library ports

Open-source libraries ported to AmigaOS 3.2 (m68k), first for GFOpenBrowser.
Each repository holds the Amiga build (script, patches, configuration), a
smoke test with its output, and the library's upstream licence; the Amiga
changes are MIT. "Working" means it builds and its smoke test passed on
AmigaOS 3.2.3 under AmiCradle; none has been run on real hardware yet.

| Repository | Library | Version | State, 4 October 2026 |
| --- | --- | --- | --- |
| [gfopencurl](https://github.com/DalsinAI/gfopencurl) | libcurl, with TLS through AmiSSL | 8.22.0 | Working |
| [gfopencairo](https://github.com/DalsinAI/gfopencairo) | cairo and pixman | 1.18.6, 0.46.4 | Working |
| [gfopenfreetype](https://github.com/DalsinAI/gfopenfreetype) | FreeType | 2.14.3 | Working |
| [gfopenharfbuzz](https://github.com/DalsinAI/gfopenharfbuzz) | HarfBuzz | 14.5.1 | Working |
| [gfopenfontconfig](https://github.com/DalsinAI/gfopenfontconfig) | Fontconfig | 2.18.3 | Working |
| [gfopenxml](https://github.com/DalsinAI/gfopenxml) | libxml2 and Expat | 2.15.4, 2.8.2 | Working |
| [gfopenimage](https://github.com/DalsinAI/gfopenimage) | zlib, libpng and libjpeg; the project's datatypes (below) | 1.3.1, 1.6.58, 9f | Working |
| [gfopenmedialibrary](https://github.com/DalsinAI/gfopenmedialibrary) | libwebp and libvpx (WebP pictures, VP8 and VP9 video), decoders only and without FPU code | 1.6.0, 1.17.0 | Working |
| [gfopensqlite](https://github.com/DalsinAI/gfopensqlite) | SQLite | 3.53.4 | Working |
| [gfopenpsl](https://github.com/DalsinAI/gfopenpsl) | libpsl (Public Suffix List) | 0.23.3 | Working |

## Datatypes

Datatypes the project builds, so any datatypes program (MultiView,
GFOpenBrowser, a picture viewer) opens more formats. They all live in
[gfopenimage](https://github.com/DalsinAI/gfopenimage)'s `Datatypes`
drawer, are built for the 68040 (no FPU instructions), and decode on AmigaOS 3.2.3
under AmiCradle exactly as their libraries do on x86 cores; none has been run on
real hardware yet.

| Datatype | Opens | Built on | State, 4 October 2026 |
| --- | --- | --- | --- |
| `webp.datatype` | WebP pictures: lossy, lossless, alpha (first frame of an animated one) | libwebp 1.6.0 (gfopenmedialibrary) | Working |
| `webm.datatype` | WebM video, VP8 and VP9, as an animation in 256 colours; no sound yet | libvpx 1.17.0 (gfopenmedialibrary) | Frames decode; playback in MultiView not yet checked |

## AmiCradle tools

| Repository | What it is |
| --- | --- |
| [amicradle-stoves](https://github.com/DalsinAI/amicradle-stoves) | Cross-compiler toolchains used by AmiCradle's Kitchen |
| [amicradle-gameports](https://github.com/DalsinAI/amicradle-gameports) | Game ports and compatibility work for m68k AROS |

## Licence

This index is MIT licensed (`LICENSE`, Copyright (c) 2026 AmiCradle Team).
AmiCradle Team's own projects are MIT; library ports and other third-party
code keep their upstream licences, as each repository states.

## Contributors

GFOpenAmiga is created and maintained by [SacredTrees](https://github.com/SacredTrees) with The AmiCradle Team, copyright AmiCradle Team. Everyone whose work it includes is credited in [`CONTRIBUTORS.md`](CONTRIBUTORS.md).
