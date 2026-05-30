---
title: Uninstall GIMP
summary: Uninstalling GIMP on linux.
subtitle: Uninstalling GIMP on linux.
date: 2025-05-18T11:19:00+08:00
lastmod: 2025-05-18T11:19:00+08:00
_build:
  render: always
  list: always
draft: false
categories: 📝 Notes
tags:
  - linux
---
1. Open a terminal (`Ctrl` + `Alt` + `T`).
2. Run the following command:

    ```bash
    sudo apt remove --purge gimp
    ```

3. (Optional) To remove unused dependencies:

    ```bash
    sudo apt autoremove
    ```

4. (Optional) To remove GIMP's configuration files in your home directory:

    ```bash
    rm -r ~/.config/GIMP ~/.gimp-*
    ```
