Resource Switcher

A lightweight, full-screen web resource switcher that lets you open multiple web resources from a single interface.

The project is designed to feel more like a simple standalone application than a traditional webpage.

Features

Full-screen iframe interface

Floating ≡ resource menu

Smooth menu animations

Active-resource indicator

Mobile-friendly layout

Click-outside menu closing

Escape-key menu closing

Support for older browsers

Web App Manifest support

Standalone/PWA installation support

Custom application icons

No external JavaScript libraries required

Project Structure
/
├── index.html
├── manifest.json
├── readme.md
├── how-to-use.md
└── icons/
    ├── icon-192.png
    └── icon-512.png

Files
index.html

The main application.

It contains:

The full-screen iframe

The ≡ menu button

The resource list

The menu styling

The resource-switching logic

Legacy browser compatibility code

manifest.json

Defines the web application metadata.

It provides:

Application name

Short application name

Description

Start URL

Application scope

Standalone display mode

Theme color

Background color

Application icons

readme.md

Provides an overview of the project and its structure.

how-to-use.md

Provides instructions for configuring and using the application.

icons/

Contains the application icons referenced by manifest.json.

Requirements

The application does not require a server-side backend.

A modern web browser is recommended.

Some older browsers may have limited support for Progressive Web App features even though the application itself can still function.

Important iframe limitation

The application uses an <iframe> to display the selected resources.

A website may prevent itself from being displayed inside an iframe using security policies such as:

X-Frame-Options

Content-Security-Policy

When a website blocks iframe embedding, the Resource Switcher cannot override that restriction from normal client-side JavaScript.

The resource may still work when opened directly in a browser tab.

Adding Resources

Resources are defined in index.html.

Each resource uses a button similar to:

<button
    class="resource-button"
    type="button"
    data-url="https://example.com">

    Example Resource

</button>


The text between the button tags is what appears in the resource menu.

The data-url attribute contains the webpage that should be loaded into the iframe.

License

No license has been specified yet.
