# Git CheatSheet

Git adalah sistem kontrol versi yang memungkinkan Anda melacak perubahan pada file dan folder. Ini adalah alat canggih yang dapat digunakan untuk segala hal mulai dari proyek pribadi kecil hingga aplikasi perusahaan berskala besar.

Panduan ini adalah referensi singkat ke perintah Git yang paling umum. Ini tidak dimaksudkan sebagai panduan komprehensif tentang Git, melainkan referensi singkat ke perintah-perintah yang paling umum.

# Setup and Configuration

```
// Initialize a new Git repository
git init
// Clone and create a local copy of a remote repository
git clone <url>
// Configure global Git settings
git config --global <setting_name> <value>
// Configure local Git settings for a specific repo
git config --local <setting_name> <value>

# --------------- Advanced ------------------

// Show a summary of your Git configuration settings
git config --list
// Set a custom text editor for Git messages
git config --global core.editor "<editor_command>"
// Create a Git command alias
git config --global alias.<shortcut> <command>
// Enable automatic colorization of Git output
git config --global color.ui auto
// Cache Git credentials for a certain amount of time
git config --global credential.helper 'cache --timeout=<seconds>'
// Configure git to detect specific types of whitespace errors
git config --global core.whitespace <options>
// Automatically prune remote-tracking branches when fetching updates
git config --global fetch.prune true
// Set a custom diff tool for Git
git config --global diff.tool <tool>
// Set a custom merge tool for Git
git config --global merge.tool <tool>
// Compare changes using a custom diff tool
git difftool
// Resolve merge conflicts with a custom merge tool
git mergetool
```
