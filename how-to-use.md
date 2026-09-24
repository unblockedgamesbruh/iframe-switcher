How to Use Resource Switcher
1. Project Setup

Place the project files in the following structure:

/
├── index.html
├── manifest.json
├── readme.md
├── how-to-use.md
└── icons/
    ├── icon-192.png
    └── icon-512.png


The main page should be named:

index.html

2. Opening the Application

Open index.html in a compatible browser.

The first resource in the resource list will automatically load into the full-screen iframe.

The application interface consists primarily of the embedded webpage.

The ≡ button in the upper-left corner opens the resource menu.

3. Selecting a Resource

Click the ≡ button.

A resource menu will appear.

Select a resource from the list.

The application will:

Load the selected URL.

Mark the selected resource as active.

Close the resource menu.

The selected webpage will then occupy the full browser window.

4. Closing the Menu

The resource menu can be closed by:

Clicking the ≡ button again.

Selecting a resource.

Clicking outside the menu.

Pressing the Escape key.

5. Adding a Resource

Open index.html.

Find the resource list:

<div
    class="resource-list"
    id="resourceList">


Add another button inside it:

<button
    class="resource-button"
    type="button"
    data-url="https://example.com">

    Example Resource

</button>


Replace:

https://example.com


with the URL you want to load.

Replace:

Example Resource


with the name you want displayed in the menu.

For example:

<button
    class="resource-button"
    type="button"
    data-url="https://example.org">

    Example Website

</button>


No JavaScript changes are necessary.

6. Changing the First Resource

The first resource in the list is automatically loaded when the application starts.

For example:

<button
    class="resource-button active"
    type="button"
    data-url="https://example.com">

    Example Website

</button>


The active class identifies the initial resource.

7. Changing the Application Name

Open manifest.json.

Change:

"name": "Resource Switcher"


to the desired application name.

You can also change:

"short_name": "Resources"


The short name is useful when the available space is limited, such as underneath an installed application icon.

8. Changing the Application Colors

The manifest currently uses:

"background_color": "#111111",
"theme_color": "#111111"


You can replace these hexadecimal colors with your preferred colors.

For example:

"background_color": "#000000",
"theme_color": "#2563eb"

9. Application Icons

The manifest expects these files:

icons/icon-192.png
icons/icon-512.png


The files should be PNG images with the corresponding dimensions:

icon-192.png — 192 × 192 pixels

icon-512.png — 512 × 512 pixels

The same visual design should normally be used for both icons.

The ≡ symbol can be used as the basis of the application icon.

10. Installing as an App

When the application is hosted on a compatible HTTPS website, a supported browser may offer an installation option.

Depending on the browser and device, this may appear as:

Install

Install app

Add to Home Screen

Add to desktop

Once installed, the application can launch using the standalone display mode specified in manifest.json.

11. Hosting

For the best results, host the project from a web server.

For example:

https://example.com/


The application files can then be placed at:

https://example.com/index.html
https://example.com/manifest.json
https://example.com/readme.md
https://example.com/how-to-use.md


The icon files would be available at:

https://example.com/icons/icon-192.png
https://example.com/icons/icon-512.png


HTTPS is recommended, particularly when using Progressive Web App installation features.

12. If a Resource Does Not Load

If a resource doesn't appear inside the iframe, first try opening its URL directly in a new browser tab.

If it works directly but not inside Resource Switcher, the website may be blocking iframe embedding.

Common mechanisms include:

X-Frame-Options
Content-Security-Policy


These restrictions are controlled by the website being embedded and normally cannot be bypassed by the Resource Switcher.

13. Updating Resources

To change an existing resource, find its button in index.html and change its data-url.

For example:

<button
    class="resource-button"
    type="button"
    data-url="https://new-example.com">

    New Example

</button>


Save the file and reload the application.

14. Recommended Backup

Before making substantial changes, keep a backup of:

index.html
manifest.json


The Markdown documentation files can also be kept under version control if the project is being developed over time.
