https://github.com/Mitul-Sharma/DownList/releases

# DownList: Download Unlimited Netease Playlist Music on Desktop

[![Releases](https://img.shields.io/badge/DownList-Releases-blue?logo=github&logoColor=white)](https://github.com/Mitul-Sharma/DownList/releases)

![Music notes illustration](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Musical_note.svg/1200px-Musical_note.svg.png)

DownList is a desktop application designed to help you manage and download music from Netease playlists. It provides a straightforward workflow to grab tracks from playlists you own or have rights to, and store them on your computer for offline listening. The goal is to give you a reliable, fast, and simple experience for organizing music from Netease playlists in a local library. This README covers what the app does, how it works, how to install, how to use it, and how to contribute to the project.

If you want to grab the latest builds directly, you should head to the Releases page. The link to that page is the same as above, and you can download the installer or portable version for your platform there. https://github.com/Mitul-Sharma/DownList/releases

Table of contents
- Why DownList
- Core ideas and design goals
- Features at a glance
- Supported platforms
- How to install
- How to use
- Download management and playlists
- Quality, formats, and metadata
- Performance and reliability
- Security and privacy (aspects covered)
- Architecture and tech stack
- Building from source
- Testing and quality assurance
- Local development workflow
- Versioning and releases
- Documentation and help
- Roadmap and future plans
- Contributing to DownList
- Community and support
- File layout and project structure
- License and rights
- FAQ
- Changelog

Why DownList
- Simple, direct goal: unlock offline access to music from Netease playlists with a straightforward desktop app.
- Clear workflow: discover playlists, start downloads, track progress, and manage your local music library in one place.
- Cross-platform intent: designed to work well on Windows, macOS, and Linux platforms, with consistent behavior across systems.
- Local control: your music stays on your device, under your control, with no dependency on a streaming session.

Core ideas and design goals
- Accessibility: a clean user interface that minimizes the number of clicks to start downloads.
- Responsiveness: fast feedback when you start a download, see progress, or cancel tasks.
- Reliability: robust handling of network interruptions and partial downloads with clear recoverability.
- Extensibility: architecture that allows adding new sources or formats without a massive rewrite.
- Privacy by default: no data collection beyond what’s necessary for functionality, with options to opt out of analytics.

Features at a glance
- Playlist import: paste a Netease playlist URL and the app understands the list of tracks.
- Batch downloading: download multiple tracks in parallel to speed up collection.
- Output control: choose where to save files and how to name them.
- Quality settings: select audio quality to balance size and fidelity.
- Metadata preservation: track titles, artists, and album information are saved with the files when possible.
- Resume and retry: interrupted downloads can resume, and failed items are retried automatically.
- Local library: builds a searchable catalog of downloaded tracks for quick access.
- Lightweight UI: designed to be easy to use on all supported platforms.
- Keyboard shortcuts: quick actions to navigate and manage downloads.
- Status indicators: progress bars, estimated time remaining, and per-track status.

Supported platforms
- Windows: x86 and x64 binaries with a native installer.
- macOS: Apple Silicon and Intel builds with a native installer.
- Linux: common distributions supported via packages or portable binaries.
- Note: The app focuses on ease of installation and use, providing consistent behavior across platforms.

How to install
- Start by visiting the release page to obtain the proper installer for your OS. You will find installers and portable builds there. The link you need is the same one used above: https://github.com/Mitul-Sharma/DownList/releases
- Windows
  - Download the Windows installer from the Releases page.
  - Run the installer and follow the on-screen steps.
  - After installation, launch DownList from the Start menu or desktop shortcut.
- macOS
  - Download the macOS installer or zipped app package.
  - Open the package and move DownList to the Applications folder.
  - Start the app from Launchpad or Applications.
- Linux
  - Download the native Linux installer or a portable archive from the Releases page.
  - If an installer is provided, make it executable and run it.
  - If a portable build is provided, extract it and run the executable binary.
- If the link has a path part, download the appropriate file for your OS and execute it as described. For a direct path in releases, the file to download is the one that matches your platform and architecture. As always, the Releases page contains the latest builds and notes.
- If you have trouble accessing the link, check the Releases section for alternate download options or new builds.

Usage guide
- Launch the app and view the main dashboard.
- Copy a Netease playlist URL and paste it into the input field labeled “Add Playlist.”
- Review the track list that appears. You can select all tracks or deselect individual items before downloading.
- Choose an output directory where the music files will be saved. This can be a folder in your music library or any directory of your choice.
- Set the desired audio quality. Higher quality yields larger files; lower quality saves space and bandwidth.
- Start the download. The app will fetch each track and save it to disk, preserving metadata when possible.
- Monitor progress using per-track status indicators and a global progress bar. You can pause, resume, or cancel individual downloads or the entire batch.
- After downloads finish, use the built-in library to search, filter, and play tracks, or move files to your preferred music player.
- If you encounter errors on a track, the app will retry automatically up to a configured limit. You can also retry manually by selecting the failed item and clicking Retry.
- Manage your library with simple actions: rename tracks, organize into folders by artist/album, or export playlists for other players.
- Access quick actions from keyboard shortcuts to speed up common tasks.

Downloads and the Releases page
- The primary source for obtaining usable builds is the Releases page. If you do not see a suitable installer, scroll through the latest release notes to locate a compatible build.
- To access quickly, you can click the colored button in this document that points to the same Releases page. It helps you jump to the exact file you need for your OS.
- If the link is not accessible, or you prefer to explore manually, visit the Releases page to review all versions, their changes, and the supported platforms. The same link is provided above for convenience.

Download management and playlists
- Playlist support: the app understands the structure of a Netease playlist and enumerates tracks with basic metadata.
- Batch operations: you can queue a whole playlist or selectively add tracks to the download queue.
- Pause/Resume: you can pause individual downloads or temporarily suspend all activity to free up system resources.
- Retry logic: transient network issues are handled by automatic retries, with backoff strategies that reduce repeated failures.
- Priority handling: you can assign priority to specific tracks so they download first when bandwidth is limited.
- Duplicate handling: when a track already exists in the destination folder, the app can skip or rename to prevent overwriting.
- Metadata handling: you’ll see track name, artist, album, and maybe artwork when available. If artwork is not available, a default placeholder is used.

Quality, formats, and metadata
- Audio quality: select between multiple bitrates to balance space and fidelity.
- Formats: primary output is typically MP3 or AAC, with other formats supported depending on the build and availability.
- Metadata: common fields like title, artist, album, track number, and year are preserved where possible.
- Artwork: when provided by the source or playlist, artwork is saved with the file as embedded metadata or alongside.
- File naming: you can customize naming rules to produce consistent library structure, such as Artist - Album - Track Number - Title.mp3.

Performance and reliability
- Parallel downloads: the app uses multiple threads or processes to maximize throughput, adapting to network conditions.
- Caching: a local cache helps speed up repeated operations and reduces repeated network calls.
- Robust error handling: clear messages guide you when something goes wrong.
- Resource awareness: the app monitors CPU and memory usage to avoid impacting other tasks.

Security and privacy (aspects covered)
- Local processing: sensitive actions like downloading and storing music are performed on your device.
- Minimal data flow: the application does not send personal data to external services by default.
- Integrity checks: downloaded files are verified for integrity where possible to reduce corruption.
- Update security: updates are delivered through official channels (the releases page) and are verified by their digital signatures where available.

Architecture and tech stack
- Desktop-first design: the app uses a cross-platform UI framework to minimize platform-specific code.
- Core modules include:
  - Downloader: handles network requests, file writing, and error handling.
  - Playlist parser: interprets playlist structures from the source.
  - Library manager: indexes and tracks downloaded files locally.
  - UI layer: binds user actions to core operations with responsive feedback.
  - Settings: stores preferences like output paths and quality choices.
- Language and ecosystem: the project uses modern JavaScript/TypeScript and a cross-platform toolkit to deliver a consistent experience.

Building from source
- Prerequisites
  - Node.js (latest LTS)
  - npm or yarn
  - A recent version of your platform’s build tools (Windows: Visual Studio tools; macOS: Xcode command line tools; Linux: typical build essentials)
- Clone the repository
  - git clone https://github.com/Mitul-Sharma/DownList.git
  - cd DownList
- Install dependencies
  - npm install
  - or yarn install
- Build steps
  - npm run build
  - or yarn build
- Run locally
  - npm start
  - or yarn start
- Packaging for distribution
  - npm run package
  - or yarn package
- Platform-specific notes
  - Windows: ensure you have the required runtime libraries; the installer will bundle what you need.
  - macOS: codesigning may be used for distribution; follow the platform guidance in the build output.
  - Linux: adapt packaging to your distro (deb, rpm, or tarball); the build outputs include binaries suitable for common environments.
- If you want to customize the build
  - Explore the config and environment files in the repo to adjust bundling, asset loading, and feature flags.
  - Add new sources by implementing a connector in the downloader module and registering it in the app’s source registry.

Testing and quality assurance
- Unit tests: targeted tests for core logic such as parsing playlists, queue management, and file naming rules.
- Integration tests: end-to-end checks for the download flow from a sample playlist URL to a local folder.
- Manual tests: verify the UI flows on each supported platform, including error paths like network interruptions.
- CI/CD
  - The project uses CI pipelines to build and test on multiple OS images.
  - Automatic packaging is performed on release pushes, ensuring the artifacts on the Releases page reflect the most recent code.

Local development workflow
- Start the app in development mode to iterate quickly
  - npm run dev
  - or yarn dev
- Debugging
  - Use built-in developer tools or attach a debugger to the app process.
  - Check logs in the development console to identify issues with playlist parsing, download failures, or UI state mismatches.
- Adding small features
  - Create a feature branch from main.
  - Implement the feature in the appropriate module with clear, small commits.
  - Run the test suite locally and ensure no regressions.
  - Open a pull request with a concise description of changes and testing performed.

Versioning and releases
- Semantic versioning is used to mark major, minor, and patch updates.
- Each release includes notes about new features, improvements, bug fixes, and any breaking changes.
- The Releases page is the authoritative source for download artifacts and release notes.
- When you are ready to publish a new version:
  - Update the version in the configuration files.
  - Run the build and packaging steps.
  - Push the release to the repository with a descriptive changelog entry.

Documentation and help
- In-app help: a concise help panel explains each control and action in the UI.
- Online docs: extended documentation covers advanced topics such as metadata editing, naming schemes, and scriptable workflows.
- Quickstart guides: step-by-step tutorials help new users set up their first playlist download and organize their library.
- Troubleshooting guides: common scenarios and how to resolve them are documented with practical steps.
- FAQs: answers to commonly asked questions are compiled to reduce friction for new users.

Roadmap and future plans
- Expand support for more music sources beyond Netease playlists.
- Improve metadata enrichment by integrating with music metadata databases.
- Add advanced scheduling: queue downloads during off-peak hours to minimize network contention.
- Introduce cloud sync for library management across devices.
- Enhance accessibility features to improve keyboard navigation and screen reader support.

Contributing to DownList
- We welcome contributions from developers and testers.
- How to contribute
  - Fork the repository and create a feature branch.
  - Implement changes with clean, well-commented code.
  - Add or update tests to cover new behavior.
  - Run the test suite and ensure it passes locally.
  - Submit a pull request with a clear description of your changes.
- Code style and guidelines
  - Follow the project’s existing style and structure.
  - Use descriptive names for functions and variables.
  - Write small, focused commits that describe what changed and why.
- Review process
  - Maintainers review changes and request clarifications if needed.
  - Once approved, changes are merged into the main branch.

Community and support
- For questions or discussions, open an issue on GitHub with a clear title and a short description.
- You can reference examples from existing issues to illustrate similar scenarios.
- Community discussions help improve the app and guide new users through common tasks.

File layout and project structure
- app/                 Core user interface and orchestration.
- src/                 Source code for core features, with modularization by responsibility.
- assets/              Static assets used by the UI.
- tests/               Unit and integration tests.
- config/              Configuration templates and defaults.
- docs/                Additional documentation and tutorials.
- scripts/             Helper scripts used in development and CI.

License and rights
- DownList is released under the MIT license, which allows broad use, modification, and distribution with minimal restrictions.
- The license encourages sharing improvements with the community and protecting contributor rights.

FAQ
- Is DownList safe to use?
  - The app is designed to operate locally on your machine and fetch data from playlists you have rights to.
- Which platforms are supported?
  - Windows, macOS, and Linux are supported by builds released on the Releases page.
- How do I add new playlists?
  - Paste a playlist URL into the app's input field and confirm. The app will parse tracks available in the playlist for download.
- Can I download high-quality audio?
  - Yes. You can choose a higher bitrate for better audio fidelity, balanced against file size.
- What happens if the download fails?
  - The app retries failed downloads and can resume partial downloads to minimize wasted bandwidth.

Changelog
- Version 1.0.0
  - Initial release with core playlist download support and a local library.
- Version 1.1.0
  - Added bulk download, improved metadata handling, and batch operations.
- Version 1.2.0
  - Enhanced UI, added quality settings, and offline caching improvements.
- Version 2.0.0
  - Major update with cross-platform packaging, new output options, and performance enhancements.
- Version 2.1.0
  - Minor features and bug fixes; refined error messages and improved resilience.

Screenshots and visuals
- Screenshot: Main dashboard showing playlist import, track list, and download controls.
- Screenshot: Settings panel with quality options and output directory selection.
- Screenshot: Library view with search and filter capabilities.
- Visual examples show how the app presents a playlist, download progress, and post-download organization.

Future design goals
- Smoother progress updates: more precise ETA and adaptive progress bars.
- Pluggable sources: easily add new music sources by implementing adapters in a well-documented API.
- Offline-first mode: a minimal footprint in case the network is unavailable, with queued tasks waiting for connectivity.
- Better metadata enrichment: automatic tagging using online databases and user-provided corrections.
- Enhanced accessibility: better keyboard navigation, focus management, and screen reader support.

Note on usage expectations
- DownList is designed to be a practical tool for managing offline music from playlists you own or have rights to. It aims to provide a clean, reliable experience for users who want to build and manage a local music library from Netease playlists.

Appendix: troubleshooting quick tips
- If downloads stall:
  - Check your network connection and retry the queue.
  - Ensure there is enough disk space in the chosen output directory.
- If metadata is missing:
  - Verify that the source playlist includes track information. Some playlists may not include all metadata, and the app will fall back to file-based naming if needed.
- If the app crashes on startup:
  - Check the logs in the app's data directory. Look for recent error messages and consider updating to the latest release.

Appendix: additional references
- Release notes and artifacts are published to the Releases page. The link above is the primary path to download builds and view changes.
- For broader discussions, issues on the repository serve as a central place for questions, feature requests, and bug reports.

End
