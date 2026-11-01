# GFOpenAmiga

An index of the GFOpenAmiga family: free software for AmigaOS 3.2 (m68k) from
the AmiCradle Team, made for AmiCradle and usable on real Amigas and PiStorm.
Each project lives in its own repository with its own README and licence.

## Programs and system parts

| Repository | What it is | State, 4 October 2026 |
| --- | --- | --- |
| [openamigasocket](https://github.com/DalsinAI/openamigasocket) | GFOpenSocket: `bsdsocket.library`, its driver, a Commodity and network tools | Working in AmiCradle |
| [openamigamail](https://github.com/DalsinAI/openamigamail) | GFOpenMail: IMAP/SMTP email client with TLS and OAuth sign-in | In progress |
| [openamigaprint](https://github.com/DalsinAI/openamigaprint) | GFOpenPrint: printing stack from `printer.device` to PDF and IPP printers | In progress |
| [openamigabrowser](https://github.com/DalsinAI/openamigabrowser) | GFOpenBrowser: WebKit-based web browser (68040 with FPU) | In progress |
| [openamigawrite](https://github.com/DalsinAI/openamigawrite) | GFOpenWrite: word processor that opens and saves DOCX and ODT and opens the Amiga word processors' documents; `C:OWConvert` converts on any Amiga | In progress |
| [openamigartg](https://github.com/DalsinAI/openamigartg) | GFOpenRTG: RTG graphics system with `gfopenrtg.library`, GFOpenGPU and Warp3D | In progress |
| [openamigamedia](https://github.com/DalsinAI/openamigamedia) | GFOpenMedia: `gfopenmedia.library` for hardware video decode and encode | Designed |
| [openamigavlc](https://github.com/DalsinAI/openamigavlc) | Unofficial VLC media player port | Planned |
| [openamigaprefs](https://github.com/DalsinAI/openamigaprefs) | GFOpenPrefs: GadTools preferences editors | Designed |
| [openamigamulticore](https://github.com/DalsinAI/openamigamulticore) | GFOpenMulticore: spec and library for running jobs on extra cores | Specified |

## Library ports

Open-source libraries ported to AmigaOS 3.2 (m68k), first for GFOpenBrowser.
Each repository holds the Amiga build (script, patches, configuration), a
smoke test with its output, and the library's upstream licence; the Amiga
changes are MIT. "Working" means it builds and its smoke test passed on
AmigaOS 3.2.3 under AmiCradle; none has been run on real hardware yet.

| Repository | Library | Version | State, 4 October 2026 |
| --- | --- | --- | --- |
| [openamigacurl](https://github.com/DalsinAI/openamigacurl) | libcurl, with TLS through AmiSSL | 8.22.0 | Working |
| [openamigacairo](https://github.com/DalsinAI/openamigacairo) | cairo and pixman | 1.18.6, 0.46.4 | Working |
| [openamigafreetype](https://github.com/DalsinAI/openamigafreetype) | FreeType | 2.14.3 | Working |
| [openamigaharfbuzz](https://github.com/DalsinAI/openamigaharfbuzz) | HarfBuzz | 14.5.1 | Working |
| [openamigafontconfig](https://github.com/DalsinAI/openamigafontconfig) | Fontconfig | 2.18.3 | Working |
| [openamigaxml](https://github.com/DalsinAI/openamigaxml) | libxml2 and Expat | 2.15.4, 2.8.2 | Working |
| [openamigaimage](https://github.com/DalsinAI/openamigaimage) | zlib, libpng and libjpeg; the project's datatypes (below) | 1.3.1, 1.6.58, 9f | Working |
| [openamigamedialibrary](https://github.com/DalsinAI/openamigamedialibrary) | libwebp and libvpx (WebP pictures, VP8 and VP9 video), decoders only and without FPU code | 1.6.0, 1.17.0 | Working |
| [openamigasqlite](https://github.com/DalsinAI/openamigasqlite) | SQLite | 3.53.4 | Working |
| [openamigapsl](https://github.com/DalsinAI/openamigapsl) | libpsl (Public Suffix List) | 0.23.3 | Working |

## Datatypes

Datatypes the project builds, so any datatypes program (MultiView,
GFOpenBrowser, a picture viewer) opens more formats. They all live in
[openamigaimage](https://github.com/DalsinAI/openamigaimage)'s `Datatypes`
drawer, are built for the 68040 (no FPU instructions), and decode on AmigaOS 3.2.3
under AmiCradle exactly as their libraries do on x86 cores; none has been run on
real hardware yet.

| Datatype | Opens | Built on | State, 4 October 2026 |
| --- | --- | --- | --- |
| `webp.datatype` | WebP pictures: lossy, lossless, alpha (first frame of an animated one) | libwebp 1.6.0 (openamigamedialibrary) | Working |
| `webm.datatype` | WebM video, VP8 and VP9, as an animation in 256 colours; no sound yet | libvpx 1.17.0 (openamigamedialibrary) | Frames decode; playback in MultiView not yet checked |

## AmiCradle tools

| Repository | What it is |
| --- | --- |
| [amigachrome-stoves](https://github.com/DalsinAI/amigachrome-stoves) | Cross-compiler toolchains used by AmiCradle's Kitchen |
| [amigachrome-gameports](https://github.com/DalsinAI/amigachrome-gameports) | Game ports and compatibility work for m68k AROS |

## Licence

This index is MIT licensed (`LICENSE`, Copyright (c) 2026 AmiCradle Team).
AmiCradle Team's own projects are MIT; library ports and other third-party
code keep their upstream licences, as each repository states.

## Contributors

GFOpenAmiga is created and maintained by [SacredTrees](https://github.com/SacredTrees) with The AmiCradle Team, copyright AmiCradle Team. Everyone whose work it includes is credited in [`CONTRIBUTORS.md`](CONTRIBUTORS.md).
