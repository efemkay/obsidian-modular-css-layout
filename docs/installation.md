---
nav_order: 2
---

# Installation

This is actually just a CSS code snippets collection. So it isn't an installation per se, but rather **download and enable** in Obsidian.

### Using Snippet Downloader (recommended)
Snippet Downloader is an Obsidian community plugin by Mara Li. Since I'm planning to update this snippets from time to time, this is the recommended approach as the plugin also provides a way to update/redownload from included repository

{: .note-title }
> Lisandra-dev Snippet Downloader plugin still can be used to install MCL (updated 27Aug2023)
>
> [Lisandra-dev](https://github.com/Lisandra-dev/obsidian-snippet-downloader) recently archived the plugin, but it is still very much functional for downloading snippets. There's additional step for you to install the plugin (since it's no longer available via Community Plugins) - it is reflected below...

{: .warning }
> Please ensure your vault's /.obsidian/snippets folder is already created before doing the following steps. You can do that by going to `Settings > Appearance` and click "Open snippets folder" under CSS snippets section

1. Install **Obsidian42 - BRAT** plugin and enable it
	- Go to `Settings > Community Plugins` and under **Community plugins** click **Browse** button
	- Search for `Obsidian42 - BRAT`, install it and enable it
2. Add Snippet Downloader plugin via BRAT
	- Open Command Palette (hotkey: `Ctrl/Cmd P`)
	- Search for `Obsidian 42 - BRAT: Plugins: Add a beta plugin for testing` and press `Enter`
	- Enter Snippet Downloader URL into the input box
	   `https://github.com/Lisandra-dev/obsidian-snippet-downloader`
3. Ensure Obsidian snippets folder already created
	- Go to `Settings > Appearance`
	- Under **CSS snippets** section, click on the folder icon on the far right
	   *this will create snippets folder inside your Obsidian vault (if you don't have one yet)*
4. Add MCL snippets (https://github.com/efemkay/obsidian-modular-css-layout) via Snippets Downloader
	- Open Command Palette (hotkey: `Ctrl/Cmd P`)
	- Search for `Snippet Downloader: Adding new snippet` and press `Enter`
	- Enter MCL GitHub URL into the input box
	   `https://github.com/efemkay/obsidian-modular-css-layout`
	- Enable MCL snippets by going back to `Settings > Appearance` and under **CSS snippets** section (where you'll find the MCL snippets already downloaded into your vault)


{: .note-title }
> Example on how to install using Snippets Downloader
>
> <iframe width="560" height="315" src="https://www.youtube.com/embed/F9z5spGosDI?si=PL4EwJ9wdMyYHCUh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Manually Saving from GH

- Open your browser and go to MCL's GH [landing page](https://github.com/efemkay/obsidian-modular-css-layout)
- Click on the snippet you want to save, (on the blob page) click on "Raw" at the top left, and (on the raw page) copy the entire text
> *GH raw page will open up the css file within your browser in plain-text format for easy copy pasting*
- Open any text editor in your desktop and paste the snippet
- Save the file as a `.css` file into your `[vault]/.obsidian/snippets` folder. Filename can be anything.
- Open Obisidian and go to `Settings > Appearance > CSS snippets` to enable the snippet.
> *Click on "Reload snippets" button if the snippet does not appear in the list.*
