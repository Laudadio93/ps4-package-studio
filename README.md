# PS4 Package Studio

Create PS4 Classics fPKG packages from supported PS1 and PS2 disc images on Windows. The standalone application includes its desktop runtime, standard packaging resources, and disc catalogs.

**[Download the latest Windows ZIP](https://github.com/Laudadio93/ps4-package-studio/releases/latest)**, extract it, and open **PS4 Package Studio.exe**. The built-in workflows do not require users to install Python, .NET, or a separate packaging app.

## What you can do

- Build PS4 fPKGs from supported PS1 BIN or raw 2352-byte ISO images with a matching CUE, or PS2 DVD ISOs.
- Add multiple games, reorder or remove them, and build one package at a time in a queue.
- Group up to four PS1 discs or five PS2 discs in supported multi-disc mode. The first disc supplies the package identity and artwork.
- Populate game IDs from local data and review detected title and disc information before building.
- Review artwork in advance, choose standard or 3D covers where available, supply custom icon or background images, and preview an illustrative PS4 home screen.
- Follow build activity, progress, estimated remaining time where available, and the output location. Cancel a running build.

## Getting started

1. Download and extract the Windows ZIP, then launch **PS4 Package Studio.exe**.
2. Select the game system and add your own disc image. For PS1 games, keep the CUE and its referenced image together.
3. Review the game ID, title, disc status, and artwork. Choose compatibility settings and patches as needed.
4. Select the output folder, check that there is room for working files and the result, and start the build.
5. Review the completion message and output path. Installation and gameplay depend on the target PS4 environment and game.

## PS1 images and settings

- The PS1 packaging path expects a CUE referencing one BIN or raw 2352-byte ISO image file.
- Enable analog controls, skip the PS1 boot logo, or force 60 Hz when appropriate.
- A recognized single-disc LibCrypt entry can supply a game-specific setting. The app detects an adjacent SBI file but does not import it. Recognized LibCrypt multi-disc packages are outside this workflow.
- Apply a supported PPF2, PPF3, or xdelta patch to a single PS1 disc working copy. Match the patch to the correct game revision.
- Supply a custom PS4 Lua configuration for a single PS1 disc.

## PS2 images and settings

- Select an automatic Lua compatibility profile by game ID, disable MTVU, or apply available graphics compatibility settings.
- Optional widescreen matches a single disc by its boot-executable CRC. Patch availability depends on the game and revision.
- A custom Lua configuration and automatic widescreen are mutually exclusive. Widescreen takes priority over the automatic compatibility profile.
- Supply a custom PS4 Lua configuration for a single PS2 disc when needed.

## Disc checks, artwork, and manuals

The app includes offline Redump snapshots for supported PS2 DVD ISOs and PS1 CUE/BIN layouts. PS1 multi-track verification expects one BIN per track, one INDEX 01 at 00:00:00 per track, and no gap directives. PS2 CD images, CHD images, and merged multi-track BINs are outside this check. A match identifies a known dump; console gameplay remains dependent on the game and configuration.

Artwork can be looked up and previewed before creation. Downloaded covers can be cached for offline use. The PC manual viewer opens supported PDFs and ZIP/CBZ page-image archives. Optional online lookup can search the indexed U.S. PS2 manual collection when a local match is unavailable. Availability varies by title and region. Manuals are PC previews and are excluded from PS4 packages.

## Output and compatibility

The studio checks for an existing output and asks the packaging toolkit to inspect the finished package. Compatible PS4 software and game-specific configurations may still be required. Use your own disc images and review the detected title, ID, patch, and output path.

## Credits

- **SvenGDK and contributors** created [PS Classics fPKG Builder](https://github.com/SvenGDK/PS-Classics-fPKG-Builder), the reference for the packaging workflow, game IDs, LibCrypt data, and PS4 Lua profiles.
- **PCSX2 patch authors and contributors** maintain the [PCSX2 patches](https://github.com/PCSX2/pcsx2_patches) used for supported widescreen matching.
- **Redump contributors** and **tsitokely** provide disc-verification data. [Redump](https://redump.org/) · [ps2-iso-renamer](https://github.com/tsitokely/ps2-iso-renamer)
- **xlenore and contributors** organize [PS1 covers](https://github.com/xlenore/psx-covers) and [PS2 covers](https://github.com/xlenore/ps2-covers).
- **Kirkland's Manual Labor** and the **Internet Archive** preserve and host PS2 manuals. **Ronnie Sahlberg and pop-fe2 contributors** provide manual-matching references. [Manual collection](https://archive.org/details/kirklands-manual-labor-sony-playstation-2-usa-4k-version) · [pop-fe2](https://github.com/sahlberg/pop-fe2)
- **PDFium contributors**, **Joshua MacDonald and xdelta contributors**, **Igor Pavlov and 7-Zip contributors**, and the **ps3dev-net**, **Cygwin**, and **zlib** teams provide supporting tools and libraries. [PDFium](https://pdfium.googlesource.com/pdfium/) · [xdelta](https://github.com/jmacd/xdelta) · [7-Zip](https://www.7-zip.org/) · [Cygwin](https://www.cygwin.com/) · [zlib](https://zlib.net/)
- **Laudadio93** maintains the application. PlayStation systems, software, and marks belong to Sony Interactive Entertainment and their respective owners. The application's About window contains additional notices.

Redistribution rights for the bundled PS4 emulator components, PS4 package tool, and inherited PS3 placeholder license have not been confirmed.
