# Git CheatSheet

Git adalah sistem kontrol versi yang memungkinkan Anda melacak perubahan pada file dan folder. Ini adalah alat canggih yang dapat digunakan untuk segala hal mulai dari proyek pribadi kecil hingga aplikasi perusahaan berskala besar.

Panduan ini adalah referensi singkat ke perintah Git yang paling umum. Ini tidak dimaksudkan sebagai panduan komprehensif tentang Git, melainkan referensi singkat ke perintah-perintah yang paling umum.

# Setup and Configuration

```

git init // Initialize a new Git repository

git clone <url> // Clone and create a local copy of a remote repository

git config --global <setting_name> <value> // Configure global Git settings

git config --local <setting_name> <value> // Configure local Git settings for a specific repo

# --------------- Advanced ------------------


git config --list // Show a summary of your Git configuration settings

git config --global core.editor "<editor_command>" // Set a custom text editor for Git messages

git config --global alias.<shortcut> <command> // Create a Git command alias

git config --global color.ui auto // Enable automatic colorization of Git output

git config --global credential.helper 'cache --timeout=<seconds>' // Cache Git credentials for a certain amount of time

git config --global core.whitespace <options> // Configure git to detect specific types of whitespace errors

git config --global fetch.prune true // Automatically prune remote-tracking branches when fetching updates

git config --global diff.tool <tool> // Set a custom diff tool for Git

git config --global merge.tool <tool> // Set a custom merge tool for Git

git difftool // Compare changes using a custom diff tool

git mergetool // Resolve merge conflicts with a custom merge tool
```
