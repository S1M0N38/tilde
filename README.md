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

## Usage

Access the page at http://localhost:5130

- Press any key to activate the search dialog
- Use configured shortcuts (examples: 'c' for Claude, 'g' for GitHub)
- Type 'shortcut/path' to navigate to specific paths
- Type 'shortcut search-term' to search within a site

## Customization

Edit the `COMMANDS` map in `index.html` to modify shortcuts.
