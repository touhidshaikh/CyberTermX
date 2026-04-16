# CyberTermX Theme (Jekyll)

A terminal-themed, hacker-aesthetic Jekyll portfolio designed specifically for cybersecurity professionals, exploit developers, and bug bounty hunters. 

This theme is **100% dynamic**. You do not need to touch any HTML to update your portfolio. Everything is managed through simple YAML configuration files.

## Features
- **Hacker Aesthetic:** Matrix background, CRT scanlines, and neon-terminal UI built with Tailwind CSS.
- **Fully Configurable:** Update your identity, skills, projects, and CVEs strictly through `_config.yml` and the `_data/` directory.
- **Interactive Terminal:** A working web-based shell that visitors can use to run commands (`whoami`, `ls`, `neofetch`, `crack`, `hack`, etc.).
- **Dynamic RSS Integration:** Automatically pulls your latest blog posts from your WordPress site via the rss2json API.
- **Easter Eggs:** Hidden commands, Konami code integration, and cinematic "Hollywood hacking" sequences.
- **Mobile Responsive:** Looks great on desktop monitors and mobile devices.

## Quick Start

1. **Fork this repository** to your own GitHub account.
2. Rename the repository to `yourusername.github.io`.
3. Go to repository **Settings > Pages** and ensure GitHub Pages is building from the `main` branch.
4. Edit the `_config.yml` file with your personal details.
5. Your site will be live at `https://yourusername.github.io`!

### Local Development
If you want to run the site locally:
```bash
git clone https://github.com/Writeup-DB/CyberTermX.git
cd yourusername.github.io
bundle install
bundle exec jekyll serve
```
Then navigate to http://localhost:4000 in your browser.

### Directory Structure
```plaintext
.
├── _config.yml          # Core settings (Name, Socials, Certs)
├── terminal.json        # Data bridge for the interactive shell
├── _data/               # YAML files for your content
│   ├── broadcasts.yml   # Talks, presentations, conferences
│   ├── cves.yml         # Vulnerability research
│   ├── honors.yml       # Text-based awards/recognitions
│   ├── projects.yml     # GitHub repos and tools
│   ├── publications.yml # Articles and writeups
│   └── testimonials.yml # LinkedIn recommendations
├── _includes/           # Core HTML components (do not edit unless customizing)
│   ├── easter-egg.html  # Hidden terminal scripts
│   ├── head.html        # Meta tags and CSS
│   ├── scripts.html     # Terminal logic and API calls
│   └── sidebar.html     # Left-column profile layout
├── _layouts/
│   └── default.html     # Main grid structure
└── index.html           # Right-column content layout

```

### Documentation
Please see [CONFIGURATION.md](CONFIGURATION.md) for detailed instructions on how to update your data, add CVEs, and customize the interactive terminal.

### `CONFIGURATION.md`
This file acts as a manual, explaining exactly how another user can swap out your details for theirs.

### Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

### License 
This project is open-source and available under the MIT License.
