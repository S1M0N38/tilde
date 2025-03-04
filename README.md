<h1 align="center">~</h1>

A minimal custom browser startpage with command shortcuts.

Based on [original tilde project](https://github.com/xvvvyz/tilde).

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/S1M0N38/tilde.git
   cd tilde
   ```

2. Set up auto-start with launchd (macOS):

   ```bash
   # Copy the launchd plist to your LaunchAgents directory
   cp com.simo.httpserver.plist ~/Library/LaunchAgents/

   # Load the service
   launchctl load ~/Library/LaunchAgents/com.simo.httpserver.plist
   ```

3. Configure your browser to use http://localhost:5130 as your homepage.

## Managing the Service

To manage the launchd service:

```bash
# Start the service
launchctl start com.simo.httpserver

# Stop the service
launchctl stop com.simo.httpserver

# Restart the service
launchctl stop com.simo.httpserver
launchctl start com.simo.httpserver

# Unload service (to disable autostart)
launchctl unload ~/Library/LaunchAgents/com.simo.httpserver.plist

# Check service status
launchctl list | grep com.simo.httpserver
```

## Usage

Once running, access the startpage at http://localhost:5130

### Navigation

- Press any key to activate the search dialog
- Use configured shortcuts:
  - `c` - Claude AI
  - `p` - Projects
  - `g` - GitHub
  - `r` - Reddit
  - `t` - Google Translate
  - `s` - Spotify
  - `y` - YouTube
  - `0` - localhost

### Advanced Usage

- Type `shortcut/path` to navigate to specific paths
  - Example: `g/S1M0N38` navigates to your GitHub profile
- Type `shortcut search-term` to search within a site
  - Example: `g tilde` searches GitHub for "tilde"

## Customization

Edit the `COMMANDS` map in `index.html` to modify shortcuts and add your own favorite sites.
