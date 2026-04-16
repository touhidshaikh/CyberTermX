# Configuration Guide

This theme is designed to be managed entirely via YAML files. This guide explains how to customize your portfolio.

## 1. Global Settings (`_config.yml`)
The `_config.yml` file acts as the brain of your website. Update the following fields:

```yaml
title: YOUR NAME | SECURITY RESEARCHER
url: "[https://yourdomain.com](https://yourdomain.com)" # Your actual domain
drive_link_resume: "[https://drive.google.com/](https://drive.google.com/)..." # Link for terminal 'download' command
rss2json_api_key: "YOUR_API_KEY" # Get a free key from rss2json.com for your blog feed

author:
  name: "Your Name"
  role: "Security_Researcher // Exploit_Developer"
  location: "City, Country"
  ip_address: "127.0.0.1" # Change to a fun IP if desired
  pgp_public_key: |
    -----BEGIN PGP PUBLIC KEY BLOCK-----
    ...
    -----END PGP PUBLIC KEY BLOCK-----

# Update your certifications here. They will appear in the header and terminal.
certifications:
  - name: "OSCP"
    url: "[https://link-to-cert.com](https://link-to-cert.com)"

# Update your skills. These appear in the sidebar and terminal 'cat skills.txt'
skills: ["VAPT", "WEB_EXPLOIT", "PYTHON"]

# Add your usernames. If left blank, the section will disappear.
social:
  github: "username"
  linkedin: "username"
  twitter: "username"
  hackthebox: "userid"
  bugcrowd: "username"

```

## 2. Managing Content (_data/)
Instead of editing HTML, you update the files in the `_data` folder. The theme automatically loops through these files and formats them into the terminal UI.

### Adding a CVE (`_data/cves.yml`)
```yaml
- id: "CVE-2024-XXXXX"
  title: "Target Name - Vulnerability Type."
```

### Adding a Project (`_data/projects.yml`)
```yaml
- name: "ToolName"
  url: "[https://github.com/](https://github.com/)..."
  desc: "A brief description of what the tool does."
```

### Adding a Testimonial (`_data/testimonials.yml`)
```yaml
- name: John Doe
  org: Company Name
  quote: "An outstanding penetration tester..."
  border_color: "border-blue-900" # Tailwind border color
```

## 3. The Interactive Terminal
The terminal logic is located in `_includes/scripts.html`. It automatically reads from your `_config.yml` and `_data/` files using a JSON bridge (`terminal.json`).

### Built-in Commands:
- `help` - Lists available commands.
- `whoami` - Prints your name and role.
- `ls` - Lists simulated files.
- `cat skills.txt` - Prints your skills array.
- `cat cve_list.txt` - Prints your `cves.yml` IDs.
- `certs` - Prints your certifications.
- `neofetch` - Prints a stylized system info block.
- `download` - Opens your `drive_link_resume` URL.
- `clear` - Clears the terminal.

### Easter Eggs (Spoilers!)
The terminal includes hidden commands configured in `_includes/easter-egg.html`:
- `crack`: Triggers a Fallout-style terminal password cracking mini-game. (Type exit to abort).
- `hack` or `pwned`: Triggers an automated Hollywood-style hacking sequence simulating a buffer overflow and memory brute-force.
- `rm -rf /`: Triggers a fake kernel panic, turning the screen red, hiding elements, and dropping the user into the Matrix.
- Konami Code: Entering `Up Up Down Down Left Right Left Right B A` on the keyboard inverts the site colors.