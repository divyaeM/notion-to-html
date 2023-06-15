# Why this fork?

- Added possibility to export other files in addition to .pdf files.
- Added possibility to scrape additional data which could be used to

```
    _   __      __  _                _____                        __          __
   / | / /___  / /_(_)___  ____     / ___/____  ____ _____  _____/ /_  ____  / /_
  /  |/ / __ \/ __/ / __ \/ __ \    \__ \/ __ \/ __ `/ __ \/ ___/ __ \/ __ \/ __/
 / /|  / /_/ / /_/ / /_/ / / / /   ___/ / / / / /_/ / /_/ (__  ) / / / /_/ / /_
/_/ |_/\____/\__/_/\____/_/ /_/   /____/_/ /_/\__,_/ .___/____/_/ /_/\____/\__/
                                                    /_/

Back up your data – free yourself from the Notion lock-in.
```

| <img width="685" src="docs/assets/export.jpeg"> | <img width="685" src="docs/assets/snapshot.jpeg"> | <img width="685" src="docs/assets/original.jpeg"> |
| :---------------------------------------------: | :-----------------------------------------------: | :-----------------------------------------------: |
|                 Export with Notion              |        Export with **✨NotionSnapshot✨**          |                   Original page                   |

Notion's default HTML export lacks style (and even content), while our files retain the original page's appearance and remove unnecessary JavaScript resulting in smaller file sizes and faster load times.

<br><br><br>

# How to use

### 1. Make Notion page public

To export a page from Notion to HTML and make it publicly accessible, follow these steps:

1. Open the desired page in Notion
2. Navigate to the `Publish` tab
3. Locate the `Publish to web` button and click on it
4. A link to the page will be generated. Click on the `Copy web link` button to save the link

Remember to store the copied link in a place where you can easily find it later.

<br>

### 2. Install Python and Chrome

Next, ensure that you have the necessary apps installed on your machine:

-   [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) if you're running Windows, as this tool is designed for Unix systems

-   [Python 3](https://www.python.org/downloads/)

-   [Chrome](https://www.google.com/chrome/)

Installing Chrome on WSL/Ubuntu may require a few extra steps, but you can follow this method:

```bash
sudo apt update && sudo apt upgrade -y
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt --fix-broken install
rm -rf google-chrome-stable_current_amd64.deb
```

<br>

### 3. Run script

Then just run the script like so:

```bash
git clone https://github.com/sueszli/notionSnapshot.git
cd notionSnapshot
python3 notionsnapshot --dark-mode <insert your url here>

# for help run:
# python3 notionsnapshot --help
```

Our test pages are listed in the `test.sh` file.

<br><br><br><br>

---

Special thanks to:

-   Leonardo Cavaletti who laid the foundation of this project with his lovely loconotion project
-   [MJDeligan](https://github.com/MJDeligan) the main contributor
-   Stefan Brandmair, Thomas Biedermann and Berndt Uhlig who helped me set the project up

