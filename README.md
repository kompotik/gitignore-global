Нужно подключение к интернету для успешного завершения команд, которые нужны выполнить в терминале, чтобы создать глобальный gitignore-файл:
```bash
echo -e '# This file based on https://github.com/github/gitignore' > ~/.gitignore_global
echo -e '\n\n### MacOS\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/macOS.gitignore >> ~/.gitignore_global
echo -e '\n\n### Linux\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/Linux.gitignore >> ~/.gitignore_global
echo -e '\n\n### Windows\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/Windows.gitignore >> ~/.gitignore_global
echo -e '\n\n### Vim\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/Vim.gitignore >> ~/.gitignore_global
echo -e '\n\n### SublimeText\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/SublimeText.gitignore >> ~/.gitignore_global
echo -e '\n\n### Visual Studio Code\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/VisualStudioCode.gitignore >> ~/.gitignore_global
echo -e '\n\n### JetBrains\n' >> ~/.gitignore_global
curl https://raw.githubusercontent.com/github/gitignore/master/Global/JetBrains.gitignore >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
cat ~/.gitignore_global
```


Последняя команда `cat ~/.gitignore_global`, должна вывести на экран, примерно, следующее:
```text
# This file based on https://github.com/github/gitignore


### MacOS

# General
*.DS_Store
.AppleDouble
.LSOverride

# Icon must end with two \r
Icon


# Thumbnails
._*

# Files that might appear in the root of a volume
.DocumentRevisions-V100
.fseventsd
.Spotlight-V100
.TemporaryItems
.Trashes
.VolumeIcon.icns
.com.apple.timemachine.donotpresent

# Directories potentially created on remote AFP share
.AppleDB
.AppleDesktop
Network Trash Folder
Temporary Items
.apdisk


### Linux

*~

# temporary files which can be created if a process still has a handle open of a deleted file
.fuse_hidden*

# KDE directory preferences
.directory

# Linux trash folder which might appear on any partition or disk
.Trash-*

# .nfs files are created when an open file is removed but is still being accessed
.nfs*


### Windows

# Windows thumbnail cache files
Thumbs.db
ehthumbs.db
ehthumbs_vista.db

# Dump file
*.stackdump

# Folder config file
Desktop.ini

# Recycle Bin used on file shares
$RECYCLE.BIN/

# Windows Installer files
*.cab
*.msi
*.msm
*.msp

# Windows shortcuts
*.lnk


### Vim

# Swap
[._]*.s[a-v][a-z]
[._]*.sw[a-p]
[._]s[a-v][a-z]
[._]sw[a-p]

# Session
Session.vim

# Temporary
.netrwhist
*~
# Auto-generated tag files
tags


### SublimeText

# Cache files for Sublime Text
*.tmlanguage.cache
*.tmPreferences.cache
*.stTheme.cache

# Workspace files are user-specific
*.sublime-workspace

# Project files should be checked into the repository, unless a significant
# proportion of contributors will probably not be using Sublime Text
# *.sublime-project

# SFTP configuration file
sftp-config.json

# Package control specific files
Package Control.last-run
Package Control.ca-list
Package Control.ca-bundle
Package Control.system-ca-bundle
Package Control.cache/
Package Control.ca-certs/
Package Control.merged-ca-bundle
Package Control.user-ca-bundle
oscrypto-ca-bundle.crt
bh_unicode_properties.cache

# Sublime-github package stores a github token in this file
# https://packagecontrol.io/packages/sublime-github
GitHub.sublime-settings


### Visual Studio Code

.vscode/*
!.vscode/settings.json
!.vscode/tasks.json
!.vscode/launch.json
!.vscode/extensions.json


### JetBrains

# Covers JetBrains IDEs: IntelliJ, RubyMine, PhpStorm, AppCode, PyCharm, CLion, Android Studio and Webstorm
# Reference: https://intellij-support.jetbrains.com/hc/en-us/articles/206544839

# User-specific stuff:
.idea/**/workspace.xml
.idea/**/tasks.xml
.idea/dictionaries

# Sensitive or high-churn files:
.idea/**/dataSources/
.idea/**/dataSources.ids
.idea/**/dataSources.xml
.idea/**/dataSources.local.xml
.idea/**/sqlDataSources.xml
.idea/**/dynamic.xml
.idea/**/uiDesigner.xml

# Gradle:
.idea/**/gradle.xml
.idea/**/libraries

# CMake
cmake-build-debug/

# Mongo Explorer plugin:
.idea/**/mongoSettings.xml

## File-based project format:
*.iws

## Plugin-specific files:

# IntelliJ
/out/

# mpeltonen/sbt-idea plugin
.idea_modules/

# JIRA plugin
atlassian-ide-plugin.xml

# Cursive Clojure plugin
.idea/replstate.xml

# Crashlytics plugin (for Android Studio and IntelliJ)
com_crashlytics_export_strings.xml
crashlytics.properties
crashlytics-build.properties
fabric.properties

```


Если что-то не так, можно запустить комманды снова.
