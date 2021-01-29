# WSU Reuther ArchivesSpace Customizations

This ArchivesSpace plugins includes customizations to the Wayne State University Library's ArchivesSpace Public User Interface: http://archives.wayne.edu

## Installation

Clone this repository to `/path/to/archivesspace/plugins` and enable the plugin by editing the `/path/to/archivesspace/config/config.rb`:

```
AppConfig[:plugins] = ['reuther_aspace_pui_customizations']
```

## How it Works

This plugin includes the following modifications to the ArchivesSpace PUI:

### Styling and Branding

`public/assets/wsu.css` overrides default theming for various elements. Images included in the `public/assets` directory are used for branding purposes.

### Translations

`public/locales/en.yml` adds custom translations for various labels throughout the application.

### Home

`public/plugin_init.rb` adds a Home link to the ArchivesSpace navigation menu.

### Welcome Page

`public/views/welcome/show.html.erb` overrides a default ArchivesSpace template to move text below search and customize the introductory language included on the welcome page.

### Header and Footer

`public/views/shared/_header.html.erb` overrides a default ArchivesSpace template to add a request for feedback alert to the header. `public/views/shared/_footer.html.erb` overrides a default ArchivesSpace template to remove the feedback link.

### Analytics

Add the following to `/path/to/archivesspace/config/config.rb` to enable the Google Analytics tracking snippet in `public/views/layout_head.html.erb`:

```
AppConfig[:google_analytics_key] = 'your_key_here'
```
