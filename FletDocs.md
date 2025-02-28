  Introduction | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs//img/logo.svg)![Flet Logo](https://flet.dev/docs//img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs//img/logo.svg)![Flet Logo](https://flet.dev/docs//img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   Introduction

On this page

# Introduction

## What is Flet?[​](#what-is-flet "Direct link to What is Flet?")

Flet is a framework that allows building web, desktop and mobile applications in Python without prior experience in frontend development.

You can build a UI for your program with Flet [controls](/docs/controls) which are based on [Flutter](https://flutter.dev) by Google. Flet goes beyond merely wrapping Flutter widgets. It adds its own touch by combining smaller widgets, simplifying complexities, implementing UI best practices, and applying sensible defaults. This ensures that your applications look stylish and polished without requiring additional design efforts on your part.

## Flet app example[​](#flet-app-example "Direct link to Flet app example")

Create a sample "Counter" app:

counter.py

```
import flet as ftdef main(page: ft.Page):    page.title = "Flet counter example"    page.vertical_alignment = ft.MainAxisAlignment.CENTER    txt_number = ft.TextField(value="0", text_align=ft.TextAlign.RIGHT, width=100)    def minus_click(e):        txt_number.value = str(int(txt_number.value) - 1)        page.update()    def plus_click(e):        txt_number.value = str(int(txt_number.value) + 1)        page.update()    page.add(        ft.Row(            [                ft.IconButton(ft.Icons.REMOVE, on_click=minus_click),                txt_number,                ft.IconButton(ft.Icons.ADD, on_click=plus_click),            ],            alignment=ft.MainAxisAlignment.CENTER,        )    )ft.app(main)
```

To run the app install `flet` module ([create a new Flet environment](/docs/getting-started)):

```
pip install flet
```

and [run the program](/docs/getting-started/running-app):

```
flet run counter.py
```

The app will be started in a native OS window - what a nice alternative to Electron!

### macOS

![](https://flet.dev/docs//img/docs/getting-started/flet-counter-macos.png)

### Windows

![](https://flet.dev/docs//img/docs/getting-started/flet-counter-windows.png)

Now, run your app as a web app:

```
flet run --web counter.py
```

A new browser window or tab will be opened:

![](https://flet.dev/docs//img/docs/getting-started/flet-counter-safari.png)

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/introduction.md)

[

Next

Getting started

](/docs/getting-started/)

-   [What is Flet?](#what-is-flet)
-   [Flet app example](#flet-app-example)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Gallery | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/gallery/img/logo.svg)![Flet Logo](https://flet.dev/gallery/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

# Gallery

[![](https://flet.dev/gallery/img/gallery/controls-gallery.png)

## Controls gallery

Interactive showcase app for Flet controls with code samples.

](https://flet-controls-gallery.fly.dev/)

[](https://github.com/flet-dev/examples/tree/main/python/apps/controls-gallery "View source code")

[![](https://flet.dev/gallery/img/gallery/todo.png)

## To-Do

A classic To-Do app inspired by TodoMVC project.

](https://gallery.flet.dev/todo/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/todo/todo.py "View source code")

[![](https://flet.dev/gallery/img/gallery/icons-browser.png)

## Icons browser

Quickly search through icons collection to use in your app.

](https://gallery.flet.dev/icons-browser/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/icons-browser/main.py "View source code")

[![](https://flet.dev/gallery/img/gallery/calc.png)

## Calculator

A simple calculator app.

](https://gallery.flet.dev/calculator/)

[](https://github.com/flet-dev/examples/blob/main/python/tutorials/calc/calc.py "View source code")

[![](https://flet.dev/gallery/img/gallery/solitaire.png)

## Solitaire

Learn how to handle gestures and position controls on a page.

](https://gallery.flet.dev/solitaire/)

[](https://github.com/flet-dev/examples/tree/main/python/tutorials/solitaire/solitaire-final-part1 "View source code")

[![](https://flet.dev/gallery/img/gallery/chat.gif)

## Chat

Multi-user realtime chat.

](https://flet-chat.fly.dev)

[](https://github.com/flet-dev/examples/blob/main/python/tutorials/chat/chat.py "View source code")

[![](https://flet.dev/gallery/img/gallery/trolli.png)

## Trolli

A clone of Trello.

](https://gallery.flet.dev/trolli/)

[](https://github.com/flet-dev/examples/tree/main/python/apps/trolli "View source code")

[![](https://flet.dev/gallery/img/gallery/flet-animation.png)

## Flet animation

Implicit animations in Flet.

](https://gallery.flet.dev/flet-animation/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/flet-animation/main.py "View source code")

[![](https://flet.dev/gallery/img/gallery/counter.png)

## Counter

Counter with button click event handlers.

](https://gallery.flet.dev/counter/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/counter/counter.py "View source code")

[![](https://flet.dev/gallery/img/gallery/routing.gif)

## Routing

URL routing between views.

](https://gallery.flet.dev/simple-routing/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/routing-navigation/home-store.py "View source code")

[![](https://flet.dev/gallery/img/gallery/hello-world.png)

## Hello, world!

All examples start with that!

](https://gallery.flet.dev/hello-world/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/hello-world/hello.py "View source code")

[![](https://flet.dev/gallery/img/gallery/greeter.png)

## Greeter

Interactive form in Flet.

](https://gallery.flet.dev/greeter/)

[](https://github.com/flet-dev/examples/blob/main/python/apps/greeter/greeter.py "View source code")

[![](https://flet.dev/gallery/img/gallery/emoji-enigma.png)

## Emoji Enigma

Guess 20 words using the emote icons as clues

](https://ee.lshss.app/)

[](https://github.com/vihutuo/emoji_riddles "View source code")

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Roadmap | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/roadmap/img/logo.svg)![Flet Logo](https://flet.dev/roadmap/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

# Roadmap

## 2025[​](#2025 "Direct link to 2025")

### Flet 1.0[​](#flet-10 "Direct link to Flet 1.0")

-   **Long-term maintainability:** Controls are implemented using Python **dataclasses**, while the Flutter client adopts the built-in state management approach, eliminating the need for Redux. Ensures symmetric data structures in Python and Dart.
-   **Enhanced Developer Experience (DX):** Control documentation is generated directly from source code, preventing discrepancies between docs, comments, and examples. Provides accurate IDE assistance.
-   **Optimized Communication:** A binary protocol between Python and Dart eliminates unnecessary base64-to-bytes conversions, reducing CPU overhead and improving memory efficiency.

Flet 0.90 will be released as a preparatory step for Flet 1.0, introducing major changes, including breaking updates.

### Website[​](#website "Direct link to Website")

-   **Ecosystem:** Community gallery for apps, extensions and educational materials (videos, tutorials, talks, etc.).

### Testing[​](#testing "Direct link to Testing")

-   Test suite for Flet controls.
-   Test suite for non-pure Python modules.

### Controls[​](#controls "Direct link to Controls")

-   ✅ [Google Mobile Ads](https://github.com/flet-dev/flet/issues/286)
-   ✅ [DropdownMenu](https://github.com/flet-dev/flet/issues/1088)
-   🚧 [Camera](https://github.com/flet-dev/flet/issues/1281)
-   [DataTable2](https://github.com/flet-dev/flet/issues/4576)
-   [Context menu](https://github.com/flet-dev/flet/issues/1804)
-   [InAppPurchase](https://github.com/flet-dev/flet/issues/853)
-   [PlatformMenuBar](https://github.com/flet-dev/flet/issues/285) (and [#116](https://github.com/flet-dev/flet/issues/116))
-   [SliverAppBar](https://github.com/flet-dev/flet/issues/1843)
-   [TreeView](https://github.com/flet-dev/flet/issues/961)
-   [Sms](https://github.com/flet-dev/flet/issues/3195)

### Community[​](#community "Direct link to Community")

-   Presenting poster at [PyCon US 2025](https://us.pycon.org/2025/)

### Packaging[​](#packaging "Direct link to Packaging")

-   Flet Packaging and Publishing Service (FPS).

-   [2025](#2025)
    -   [Flet 1.0](#flet-10)
    -   [Website](#website)
    -   [Testing](#testing)
    -   [Controls](#controls)
    -   [Community](#community)
    -   [Packaging](#packaging)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Blog | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/blog/img/logo.svg)![Flet Logo](https://flet.dev/blog/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

All posts

### 2025

-   [Tap into native Android and iOS APIs with Pyjnius and Pyobjus](/blog/tap-into-native-android-and-ios-apis-with-Pyjnius-and-pyobjus)
-   [Flet v0.27.0 Release Announcement](/blog/flet-v-0-27-release-announcement)
-   [Flet v0.26.0 Release Announcement](/blog/flet-v-0-26-release-announcement)

### 2024

-   [Flet v0.25.0 Release Announcement](/blog/flet-v-0-25-release-announcement)
-   [pyproject.toml support for flet build command](/blog/pyproject-toml-support-for-flet-build-command)
-   [Flet new packaging pre-release](/blog/flet-new-packaging-pre-release)
-   [Flet v0.24.0 Release Announcement](/blog/flet-v-0-24-release-announcement)
-   [Flet v0.23.0 Release Announcement](/blog/flet-v-0-23-release-announcement)
-   [Flet at PyCon US 2024](/blog/flet-at-pycon-us-2024)
-   [Flet packaging update](/blog/flet-packaging-update)
-   [Controls and theming enhancements](/blog/controls-and-theming-enhancements)
-   [Flet FastAPI and async API improvements](/blog/flet-fastapi-and-async-api-improvements)
-   [Flet adaptive UI and custom controls release](/blog/flet-adaptive-and-custom-controls)

### 2023

-   [Packaging apps for distribution](/blog/packaging-apps-for-distribution)
-   [Flet for FastAPI](/blog/flet-for-fastapi)
-   [Flet for Android](/blog/flet-for-android)
-   [Flet for iOS](/blog/flet-for-ios)
-   [Scrolling controls and Theming](/blog/scrolling-controls-and-theming)
-   [Canvas](/blog/canvas)
-   [Flet Charts](/blog/flet-charts)
-   [Standalone Flet web apps with Pyodide](/blog/standalone-flet-web-apps-with-pyodide)
-   [Packaging desktop apps with a custom icon](/blog/packaging-desktop-apps-with-custom-icon)

### 2022

-   [Flet mobile update](/blog/flet-mobile-update)
-   [Flet versioning and pre-releases](/blog/flet-versioning-and-pre-releases)
-   [ResponsiveRow and mobile controls](/blog/responsive-row-and-mobile-controls)
-   [Matplotlib and Plotly charts](/blog/matplotlib-and-plotly-charts)
-   [Gesture detector](/blog/gesture-detector)
-   [User authentication](/blog/user-authentication)
-   [File picker and uploads](/blog/file-picker-and-uploads)
-   [Fun with animations](/blog/fun-with-animations)
-   [Beautiful gradients, button styles and TextField rounded corners in a new Flet release](/blog/gradients-button-textfield-styles)
-   [Control Refs](/blog/control-refs)
-   [Flet Mobile Strategy](/blog/flet-mobile-strategy)
-   [Navigation and Routing](/blog/navigation-and-routing)
-   [New release: Drag and Drop, absolute positioning and clickable container](/blog/drag-and-drop-release)
-   [Using custom fonts in a Flet app](/blog/using-custom-fonts-in-flet-app)
-   [Introducing Flet](/blog/introducing-flet)

## [Tap into native Android and iOS APIs with Pyjnius and Pyobjus](/blog/tap-into-native-android-and-ios-apis-with-Pyjnius-and-pyobjus)

February 23, 2025 · 3 min read

[![Feodor Fitsner](https://avatars0.githubusercontent.com/u/5041459?s=400&v=4)](https://github.com/FeodorFitsner)

[Feodor Fitsner](https://github.com/FeodorFitsner)

Flet founder and developer

When building mobile apps with Flet, you may need to interact directly with platform-specific APIs. Whether it’s accessing system information, managing Bluetooth devices, or working with user preferences, **Pyjnius** and **Pyobjus** by Kivy provide a seamless way to bridge Python with Java (for Android) and Objective-C (for iOS).

You can now integrate both Pyjnius and Pyobjus into your Flet apps! 🚀

**Tags:**

-   [releases](/blog/tags/releases)

[**Read more**](/blog/tap-into-native-android-and-ios-apis-with-Pyjnius-and-pyobjus)

## [Flet v0.27.0 Release Announcement](/blog/flet-v-0-27-release-announcement)

February 20, 2025 · 5 min read

[![Feodor Fitsner](https://avatars0.githubusercontent.com/u/5041459?s=400&v=4)](ttps://github.com/FeodorFitsner)

[Feodor Fitsner](ttps://github.com/FeodorFitsner)

Flet founder and developer

[](https://github.com/FeodorFitsner "GitHub")[](https://x.com/fletdev "X")

Flet 0.27.0 is now released with exciting new features and improvements!

-   **iOS packaging & signing updates** – ensures compliance with App Store Connect verification requirements.
-   **Reduced startup delay** – faster initial launch for desktop applications.
-   **Faster incremental re-builds** – enhances development efficiency with quicker iteration times.
-   **Enhanced Dropdown control** – improved functionality and user experience.
-   **Bug fixes & stability improvements** – various fixes to enhance overall performance and reliability.

**Tags:**

-   [releases](/blog/tags/releases)

[**Read more**](/blog/flet-v-0-27-release-announcement)

## [Flet v0.26.0 Release Announcement](/blog/flet-v-0-26-release-announcement)

January 24, 2025 · 4 min read

[![Feodor Fitsner](https://avatars0.githubusercontent.com/u/5041459?s=400&v=4)](ttps://github.com/FeodorFitsner)

[Feodor Fitsner](ttps://github.com/FeodorFitsner)

Flet founder and developer

[](https://github.com/FeodorFitsner "GitHub")[](https://x.com/fletdev "X")

The Flet 0.26.0 release is here, featuring a significant update to the extensibility approach!

In summary, a Flet extension is now a single Python package that bundles both Python and Flutter code. This package can be part of your Flet project or hosted in a public Git repository or PyPI.

Built-in Flet extensions, such as `Audio`, `Video`, and `Map`, have been moved to their own repositories. You’re welcome to fork these extensions to create your own or contribute to Flet! These extensions have been published to PyPI, making them easy to include in your Flet app. To use them, simply add the desired extensions to the `dependencies` section of your `pyproject.toml` file.

**Tags:**

-   [releases](/blog/tags/releases)

[**Read more**](/blog/flet-v-0-26-release-announcement)

## [Flet v0.25.0 Release Announcement](/blog/flet-v-0-25-release-announcement)

November 27, 2024 · 10 min read

[![Feodor Fitsner](https://avatars0.githubusercontent.com/u/5041459?s=400&v=4)](ttps://github.com/FeodorFitsner)

[Feodor Fitsner](ttps://github.com/FeodorFitsner)

Flet founder and developer

[](https://github.com/FeodorFitsner "GitHub")[](https://x.com/fletdev "X")

Hey Flet developers, we’ve got something exciting to share — Flet 0.25.0 is officially released!

The biggest news? No more Kivy for iOS and Android packaging. No more dealing with frustrating Python binary dependencies — Flet now uses its own custom Python runtime, so your app builds are easier than ever. Plus, we’ve added loads of new features like better permissions control, faster rebuilds, and even a lightweight Linux client that skips the bloat.

Let’s dive into all the cool stuff Flet 0.25.0 has to offer! 🚀

**Tags:**

-   [releases](/blog/tags/releases)

[**Read more**](/blog/flet-v-0-25-release-announcement)

## [pyproject.toml support for flet build command](/blog/pyproject-toml-support-for-flet-build-command)

October 15, 2024 · 5 min read

[![Feodor Fitsner](https://avatars0.githubusercontent.com/u/5041459?s=400&v=4)](ttps://github.com/FeodorFitsner)

[Feodor Fitsner](ttps://github.com/FeodorFitsner)

Flet founder and developer

[](https://github.com/FeodorFitsner "GitHub")[](https://x.com/fletdev "X")

The number of options for `flet build` command grew substantially over the time and it's been inconvenient to carry all these settings in a command line.

Today, we are excited to announce another Flet pre-release which now allows configuring app build settings in `pyproject.toml`!

[**Read more**](/blog/pyproject-toml-support-for-flet-build-command)

[

Older entries

](/blog/page/2)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Getting started | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started//img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started//img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started//img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started//img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   Getting started

On this page

# Getting started

Before you can create your first Flet app you need to setup your development environment which requires Python 3.9 or above and `flet` package.

We recommend installing Flet in a virtual environment which can be done in a number of different ways.

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

### macOS[​](#macos "Direct link to macOS")

Flet supports macOS 11 (Big Sur) or later.

### Windows[​](#windows "Direct link to Windows")

Flet supports 64-bit version of Microsoft Windows 10 or later.

### Linux[​](#linux "Direct link to Linux")

Flet supports Debian Linux 11 or later and Ubuntu Linux 20.04 LTS or later.

There are additional [prerequisites](/docs/publish/linux#prerequisites) when developing and running Flet apps on Linux.

Windows Subsystem for Linux (WSL)

Flet apps can be run on WSL 2 (Windows Subsystem for Linux 2). If you are getting `cannot open display` error [following this guide](https://github.com/microsoft/wslg/wiki/Diagnosing-%22cannot-open-display%22-type-issues-with-WSLg) for troubleshooting.

#### Audio support[​](#audio-support "Direct link to Audio support")

If you recieve `error while loading shared libraries: libgstapp-1.0.so.0` GStreamer is not installed in your WSL environment.

To install GStreamer run the following command:

```
apt install -y libgstreamer1.0-0 gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-tools
```

#### Video support[​](#video-support "Direct link to Video support")

Video support in Flet on WSL requires `libmpv` library.

If you recieve `error while loading shared libraries: libmpv.so.1: cannot open shared object file: No such file or directory` it means the library is not installed.

To install `libmpv` run the following commands:

```
sudo apt updatesudo apt install libmpv-dev libmpv2sudo ln -s /usr/lib/x86_64-linux-gnu/libmpv.so /usr/lib/libmpv.so.1
```

## Virtual environment[​](#virtual-environment "Direct link to Virtual environment")

You can create virtual environment by running the following commands in your terminal:

-   macOS
-   Linux
-   Windows

```
mkdir first-flet-appcd first-flet-apppython3 -m venv .venvsource .venv/bin/activate
```

```
mkdir first-flet-appcd first-flet-apppython3 -m venv .venvsource .venv/bin/activate
```

```
md first-flet-appcd first-flet-apppython -m venv .venv.venv\Scripts\activate
```

Once you activated virtual environment, you'll see that your prompt now shows `(.venv)` prefix.

Now you can install the latest version of Flet in `.venv` virtual environment:

-   macOS
-   Linux
-   Windows

```
pip install 'flet[all]'
```

```
pip install flet[all]
```

```
pip install flet[all]
```

To check what version of Flet was installed:

```
flet --version
```

You can read more about Python `venv` module [here](https://docs.python.org/3/library/venv.html).

Now you are ready to [create your first Flet app](/docs/getting-started/create-flet-app).

## Poetry[​](#poetry "Direct link to Poetry")

Another way to setup a virtual environment for your Flet project is using [Poetry](https://python-poetry.org/docs/).

Poetry 2.0

All Poetry examples in Flet docs is for Poetry 2.0 as it supports standard `[project]` section in `pyproject.toml`.

Once you have Poetry [installed](https://python-poetry.org/docs/#installation), run the following commands in your terminal:

```
mkdir my-appcd my-apppoetry init --dev-dependency='flet[all]' --python='>=3.9' --no-interaction
```

This command will create `pyproject.toml` in `my-app` directory.

Run the following command to install Flet and other dependencies:

```
poetry install --no-root
```

Make sure Flet CLI has been installed and can be run:

```
poetry run flet --version
```

Now you are ready to [create your first Flet app](/docs/getting-started/create-flet-app).

note

When [creating](/docs/getting-started/create-flet-app) and [running](/docs/getting-started/running-app) Flet app using Poetry, you'll need to use `poetry run` before each command!

## uv[​](#uv "Direct link to uv")

**uv** is "An extremely fast Python package and project manager, written in Rust."

[Install `uv`](https://github.com/astral-sh/uv?tab=readme-ov-file#installation) and run the following commands in your terminal:

```
mkdir my-appcd my-appuv init
```

This command will create `pyproject.toml` in `my-app` directory.

Run the following command to add Flet as dependency:

```
uv add 'flet[all]' --dev
```

Make sure Flet CLI has been installed and can be run:

```
uv run flet --version
```

Now you are ready to [create your first Flet app](/docs/getting-started/create-flet-app).

note

When [creating](/docs/getting-started/create-flet-app) and [running](/docs/getting-started/running-app) Flet app using uv, you'll need to use `uv run` before each command!

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/index.md)

[

Previous

Introduction

](/docs/)[

Next

Create a new Flet app

](/docs/getting-started/create-flet-app)

-   [Prerequisites](#prerequisites)
    -   [macOS](#macos)
    -   [Windows](#windows)
    -   [Linux](#linux)
-   [Virtual environment](#virtual-environment)
-   [Poetry](#poetry)
-   [uv](#uv)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Create a new Flet app | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/create-flet-app/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/create-flet-app/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/create-flet-app/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/create-flet-app/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Create a new Flet app

# Create a new Flet app

Create a new directory (or directory with `pyproject.toml` already exists if initialized with `poetry` or `uv`) and switch into it.

To create a new "minimal" Flet app run the following command:

-   venv
-   uv
-   poetry

```
flet create
```

```
uv run flet create
```

```
poetry run flet create
```

The command will create the following directory structure:

```
├── README.md├── pyproject.toml├── src│   ├── assets│   │   └── icon.png│   └── main.py└── storage    ├── data    └── temp
```

note

Original `pyproject.toml` created by `uv init` or `poetry init` will be replaced with the one from Flet app template.

`src/main.py` contains Flet program. It has `main()` function where you would add UI elements ([controls](/docs/getting-started/flet-controls)) to a page or a window. The application ends with a blocking `ft.app()` function which initializes Flet app and [runs](/docs/getting-started/running-app) `main()`.

You can find more information about `flet create` command [here](/docs/reference/cli/create).

Now let's see Flet in action by [running the app](/docs/getting-started/running-app)!

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/create-flet-app.md)

[

Previous

Getting started

](/docs/getting-started/)[

Next

Running Flet app

](/docs/getting-started/running-app)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Running Flet app | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/running-app/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/running-app/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/running-app/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/running-app/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Running Flet app

On this page

# Running Flet app

Flet app can be run as a desktop or web app using a single `flet run` command.

## Run as a desktop app[​](#run-as-a-desktop-app "Direct link to Run as a desktop app")

To run Flet app as a desktop app, use the following command:

```
flet run
```

This command will run `main.py` located in the current directory.

If you need to provide a different path to the file, use the following command:

```
flet run [script]
```

To run `main.py` located in a different directory, provide an absolute or a relative path to the directory where it is located, for example:

```
flet run /Users/JohnSmith/Documents/projects/flet-app
```

To run script with a name other than `main.py`, provide an absolute or a relative path to the file, for example:

```
flet run counter.py
```

The app will be started in a native OS window:

### macOS

![](https://flet.dev/docs/getting-started/running-app/img/docs/getting-started/flet-counter-macos.png)

### Windows

![](https://flet.dev/docs/getting-started/running-app/img/docs/getting-started/flet-counter-windows.png)

## Run as a web app[​](#run-as-a-web-app "Direct link to Run as a web app")

To run Flet app as a web app, use the following command:

```
flet run --web [script]
```

A new browser window/tab will be opened and the app will be using a random TCP port:

![](https://flet.dev/docs/getting-started/running-app/img/docs/getting-started/flet-counter-safari.png)

To run on a fixed port use `--port` (`-p`) option, for example:

```
flet run --web --port 8000 app.py
```

## Hot reload[​](#hot-reload "Direct link to Hot reload")

By default, Flet will watch the script file that was run and reload the app whenever the file is changed and saved, but will not watch for changes in other files.

To watch all the files in the same directory, use the following command:

```
poetry run flet run -d [script]
```

To watch script directory and all sub-directories recursively, use the following command:

```
poetry run flet run -d -r [script]
```

You can find more information about `flet run` command [here](/docs/reference/cli/run).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/running-app.md)

[

Previous

Create a new Flet app

](/docs/getting-started/create-flet-app)[

Next

Flet controls

](/docs/getting-started/flet-controls)

-   [Run as a desktop app](#run-as-a-desktop-app)
-   [Run as a web app](#run-as-a-web-app)
-   [Hot reload](#hot-reload)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Flet controls | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/flet-controls/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/flet-controls/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/flet-controls/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/flet-controls/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Flet controls

On this page

# Flet controls

User interface is made of **Controls** (aka widgets). To make controls visible to a user they must be added to a `Page` or inside other controls. Page is the top-most control. Nesting controls into each other could be represented as a tree with Page as a root.

Controls are just regular Python classes. Create control instances via constructors with parameters matching their properties, for example:

```
t = ft.Text(value="Hello, world!", color="green")
```

To display control on a page add it to `controls` list of a Page and call `page.update()` to send page changes to a browser or desktop client:

```
import flet as ftdef main(page: ft.Page):    t = ft.Text(value="Hello, world!", color="green")    page.controls.append(t)    page.update()ft.app(main)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/controls-text.png)

note

In the following examples we will be showing just the contents of `main` function.

You can modify control properties and the UI will be updated on the next `page.update()`:

```
t = ft.Text()page.add(t) # it's a shortcut for page.controls.append(t) and then page.update()for i in range(10):    t.value = f"Step {i}"    page.update()    time.sleep(1)
```

Some controls are "container" controls (like Page) which could contain other controls. For example, `Row` control allows arranging other controls in a row one-by-one:

```
page.add(    ft.Row(controls=[        ft.Text("A"),        ft.Text("B"),        ft.Text("C")    ]))
```

or `TextField` and `ElevatedButton` next to it:

```
page.add(    ft.Row(controls=[        ft.TextField(label="Your name"),        ft.ElevatedButton(text="Say my name!")    ]))
```

`page.update()` is smart enough to send only the changes made since its last call, so you can add a couple of new controls to the page, remove some of them, change other controls' properties and then call `page.update()` to do a batched update, for example:

```
for i in range(10):    page.controls.append(ft.Text(f"Line {i}"))    if i > 4:        page.controls.pop(0)    page.update()    time.sleep(0.3)
```

Some controls, like buttons, could have event handlers reacting on a user input, for example `ElevatedButton.on_click`:

```
def button_clicked(e):    page.add(ft.Text("Clicked!"))page.add(ft.ElevatedButton(text="Click me", on_click=button_clicked))
```

and more advanced example for a simple To-Do:

```
import flet as ftdef main(page):    def add_clicked(e):        page.add(ft.Checkbox(label=new_task.value))        new_task.value = ""        new_task.focus()        new_task.update()    new_task = ft.TextField(hint_text="What's needs to be done?", width=300)    page.add(ft.Row([new_task, ft.ElevatedButton("Add", on_click=add_clicked)]))ft.app(main)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/simple-ToDo.png)

info

Flet implements *imperative* UI model where you "manually" build application UI with stateful controls and then mutate it by updating control properties. Flutter implements *declarative* model where UI is automatically re-built on application data changes. Managing application state in modern frontend applications is inherently complex task and Flet's "old-school" approach could be more attractive to programmers without frontend experience.

### `visible` property[​](#visible-property "Direct link to visible-property")

Every control has `visible` property which is `true` by default - control is rendered on the page. Setting `visible` to `false` completely prevents control (and all its children if any) from rendering on a page canvas. Hidden controls cannot be focused or selected with a keyboard or mouse and they do not emit any events.

### `disabled` property[​](#disabled-property "Direct link to disabled-property")

Every control has `disabled` property which is `false` by default - control and all its children are enabled. `disabled` property is mostly used with data entry controls like `TextField`, `Dropdown`, `Checkbox`, buttons. However, `disabled` could be set to a parent control and its value will be propagated down to all children recursively.

For example, if you have a form with multiple entry control you can set `disabled` property for each control individually:

```
first_name = ft.TextField()last_name = ft.TextField()first_name.disabled = Truelast_name.disabled = Truepage.add(first_name, last_name)
```

or you can put form controls into container, e.g. `Column` and then set `disabled` for the column:

```
first_name = ft.TextField()last_name = ft.TextField()c = ft.Column(controls=[    first_name,    last_name])c.disabled = Truepage.add(c)
```

## Buttons[​](#buttons "Direct link to Buttons")

`Button` is the most essential input control which generates `click` event when pressed:

```
btn = ft.ElevatedButton("Click me!")page.add(btn)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/getting-user-input-elevated-button.png)

All events generated by controls on a web page are continuously sent back to your script, so how do you respond to a button click?

## Event handlers[​](#event-handlers "Direct link to Event handlers")

Buttons with events in "Counter" app:

```
import flet as ftdef main(page: ft.Page):    page.title = "Flet counter example"    page.vertical_alignment = ft.MainAxisAlignment.CENTER    txt_number = ft.TextField(value="0", text_align="right", width=100)    def minus_click(e):        txt_number.value = str(int(txt_number.value) - 1)        page.update()    def plus_click(e):        txt_number.value = str(int(txt_number.value) + 1)        page.update()    page.add(        ft.Row(            [                ft.IconButton(ft.Icons.REMOVE, on_click=minus_click),                txt_number,                ft.IconButton(ft.Icons.ADD, on_click=plus_click),            ],            alignment=ft.MainAxisAlignment.CENTER,        )    )ft.app(main)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/getting-user-input-event-handlers.png)

## Textbox[​](#textbox "Direct link to Textbox")

Flet provides a number of [controls](/docs/controls) for building forms: [TextField](/docs/controls/textfield), [Checkbox](/docs/controls/checkbox), [Dropdown](/docs/controls/dropdown), [ElevatedButton](/docs/controls/elevatedbutton).

Let's ask a user for a name:

```
import flet as ftdef main(page):    def btn_click(e):        if not txt_name.value:            txt_name.error_text = "Please enter your name"            page.update()        else:            name = txt_name.value            page.clean()            page.add(ft.Text(f"Hello, {name}!"))    txt_name = ft.TextField(label="Your name")    page.add(txt_name, ft.ElevatedButton("Say hello!", on_click=btn_click))ft.app(main)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/getting-user-input-textbox.png)

## Checkbox[​](#checkbox "Direct link to Checkbox")

The [Checkbox](/docs/controls/checkbox) control provides you with various properties and events emmiters for ease of use.

Let's create a one checkbox ToDo:

```
import flet as ftdef main(page):    def checkbox_changed(e):        output_text.value = (            f"You have learned how to ski :  {todo_check.value}."        )        page.update()    output_text = ft.Text()    todo_check = ft.Checkbox(label="ToDo: Learn how to use ski", value=False, on_change=checkbox_changed)    page.add(todo_check, output_text)ft.app(main)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/getting-user-input-checkbox.png)

## Dropdown[​](#dropdown "Direct link to Dropdown")

```
import flet as ftdef main(page: ft.Page):    def button_clicked(e):        output_text.value = f"Dropdown value is:  {color_dropdown.value}"        page.update()    output_text = ft.Text()    submit_btn = ft.ElevatedButton(text="Submit", on_click=button_clicked)    color_dropdown = ft.Dropdown(        width=100,        options=[            ft.dropdown.Option("Red"),            ft.dropdown.Option("Green"),            ft.dropdown.Option("Blue"),        ],    )    page.add(color_dropdown, submit_btn, output_text)ft.app(main)
```

![](https://flet.dev/docs/getting-started/flet-controls/img/docs/getting-started/getting-user-input-dropdown.png)

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/flet-controls.md)

[

Previous

Running Flet app

](/docs/getting-started/running-app)[

Next

Custom controls

](/docs/getting-started/custom-controls)

-   [`visible` property](#visible-property)
-   [`disabled` property](#disabled-property)
-   [Buttons](#buttons)
-   [Event handlers](#event-handlers)
-   [Textbox](#textbox)
-   [Checkbox](#checkbox)
-   [Dropdown](#dropdown)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Custom controls | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/custom-controls/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/custom-controls/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/custom-controls/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/custom-controls/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Custom controls

On this page

# Custom controls

While Flet provides 100+ built-in controls that can be used on their own, the real beauty of programming with Flet is that all those controls can be utilized for creating your own reusable UI components using Python object-oriented programming concepts.

You can create custom controls in Python by styling and/or combining existing Flet controls.

## Styled controls[​](#styled-controls "Direct link to Styled controls")

The most simple custom control you can create is a styled control, for example, a button of a certain color and behaviour that will be used multiple times throughout your app.

To create a styled control, you need to create a new class in Python that inherits from the Flet control you are going to customize, `ElevatedButton` in this case:

```
class MyButton(ft.ElevatedButton):    def __init__(self, text):        super().__init__()        self.bgcolor = ft.Colors.ORANGE_300        self.color = ft.Colors.GREEN_800        self.text = text     
```

Your control has a constructor to customize properties and events and pass custom data. Note that you must call `super().__init__()` in your own constructor to have access to the properties and methods of the Flet control from which you inherit.

Now you can use your brand-new control in your app:

```
import flet as ftdef main(page: ft.Page):    page.add(MyButton(text="OK"), MyButton(text="Cancel"))ft.app(main)
```

![](https://flet.dev/docs/getting-started/custom-controls/img/docs/custom-controls/styled-controls.png)

See example of using styled controls in [Calculator App tutorial](/docs/tutorials/python-calculator#styled-controls).

### Handling events[​](#handling-events "Direct link to Handling events")

Similar to properties, you can pass event handlers as parameters into your custom control class constructor:

```
import flet as ftclass MyButton(ft.ElevatedButton):    def __init__(self, text, on_click):        super().__init__()        self.bgcolor = ft.Colors.ORANGE_300        self.color = ft.Colors.GREEN_800        self.text = text        self.on_click = on_clickdef main(page: ft.Page):    def ok_clicked(e):        print("OK clicked")        def cancel_clicked(e):        print("Cancel clicked")    page.add(        MyButton(text="OK", on_click=ok_clicked),        MyButton(text="Cancel", on_click=cancel_clicked),    )ft.app(main)
```

## Composite controls[​](#composite-controls "Direct link to Composite controls")

Composite custom controls inherit from container controls such as `Column`, `Row`, `Stack` or even `View` to combine multiple Flet controls. The example below is a `Task` control that can be used in a To-Do app:

```
import flet as ftclass Task(ft.Row):    def __init__(self, text):        super().__init__()        self.text_view = ft.Text(text)        self.text_edit = ft.TextField(text, visible=False)        self.edit_button = ft.IconButton(icon=ft.Icons.EDIT, on_click=self.edit)        self.save_button = ft.IconButton(            visible=False, icon=ft.Icons.SAVE, on_click=self.save        )        self.controls = [            ft.Checkbox(),            self.text_view,            self.text_edit,            self.edit_button,            self.save_button,        ]    def edit(self, e):        self.edit_button.visible = False        self.save_button.visible = True        self.text_view.visible = False        self.text_edit.visible = True        self.update()    def save(self, e):        self.edit_button.visible = True        self.save_button.visible = False        self.text_view.visible = True        self.text_edit.visible = False        self.text_view.value = self.text_edit.value        self.update()def main(page: ft.Page):    page.add(        Task(text="Do laundry"),        Task(text="Cook dinner"),    )ft.app(main)
```

![](https://flet.dev/docs/getting-started/custom-controls/img/docs/custom-controls/composite-controls.gif)

You can find more examples of composite custom controls in [community examples](https://github.com/flet-dev/examples/tree/main/python/community) and [flet-contrib](https://github.com/flet-dev/flet-contrib/tree/main/flet_contrib) repos.

## Life-cycle methods[​](#life-cycle-methods "Direct link to Life-cycle methods")

Custom controls provide life-cycle "hook" methods that you may need to use for different use cases in your app.

### `build()`[​](#build "Direct link to build")

`build()` method is called when the control is being created and assigned its `self.page`.

Override `build()` method if you need to implement logic that cannot be executed in control's constructor because it requires access to the `self.page`. For example, choose the right icon depending on `self.page.platform` for your [adaptive app](/docs/getting-started/adaptive-apps/#custom-adaptive-controls).

### `did_mount()`[​](#did_mount "Direct link to did_mount")

`did_mount()` method is called after the control is added to the page and assigned transient `uid`.

Override `did_mount()` method if you need to implement logic that needs to be executed after the control was added to the page, for example [Weather widget](https://github.com/flet-dev/examples/tree/main/python/community/weather_widget) which calls Open Weather API every minute to update itself with the new weather conditions.

### `will_unmount()`[​](#will_unmount "Direct link to will_unmount")

`will_unmount()` method is called before the control is removed from the page.

Override `will_unmount()` method to execute clean-up code.

### `before_update()`[​](#before_update "Direct link to before_update")

`before_update()` method is called every time when the control is being updated.

Make sure not to call `update()` method within `before_update()`.

## Isolated controls[​](#isolated-controls "Direct link to Isolated controls")

Custom control has `is_isolated` property which defaults to `False`.

If you set `is_isolated` to `True`, your control will be isolated from outside layout, i.e. when `update()` method is called for the parent control, the control itself will be updated but any changes to the controls' children are not included into the update digest. Isolated controls should call `self.update()` to push its changes to a Flet page.

As a best practice, any custom control that calls `self.update()` inside its class methods should be isolated.

In the above examples, simple styled `MyButton` doesn't need to be isolated, but the `Task` should be:

```
class Task(ft.Row):    def __init__(self, text):        super().__init__()        self.isolated = True
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/custom-controls.md)

[

Previous

Flet controls

](/docs/getting-started/flet-controls)[

Next

Adaptive apps

](/docs/getting-started/adaptive-apps)

-   [Styled controls](#styled-controls)
    -   [Handling events](#handling-events)
-   [Composite controls](#composite-controls)
-   [Life-cycle methods](#life-cycle-methods)
    -   [`build()`](#build)
    -   [`did_mount()`](#did_mount)
    -   [`will_unmount()`](#will_unmount)
    -   [`before_update()`](#before_update)
-   [Isolated controls](#isolated-controls)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Adaptive apps | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/adaptive-apps/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/adaptive-apps/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/adaptive-apps/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/adaptive-apps/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Adaptive apps

On this page

# Adaptive apps

Flet framework allows you to develop adaptive apps which means having a single codebase that will deliver different look depending on the device's platform.

Below is the example of a very simple app that has a different look on iOS and Android platforms:

```
import flet as ftdef main(page):    page.adaptive = True    page.appbar = ft.AppBar(        leading=ft.TextButton("New", style=ft.ButtonStyle(padding=0)),        title=ft.Text("Adaptive AppBar"),        actions=[            ft.IconButton(ft.cupertino_icons.ADD, style=ft.ButtonStyle(padding=0))        ],        bgcolor=ft.Colors.with_opacity(0.04, ft.CupertinoColors.SYSTEM_BACKGROUND),    )    page.navigation_bar = ft.NavigationBar(        destinations=[            ft.NavigationBarDestination(icon=ft.Icons.EXPLORE, label="Explore"),            ft.NavigationBarDestination(icon=ft.Icons.COMMUTE, label="Commute"),            ft.NavigationBarDestination(                icon=ft.Icons.BOOKMARK_BORDER,                selected_icon=ft.Icons.BOOKMARK,                label="Bookmark",            ),        ],        border=ft.Border(            top=ft.BorderSide(color=ft.CupertinoColors.SYSTEM_GREY2, width=0)        ),    )    page.add(        ft.SafeArea(            ft.Column(                [                    ft.Checkbox(value=False, label="Dark Mode"),                    ft.Text("First field:"),                    ft.TextField(keyboard_type=ft.KeyboardType.TEXT),                    ft.Text("Second field:"),                    ft.TextField(keyboard_type=ft.KeyboardType.TEXT),                    ft.Switch(label="A switch"),                    ft.FilledButton(content=ft.Text("Adaptive button")),                    ft.Text("Text line 1"),                    ft.Text("Text line 2"),                    ft.Text("Text line 3"),                ]            )        )    )ft.app(main)
```

By setting just `page.adaptive = True` you can make you app looking awesome on both iOS and Android devices:

### iPhone

![](https://flet.dev/docs/getting-started/adaptive-apps/img/blog/adaptive/iphone-adaptive-app.png)

### Android

![](https://flet.dev/docs/getting-started/adaptive-apps/img/blog/adaptive/android-adaptive-app.png)

## Material and Cupertino controls[​](#material-and-cupertino-controls "Direct link to Material and Cupertino controls")

Most of Flet controls are based on [Material design](https://m3.material.io/).

There is also a number of iOS-style controls in Flet that are called Cupertino controls.

Cupertino controls usually have a matching Material control that has [`adaptive`](/docs/controls#adaptive) property which defaults to`False`. When using a Material control with `adaptive` property set to `True`, a different control will be created depending on the platform, for example:

```
ft.Checkbox(adaptive=True, value=True, label="Adaptive Checkbox")
```

Flet checks the value of [`page.platform`](/docs/controls/page#platform) property and if it is `ft.PagePlatform.IOS` or `ft.PagePlatform.MACOS`, Cupertino control will be created; in all other cases Material control will be created.

note

[`adaptive`](/docs/controls#adaptive) property can be set for an individual control or a container control such as `Row`, `Column` or any other control that has `content` or `controls` property. If container control is adaptive, all its child controls will be adaptive, unless `adaptive` property is explicitly set to `False` for a child control.

Below is the list of adaptive Material controls and their matching Cupertino controls:

[AlertDialog](/docs/controls/alertdialog)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/alertdialog.png)

[CupertinoAlertDialog](/docs/controls/cupertinoalertdialog)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinoalertdialog.png)

[Any button in Dialog actions](/docs/controls/buttons)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/dialogactions.png)

[CupertinoDialogAction](/docs/controls/cupertinodialogaction)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinodialogactions.png)

[AppBar](/docs/controls/appbar)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/appbar.png)

[CupertinoAppBar](/docs/controls/cupertinoappbar)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinoappbar.png)

[NavigationBar](/docs/controls/navigationbar)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/navigationbar.png)

[CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinonavigationbar.png)

[ListTile](/docs/controls/listtile)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/listtile.png)

[CupertinoListTile](/docs/controls/cupertinolisttile)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinolisttile.png)

[TextField](/docs/controls/textfield)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/textfield.png)

[CupertinoTextField](/docs/controls/cupertinotextfield)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinotextfield.png)

[Checkbox](/docs/controls/checkbox)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/checkbox.png)

[CupertinoCheckbox](/docs/controls/cupertinocheckbox)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinocheckbox.png)

[Slider](/docs/controls/slider)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/slider.png)

[CupertinoSlider](/docs/controls/cupertinoslider)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinoslider.png)

[Switch](/docs/controls/switch)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/switch.png)

[CupertinoSwitch](/docs/controls/cupertinoswitch)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinoswitch.png)

[Radio](/docs/controls/radio)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/radio.png)

[CupertinoRadio](/docs/controls/cupertinoradio)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinoradio.png)

[FilledButton](/docs/controls/filledbutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/filledbutton.png)

[CupertinoFilledButton](/docs/controls/cupertinobutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinofilledbutton.png)

[FilledTonalButton](/docs/controls/filledtonalbutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/filledtonalbutton.png)

[CupertinoButton](/docs/controls/cupertinobutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinobutton-filledtonal.png)

[IconButton](/docs/controls/iconbutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/icon-button.png)

[CupertinoButton](/docs/controls/cupertinobutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/icon-button-cupertino.png)

[ElevatedButton](/docs/controls/elevatedbutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/elevatedbutton.png)

[CupertinoButton](/docs/controls/cupertinobutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/cupertinobutton.png)

[OutlinedButton](/docs/controls/outlinedbutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/outlinedbutton.png)

[TextButton](/docs/controls/textbutton)![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/textbutton.png)

## Custom adaptive controls[​](#custom-adaptive-controls "Direct link to Custom adaptive controls")

While Flet offers a number of [controls](#material-and-cupertino-controls) that will be adapted to a platform automatically using their [`adaptive`](/docs/controls#adaptive) property, there will be cases when you need more specific adaptive UI presentation, for example, using different icon, background color, padding etc. depending on the platform.

With Flet, you can create your own reusable custom controls in Python that will inherit from a Flet control and implement specific properties you need. In the example below, we are creating a new `AdaptiveNavigationBarDestination` control that will be displaying different icon on iOS and Android:

```
class AdaptiveNavigationBarDestination(ft.NavigationBarDestination):    def __init__(self, ios_icon, android_icon, label):        super().__init__()        self._ios_icon = ios_icon        self._android_icon = android_icon        self.label = label    def build(self):        # we can check for platform in build method because self.page is known        self.icon = (            self._ios_icon            if self.page.platform == ft.PagePlatform.IOS            or self.page.platform == ft.PagePlatform.MACOS            else self._android_icon        )
```

We will use `AdaptiveNavigationBarDestination` in `NavigationBar`:

```
import flet as ftfrom adaptive_navigation_destination import AdaptiveNavigationBarDestinationdef main(page):    page.adaptive = True    page.navigation_bar = ft.NavigationBar(        selected_index=2,        destinations=[            AdaptiveNavigationBarDestination(                ios_icon=ft.cupertino_icons.PERSON_3_FILL,                android_icon=ft.Icons.PERSON,                label="Contacts",            ),            AdaptiveNavigationBarDestination(                ios_icon=ft.cupertino_icons.CHAT_BUBBLE_2,                android_icon=ft.Icons.CHAT,                label="Chats",            ),            AdaptiveNavigationBarDestination(                ios_icon=ft.cupertino_icons.SETTINGS,                android_icon=ft.Icons.SETTINGS,                label="Settings",            ),        ],    )    page.update()ft.app(main)
```

Now the NavigationBar and icons within it will look like different on Android and iOS:

### iOS

![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/navigation-bar-custom-ios.png)

### Android

![](https://flet.dev/docs/getting-started/adaptive-apps/img/docs/adaptive-apps/navigation-bar-custom-android.png)

note

You may utilise [reusable controls approach](/docs/getting-started/custom-controls) to adapt your app not only depending on the [`platform`](/docs/controls/page#platform) but also use [`page.web`](/docs/controls/page#web) property to have different UI depending on wether the app is running in a browser or not, or even combine `platform` and `web` properties to have specific UI for your MACOS or Windows desktop apps.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/adaptive-apps.md)

[

Previous

Custom controls

](/docs/getting-started/custom-controls)[

Next

Navigation and routing

](/docs/getting-started/navigation-and-routing)

-   [Material and Cupertino controls](#material-and-cupertino-controls)
-   [Custom adaptive controls](#custom-adaptive-controls)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Navigation and routing | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/navigation-and-routing/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/navigation-and-routing/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/navigation-and-routing/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/navigation-and-routing/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Navigation and routing

On this page

# Navigation and routing

Navigation and routing is an essential feature of Single Page Applications (SPA) which allows organizing application user interface into virtual pages (views) and "navigate" between them while application URL reflects the current state of the app.

For mobile apps navigation and routing serves as a [deep linking](https://docs.flutter.dev/development/ui/navigation/deep-linking) to specific application parts.

Well, it took [more efforts](https://github.com/flet-dev/flet/pull/95/files) than expected to add navigation and routing into Flet as the implementation is based on [Navigator 2.0](https://medium.com/flutter/learning-flutters-new-navigation-and-routing-system-7c9068155ade) Flutter API and required to replace Flet's "Page" abstraction with "Page and Views". Flutter's newer navigation and routing API has substantial improvements such as:

1.  Programmatic control over history stack.
2.  An easy way to intercept a call to "Back" button in AppBar.
3.  Robust synchronization with browser history.

![](https://flet.dev/docs/getting-started/navigation-and-routing/img/docs/navigation-routing/routing-app-example.gif)

Explore [source code](https://github.com/flet-dev/examples/blob/main/python/apps/routing-navigation/building-views-on-route-change.py) of the example above.

## Page route[​](#page-route "Direct link to Page route")

Page route is a portion of application URL after `#` symbol:

![](https://flet.dev/docs/getting-started/navigation-and-routing/img/docs/navigation-routing/page-address-route.png)

Default application route, if not set in application URL by the user, is `/`. All routes start with `/`, for example `/store`, `/authors/1/books/2`.

Application route can be obtained by reading `page.route` property, for example:

```
import flet as ftdef main(page: ft.Page):    page.add(ft.Text(f"Initial route: {page.route}"))ft.app(main, view=ft.AppView.WEB_BROWSER)
```

Grab application URL, open a new browser tab, paste the URL, modify its part after `#` to `/test` and hit enter. You should see "Initial route: /test".

Every time the route in the URL is changed (by editing the URL or navigating browser history with Back/Forward buttons) Flet calls `page.on_route_change` event handler:

```
import flet as ftdef main(page: ft.Page):    page.add(ft.Text(f"Initial route: {page.route}"))    def route_change(e: ft.RouteChangeEvent):        page.add(ft.Text(f"New route: {e.route}"))    page.on_route_change = route_change    page.update()ft.app(main, view=ft.AppView.WEB_BROWSER)
```

Now try updating URL hash a few times and then use Back/Forward buttons! You should see a new message added to a page each time the route changes:

![](https://flet.dev/docs/getting-started/navigation-and-routing/img/docs/navigation-routing/page-route-change-event.gif)

Route can be changed programmatically, by updating `page.route` property:

```
import flet as ftdef main(page: ft.Page):    page.add(ft.Text(f"Initial route: {page.route}"))    def route_change(e: ft.RouteChangeEvent):        page.add(ft.Text(f"New route: {e.route}"))    def go_store(e):        page.route = "/store"        page.update()    page.on_route_change = route_change    page.add(ft.ElevatedButton("Go to Store", on_click=go_store))ft.app(main, view=ft.AppView.WEB_BROWSER)
```

Click "Go to Store" button and you'll see application URL is changed and a new item is pushed in a browser history. You can use browser "Back" button to navigate to a previous route.

## Page views[​](#page-views "Direct link to Page views")

Flet's [Page](/docs/controls/page) now is not just a single page, but a container for [View](/docs/controls/view) layered on top of each other like a sandwich:

![](https://flet.dev/docs/getting-started/navigation-and-routing/img/docs/navigation-routing/page-views.svg)

A collection of views represents navigator history. Page has [`page.views`](/docs/controls/page#views) property to access views collection.

The last view in the list is the one currently displayed on a page. Views list must have at least one element (root view).

To simulate a transition between pages change `page.route` and add a new `View` in the end of `page.view` list.

Pop the last view from the collection and change route to a "previous" one in [`page.on_view_pop`](/docs/controls/page#on_view_pop) event handler to go back.

## Building views on route change[​](#building-views-on-route-change "Direct link to Building views on route change")

To build a reliable navigation there must be a single place in the program which builds a list of views depending on the current route. Other words, navigation history stack (represented by the list of views) must be a function of a route.

This place is [`page.on_route_change`](/docs/controls/page#on_route_change) event handler.

Let's put everything together into a complete example which allows navigating between two pages:

```
import flet as ftdef main(page: ft.Page):    page.title = "Routes Example"    def route_change(route):        page.views.clear()        page.views.append(            ft.View(                "/",                [                    ft.AppBar(title=ft.Text("Flet app"), bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST),                    ft.ElevatedButton("Visit Store", on_click=lambda _: page.go("/store")),                ],            )        )        if page.route == "/store":            page.views.append(                ft.View(                    "/store",                    [                        ft.AppBar(title=ft.Text("Store"), bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST),                        ft.ElevatedButton("Go Home", on_click=lambda _: page.go("/")),                    ],                )            )        page.update()    def view_pop(view):        page.views.pop()        top_view = page.views[-1]        page.go(top_view.route)    page.on_route_change = route_change    page.on_view_pop = view_pop    page.go(page.route)ft.app(main, view=ft.AppView.WEB_BROWSER)
```

Try navigating between pages using "Visit Store" and "Go Home" buttons, Back/Forward browser buttons, manually changing route in the URL - it works no matter what! :)

note

To "navigate" between pages we used [`page.go(route)`](/docs/controls/page#goroute) - a helper method that updates [`page.route`](/docs/controls/page#route), calls [`page.on_route_change`](/docs/controls/page#on_route_change) event handler to update views and finally calls `page.update()`.

Notice the usage of [`page.on_view_pop`](/docs/controls/page#on_view_pop) event handler. It fires when the user clicks automatic "Back" button in [`AppBar`](/docs/controls/appbar) control. In the handler we remove the last element from views collection and navigate to view's root "under" it.

## Route templates[​](#route-templates "Direct link to Route templates")

Flet offers [`TemplateRoute`](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet-core/src/flet_core/template_route.py) - an utility class based on [repath](https://github.com/nickcoutsos/python-repath) library which allows matching ExpressJS-like routes and parsing their parameters, for example `/account/:account_id/orders/:order_id`.

`TemplateRoute` plays great with route change event:

```
troute = TemplateRoute(page.route)if troute.match("/books/:id"):    print("Book view ID:", troute.id)elif troute.match("/account/:account_id/orders/:order_id"):    print("Account:", troute.account_id, "Order:", troute.order_id)else:    print("Unknown route")
```

You can read more about template syntax supported by `repath` library [here](https://github.com/nickcoutsos/python-repath#parameters).

## URL strategy for web[​](#url-strategy-for-web "Direct link to URL strategy for web")

Flet web apps support two ways of configuring URL-based routing:

-   **Path** (default) - paths are read and written without a hash. For example, `fletapp.dev/path/to/view`.
-   **Hash** - paths are read and written to the [hash fragment](https://en.wikipedia.org/wiki/Uniform_Resource_Locator#Syntax). For example, `fletapp.dev/#/path/to/view`.

To change URL strategy use `route_url_strategy` parameter of `flet.app()` method, for example:

```
ft.app(main, route_url_strategy="hash")
```

URL strategy for Flet Server can be configured with `FLET_ROUTE_URL_STRATEGY` environment variable which could be set to either `path` (default) or `hash`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/navigation-and-routing.md)

[

Previous

Adaptive apps

](/docs/getting-started/adaptive-apps)[

Next

Testing on iOS

](/docs/getting-started/testing-on-ios)

-   [Page route](#page-route)
-   [Page views](#page-views)
-   [Building views on route change](#building-views-on-route-change)
-   [Route templates](#route-templates)
-   [URL strategy for web](#url-strategy-for-web)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Testing Flet app on iOS | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/testing-on-ios/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/testing-on-ios/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/testing-on-ios/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/testing-on-ios/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Testing on iOS

# Testing Flet app on iOS

Start building awesome mobile apps in Python using just your computer and mobile phone!

Install [Flet](https://apps.apple.com/app/flet/id1624979699) app to your iOS device. You will be using this app to see how your Flet project is working on iPhone or iPad.

[![](https://flet.dev/docs/getting-started/testing-on-ios/img/docs/getting-started/testing-on-ios/qr-code.jpg)](https://apps.apple.com/app/flet/id1624979699)

To get started on your computer you need Python 3.9 or greater installed.

Important

Your iOS device and computer must be connected to the same Wi-Fi or local network.

It's recommended to start with the creation of a new virtual environment:

-   macOS
-   Linux
-   Windows

```
python3 -m venv .venvsource .venv/bin/activate
```

```
python3 -m venv .venvsource .venv/bin/activate
```

```
python.exe -m venv .venv.venv\Scripts\activate.bat
```

Next, install the latest `flet` package:

```
pip install flet --upgrade
```

Ensure that Flet has successfully installed and Flet CLI is available in `PATH` by running:

```
flet --version
```

Create a new Flet project:

```
flet create my-appcd my-app
```

Run the following command to start Flet development server with your app:

```
flet run --ios
```

A QR code with encoded project URL will be displayed in the terminal:

![](https://flet.dev/docs/getting-started/testing-on-ios/img/docs/getting-started/testing-on-ios/app-qr-code.png)

Open **Camera** app on your iOS device, point to a QR code and click **Open in Flet** link.

A dialog asking for permissions to access your local network will popup:

![](https://flet.dev/docs/getting-started/testing-on-ios/img/docs/getting-started/testing-on-ios/flet-local-network.png)

Click **Allow** and you should see your Flet app running.

Try updating `main.py` (for example, replace a greeting of `Text` control) - the app will be instantly refreshed on your iOS device.

You can try more complex Flet example from [Introduction](/docs/#flet-app-example).

To return to "Home" tab either:

-   Long-press anywhere on the screen with 3 fingers or
-   Shake your iOS device.

You can also "manually" add a new project by clicking **"+"** button and typing its URL.

Quick test

There is "Counter" Flet project hosted on the internet that you can add to Flet app to make sure everything works:

```
https://flet-counter-test-ios.fly.dev
```

Check "Gallery" tab for some great examples of what kind of projects could be done with Flet.

Explore [Flet examples](https://github.com/flet-dev/examples/tree/main/python) for even more examples.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/testing-on-ios.md)

[

Previous

Navigation and routing

](/docs/getting-started/navigation-and-routing)[

Next

Testing on Android

](/docs/getting-started/testing-on-android)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ListTile | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/listtile/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/listtile/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/listtile/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/listtile/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   ListTile

On this page

# ListTile

A single fixed-height row that typically contains some text as well as a leading or trailing icon.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/listtile)

![](https://flet.dev/docs/controls/listtile/img/docs/controls/listtile/listtiles.png)

-   Python

```
import flet as ftdef main(page):    page.title = "ListTile Examples"    page.add(        ft.Card(            content=ft.Container(                width=500,                content=ft.Column(                    [                        ft.ListTile(                            title=ft.Text("One-line list tile"),                        ),                        ft.ListTile(title=ft.Text("One-line dense list tile"), dense=True),                        ft.ListTile(                            leading=ft.Icon(ft.Icons.SETTINGS),                            title=ft.Text("One-line selected list tile"),                            selected=True,                        ),                        ft.ListTile(                            leading=ft.Image(src="/icons/icon-192.png", fit="contain"),                            title=ft.Text("One-line with leading control"),                        ),                        ft.ListTile(                            title=ft.Text("One-line with trailing control"),                            trailing=ft.PopupMenuButton(                                icon=ft.Icons.MORE_VERT,                                items=[                                    ft.PopupMenuItem(text="Item 1"),                                    ft.PopupMenuItem(text="Item 2"),                                ],                            ),                        ),                        ft.ListTile(                            leading=ft.Icon(ft.Icons.ALBUM),                            title=ft.Text("One-line with leading and trailing controls"),                            trailing=ft.PopupMenuButton(                                icon=ft.Icons.MORE_VERT,                                items=[                                    ft.PopupMenuItem(text="Item 1"),                                    ft.PopupMenuItem(text="Item 2"),                                ],                            ),                        ),                        ft.ListTile(                            leading=ft.Icon(ft.Icons.SNOOZE),                            title=ft.Text("Two-line with leading and trailing controls"),                            subtitle=ft.Text("Here is a second title."),                            trailing=ft.PopupMenuButton(                                icon=ft.Icons.MORE_VERT,                                items=[                                    ft.PopupMenuItem(text="Item 1"),                                    ft.PopupMenuItem(text="Item 2"),                                ],                            ),                        ),                    ],                    spacing=0,                ),                padding=ft.padding.symmetric(vertical=10),            )        )    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive ListTile is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoListTile`](/docs/controls/cupertinolisttile) is created, which has matching functionality and presentation as `ListTile`, and the graphics as expected on iOS. On other platforms, a Material ListTile is created.

If a `CupertinoListTile` is created, the following parameters are ignored: `autofocus`, `dense`, `is_three_line`, `selected` and `on_long_press` event.

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

`True` if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The list tile's background [color](/docs/reference/colors).

### `bgcolor_activated`[​](#bgcolor_activated "Direct link to bgcolor_activated")

The list tile's splash [color](/docs/reference/colors) after the tile was tapped.

### `content_padding`[​](#content_padding "Direct link to content_padding")

The tile's internal padding. Insets a ListTile's contents: its `leading`, `title`, `subtitle`, and `trailing` controls.

Value is of type [`Padding`](/docs/reference/types/padding) and defaults to `padding.symmetric(horizontal=16)`.

### `dense`[​](#dense "Direct link to dense")

Whether this list tile is part of a vertically dense list. Dense list tiles default to a smaller height.

### `enable_feedback`[​](#enable_feedback "Direct link to enable_feedback")

Whether detected gestures should provide acoustic and/or haptic feedback. On Android, for example, setting this to `True` produce a click sound and a long-press will produce a short vibration.

Defaults to `True`.

### `horizontal_spacing`[​](#horizontal_spacing "Direct link to horizontal_spacing")

The horizontal gap between the `title` and the `leading`/`trailing` controls.

Defaults to `16`.

### `hover_color`[​](#hover_color "Direct link to hover_color")

The tile's [color](/docs/reference/colors) when hovered.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Defines the default [color](/docs/reference/colors) for the `Icon`s present in `leading` and `trailing`.

### `is_three_line`[​](#is_three_line "Direct link to is_three_line")

Whether this list tile is intended to display three lines of text.

If `True`, then subtitle must be non-null (since it is expected to give the second and third lines of text).

If `False`, the list tile is treated as having one line if the subtitle is null and treated as having two lines if the subtitle is non-null.

When using a Text control for title and subtitle, you can enforce line limits using [`Text.max_lines`](/docs/controls/text#max_lines).

### `leading`[​](#leading "Direct link to leading")

A `Control` to display before the title.

### `leading_and_trailing_text_style`[​](#leading_and_trailing_text_style "Direct link to leading_and_trailing_text_style")

The [`TextStyle`](/docs/reference/types/textstyle) for the `leading` and `trailing` controls.

### `min_height`[​](#min_height "Direct link to min_height")

The minimum height allocated for this control.

If `None` or not set, default tile heights are `56.0`, `72.0`, and `88.0` for one, two, and three lines of text respectively. If [`dense`](#dense) is `True`, these defaults are changed to `48.0`, `64.0`, and `76.0`.

Note that, a visual density value or a large title will also adjust the default tile heights.

### `min_leading_width`[​](#min_leading_width "Direct link to min_leading_width")

The minimum width allocated for the `leading` control.

Defaults to `40`.

### `min_vertical_padding`[​](#min_vertical_padding "Direct link to min_vertical_padding")

The minimum padding on the top and bottom of the `title` and `subtitle` controls.

Defaults to `4`.

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor to be displayed when a mouse pointer enters or is hovering over this control. The value is [`MouseCursor`](/docs/reference/types/mousecursor) enum.

### `selected`[​](#selected "Direct link to selected")

If this tile is also enabled then icons and text are rendered with the same color. By default the selected color is the theme's primary color.

### `selected_color`[​](#selected_color "Direct link to selected_color")

Defines the [color](/docs/reference/colors) used for icons and text when `selected=True`.

### `selected_tile_color`[​](#selected_tile_color "Direct link to selected_tile_color")

Defines the background [color](/docs/reference/colors) of ListTile when `selected=True`.

### `shape`[​](#shape "Direct link to shape")

The tile's shape. The value is an instance of [`OutlinedBorder`](/docs/reference/types/outlinedborder) class.

### `subtitle`[​](#subtitle "Direct link to subtitle")

Additional content displayed below the title. Typically a [`Text`](/docs/controls/text) widget.

If `is_three_line` is `False`, this should not wrap. If `is_three_line` is `True`, this should be configured to take a maximum of two lines. For example, you can use [`Text.max_lines`](/docs/controls/text#max_lines) to enforce the number of lines.

### `subtitle_text_style`[​](#subtitle_text_style "Direct link to subtitle_text_style")

The [`TextStyle`](/docs/reference/types/textstyle) for the `subtitle` control.

### `style`[​](#style "Direct link to style")

Defines the font used for the title.

Value is of type [`ListTileStyle`](/docs/reference/types/listtilestyle) and defaults to `ListTileStyle.LIST`.

### `text_color`[​](#text_color "Direct link to text_color")

The [color](/docs/reference/colors) used for text. Defines the color of `Text` controls found in `title`, `subtitle`, `leading`, and `trailing`.

### `title`[​](#title "Direct link to title")

A `Control` to display as primary content of the list tile.

Typically a [`Text`](/docs/controls/text) control. This should not wrap. To enforce the single line limit, use [`Text.max_lines`](/docs/controls/text#max_lines).

### `title_alignment`[​](#title_alignment "Direct link to title_alignment")

Defines how `leading` and `trailing` are vertically aligned relative to the titles (`title` and `subtitle`).

Value is of type [`ListTileAlignment`](/docs/reference/types/listtilealignment) and defaults to `ListTileAlignment.THREE_LINE` in Material 3 or `ListTileAlignment.TITLE_HEIGHT` in Material 2.

### `title_text_style`[​](#title_text_style "Direct link to title_text_style")

The [`TextStyle`](/docs/reference/types/textstyle) for the `title` control.

### `toggle_inputs`[​](#toggle_inputs "Direct link to toggle_inputs")

Whether clicking on a list tile should toggle the state of `Radio`, `Checkbox` or `Switch` inside the tile.

Defaults to `False`.

### `trailing`[​](#trailing "Direct link to trailing")

A `Control` to display after the title. Typically an [`Icon`](/docs/controls/icon) control.

### `url`[​](#url "Direct link to url")

The URL to open when the list tile is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

### `visual_density`[​](#visual_density "Direct link to visual_density")

Defines how compact the control's layout will be.

Value is of type [`VisualDensity`](/docs/reference/types/visualdensity).

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks or taps the list tile.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the user long-presses on this list tile.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/listtile.md)

[

Previous

GridView

](/docs/controls/gridview)[

Next

ListView

](/docs/controls/listview)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`bgcolor`](#bgcolor)
    -   [`bgcolor_activated`](#bgcolor_activated)
    -   [`content_padding`](#content_padding)
    -   [`dense`](#dense)
    -   [`enable_feedback`](#enable_feedback)
    -   [`horizontal_spacing`](#horizontal_spacing)
    -   [`hover_color`](#hover_color)
    -   [`icon_color`](#icon_color)
    -   [`is_three_line`](#is_three_line)
    -   [`leading`](#leading)
    -   [`leading_and_trailing_text_style`](#leading_and_trailing_text_style)
    -   [`min_height`](#min_height)
    -   [`min_leading_width`](#min_leading_width)
    -   [`min_vertical_padding`](#min_vertical_padding)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`selected`](#selected)
    -   [`selected_color`](#selected_color)
    -   [`selected_tile_color`](#selected_tile_color)
    -   [`shape`](#shape)
    -   [`subtitle`](#subtitle)
    -   [`subtitle_text_style`](#subtitle_text_style)
    -   [`style`](#style)
    -   [`text_color`](#text_color)
    -   [`title`](#title)
    -   [`title_alignment`](#title_alignment)
    -   [`title_text_style`](#title_text_style)
    -   [`toggle_inputs`](#toggle_inputs)
    -   [`trailing`](#trailing)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
    -   [`visual_density`](#visual_density)
-   [Events](#events)
    -   [`on_click`](#on_click)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ListView | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/listview/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/listview/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/listview/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/listview/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   ListView

On this page

# ListView

A scrollable list of controls arranged linearly.

ListView is the most commonly used scrolling control. It displays its children one after another in the scroll direction. In the cross axis, the children are required to fill the ListView.

info

ListView is very effective for large lists (thousands of items). Prefer it over [`Column`](/docs/controls/column) or [`Row`](/docs/controls/row) for smooth scrolling.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/listview)

### Auto-scrolling ListView[​](#auto-scrolling-listview "Direct link to Auto-scrolling ListView")

-   Python

```
from time import sleepimport flet as ftdef main(page: ft.Page):    page.title = "Auto-scrolling ListView"    lv = ft.ListView(expand=1, spacing=10, padding=20, auto_scroll=True)    count = 1    for i in range(0, 60):        lv.controls.append(ft.Text(f"Line {count}"))        count += 1    page.add(lv)    for i in range(0, 60):        sleep(1)        lv.controls.append(ft.Text(f"Line {count}"))        count += 1        page.update()ft.app(main)
```

![](https://flet.dev/docs/controls/listview/img/docs/controls/listview/custom-listview.gif)

## Properties[​](#properties "Direct link to Properties")

### `auto_scroll`[​](#auto_scroll "Direct link to auto_scroll")

`True` if scrollbar should automatically move its position to the end when children updated. Must be `False` for `scroll_to()` method to work.

Defaults to `False`.

### `build_controls_on_demand`[​](#build_controls_on_demand "Direct link to build_controls_on_demand")

Whether the `controls` should be built lazily/on-demand, i.e. only when they are about to become visible. This is particularly useful when dealing with a large number of controls.

Defaults to `True`.

### `cache_extent`[​](#cache_extent "Direct link to cache_extent")

Items that fall in the cache area (area before or after the visible area that are about to become visible when the user scrolls) are laid out even though they are not (yet) visible on screen. The cacheExtent describes how many pixels the cache area extends before the leading edge and after the trailing edge of the viewport.

The total extent, which the viewport will try to cover with `controls`, is `cache_extent` before the leading edge + extent of the main axis + `cache_extent` after the trailing edge.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.HARD_EDGE`.

### `controls`[​](#controls "Direct link to controls")

A list of `Control`s to display inside ListView.

### `divider_thickness`[​](#divider_thickness "Direct link to divider_thickness")

If greater than `0` then Divider is used as a spacing between list view items.

### `first_item_prototype`[​](#first_item_prototype "Direct link to first_item_prototype")

`True` if the dimensions of the first item should be used as a "prototype" for all other items, i.e. their height or width will be the same as the first item.

Defaults to `False`.

### `horizontal`[​](#horizontal "Direct link to horizontal")

`True` to layout ListView items horizontally.

### `item_extent`[​](#item_extent "Direct link to item_extent")

A fixed height or width (for `horizontal` ListView) of an item to optimize rendering.

### `on_scroll_interval`[​](#on_scroll_interval "Direct link to on_scroll_interval")

Throttling in milliseconds for `on_scroll` event.

Defaults to `10`.

### `padding`[​](#padding "Direct link to padding")

The amount of space by which to inset the children.

Value is of type[`Padding`](/docs/reference/types/padding).

### `reverse`[​](#reverse "Direct link to reverse")

Defines whether the scroll view scrolls in the reading direction.

Defaults to `False`.

### `semantic_child_count`[​](#semantic_child_count "Direct link to semantic_child_count")

The number of children that will contribute semantic information.

### `spacing`[​](#spacing "Direct link to spacing")

The height of Divider between ListView items. No spacing between items if not specified.

## Methods[​](#methods "Direct link to Methods")

### `scroll_to(offset, delta, key, duration, curve)`[​](#scroll_tooffset-delta-key-duration-curve "Direct link to scroll_tooffset-delta-key-duration-curve")

Moves scroll position to either absolute `offset`, relative `delta` or jump to the control with specified `key`.

See [`Column.scroll_to()`](/docs/controls/column#scroll_tooffset-delta-key-duration-curve) for method details and examples.

## Events[​](#events "Direct link to Events")

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when scroll position is changed by a user.

Event handler argument is an instance of [`OnScrollEvent`](/docs/reference/types/onscrollevent) class.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/listview.md)

[

Previous

ListTile

](/docs/controls/listtile)[

Next

Page

](/docs/controls/page)

-   [Examples](#examples)
    -   [Auto-scrolling ListView](#auto-scrolling-listview)
-   [Properties](#properties)
    -   [`auto_scroll`](#auto_scroll)
    -   [`build_controls_on_demand`](#build_controls_on_demand)
    -   [`cache_extent`](#cache_extent)
    -   [`clip_behavior`](#clip_behavior)
    -   [`controls`](#controls)
    -   [`divider_thickness`](#divider_thickness)
    -   [`first_item_prototype`](#first_item_prototype)
    -   [`horizontal`](#horizontal)
    -   [`item_extent`](#item_extent)
    -   [`on_scroll_interval`](#on_scroll_interval)
    -   [`padding`](#padding)
    -   [`reverse`](#reverse)
    -   [`semantic_child_count`](#semantic_child_count)
    -   [`spacing`](#spacing)
-   [Methods](#methods)
    -   [`scroll_to(offset, delta, key, duration, curve)`](#scroll_tooffset-delta-key-duration-curve)
-   [Events](#events)
    -   [`on_scroll`](#on_scroll)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ResponsiveRow | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/responsiverow/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/responsiverow/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/responsiverow/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/responsiverow/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   ResponsiveRow

On this page

# ResponsiveRow

`ResponsiveRow` borrows the idea of grid layout from [Bootstrap](https://getbootstrap.com/docs/5.2/layout/grid/) web framework.

`ResponsiveRow` allows aligning child controls to virtual columns. By default, a virtual grid has 12 columns, but that can be customized with `ResponsiveRow.columns` property.

Similar to `expand` property, every control now has `col` property which allows specifying how many columns a control should span. For example, to make a layout consisting of two columns spanning 6 virtual columns each:

```
import flet as ftft.ResponsiveRow([    ft.Column(col=6, controls=[ft.Text("Column 1")]),    ft.Column(col=6, controls=[ft.Text("Column 2")])])
```

`ResponsiveRow` is "responsive" because it can adapt the size of its children to a changing screen (page, window) size. `col` property in the example above is a constant number which means the child will span 6 columns for any screen size.

If `ResponsiveRow`'s child doesn't have `col` property specified it spans the maximum number of columns.

`col` can be configured to have a different value for specific "breakpoints". Breakpoints are named dimension ranges:

Breakpoint

Dimension

xs

<576px

sm

≥576px

md

≥768px

lg

≥992px

xl

≥1200px

xxl

≥1400px

For example, the following example collapses content into a single column on a mobile device and takes two columns on larger screens:

```
import flet as ftft.ResponsiveRow([    ft.Column(col={"sm": 6}, controls=[ft.Text("Column 1")]),    ft.Column(col={"sm": 6}, controls=[ft.Text("Column 2")])])
```

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/responsiverow)

### ResponsiveRow[​](#responsiverow "Direct link to ResponsiveRow")

![](https://flet.dev/docs/controls/responsiverow/img/docs/controls/responsive-row/responsive-layout.gif)

-   Python

```
import flet as ftdef main(page: ft.Page):    def page_resize(e):        pw.value = f"{page.width} px"        pw.update()    page.on_resize = page_resize    pw = ft.Text(bottom=50, right=50, style="displaySmall")    page.overlay.append(pw)    page.add(        ft.ResponsiveRow(            [                ft.Container(                    ft.Text("Column 1"),                    padding=5,                    bgcolor=ft.Colors.YELLOW,                    col={"sm": 6, "md": 4, "xl": 2},                ),                ft.Container(                    ft.Text("Column 2"),                    padding=5,                    bgcolor=ft.Colors.GREEN,                    col={"sm": 6, "md": 4, "xl": 2},                ),                ft.Container(                    ft.Text("Column 3"),                    padding=5,                    bgcolor=ft.Colors.BLUE,                    col={"sm": 6, "md": 4, "xl": 2},                ),                ft.Container(                    ft.Text("Column 4"),                    padding=5,                    bgcolor=ft.Colors.PINK_300,                    col={"sm": 6, "md": 4, "xl": 2},                ),            ],        ),        ft.ResponsiveRow(            [                ft.TextField(label="TextField 1", col={"md": 4}),                ft.TextField(label="TextField 2", col={"md": 4}),                ft.TextField(label="TextField 3", col={"md": 4}),            ],            run_spacing={"xs": 10},        ),    )    page_resize(None)ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `alignment`[​](#alignment "Direct link to alignment")

How the child Controls should be placed horizontally.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment) and defaults to `MainAxisAlignment.START`.

### `columns`[​](#columns "Direct link to columns")

The number of virtual columns to layout children.

Defaults to `12`.

### `controls`[​](#controls "Direct link to controls")

A list of Controls to display inside the ResponsiveRow.

### `rtl`[​](#rtl "Direct link to rtl")

`True` to set text direction to right-to-left.

Defaults to `False`.

### `run_spacing`[​](#run_spacing "Direct link to run_spacing")

Spacing between runs when row content is wrapped on multiple lines.

Defaults to `10`.

### `spacing`[​](#spacing "Direct link to spacing")

Spacing between controls in a row in virtual pixels. It is applied only when `alignment` is set to `MainAxisAlignment.START`, `MainAxisAlignment.END` or `MainAxisAlignment.CENTER`.

Defaults to `10`.

### `vertical_alignment`[​](#vertical_alignment "Direct link to vertical_alignment")

How the child Controls should be placed vertically.

Value is of type [`CrossAxisAlignment`](/docs/reference/types/crossaxisalignment) and defaults to `CrossAxisAlignment.START`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/responsiverow.md)

[

Previous

ReorderableListView

](/docs/controls/reorderablelistview)[

Next

Row

](/docs/controls/row)

-   [Examples](#examples)
    -   [ResponsiveRow](#responsiverow)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`columns`](#columns)
    -   [`controls`](#controls)
    -   [`rtl`](#rtl)
    -   [`run_spacing`](#run_spacing)
    -   [`spacing`](#spacing)
    -   [`vertical_alignment`](#vertical_alignment)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Row | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/row/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/row/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/row/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/row/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Row

On this page

# Row

A control that displays its children in a horizontal array.

To cause a child control to expand and fill the available horizontal space set its `expand` property.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/row)

### Row spacing[​](#row-spacing "Direct link to Row spacing")

![](https://flet.dev/docs/controls/row/img/docs/controls/row/row-spacing.gif)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER,                    border_radius=ft.border_radius.all(5),                )            )        return items    def gap_slider_change(e):        row.spacing = int(e.control.value)        row.update()    gap_slider = ft.Slider(        min=0,        max=50,        divisions=50,        value=0,        label="{value}",        on_change=gap_slider_change,    )    row = ft.Row(spacing=0, controls=items(10))    page.add(ft.Column([ ft.Text("Spacing between items"), gap_slider]), row)ft.app(main)
```

### Row wrapping[​](#row-wrapping "Direct link to Row wrapping")

![](https://flet.dev/docs/controls/row/img/docs/controls/row/row-wrap.gif)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER,                    border_radius=ft.border_radius.all(5),                )            )        return items    def slider_change(e):        row.width = float(e.control.value)        row.update()    width_slider = ft.Slider(        min=0,        max=page.window.width,        divisions=20,        value=page.window.width,        label="{value}",        on_change=slider_change,    )    row = ft.Row(        wrap=True,        spacing=10,        run_spacing=10,        controls=items(30),        width=page.window.width,    )    page.add(        ft.Column(            [                ft.Text(                    "Change the row width to see how child items wrap onto multiple rows:"                ),                width_slider,            ]        ),        row,    )ft.app(main)
```

### Row horizontal alignments[​](#row-horizontal-alignments "Direct link to Row horizontal alignments")

![](https://flet.dev/docs/controls/row/img/docs/controls/row/row-alignment.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER_500,                )            )        return items    def row_with_alignment(align: ft.MainAxisAlignment):        return ft.Column(            [                ft.Text(str(align), size=16),                ft.Container(                    content=ft.Row(items(3), alignment=align),                    bgcolor=ft.Colors.AMBER_100,                ),            ]        )    page.add(        row_with_alignment(ft.MainAxisAlignment.START),        row_with_alignment(ft.MainAxisAlignment.CENTER),        row_with_alignment(ft.MainAxisAlignment.END),        row_with_alignment(ft.MainAxisAlignment.SPACE_BETWEEN),        row_with_alignment(ft.MainAxisAlignment.SPACE_AROUND),        row_with_alignment(ft.MainAxisAlignment.SPACE_EVENLY),    )ft.app(main)
```

### Row vertical[​](#row-vertical "Direct link to Row vertical")

![](https://flet.dev/docs/controls/row/img/docs/controls/row/row-vertical-alignment.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER_500,                )            )        return items    def row_with_vertical_alignment(align: ft.CrossAxisAlignment):        return ft.Column(            [                ft.Text(str(align), size=16),                ft.Container(                    content=ft.Row(items(3), vertical_alignment=align),                    bgcolor=ft.Colors.AMBER_100,                    height=150,                ),            ]        )    page.add(        row_with_vertical_alignment(ft.CrossAxisAlignment.START),        row_with_vertical_alignment(ft.CrossAxisAlignment.CENTER),        row_with_vertical_alignment(ft.CrossAxisAlignment.END),    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `alignment`[​](#alignment "Direct link to alignment")

How the child Controls should be placed horizontally.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment) and defaults to `MainAxisAlignment.START`.

### `auto_scroll`[​](#auto_scroll "Direct link to auto_scroll")

`True` if scrollbar should automatically move its position to the end when children updated. Must be `False` for `scroll_to()` method to work.

### `controls`[​](#controls "Direct link to controls")

A list of Controls to display inside the Row.

### `rtl`[​](#rtl "Direct link to rtl")

`True` to set text direction to right-to-left.

Defaults to `False`.

### `run_alignment`[​](#run_alignment "Direct link to run_alignment")

How the runs should be placed in the cross-axis when `wrap=True`.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment) and defaults to `MainAxisAlignment.START`.

### `run_spacing`[​](#run_spacing "Direct link to run_spacing")

Spacing between runs when `wrap=True`.

Defaults to `10`.

### `scroll`[​](#scroll "Direct link to scroll")

Enables horizontal scrolling for the Row to prevent its content overflow.

Value is of type [`ScrollMode`](/docs/reference/types/scrollmode).

### `spacing`[​](#spacing "Direct link to spacing")

Spacing between controls in a row. Default value is 10 virtual pixels. Spacing is applied only when `alignment` is set to `MainAxisAlignment.START`, `MainAxisAlignment.END` or `MainAxisAlignment.CENTER`.

### `on_scroll_interval`[​](#on_scroll_interval "Direct link to on_scroll_interval")

Throttling in milliseconds for `on_scroll` event.

Defaults to `10`.

### `tight`[​](#tight "Direct link to tight")

Specifies how much space should be occupied horizontally.

Defaults to `False`, meaning all space is allocated to children.

### `vertical_alignment`[​](#vertical_alignment "Direct link to vertical_alignment")

How the child Controls should be placed vertically.

Value is of type [`CrossAxisAlignment`](/docs/reference/types/crossaxisalignment) and defaults to `CrossAxisAlignment.START`.

### `wrap`[​](#wrap "Direct link to wrap")

When set to `True` the Row will put child controls into additional rows (runs) if they don't fit a single row.

## Methods[​](#methods "Direct link to Methods")

### `scroll_to(offset, delta, key, duration, curve)`[​](#scroll_tooffset-delta-key-duration-curve "Direct link to scroll_tooffset-delta-key-duration-curve")

Moves scroll position to either absolute `offset`, relative `delta` or jump to the control with specified `key`.

See [`Column.scroll_to()`](/docs/controls/column#scroll_tooffset-delta-key-duration-curve) for method details and examples.

## Events[​](#events "Direct link to Events")

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when scroll position is changed by a user.

Event handler argument is an instance of [`OnScrollEvent`](/docs/reference/types/onscrollevent) class.

## Expanding children[​](#expanding-children "Direct link to Expanding children")

When a child Control is placed into a Row you can "expand" it to fill the available space. Every Control has `expand` property that can have either a boolean value (`True` - expand control to fill all available space) or an integer - an "expand factor" specifying how to divide a free space with other expanded child controls. For example, this code creates a row with a TextField taking all available space and an ElevatedButton next to it:

```
r = ft.Row([  ft.TextField(hint_text="Enter your name", expand=True),  ft.ElevatedButton(text="Join chat")])
```

The following example with numeric expand factors creates a Row with 3 containers in it and having widths of `20% (1/5)`, `60% (3/5)` and `20% (1/5)` respectively:

```
r = ft.Row([  ft.Container(expand=1, content=ft.Text("A")),  ft.Container(expand=3, content=ft.Text("B")),  ft.Container(expand=1, content=ft.Text("C"))])
```

In general, the resulting width of a child in percents is calculated as `expand / sum(all expands) * 100%`.

If you need to give the child Control of the Row the flexibility to expand to fill the available space horizontally but not require it to fill the available space, set its `expand_loose` property to `True`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/row.md)

[

Previous

ResponsiveRow

](/docs/controls/responsiverow)[

Next

SafeArea

](/docs/controls/safearea)

-   [Examples](#examples)
    -   [Row spacing](#row-spacing)
    -   [Row wrapping](#row-wrapping)
    -   [Row horizontal alignments](#row-horizontal-alignments)
    -   [Row vertical](#row-vertical)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`auto_scroll`](#auto_scroll)
    -   [`controls`](#controls)
    -   [`rtl`](#rtl)
    -   [`run_alignment`](#run_alignment)
    -   [`run_spacing`](#run_spacing)
    -   [`scroll`](#scroll)
    -   [`spacing`](#spacing)
    -   [`on_scroll_interval`](#on_scroll_interval)
    -   [`tight`](#tight)
    -   [`vertical_alignment`](#vertical_alignment)
    -   [`wrap`](#wrap)
-   [Methods](#methods)
    -   [`scroll_to(offset, delta, key, duration, curve)`](#scroll_tooffset-delta-key-duration-curve)
-   [Events](#events)
    -   [`on_scroll`](#on_scroll)
-   [Expanding children](#expanding-children)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  SafeArea | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/safearea/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/safearea/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/safearea/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/safearea/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   SafeArea

On this page

# SafeArea

A control that insets its `content` by sufficient padding to avoid intrusions by the operating system.

For example, this will indent the `content` by enough to avoid the status bar at the top of the screen.

It will also indent the `content` by the amount necessary to avoid The Notch on the iPhone X, or other similar creative physical features of the display.

When a `minimum_padding` is specified, the greater of the minimum padding or the safe area padding will be applied.

## Example[​](#example "Direct link to Example")

[Live example](https://flet-controls-gallery.fly.dev/layout/safearea)

```
import flet as ftclass State:    counter = 0def main(page: ft.Page):    state = State()    def add_click(e):        state.counter += 1        counter.value = str(state.counter)        counter.update()    page.floating_action_button = ft.FloatingActionButton(        icon=ft.Icons.ADD, on_click=add_click    )    page.add(        ft.SafeArea(            ft.Container(                counter := ft.Text("0", size=50),                alignment=ft.alignment.center,            ),            expand=True,        )    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `bottom`[​](#bottom "Direct link to bottom")

Whether to avoid system intrusions on the bottom side of the screen.

Defaults to `True`.

### `content`[​](#content "Direct link to content")

A `Control` to display inside safe area.

### `left`[​](#left "Direct link to left")

Whether to avoid system intrusions on the left.

Defaults to `True`.

### `maintain_bottom_view_padding`[​](#maintain_bottom_view_padding "Direct link to maintain_bottom_view_padding")

Specifies whether the `SafeArea` should maintain the bottom `MediaQueryData.viewPadding` instead of the bottom `MediaQueryData.padding`, defaults to `False`.

For example, if there is an onscreen keyboard displayed above the SafeArea, the padding can be maintained below the obstruction rather than being consumed. This can be helpful in cases where your layout contains flexible controls, which could visibly move when opening a software keyboard due to the change in the padding value. Setting this to true will avoid the UI shift.

### `minimum_padding`[​](#minimum_padding "Direct link to minimum_padding")

This minimum padding to apply.

The greater of the minimum insets and the media padding will be applied.

### `right`[​](#right "Direct link to right")

Whether to avoid system intrusions on the right.

Defaults to `True`.

### `top`[​](#top "Direct link to top")

Whether to avoid system intrusions at the top of the screen, typically the system status bar.

Defaults to `True`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/safearea.md)

[

Previous

Row

](/docs/controls/row)[

Next

Stack

](/docs/controls/stack)

-   [Example](#example)
-   [Properties](#properties)
    -   [`bottom`](#bottom)
    -   [`content`](#content)
    -   [`left`](#left)
    -   [`maintain_bottom_view_padding`](#maintain_bottom_view_padding)
    -   [`minimum_padding`](#minimum_padding)
    -   [`right`](#right)
    -   [`top`](#top)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Stack | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/stack/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/stack/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/stack/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/stack/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Stack

On this page

# Stack

A control that positions its children on top of each other.

This control is useful if you want to overlap several children in a simple way, for example having some text and an image, overlaid with a gradient and a button attached to the bottom.

Stack is also useful if you want to implement [implicit animations](/docs/cookbook/animations) that require knowing absolute position of a target value.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/stack)

### Transparent title over an image[​](#transparent-title-over-an-image "Direct link to Transparent title over an image")

![](https://flet.dev/docs/controls/stack/img/docs/controls/stack/image-title.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    st = ft.Stack(        [            ft.Image(                src=f"https://picsum.photos/300/300",                width=300,                height=300,                fit=ft.ImageFit.CONTAIN,            ),            ft.Row(                [                    ft.Text(                        "Image title",                        color="white",                        size=40,                        weight="bold",                        opacity=0.5,                    )                ],                alignment=ft.MainAxisAlignment.CENTER,            ),        ],        width=300,        height=300,    )    page.add(st)ft.app(main)
```

### Avatar with online status[​](#avatar-with-online-status "Direct link to Avatar with online status")

![](https://flet.dev/docs/controls/stack/img/docs/controls/stack/avatar-with-status.png)

-   Python

```
import flet as ftdef main(page):    page.add(        ft.Stack(            [                ft.CircleAvatar(                    foreground_image_url="https://avatars.githubusercontent.com/u/5041459?s=88&v=4"                ),                ft.Container(                    content=ft.CircleAvatar(bgcolor=ft.Colors.GREEN, radius=5),                    alignment=ft.alignment.bottom_left,                ),            ],            width=40,            height=40,        )    )ft.app(main, view=ft.AppView.WEB_BROWSER)
```

### Absolute positioning inside Stack[​](#absolute-positioning-inside-stack "Direct link to Absolute positioning inside Stack")

![](https://flet.dev/docs/controls/stack/img/docs/controls/stack/absolute-positioned.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.add(        ft.Container(            ft.Stack(                [                    ft.Container(width=20, height=20, bgcolor=ft.Colors.RED, border_radius=5),                    ft.Container(                        width=20,                        height=20,                        bgcolor=ft.Colors.YELLOW,                        border_radius=5,                        right=0,                    ),                    ft.Container(                        width=20,                        height=20,                        bgcolor=ft.Colors.BLUE,                        border_radius=5,                        right=0,                        bottom=0,                    ),                    ft.Container(                        width=20,                        height=20,                        bgcolor=ft.Colors.GREEN,                        border_radius=5,                        left=0,                        bottom=0,                    ),                    ft.Column(                        [                            ft.Container(                                width=20,                                height=20,                                bgcolor=ft.Colors.PURPLE,                                border_radius=5,                            )                        ],                        left=35,                        top=35,                    ),                ]            ),            border_radius=8,            padding=5,            width=100,            height=100,            bgcolor=ft.Colors.BLACK,        )    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `alignment`[​](#alignment "Direct link to alignment")

The alignment of the non-positioned (those that do not specify an alignment - ex neither top nor bottom - in a particular axis and partially-positioned `controls`.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.HARD_EDGE`.

### `controls`[​](#controls "Direct link to controls")

A list of Controls to display inside the Stack. The last control in the list is displayed on top.

### `fit`[​](#fit "Direct link to fit")

How to size the non-positioned `controls`.

Value is of type [`StackFit`](/docs/reference/types/stackfit) and defaults to `StackFit.LOOSE`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/stack.md)

[

Previous

SafeArea

](/docs/controls/safearea)[

Next

Tabs

](/docs/controls/tabs)

-   [Examples](#examples)
    -   [Transparent title over an image](#transparent-title-over-an-image)
    -   [Avatar with online status](#avatar-with-online-status)
    -   [Absolute positioning inside Stack](#absolute-positioning-inside-stack)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`clip_behavior`](#clip_behavior)
    -   [`controls`](#controls)
    -   [`fit`](#fit)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoAppBar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinoappbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoappbar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinoappbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoappbar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   CupertinoAppBar

On this page

# CupertinoAppBar

An iOS-styled application bar.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/cupertinoappbar)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.theme_mode = ft.ThemeMode.LIGHT    page.appbar = ft.CupertinoAppBar(        leading=ft.Icon(ft.Icons.PALETTE),        bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST,        trailing=ft.Icon(ft.Icons.WB_SUNNY_OUTLINED),      middle=ft.Text("CupertinoAppBar Example"),    )    page.add(ft.Text("Body!"))ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinoappbar/img/docs/controls/cupertino-appbar/cupertino-appbar.png)

## Properties[​](#properties "Direct link to Properties")

### `automatic_background_visibility`[​](#automatic_background_visibility "Direct link to automatic_background_visibility")

Whether the navigation bar should appear transparent when content is scrolled under it.

If `False`, the navigation bar will display its `bgcolor`.

Defaults to `True`.

### `automatically_imply_leading`[​](#automatically_imply_leading "Direct link to automatically_imply_leading")

Controls whether we should try to imply the leading control if None.

If `True` and `leading` is null, automatically try to deduce what the leading widget should be. If `False` and `leading` is None, leading space is given to title. If leading widget is not None, this parameter has no effect.

### `automatically_imply_middle`[​](#automatically_imply_middle "Direct link to automatically_imply_middle")

Controls whether we should try to imply the middle control if None.

If `True` and `middle` is null, automatically fill in a Text control with the current route's title. If middle control is not None, this parameter has no effect.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The fill [color](/docs/reference/colors) to use for an AppBar. Default color is defined by current theme.

### `border`[​](#border "Direct link to border")

The border of the app bar. By default, a single pixel bottom border side is rendered.

Value is of type [`Border`](/docs/reference/types/border).

### `brightness`[​](#brightness "Direct link to brightness")

The brightness of the specified `bgcolor`.

Setting this value changes the style of the system status bar. It is typically used to increase the contrast ratio of the system status bar over `bgcolor`.

If `None` (the default), it's value will be inferred from the relative luminance of the `bgcolor`.

Value is of type [`Brightness`](/docs/reference/types/brightness).

### `elevation`[​](#elevation "Direct link to elevation")

This property controls the size of the shadow below the app bar.

Defaults to `4`.

### `enable_background_filter_blur`[​](#enable_background_filter_blur "Direct link to enable_background_filter_blur")

Whether to have a blur effect when a non-opaque `bgcolor` is used.

This will only be respected when `automatic_background_visibility` is `False` or until content scrolls under the navbar.

Defaults to `True`.

### `leading`[​](#leading "Direct link to leading")

A `Control` to display at the start of this app bar. Typically the leading control is an [`Icon`](/docs/controls/icon) or an [`IconButton`](/docs/controls/iconbutton).

If `None` and `automatically_imply_leading = True`, an appropriate button will be automatically created.

### `middle`[​](#middle "Direct link to middle")

A `Control` to display in the middle of this app bar. Typically a [`Text`](/docs/controls/text) or a segmented control.

### `padding`[​](#padding "Direct link to padding")

Defines the padding for the contents of the app bar.

Padding is an instance of [`Padding`](/docs/reference/types/padding) class.

If `None`, the app bar will adopt the following defaults:

-   vertically, contents will be sized to the same height as the app bar itself minus the status bar.
-   horizontally, padding will be `16` pixels according to iOS specifications unless the leading widget is an automatically inserted back button, in which case the padding will be `0`.

Vertical padding won't change the height of the app bar.

### `trailing`[​](#trailing "Direct link to trailing")

A Control to place at the end of the app bar. Normally additional actions taken on the page such as a search or edit function.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinoappbar.md)

[

Previous

BottomAppBar

](/docs/controls/bottomappbar)[

Next

CupertinoNavigationBar

](/docs/controls/cupertinonavigationbar)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`automatic_background_visibility`](#automatic_background_visibility)
    -   [`automatically_imply_leading`](#automatically_imply_leading)
    -   [`automatically_imply_middle`](#automatically_imply_middle)
    -   [`bgcolor`](#bgcolor)
    -   [`border`](#border)
    -   [`brightness`](#brightness)
    -   [`elevation`](#elevation)
    -   [`enable_background_filter_blur`](#enable_background_filter_blur)
    -   [`leading`](#leading)
    -   [`middle`](#middle)
    -   [`padding`](#padding)
    -   [`trailing`](#trailing)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoNavigationBar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinonavigationbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinonavigationbar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinonavigationbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinonavigationbar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   CupertinoNavigationBar

On this page

# CupertinoNavigationBar

An iOS-styled bottom navigation tab bar.

Navigation bars offer a persistent and convenient way to switch between primary destinations in an app.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/cupertinonavigationbar)

### A simple CupertinoNavigationBar[​](#a-simple-cupertinonavigationbar "Direct link to A simple CupertinoNavigationBar")

![](https://flet.dev/docs/controls/cupertinonavigationbar/img/docs/controls/cupertino-navigation-bar/cupertino-navigation-bar-sample.png)

```
import flet as ftdef main(page: ft.Page):    page.title = "CupertinoNavigationBar Example"    page.navigation_bar = ft.CupertinoNavigationBar(        bgcolor=ft.Colors.AMBER_100,        inactive_color=ft.Colors.GREY,        active_color=ft.Colors.BLACK,        on_change=lambda e: print("Selected tab:", e.control.selected_index),        destinations=[            ft.NavigationBarDestination(icon=ft.Icons.EXPLORE, label="Explore"),            ft.NavigationBarDestination(icon=ft.Icons.COMMUTE, label="Commute"),            ft.NavigationBarDestination(                icon=ft.Icons.BOOKMARK_BORDER,                selected_icon=ft.Icons.BOOKMARK,                label="Explore",            ),        ]    )    page.add(ft.SafeArea(ft.Text("Body!")))ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `active_color`[​](#active_color "Direct link to active_color")

The foreground [color](/docs/reference/colors) of the icon and title of the selected destination.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The [color](/docs/reference/colors) of the navigation bar itself.

### `border`[​](#border "Direct link to border")

Defines the border of this navigation bar. The value is an instance of [`Border`](/docs/reference/types/border) class.

### `destinations`[​](#destinations "Direct link to destinations")

Defines the appearance of the button items that are arrayed within the navigation bar.

The value must be a list of two or more [`NavigationBarDestination`](/docs/controls/navigationbar#navigationbardestination-properties) instances.

### `icon_size`[​](#icon_size "Direct link to icon_size")

The size of all destination icons.

Defaults to `30`.

### `inactive_color`[​](#inactive_color "Direct link to inactive_color")

The foreground [color](/docs/reference/colors) of the icon and title of the unselected destinations.

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index into `destinations` for the current selected `NavigationBarDestination` or `None` if no destination is selected.

## Events[​](#events "Direct link to Events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when selected destination changed.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinonavigationbar.md)

[

Previous

CupertinoAppBar

](/docs/controls/cupertinoappbar)[

Next

MenuBar

](/docs/controls/menubar)

-   [Examples](#examples)
    -   [A simple CupertinoNavigationBar](#a-simple-cupertinonavigationbar)
-   [Properties](#properties)
    -   [`active_color`](#active_color)
    -   [`bgcolor`](#bgcolor)
    -   [`border`](#border)
    -   [`destinations`](#destinations)
    -   [`icon_size`](#icon_size)
    -   [`inactive_color`](#inactive_color)
    -   [`selected_index`](#selected_index)
-   [Events](#events)
    -   [`on_change`](#on_change)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  MenuBar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/menubar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/menubar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/menubar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/menubar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   MenuBar

On this page

# MenuBar

A menu bar that manages cascading child menus.

It could be placed anywhere but typically resides above the main body of the application and defines a menu system for invoking callbacks in response to user selection of a menu item.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/menubar)

-   Python

```
import flet as ftdef main(page: ft.Page):    appbar_text_ref = ft.Ref[ft.Text]()    def handle_menu_item_click(e):        print(f"{e.control.content.value}.on_click")        page.open(ft.SnackBar(content=ft.Text(f"{e.control.content.value} was clicked!")))        appbar_text_ref.current.value = e.control.content.value        page.update()    def handle_submenu_open(e):        print(f"{e.control.content.value}.on_open")    def handle_submenu_close(e):        print(f"{e.control.content.value}.on_close")    def handle_submenu_hover(e):        print(f"{e.control.content.value}.on_hover")    page.appbar = ft.AppBar(        title=ft.Text("Menus", ref=appbar_text_ref),        center_title=True,        bgcolor=ft.Colors.BLUE,    )    menubar = ft.MenuBar(        expand=True,        style=ft.MenuStyle(            alignment=ft.alignment.top_left,            bgcolor=ft.Colors.RED_300,            mouse_cursor={                ft.ControlState.HOVERED: ft.MouseCursor.WAIT,                ft.ControlState.DEFAULT: ft.MouseCursor.ZOOM_OUT,            },        ),        controls=[            ft.SubmenuButton(                content=ft.Text("File"),                on_open=handle_submenu_open,                on_close=handle_submenu_close,                on_hover=handle_submenu_hover,                controls=[                    ft.MenuItemButton(                        content=ft.Text("About"),                        leading=ft.Icon(ft.Icons.INFO),                        style=ft.ButtonStyle(                            bgcolor={ft.ControlState.HOVERED: ft.Colors.GREEN_100}                        ),                        on_click=handle_menu_item_click,                    ),                    ft.MenuItemButton(                        content=ft.Text("Save"),                        leading=ft.Icon(ft.Icons.SAVE),                        style=ft.ButtonStyle(                            bgcolor={ft.ControlState.HOVERED: ft.Colors.GREEN_100}                        ),                        on_click=handle_menu_item_click,                    ),                    ft.MenuItemButton(                        content=ft.Text("Quit"),                        leading=ft.Icon(ft.Icons.CLOSE),                        style=ft.ButtonStyle(                            bgcolor={ft.ControlState.HOVERED: ft.Colors.GREEN_100}                        ),                        on_click=handle_menu_item_click,                    ),                ],            ),            ft.SubmenuButton(                content=ft.Text("View"),                on_open=handle_submenu_open,                on_close=handle_submenu_close,                on_hover=handle_submenu_hover,                controls=[                    ft.SubmenuButton(                        content=ft.Text("Zoom"),                        controls=[                            ft.MenuItemButton(                                content=ft.Text("Magnify"),                                leading=ft.Icon(ft.Icons.ZOOM_IN),                                close_on_click=False,                                style=ft.ButtonStyle(                                    bgcolor={                                        ft.ControlState.HOVERED: ft.Colors.PURPLE_200                                    }                                ),                                on_click=handle_menu_item_click,                            ),                            ft.MenuItemButton(                                content=ft.Text("Minify"),                                leading=ft.Icon(ft.Icons.ZOOM_OUT),                                close_on_click=False,                                style=ft.ButtonStyle(                                    bgcolor={                                        ft.ControlState.HOVERED: ft.Colors.PURPLE_200                                    }                                ),                                on_click=handle_menu_item_click,                            ),                        ],                    )                ],            ),        ],    )    page.add(ft.Row([menubar]))ft.app(main)
```

![](https://flet.dev/docs/controls/menubar/img/docs/controls/menu-bar/menu-bar.gif)

## Properties[​](#properties "Direct link to Properties")

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

Whether to clip the content of this control or not.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `controls`[​](#controls "Direct link to controls")

The list of menu items that are the top level children of the `MenuBar`.

### `style`[​](#style "Direct link to style")

Value is of type [`MenuStyle`](/docs/reference/types/menustyle).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/menubar.md)

[

Previous

CupertinoNavigationBar

](/docs/controls/cupertinonavigationbar)[

Next

NavigationBar

](/docs/controls/navigationbar)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`clip_behavior`](#clip_behavior)
    -   [`controls`](#controls)
    -   [`style`](#style)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  NavigationBar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/navigationbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/navigationbar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/navigationbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/navigationbar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   NavigationBar

On this page

# NavigationBar

Material 3 Navigation Bar component.

Navigation bars offer a persistent and convenient way to switch between primary destinations in an app.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/navigationbar)

### A simple NavigationBar[​](#a-simple-navigationbar "Direct link to A simple NavigationBar")

![](https://flet.dev/docs/controls/navigationbar/img/docs/controls/navigation-bar/navigation-bar-sample.gif)

```
import flet as ftdef main(page: ft.Page):    page.title = "NavigationBar Example"    page.navigation_bar = ft.NavigationBar(        destinations=[            ft.NavigationBarDestination(icon=ft.Icons.EXPLORE, label="Explore"),            ft.NavigationBarDestination(icon=ft.Icons.COMMUTE, label="Commute"),            ft.NavigationBarDestination(                icon=ft.Icons.BOOKMARK_BORDER,                selected_icon=ft.Icons.BOOKMARK,                label="Explore",            ),        ]    )    page.add(ft.Text("Body!"))ft.app(main)
```

## `NavigationBar` properties[​](#navigationbar-properties "Direct link to navigationbar-properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive `NavigationBar` is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a `CupertinoNavigationBar` is created, which has matching functionality and presentation as `NavigationBar`, and the graphics as expected on iOS. On other platforms, a Material `NavigationBar` is created.

Defaults to `False`.

### `animation_duration`[​](#animation_duration "Direct link to animation_duration")

The transition time for each destination as it goes between selected and unselected.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The [color](/docs/reference/colors) of the navigation bar itself.

### `destinations`[​](#destinations "Direct link to destinations")

Defines the appearance of the button items that are arrayed within the navigation bar.

The value must be a list of two or more `NavigationBarDestination` instances.

### `elevation`[​](#elevation "Direct link to elevation")

The elevation of the navigation bar itself.

### `indicator_color`[​](#indicator_color "Direct link to indicator_color")

The [color](/docs/reference/colors) of the selected destination indicator.

### `indicator_shape`[​](#indicator_shape "Direct link to indicator_shape")

The shape of the selected destination indicator.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder).

### `label_behavior`[​](#label_behavior "Direct link to label_behavior")

Defines how the destinations' labels will be laid out and when they'll be displayed.

Can be used to show all labels, show only the selected label, or hide all labels.

Value is of type [`NavigationBarLabelBehavior`](/docs/reference/types/navigationbarlabelbehavior) and defaults to `NavigationBarLabelBehavior.ALWAYS_SHOW`.

### `overlay_color`[​](#overlay_color "Direct link to overlay_color")

The highlight [color](/docs/reference/colors) of the `NavigationDestination` in various [`ControlState`](/docs/reference/types/controlstate) states. The following [`ControlState`](/docs/reference/types/controlstate) values are supported: `PRESSED`, `HOVERED` and `FOCUSED`.

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index into `destinations` for the current selected `NavigationBarDestination` or `None` if no destination is selected.

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) used for the drop shadow to indicate `elevation`.

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The surface tint of the Material that holds the NavigationDrawer's contents.

## `NavigationBar` events[​](#navigationbar-events "Direct link to navigationbar-events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when selected destination changed.

## `NavigationBarDestination` properties[​](#navigationbardestination-properties "Direct link to navigationbardestination-properties")

### `bgcolor`[​](#bgcolor-1 "Direct link to bgcolor-1")

The [color](/docs/reference/colors) of this destination.

### `icon`[​](#icon "Direct link to icon")

The [name of the icon](/docs/reference/icons) or `Control` of the destination.

Example with icon name:

```
icon=ft.Icons.BOOKMARK
```

Example with Control:

```
icon=ft.Icon(ft.Icons.BOOKMARK)
```

If `selected_icon` is provided, this will only be displayed when the destination is not selected.

To make the NavigationBar more accessible, consider choosing an icon with a stroked and filled version, such as `ft.Icons.CLOUD` and `ft.Icons.CLOUD_QUEUE`. The icon should be set to the stroked version and `selected_icon` to the filled version.

### `icon_content`[​](#icon_content "Direct link to icon_content")

The icon `Control` of the destination. Typically the icon is an [`Icon`](/docs/controls/icon) control. Used instead of `icon` property.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`icon`](#icon) instead.**

### `label`[​](#label "Direct link to label")

The text label that appears below the icon of this `NavigationBarDestination`.

### `selected_icon`[​](#selected_icon "Direct link to selected_icon")

The [name](/docs/reference/icons) of alternative icon or `Control` displayed when this destination is selected.

Example with icon name:

```
selected_icon=ft.Icons.BOOKMARK
```

Example with Control:

```
selected_icon=ft.Icon(ft.Icons.BOOKMARK)
```

If this icon is not provided, the NavigationBar will display `icon` in either state.

### `selected_icon_content`[​](#selected_icon_content "Direct link to selected_icon_content")

An alternative icon `Control` displayed when this destination is selected.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`selected_icon`](#selected_icon) instead.**

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/navigationbar.md)

[

Previous

MenuBar

](/docs/controls/menubar)[

Next

NavigationDrawer

](/docs/controls/navigationdrawer)

-   [Examples](#examples)
    -   [A simple NavigationBar](#a-simple-navigationbar)
-   [`NavigationBar` properties](#navigationbar-properties)
    -   [`adaptive`](#adaptive)
    -   [`animation_duration`](#animation_duration)
    -   [`bgcolor`](#bgcolor)
    -   [`destinations`](#destinations)
    -   [`elevation`](#elevation)
    -   [`indicator_color`](#indicator_color)
    -   [`indicator_shape`](#indicator_shape)
    -   [`label_behavior`](#label_behavior)
    -   [`overlay_color`](#overlay_color)
    -   [`selected_index`](#selected_index)
    -   [`shadow_color`](#shadow_color)
    -   [`surface_tint_color`](#surface_tint_color)
-   [`NavigationBar` events](#navigationbar-events)
    -   [`on_change`](#on_change)
-   [`NavigationBarDestination` properties](#navigationbardestination-properties)
    -   [`bgcolor`](#bgcolor-1)
    -   [`icon`](#icon)
    -   [`icon_content`](#icon_content)
    -   [`label`](#label)
    -   [`selected_icon`](#selected_icon)
    -   [`selected_icon_content`](#selected_icon_content)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  NavigationDrawer | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/navigationdrawer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/navigationdrawer/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/navigationdrawer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/navigationdrawer/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   NavigationDrawer

On this page

# NavigationDrawer

Material Design Navigation Drawer component.

Navigation Drawer is a panel that slides in horizontally from the left or right edge of a page to show primary destinations in an app. To add NavigationDrawer to the page, use [`page.drawer`](/docs/controls/page#drawer) and [`page.end_drawer`](/docs/controls/page#end_drawer) properties. Similarly, the NavigationDrawer can be added to a [`View`](/docs/controls/view#drawer). To display the drawer, set its `open` property to `True`.

To open this control, simply call the [`page.open()`](/docs/controls/page#opencontrol) helper-method.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/navigationdrawer)

### NavigationDrawer sliding from the left edge of a page[​](#navigationdrawer-sliding-from-the-left-edge-of-a-page "Direct link to NavigationDrawer sliding from the left edge of a page")

![](https://flet.dev/docs/controls/navigationdrawer/img/docs/controls/navigationdrawer/navigation-drawer-start.gif)

```
import flet as ftdef main(page: ft.Page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    def handle_dismissal(e):        page.add(ft.Text("Drawer dismissed"))    def handle_change(e):        page.add(ft.Text(f"Selected Index changed: {e.control.selected_index}"))        # page.close(drawer)    drawer = ft.NavigationDrawer(        on_dismiss=handle_dismissal,        on_change=handle_change,        controls=[            ft.Container(height=12),            ft.NavigationDrawerDestination(                label="Item 1",                icon=ft.Icons.DOOR_BACK_DOOR_OUTLINED,                selected_icon=ft.Icon(ft.Icons.DOOR_BACK_DOOR),            ),            ft.Divider(thickness=2),            ft.NavigationDrawerDestination(                icon=ft.Icon(ft.Icons.MAIL_OUTLINED),                label="Item 2",                selected_icon=ft.Icons.MAIL,            ),            ft.NavigationDrawerDestination(                icon=ft.Icon(ft.Icons.PHONE_OUTLINED),                label="Item 3",                selected_icon=ft.Icons.PHONE,            ),        ],    )    page.add(ft.ElevatedButton("Show drawer", on_click=lambda e: page.open(drawer)))ft.app(main)
```

### NavigationDrawer sliding from the right edge of a page[​](#navigationdrawer-sliding-from-the-right-edge-of-a-page "Direct link to NavigationDrawer sliding from the right edge of a page")

![](https://flet.dev/docs/controls/navigationdrawer/img/docs/controls/navigationdrawer/navigation-drawer-end.gif)

```
import flet as ftdef main(page: ft.Page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    def handle_dismissal(e):        page.add(ft.Text("End drawer dismissed"))    def handle_change(e):        page.add(ft.Text(f"Selected Index changed: {e.control.selected_index}"))        # page.close(end_drawer)    end_drawer = ft.NavigationDrawer(        position=ft.NavigationDrawerPosition.END,        on_dismiss=handle_dismissal,        on_change=handle_change,        controls=[            ft.NavigationDrawerDestination(icon=ft.Icons.ADD_TO_HOME_SCREEN_SHARP, label="Item 1"),            ft.NavigationDrawerDestination(icon=ft.Icon(ft.Icons.ADD_COMMENT), label="Item 2"),        ],    )    page.add(ft.ElevatedButton("Show end drawer", on_click=lambda e: page.open(end_drawer)))ft.app(main)
```

## `NavigationDrawer` properties[​](#navigationdrawer-properties "Direct link to navigationdrawer-properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The [color](/docs/reference/colors) of the navigation drawer itself.

### `controls`[​](#controls "Direct link to controls")

Defines the appearance of the items within the navigation drawer.

The list contains `NavigationDrawerDestination` items and/or other controls such as headlines and dividers.

### `elevation`[​](#elevation "Direct link to elevation")

The elevation of the navigation drawer itself.

### `indicator_color`[​](#indicator_color "Direct link to indicator_color")

The [color](/docs/reference/colors) of the selected destination indicator.

### `indicator_shape`[​](#indicator_shape "Direct link to indicator_shape")

The shape of the selected destination indicator.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder).

### `position`[​](#position "Direct link to position")

The position of this drawer.

Value is of type [`NavigationDrawerPosition`](/docs/reference/types/navigationdrawerposition) and defaults to `NavigationDrawerPosition.START`.

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index for the current selected `NavigationDrawerDestination` or null if no destination is selected.

A valid selected\_index is an integer between 0 and number of destinations - `1`. For an invalid `selected_index`, for example, `-1`, all destinations will appear unselected.

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) used for the drop shadow to indicate `elevation`.

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The surface tint of the Material that holds the NavigationDrawer's contents.

### `tile_padding`[​](#tile_padding "Direct link to tile_padding")

Defines the padding for `NavigationDrawerDestination` controls.

## `NavigationDrawer` events[​](#navigationdrawer-events "Direct link to navigationdrawer-events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when selected destination changed.

### `on_dismiss`[​](#on_dismiss "Direct link to on_dismiss")

Fires when drawer is dismissed by clicking outside of the panel or [programmatically](/docs/controls/page#closecontrol).

## `NavigationDrawerDestination` properties[​](#navigationdrawerdestination-properties "Direct link to navigationdrawerdestination-properties")

### `bgcolor`[​](#bgcolor-1 "Direct link to bgcolor-1")

The [color](/docs/reference/colors) of this destination.

### `icon`[​](#icon "Direct link to icon")

The [name of the icon](/docs/reference/icons) or `Control` of the destination.

Example with icon name:

```
icon=ft.Icons.BOOKMARK
```

Example with Control:

```
icon=ft.Icon(ft.Icons.BOOKMARK)
```

If `selected_icon` is provided, this will only be displayed when the destination is not selected.

### `icon_content`[​](#icon_content "Direct link to icon_content")

The icon `Control` of the destination. Typically the icon is an [`Icon`](/docs/controls/icon) control. Used instead of `icon` property.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`icon`](#icon) instead.**

### `label`[​](#label "Direct link to label")

The text label that appears below the icon of this `NavigationDrawerDestination`.

### `selected_icon`[​](#selected_icon "Direct link to selected_icon")

The [name](/docs/reference/icons) of alternative icon or `Control` displayed when this destination is selected.

Example with icon name:

```
selected_icon=ft.Icons.BOOKMARK
```

Example with Control:

```
selected_icon=ft.Icon(ft.Icons.BOOKMARK)
```

If this icon is not provided, the NavigationDrawer will display `icon` in either state.

### `selected_icon_content`[​](#selected_icon_content "Direct link to selected_icon_content")

An alternative icon `Control` displayed when this destination is selected.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`selected_icon`](#selected_icon) instead.**

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/navigationdrawer.md)

[

Previous

NavigationBar

](/docs/controls/navigationbar)[

Next

NavigationRail

](/docs/controls/navigationrail)

-   [Examples](#examples)
    -   [NavigationDrawer sliding from the left edge of a page](#navigationdrawer-sliding-from-the-left-edge-of-a-page)
    -   [NavigationDrawer sliding from the right edge of a page](#navigationdrawer-sliding-from-the-right-edge-of-a-page)
-   [`NavigationDrawer` properties](#navigationdrawer-properties)
    -   [`bgcolor`](#bgcolor)
    -   [`controls`](#controls)
    -   [`elevation`](#elevation)
    -   [`indicator_color`](#indicator_color)
    -   [`indicator_shape`](#indicator_shape)
    -   [`position`](#position)
    -   [`selected_index`](#selected_index)
    -   [`shadow_color`](#shadow_color)
    -   [`surface_tint_color`](#surface_tint_color)
    -   [`tile_padding`](#tile_padding)
-   [`NavigationDrawer` events](#navigationdrawer-events)
    -   [`on_change`](#on_change)
    -   [`on_dismiss`](#on_dismiss)
-   [`NavigationDrawerDestination` properties](#navigationdrawerdestination-properties)
    -   [`bgcolor`](#bgcolor-1)
    -   [`icon`](#icon)
    -   [`icon_content`](#icon_content)
    -   [`label`](#label)
    -   [`selected_icon`](#selected_icon)
    -   [`selected_icon_content`](#selected_icon_content)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Canvas | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/canvas/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/canvas/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/canvas/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/canvas/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Canvas

On this page

# Canvas

Canvas is a control for drawing arbitrary graphics using a set of primitives or "shapes" such as line, arc, path and text.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/canvas)

### Basic usage[​](#basic-usage "Direct link to Basic usage")

![](https://flet.dev/docs/controls/canvas/img/docs/controls/canvas/canvas-face.png)

```
import mathimport flet as ftimport flet.canvas as cvdef main(page: ft.Page):    stroke_paint = ft.Paint(stroke_width=2, style=ft.PaintingStyle.STROKE)    fill_paint = ft.Paint(style=ft.PaintingStyle.FILL)    cp = cv.Canvas(        [            cv.Circle(100, 100, 50, stroke_paint),            cv.Circle(80, 90, 10, stroke_paint),            cv.Circle(84, 87, 5, fill_paint),            cv.Circle(120, 90, 10, stroke_paint),            cv.Circle(124, 87, 5, fill_paint),            cv.Arc(70, 95, 60, 40, 0, math.pi, paint=stroke_paint),        ],        width=float("inf"),        expand=True,    )    page.add(cp)ft.app(main)
```

### `Path` shape example[​](#path-shape-example "Direct link to path-shape-example")

![](https://flet.dev/docs/controls/canvas/img/docs/controls/canvas/canvas-triangles.png)

```
import mathimport flet as ftimport flet.canvas as cvdef main(page: ft.Page):    cp = cv.Canvas(        [            cv.Path(                [                    cv.Path.MoveTo(25, 25),                    cv.Path.LineTo(105, 25),                    cv.Path.LineTo(25, 105),                ],                paint=ft.Paint(                    style=ft.PaintingStyle.FILL,                ),            ),            cv.Path(                [                    cv.Path.MoveTo(125, 125),                    cv.Path.LineTo(125, 45),                    cv.Path.LineTo(45, 125),                    cv.Path.Close(),                ],                paint=ft.Paint(                    stroke_width=2,                    style=ft.PaintingStyle.STROKE,                ),            ),        ],        width=float("inf"),        expand=True,    )    page.add(cp)ft.app(main)
```

### Bezier curves[​](#bezier-curves "Direct link to Bezier curves")

![](https://flet.dev/docs/controls/canvas/img/docs/controls/canvas/canvas-bezier.png)

```
import mathimport flet as ftimport flet.canvas as cvdef main(page: ft.Page):    cp = cv.Canvas(        [            cv.Path(                [                    cv.Path.MoveTo(75, 25),                    cv.Path.QuadraticTo(25, 25, 25, 62.5),                    cv.Path.QuadraticTo(25, 100, 50, 100),                    cv.Path.QuadraticTo(50, 120, 30, 125),                    cv.Path.QuadraticTo(60, 120, 65, 100),                    cv.Path.QuadraticTo(125, 100, 125, 62.5),                    cv.Path.QuadraticTo(125, 25, 75, 25),                ],                paint=ft.Paint(                    stroke_width=2,                    style=ft.PaintingStyle.STROKE,                ),            ),            cv.Path(                [                    cv.Path.SubPath(                        [                            cv.Path.MoveTo(75, 40),                            cv.Path.CubicTo(75, 37, 70, 25, 50, 25),                            cv.Path.CubicTo(20, 25, 20, 62.5, 20, 62.5),                            cv.Path.CubicTo(20, 80, 40, 102, 75, 120),                            cv.Path.CubicTo(110, 102, 130, 80, 130, 62.5),                            cv.Path.CubicTo(130, 62.5, 130, 25, 100, 25),                            cv.Path.CubicTo(85, 25, 75, 37, 75, 40),                        ],                        100,                        100,                    )                ],                paint=ft.Paint(                    gradient=ft.PaintRadialGradient(                        ft.Offset(150, 150), 50, [ft.Colors.PINK_100, ft.Colors.PINK]                    ),                    style=ft.PaintingStyle.FILL,                ),            ),        ],        width=float("inf"),        expand=True,    )    page.add(cp)ft.app(main)
```

### Drawing text[​](#drawing-text "Direct link to Drawing text")

![](https://flet.dev/docs/controls/canvas/img/docs/controls/canvas/canvas-text.png)

```
import mathimport flet as ftimport flet.canvas as cvdef main(page: ft.Page):    cp = cv.Canvas(        [            cv.Text(0, 0, "Just a text"),            cv.Circle(200, 100, 2, ft.Paint(color=ft.Colors.RED)),            cv.Text(                200,                100,                "Rotated",                ft.TextStyle(weight=ft.FontWeight.BOLD, size=30),                spans=[                    ft.TextSpan(                        "around top_center",                        ft.TextStyle(italic=True, color=ft.Colors.GREEN, size=20),                    )                ],                alignment=ft.alignment.top_center,                rotate=math.pi * 0.15,            ),            cv.Circle(400, 100, 2, ft.Paint(color=ft.Colors.RED)),            cv.Text(                400,                100,                "Rotated around top_left",                ft.TextStyle(size=20),                alignment=ft.alignment.top_left,                rotate=math.pi * -0.15,            ),            cv.Circle(600, 200, 2, ft.Paint(color=ft.Colors.RED)),            cv.Text(                600,                200,                "Rotated around center",                ft.TextStyle(size=20),                alignment=ft.alignment.center,                rotate=math.pi / 2,            ),            cv.Text(                300,                400,                "Limited to max_width and right-aligned.
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",                text_align=ft.TextAlign.RIGHT,                max_width=400,            ),            cv.Text(                200,                200,                "WOW!",                ft.TextStyle(                    weight=ft.FontWeight.BOLD,                    size=100,                    foreground=ft.Paint(                        gradient=ft.PaintLinearGradient(                            (200, 200),                            (300, 300),                            colors=[ft.Colors.YELLOW, ft.Colors.RED],                        ),                        stroke_join=ft.StrokeJoin.ROUND,                        stroke_cap=ft.StrokeCap.ROUND,                    ),                ),            ),            cv.Text(                200,                200,                "WOW!",                ft.TextStyle(                    weight=ft.FontWeight.BOLD,                    size=100,                    foreground=ft.Paint(                        color=ft.Colors.PINK,                        stroke_width=6,                        style=ft.PaintingStyle.STROKE,                        stroke_join=ft.StrokeJoin.ROUND,                        stroke_cap=ft.StrokeCap.ROUND,                    ),                ),            ),        ],        width=float("inf"),        expand=True,    )    page.add(cp)ft.app(main)
```

### Free-hand drawing tool - canvas with gesture detector[​](#free-hand-drawing-tool---canvas-with-gesture-detector "Direct link to Free-hand drawing tool - canvas with gesture detector")

![](https://flet.dev/docs/controls/canvas/img/docs/controls/canvas/canvas-flet-brush.gif)

```
import flet as ftimport flet.canvas as cvclass State:    x: float    y: floatstate = State()def main(page: ft.Page):    page.title = "Flet Brush"    def pan_start(e: ft.DragStartEvent):        state.x = e.local_x        state.y = e.local_y    def pan_update(e: ft.DragUpdateEvent):        cp.shapes.append(            cv.Line(                state.x, state.y, e.local_x, e.local_y, paint=ft.Paint(stroke_width=3)            )        )        cp.update()        state.x = e.local_x        state.y = e.local_y    cp = cv.Canvas(        [            cv.Fill(                ft.Paint(                    gradient=ft.PaintLinearGradient(                        (0, 0), (600, 600), colors=[ft.Colors.CYAN_50, ft.Colors.GREY]                    )                )            ),        ],        content=ft.GestureDetector(            on_pan_start=pan_start,            on_pan_update=pan_update,            drag_interval=10,        ),        expand=False,    )    page.add(        ft.Container(            cp,            border_radius=5,            width=float("inf"),            expand=True,        )    )ft.app(main)
```

## `Canvas` properties[​](#canvas-properties "Direct link to canvas-properties")

### `resize_interval`[​](#resize_interval "Direct link to resize_interval")

Sampling interval in milliseconds for `on_resize` event.

Defaults to `0` - call `on_resize` immediately on every change.

### `shapes`[​](#shapes "Direct link to shapes")

The list of `Shape` objects (see below) to draw on the canvas.

## `Canvas` events[​](#canvas-events "Direct link to canvas-events")

### `on_resize`[​](#on_resize "Direct link to on_resize")

Fires when the size of canvas has changed.

Event object `e` is an instance of [`CanvasResizeEvent`](/docs/reference/types/canvasresizeevent).

## `Arc` shape properties[​](#arc-shape-properties "Direct link to arc-shape-properties")

Draws an arc scaled to fit inside the given rectangle.

It starts from `start_angle` radians around the oval up to `start_angle` + `sweep_angle` radians around the oval, with zero radians being the point on the right hand side of the oval that crosses the horizontal line that intersects the center of the rectangle and with positive angles going clockwise around the oval. If `use_center` is `True`, the arc is closed back to the center, forming a circle sector. Otherwise, the arc is not closed, forming a circle segment.

\[PICTURE\] - [https://api.flutter.dev/flutter/dart-ui/Canvas/drawArc.html](https://api.flutter.dev/flutter/dart-ui/Canvas/drawArc.html)

### `height`[​](#height "Direct link to height")

Height of the rectangle containing the arc's oval.

### `paint`[​](#paint "Direct link to paint")

A style to draw an arc with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

### `start_angle`[​](#start_angle "Direct link to start_angle")

Starting angle in radians to draw arc from.

### `sweep_angle`[​](#sweep_angle "Direct link to sweep_angle")

The length of the arc in radians.

### `use_center`[​](#use_center "Direct link to use_center")

If `use_center` is `True`, the arc is closed back to the center, forming a circle sector. Otherwise, the arc is not closed, forming a circle segment.

### `width`[​](#width "Direct link to width")

Width of the rectangle containing the arc's oval.

### `x`[​](#x "Direct link to x")

The x-axis coordinate of the arc's top left point.

### `y`[​](#y "Direct link to y")

The y-axis coordinate of the arc's top left point.

## `Circle` shape properties[​](#circle-shape-properties "Direct link to circle-shape-properties")

Draws a circle.

### `paint`[​](#paint-1 "Direct link to paint-1")

A style to draw a circle with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

### `radius`[​](#radius "Direct link to radius")

Circle's radius.

### `x`[​](#x-1 "Direct link to x-1")

The x-axis coordinate of the circle's center point.

### `y`[​](#y-1 "Direct link to y-1")

The y-axis coordinate of the circle's center point.

## `Color` shape properties[​](#color-shape-properties "Direct link to color-shape-properties")

Paints the given `color` onto the canvas, applying the given `blend_mode`, with the given color being the source and the background being the destination.

### `blend_mode`[​](#blend_mode "Direct link to blend_mode")

Blend mode to apply.

Value is of type [`BlendMode`](/docs/reference/types/blendmode).

### `color`[​](#color "Direct link to color")

[Color](/docs/reference/colors) to paint onto the canvas.

## `Fill` shape properties[​](#fill-shape-properties "Direct link to fill-shape-properties")

Fills the canvas with the given `Paint`.

To fill the canvas with a solid color and blend mode, consider `Color` shape instead.

### `paint`[​](#paint-2 "Direct link to paint-2")

A style to fill the canvas with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

## `Line` shape properties[​](#line-shape-properties "Direct link to line-shape-properties")

Draws a line between the given points using the given paint. The line is stroked, the value of the `Paint.style` is ignored.

### `paint`[​](#paint-3 "Direct link to paint-3")

A style to draw a line with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

### `x1`[​](#x1 "Direct link to x1")

The x-axis coordinate of the line's starting point.

### `y1`[​](#y1 "Direct link to y1")

The y-axis coordinate of the line's starting point.

### `x2`[​](#x2 "Direct link to x2")

The x-axis coordinate of the line's end point.

### `y2`[​](#y2 "Direct link to y2")

The y-axis coordinate of the line's end point.

## `Oval` shape properties[​](#oval-shape-properties "Direct link to oval-shape-properties")

Draws an axis-aligned oval that fills the given axis-aligned rectangle with the given `Paint`. Whether the oval is filled or stroked (or both) is controlled by `Paint.style`.

### `height`[​](#height-1 "Direct link to height-1")

Height of the rectangle containing the oval.

### `paint`[​](#paint-4 "Direct link to paint-4")

A style to draw an oval with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

### `width`[​](#width-1 "Direct link to width-1")

Width of the rectangle containing the oval.

### `x`[​](#x-2 "Direct link to x-2")

The x-axis coordinate of the oval's top left point.

### `y`[​](#y-2 "Direct link to y-2")

The y-axis coordinate of the oval's top left point.

## `Path` shape properties[​](#path-shape-properties "Direct link to path-shape-properties")

Draws the a path with given `elements` with the given `Paint`.

Whether this shape is filled or stroked (or both) is controlled by `Paint.style`. If the path is filled, then sub-paths within it are implicitly closed (see `Path.Close`).

### `elements`[​](#elements "Direct link to elements")

The list of path elements:

#### `Path.MoveTo(x, y)`[​](#pathmovetox-y "Direct link to pathmovetox-y")

Starts a new sub-path at the given point (`x`,`y`).

#### `Path.LineTo(x, y)`[​](#pathlinetox-y "Direct link to pathlinetox-y")

Adds a straight line segment from the current point to the given point (`x`,`y`).

#### `Path.QuadraticTo(cp1x, cp2y, x, y, w)`[​](#pathquadratictocp1x-cp2y-x-y-w "Direct link to pathquadratictocp1x-cp2y-x-y-w")

Adds a bezier segment that curves from the current point to the given point (`x`,`y`), using the control points (`cp1x`,`cp1y`) and the weight `w`. If the weight is greater than 1, then the curve is a hyperbola; if the weight equals 1, it's a parabola; and if it is less than 1, it is an ellipse.

#### `Path.CubicTo(cp1x, cp1y, cp2x, cp2y, x, y)`[​](#pathcubictocp1x-cp1y-cp2x-cp2y-x-y "Direct link to pathcubictocp1x-cp1y-cp2x-cp2y-x-y")

Adds a cubic bezier segment that curves from the current point to the given point (`x`,`y`), using the control points (`cp1x`,`cp1y`) and (`cp2x`,`cp2y`).

#### `Path.SubPath(elements, x, y)`[​](#pathsubpathelements-x-y "Direct link to pathsubpathelements-x-y")

Adds the sub-path described by `elements` to the given point (`x`,`y`).

#### `Path.Arc(x, y, width, height, start_angle, sweep_angle)`[​](#patharcx-y-width-height-start_angle-sweep_angle "Direct link to patharcx-y-width-height-start_angle-sweep_angle")

Adds a new sub-path with one arc segment that consists of the arc that follows the edge of the oval bounded by the given rectangle with top left corner at `x` and `y` and dimensions `width` and `height`, from `start_angle` radians around the oval up to `start_angle` + `sweep_angle` radians around the oval, with zero radians being the point on the right hand side of the oval that crosses the horizontal line that intersects the center of the rectangle and with positive angles going clockwise around the oval.

#### `Path.ArcTo(x, y, radius, rotation, large_arc, clockwise)`[​](#patharctox-y-radius-rotation-large_arc-clockwise "Direct link to patharctox-y-radius-rotation-large_arc-clockwise")

Appends up to four conic curves weighted to describe an oval of `radius` and rotated by `rotation` (measured in degrees and clockwise).

The first curve begins from the last point in the path and the last ends at `x` and `y`. The curves follow a path in a direction determined by `clockwise` (bool) and `large_arc` (bool) in such a way that the sweep angle is always less than 360 degrees.

A simple line is appended if either either radii are zero or the last point in the path (`x`,`y`). The radii are scaled to fit the last path point if both are greater than zero but too small to describe an arc.

#### `Path.Oval(x, y, width, height)`[​](#pathovalx-y-width-height "Direct link to pathovalx-y-width-height")

Adds a new sub-path that consists of a curve that forms the ellipse that fills the given rectangle.

#### `Path.Rect(x, y, width, height, border_radius)`[​](#pathrectx-y-width-height-border_radius "Direct link to pathrectx-y-width-height-border_radius")

Adds a rectangle as a new sub-path.

#### `Path.Close`[​](#pathclose "Direct link to pathclose")

Closes the last sub-path, as if a straight line had been drawn from the current point to the first point of the sub-path.

### `paint`[​](#paint-5 "Direct link to paint-5")

A style to draw a path with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

## `Points` shape properties[​](#points-shape-properties "Direct link to points-shape-properties")

Draws a sequence of points according to the given `point_mode`.

### `paint`[​](#paint-6 "Direct link to paint-6")

A style to draw points with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

### `points`[​](#points "Direct link to points")

The list of `ft.Offset` describing points.

### `point_mode`[​](#point_mode "Direct link to point_mode")

Defines how a list of points is interpreted when drawing a set of points.

Value is of type [`PointMode`](/docs/reference/types/pointmode).

## `Rect` shape properties[​](#rect-shape-properties "Direct link to rect-shape-properties")

Draws a rectangle.

### `border_radius`[​](#border_radius "Direct link to border_radius")

Border radius of the rectangle.

Value is of type [`BorderRadius`](/docs/reference/types/borderradius).

### `height`[​](#height-2 "Direct link to height-2")

Height of the rectangle.

### `paint`[​](#paint-7 "Direct link to paint-7")

A style to draw a rectangle with. The value of this property is the instance of [`Paint`](/docs/reference/types/paint) class.

### `width`[​](#width-2 "Direct link to width-2")

Width of the rectangle.

### `x`[​](#x-3 "Direct link to x-3")

The x-axis coordinate of the rectangle's top left point.

### `y`[​](#y-3 "Direct link to y-3")

The y-axis coordinate of the rectangle's top left point.

## `Shadow` shape properties[​](#shadow-shape-properties "Direct link to shadow-shape-properties")

Draws a shadow for a `path` representing the given material `elevation`.

The `transparent_occluder` argument should be `True` if the occluding object is not opaque.

### `color`[​](#color-1 "Direct link to color-1")

Shadow [color](/docs/reference/colors).

### `elevation`[​](#elevation "Direct link to elevation")

Shadow elevation.

### `path`[​](#path "Direct link to path")

The list of `Path.PathElement` objects describing the path.

### `transparent_occluder`[​](#transparent_occluder "Direct link to transparent_occluder")

`True` if the occluding object is not opaque.

Defaults to `False`.

## `Text` shape properties[​](#text-shape-properties "Direct link to text-shape-properties")

Draws `text` with `style` in the given point (`x`, `y`).

### `alignment`[​](#alignment "Direct link to alignment")

A point within a text rectangle to determine its position and rotation center.

Value is of type [`Alignment`](/docs/reference/types/alignment) and defaults to `alignment.top_left`.

### `ellipsis`[​](#ellipsis "Direct link to ellipsis")

String used to ellipsize overflowing text.

### `max_lines`[​](#max_lines "Direct link to max_lines")

The maximum number of lines painted. Lines beyond this number are silently dropped. For example, if `max_lines = 1`, then only one line is rendered. If `max_lines = None`, but `ellipsis != None`, then lines after the first one that overflows the width constraints are dropped.

### `max_width`[​](#max_width "Direct link to max_width")

The maximum width of the painted text.

Defaults to `None` - infinity.

### `rotate`[​](#rotate "Direct link to rotate")

Text rotation in radians. Text is rotated around the point determined by `alignment`. See code examples above.

### `spans`[​](#spans "Direct link to spans")

The list of [`TextSpan`](/docs/reference/types/textspan) objects to build a rich text paragraph.

### `style`[​](#style "Direct link to style")

A text style to draw `text` and `spans` with. The value is the instance of [`TextStyle`](/docs/reference/types/textstyle) class.

### `text`[​](#text "Direct link to text")

The text to draw.

### `text_align`[​](#text_align "Direct link to text_align")

Text horizontal align.

Value is of type [`TextAlign`](/docs/reference/types/textalign) and defaults to `TextAlign.LEFT`.

### `x`[​](#x-4 "Direct link to x-4")

The x-axis coordinate of the text's `alignment` point.

### `y`[​](#y-4 "Direct link to y-4")

The y-axis coordinate of the text's `alignment` point.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/canvas.md)

[

Previous

InterstitialAd

](/docs/controls/interstitialad)[

Next

CircleAvatar

](/docs/controls/circleavatar)

-   [Examples](#examples)
    -   [Basic usage](#basic-usage)
    -   [`Path` shape example](#path-shape-example)
    -   [Bezier curves](#bezier-curves)
    -   [Drawing text](#drawing-text)
    -   [Free-hand drawing tool - canvas with gesture detector](#free-hand-drawing-tool---canvas-with-gesture-detector)
-   [`Canvas` properties](#canvas-properties)
    -   [`resize_interval`](#resize_interval)
    -   [`shapes`](#shapes)
-   [`Canvas` events](#canvas-events)
    -   [`on_resize`](#on_resize)
-   [`Arc` shape properties](#arc-shape-properties)
    -   [`height`](#height)
    -   [`paint`](#paint)
    -   [`start_angle`](#start_angle)
    -   [`sweep_angle`](#sweep_angle)
    -   [`use_center`](#use_center)
    -   [`width`](#width)
    -   [`x`](#x)
    -   [`y`](#y)
-   [`Circle` shape properties](#circle-shape-properties)
    -   [`paint`](#paint-1)
    -   [`radius`](#radius)
    -   [`x`](#x-1)
    -   [`y`](#y-1)
-   [`Color` shape properties](#color-shape-properties)
    -   [`blend_mode`](#blend_mode)
    -   [`color`](#color)
-   [`Fill` shape properties](#fill-shape-properties)
    -   [`paint`](#paint-2)
-   [`Line` shape properties](#line-shape-properties)
    -   [`paint`](#paint-3)
    -   [`x1`](#x1)
    -   [`y1`](#y1)
    -   [`x2`](#x2)
    -   [`y2`](#y2)
-   [`Oval` shape properties](#oval-shape-properties)
    -   [`height`](#height-1)
    -   [`paint`](#paint-4)
    -   [`width`](#width-1)
    -   [`x`](#x-2)
    -   [`y`](#y-2)
-   [`Path` shape properties](#path-shape-properties)
    -   [`elements`](#elements)
    -   [`paint`](#paint-5)
-   [`Points` shape properties](#points-shape-properties)
    -   [`paint`](#paint-6)
    -   [`points`](#points)
    -   [`point_mode`](#point_mode)
-   [`Rect` shape properties](#rect-shape-properties)
    -   [`border_radius`](#border_radius)
    -   [`height`](#height-2)
    -   [`paint`](#paint-7)
    -   [`width`](#width-2)
    -   [`x`](#x-3)
    -   [`y`](#y-3)
-   [`Shadow` shape properties](#shadow-shape-properties)
    -   [`color`](#color-1)
    -   [`elevation`](#elevation)
    -   [`path`](#path)
    -   [`transparent_occluder`](#transparent_occluder)
-   [`Text` shape properties](#text-shape-properties)
    -   [`alignment`](#alignment)
    -   [`ellipsis`](#ellipsis)
    -   [`max_lines`](#max_lines)
    -   [`max_width`](#max_width)
    -   [`rotate`](#rotate)
    -   [`spans`](#spans)
    -   [`style`](#style)
    -   [`text`](#text)
    -   [`text_align`](#text_align)
    -   [`x`](#x-4)
    -   [`y`](#y-4)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoActivityIndicator | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinoactivityindicator/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoactivityindicator/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinoactivityindicator/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoactivityindicator/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   CupertinoActivityIndicator

On this page

# CupertinoActivityIndicator

An iOS-style activity indicator that spins clockwise.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/cupertinoactivityindicator)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page):    page.theme_mode = ft.ThemeMode.LIGHT    page.add(        ft.CupertinoActivityIndicator(            radius=50,            color=ft.Colors.RED,            animating=True,        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinoactivityindicator/img/docs/controls/cupertino-activity-indicator/basic-cupertino-activity-indicator.png)

## Properties[​](#properties "Direct link to Properties")

### `animating`[​](#animating "Direct link to animating")

Whether the activity indicator is running its animation.

### `color`[​](#color "Direct link to color")

Defines the [color](/docs/reference/colors) of the activity indicator.

### `radius`[​](#radius "Direct link to radius")

The radius of the activity indicator.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinoactivityindicator.md)

[

Previous

CircleAvatar

](/docs/controls/circleavatar)[

Next

Icon

](/docs/controls/icon)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`animating`](#animating)
    -   [`color`](#color)
    -   [`radius`](#radius)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Icon | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/icon/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/icon/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/icon/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/icon/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Icon

On this page

# Icon

Displays a Material icon.

[Icons browser](https://gallery.flet.dev/icons-browser/)

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/icon)

### Icons of different colors and sizes[​](#icons-of-different-colors-and-sizes "Direct link to Icons of different colors and sizes")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Row(            [                ft.Icon(name=ft.Icons.FAVORITE, color=ft.Colors.PINK),                ft.Icon(name=ft.Icons.AUDIOTRACK, color=ft.Colors.GREEN_400, size=30),                ft.Icon(name=ft.Icons.BEACH_ACCESS, color=ft.Colors.BLUE, size=50),                ft.Icon(name="settings", color="#c1c1c1"),            ]        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/icon/img/docs/controls/icon/custom-icons.png)

## Properties[​](#properties "Direct link to Properties")

### `color`[​](#color "Direct link to color")

Icon [color](/docs/reference/colors).

### `name`[​](#name "Direct link to name")

The name of the icon. You can search through the list of all available icons using open-source [Icons browser](https://gallery.flet.dev/icons-browser/) app [written in Flet](https://github.com/flet-dev/examples/blob/main/python/apps/icons-browser/main.py).

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

The semantics label for this icon. It is not shown to the in the UI, but is announced in accessibility modes (e.g TalkBack/VoiceOver).

### `size`[​](#size "Direct link to size")

The icon's size.

Defaults to `24`.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering a mouse over the Icon.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/icon.md)

[

Previous

CupertinoActivityIndicator

](/docs/controls/cupertinoactivityindicator)[

Next

Image

](/docs/controls/image)

-   [Examples](#examples)
    -   [Icons of different colors and sizes](#icons-of-different-colors-and-sizes)
-   [Properties](#properties)
    -   [`color`](#color)
    -   [`name`](#name)
    -   [`semantics_label`](#semantics_label)
    -   [`size`](#size)
    -   [`tooltip`](#tooltip)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Image | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/image/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/image/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/image/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/image/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Image

On this page

# Image

An image is a graphic representation of something (e.g photo or illustration).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/image)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Images Example"    page.theme_mode = ft.ThemeMode.LIGHT    page.padding = 50    page.update()    img = ft.Image(        src=f"/icons/icon-512.png",        width=100,        height=100,        fit=ft.ImageFit.CONTAIN,    )    images = ft.Row(expand=1, wrap=False, scroll="always")    page.add(img, images)    for i in range(0, 30):        images.controls.append(            ft.Image(                src=f"https://picsum.photos/200/200?{i}",                width=200,                height=200,                fit=ft.ImageFit.NONE,                repeat=ft.ImageRepeat.NO_REPEAT,                border_radius=ft.border_radius.all(10),            )        )    page.update()ft.app(main)
```

![](https://flet.dev/docs/controls/image/img/docs/controls/image/custom-images.gif)

## Properties[​](#properties "Direct link to Properties")

### `anti_alias`[​](#anti_alias "Direct link to anti_alias")

Whether to paint the image with anti-aliasing.

Anti-aliasing alleviates the sawtooth artifact when the image is rotated.

### `border_radius`[​](#border_radius "Direct link to border_radius")

Clip image to have rounded corners.

Value is of type [`BorderRadius`](/docs/reference/types/borderradius).

### `cache_width`[​](#cache_width "Direct link to cache_width")

The size at which the image should be decoded.

The image will, however, be rendered to the constraints of the layout regardless of this parameter.

### `cache_height`[​](#cache_height "Direct link to cache_height")

The size at which the image should be decoded.

The image will, however, be rendered to the constraints of the layout regardless of this parameter.

### `color`[​](#color "Direct link to color")

If set, this [color](/docs/reference/colors) is blended with each image pixel using `color_blend_mode`.

### `color_blend_mode`[​](#color_blend_mode "Direct link to color_blend_mode")

Used to combine `color` with the image. In terms of the blend mode, color is the source and this image is the destination.

Value is of type [`BlendMode`](/docs/reference/types/blendmode) and defaults to `BlendMode.COLOR`.

### `error_content`[​](#error_content "Direct link to error_content")

Fallback `Control` to display if the image cannot be loaded from the source.

### `exclude_from_semantics`[​](#exclude_from_semantics "Direct link to exclude_from_semantics")

Whether to exclude this image from semantics.

Defaults to `False`.

### `filter_quality`[​](#filter_quality "Direct link to filter_quality")

The rendering quality of the image.

Value is of type [`FilterQuality`](/docs/reference/types/filterquality) and defaults to `FilterQuality.MEDIUM`.

### `fit`[​](#fit "Direct link to fit")

How to inscribe the image into the space allocated during layout.

Value is of type [`ImageFit`](/docs/reference/types/imagefit) and defaults to `ImageFit.NONE`.

### `gapless_playback`[​](#gapless_playback "Direct link to gapless_playback")

Whether to continue showing the old image (`True`), or briefly show nothing (`False`), when the image provider changes.

Defaults to `False`.

### `height`[​](#height "Direct link to height")

If set, require the image to have this height.

If not set, the image will pick a size that best preserves its intrinsic aspect ratio.

note

It is strongly recommended that either both the width and the height be specified, or that the Image be placed in a context that sets tight layout constraints, so that the image does not change size as it loads. Consider using `fit` to adapt the image's rendering to fit the given width and height if the exact image dimensions are not known in advance.

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

A semantic description of the image. Used to provide a description of the image to TalkBack on Android, and VoiceOver on iOS.

### `src`[​](#src "Direct link to src")

The image source. This could be an external URL or a local [asset file](/docs/cookbook/assets).

### `src_base64`[​](#src_base64 "Direct link to src_base64")

Displays an image from Base-64 encoded string, for example:

```
import flet as ftdef main(page: ft.Page):    page.add(ft.Image(src_base64="iVBORw0KGgoAAAANSUhEUgAAABkAAAAgCAYAAADnnNMGAAAACXBIWXMAAAORAAADkQFnq8zdAAAAGXRFWHRTb2Z0d2FyZQB3d3cuaW5rc2NhcGUub3Jnm+48GgAAA6dJREFUSImllltoHFUYx3/fzOzm0lt23ZrQ1AQbtBehNpvQohgkBYVo410RwQctNE3Sh0IfiiBoIAjqi6TYrKnFy4O3oiiRavDJFi3mXomIBmOxNZe63ay52GR3Zj4f2sTEzmx3m//TYf7/c35zvgPnO6KqrESXqpq3muocAikv6m+/zytj3ejik1VN21G31YA9CgJ6xC+bMyQZPVCuarciPAMYC99V6Vw5pLbFSibHmlVoRVj9P3cmPBM8tSJI/M6mzabpfoAQ9fIF7WK4bd5vvuFnLGgy2vi0abg94A0AcJGvMq3hDxGRyar9r4F+iLAm0yIiRk8m37tctS1WsrIhhrI30+Srmg+J87OXUf3lWGS1q89dC6ltsSanxk4Aj2QBABii96300g87P/rtlrWr8l+vyDMfdlXSyyEikqxsiOUAQJCBhfHdXRfCq1LSsSlcWG+KBAGStvvrMkgiuv8lUc2mREukPwLUfHG+uTQv8Eown7VL3XlbBxYhf1c17hbVF3MDwA9bts280TnaU1YYqPby07aeFlUlHt27wSQ4CLo+F8AvoTCvHmyKF+ZbEb/M77P2LgvAwmrTHAHflN3KZxVbMC2jMFNOpgPnrMSOhvvFkMezXdwV4ePbtvHtxnJAMQ0j4JtVnO+eLb5oiSlt5HDbv7t1O90lpYCCCKbhfzW5kAIwUAazR0BlfII8Ow0I6uoVmI9MyAMwbMs8CExmDbk4zgu931MyO4OI4KrYflkRjOoTI+uM9d1vjotwKPu9QMk/sxzuO8POiVFcdZ1M2YBVsMEAKOqLvaPIe7mACuw0z/80SMH58SMplxlfiDhVi7dw2pltRhjKBQTQdrSja2KKTfE551NHuaZ0QVPvWYQUn31/Vm2nDvgjF4grVJx6suSvrvrSJ/6cSW2Oz9mf264uNrB806xZ1k/CZ49dUKgDEtlCROX2hfHpx8pGuuo3PpqYulw8fjndOp1yhgtNKRevJ1FyR2Ola+jXAjdnwTkZ6o896GdWdxDw7IxFg+0DpmXchTKSBWQnIuJn9u4j7dt+13UfHXEkXQOcuQ4kMhVtqsgUyPiQiPQfHw1NB2sRjmXKuTg1NwwBYLhtPtQX26eqTwGXPDOqvmcC4Hnwfrrad94GrVsOYTqUTkQY+iTlNe/6O1miSP/x0VB/+wMIDwHn/vtV1iQC4Xv95uUEWVCoL9Y5Z+gdovoyMHUFJHv88jmVy0vTuw7cZNv2YaA61Bfb7ZX5F8SaUv2xwZevAAAAAElFTkSuQmCC"))ft.app(main)
```

Use `base64` command (Linux, macOS, WSL) to convert file to Base64 format, for example:

```
base64 -i <image.png> -o <image-base64.txt>
```

On Windows you can use PowerShell to encode string into Base64 format:

```
[convert]::ToBase64String((Get-Content -path "your_file_path" -Encoding byte))
```

### `repeat`[​](#repeat "Direct link to repeat")

How to paint any portions of the layout bounds not covered by the image.

Values is of type [`ImageRepeat`](/docs/reference/types/imagerepeat) and defaults to `ImageRepeat.NO_REPEAT`.

### `semantics_label`[​](#semantics_label-1 "Direct link to semantics_label-1")

A semantics label for this image.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering a mouse over the Image.

### `width`[​](#width "Direct link to width")

If set, require the image to have this width.

If not set, the image will pick a size that best preserves its intrinsic aspect ratio.

note

It is strongly recommended that either both the width and the height be specified, or that the Image be placed in a context that sets tight layout constraints, so that the image does not change size as it loads. Consider using `fit` to adapt the image's rendering to fit the given width and height if the exact image dimensions are not known in advance.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/image.md)

[

Previous

Icon

](/docs/controls/icon)[

Next

Map

](/docs/controls/map)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`anti_alias`](#anti_alias)
    -   [`border_radius`](#border_radius)
    -   [`cache_width`](#cache_width)
    -   [`cache_height`](#cache_height)
    -   [`color`](#color)
    -   [`color_blend_mode`](#color_blend_mode)
    -   [`error_content`](#error_content)
    -   [`exclude_from_semantics`](#exclude_from_semantics)
    -   [`filter_quality`](#filter_quality)
    -   [`fit`](#fit)
    -   [`gapless_playback`](#gapless_playback)
    -   [`height`](#height)
    -   [`semantics_label`](#semantics_label)
    -   [`src`](#src)
    -   [`src_base64`](#src_base64)
    -   [`repeat`](#repeat)
    -   [`semantics_label`](#semantics_label-1)
    -   [`tooltip`](#tooltip)
    -   [`width`](#width)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Map | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/map/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/map/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/map/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/map/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Map

On this page

# Map

Used to display a map with various layers.

Packaging

To build your Flet app that uses `Map` control add `--include-packages flet_map` to `flet build` command, for example:

```
flet build apk --include-packages flet_map
```

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/map)

### Example[​](#example "Direct link to Example")

-   Python

```
import randomimport flet as ftimport flet.map as mapdef main(page: ft.Page):    marker_layer_ref = ft.Ref[map.MarkerLayer]()    circle_layer_ref = ft.Ref[map.CircleLayer]()    def handle_tap(e: map.MapTapEvent):        print(e)        if e.name == "tap":            marker_layer_ref.current.markers.append(                map.Marker(                    content=ft.Icon(                        ft.Icons.LOCATION_ON, color=ft.cupertino_colors.DESTRUCTIVE_RED                    ),                    coordinates=e.coordinates,                )            )        elif e.name == "secondary_tap":            circle_layer_ref.current.circles.append(                map.CircleMarker(                    radius=random.randint(5, 10),                    coordinates=e.coordinates,                    color=ft.Colors.random_color(),                    border_color=ft.Colors.random_color(),                    border_stroke_width=4,                )            )        page.update()    def handle_event(e: map.MapEvent):        print(e)    page.add(        ft.Text("Click anywhere to add a Marker, right-click to add a CircleMarker."),        map.Map(            expand=True,            initial_center=map.MapLatitudeLongitude(15, 10),            initial_zoom=4.2,            interaction_configuration=map.MapInteractionConfiguration(                flags=map.MapInteractiveFlag.ALL            ),            on_init=lambda e: print(f"Initialized Map"),            on_tap=handle_tap,            on_secondary_tap=handle_tap,            on_long_press=handle_tap,            on_event=lambda e: print(e),            layers=[                map.TileLayer(                    url_template="https://tile.openstreetmap.org/{z}/{x}/{y}.png",                    on_image_error=lambda e: print("TileLayer Error"),                ),                map.RichAttribution(                    attributions=[                        map.TextSourceAttribution(                            text="OpenStreetMap Contributors",                            on_click=lambda e: e.page.launch_url(                                "https://openstreetmap.org/copyright"                            ),                        ),                        map.TextSourceAttribution(                            text="Flet",                            on_click=lambda e: e.page.launch_url("https://flet.dev"),                        ),                    ]                ),                map.SimpleAttribution(                    text="Flet",                    alignment=ft.alignment.top_right,                    on_click=lambda e: print("Clicked SimpleAttribution"),                ),                map.MarkerLayer(                    ref=marker_layer_ref,                    markers=[                        map.Marker(                            content=ft.Icon(ft.Icons.LOCATION_ON),                            coordinates=map.MapLatitudeLongitude(30, 15),                        ),                        map.Marker(                            content=ft.Icon(ft.Icons.LOCATION_ON),                            coordinates=map.MapLatitudeLongitude(10, 10),                        ),                        map.Marker(                            content=ft.Icon(ft.Icons.LOCATION_ON),                            coordinates=map.MapLatitudeLongitude(25, 45),                        ),                    ],                ),                map.CircleLayer(                    ref=circle_layer_ref,                    circles=[                        map.CircleMarker(                            radius=10,                            coordinates=map.MapLatitudeLongitude(16, 24),                            color=ft.Colors.RED,                            border_color=ft.Colors.BLUE,                            border_stroke_width=4,                        ),                    ],                ),                map.PolygonLayer(                    polygons=[                        map.PolygonMarker(                            label="Popular Touristic Area",                            label_text_style=ft.TextStyle(                                color=ft.Colors.BLACK,                                size=15,                                weight=ft.FontWeight.BOLD,                            ),                            color=ft.Colors.with_opacity(0.3, ft.Colors.BLUE),                            coordinates=[                                map.MapLatitudeLongitude(10, 10),                                map.MapLatitudeLongitude(30, 15),                                map.MapLatitudeLongitude(25, 45),                            ],                        ),                    ],                ),                map.PolylineLayer(                    polylines=[                        map.PolylineMarker(                            border_stroke_width=3,                            border_color=ft.Colors.RED,                            gradient_colors=[ft.Colors.BLACK, ft.Colors.BLACK],                            color=ft.Colors.with_opacity(0.6, ft.Colors.GREEN),                            coordinates=[                                map.MapLatitudeLongitude(10, 10),                                map.MapLatitudeLongitude(30, 15),                                map.MapLatitudeLongitude(25, 45),                            ],                        ),                    ],                ),            ],        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/map/img/docs/controls/map/map-example.png)

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The background color.

### `initial_center`[​](#initial_center "Direct link to initial_center")

The initial center of the map.

Value is of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).

### `initial_rotation`[​](#initial_rotation "Direct link to initial_rotation")

The initial rotation value.

### `initial_zoom`[​](#initial_zoom "Direct link to initial_zoom")

The initial zoom level.

### `interaction_configuration`[​](#interaction_configuration "Direct link to interaction_configuration")

The interaction configuration.

Value is of type [`MapInteractionConfiguration`](/docs/reference/types/mapinteractionconfiguration).

### `keep_alive`[​](#keep_alive "Direct link to keep_alive")

A boolean value to keep the map alive.

### `max_zoom`[​](#max_zoom "Direct link to max_zoom")

The maximum zoom level.

### `min_zoom`[​](#min_zoom "Direct link to min_zoom")

The minimum zoom level.

### `layers`[​](#layers "Direct link to layers")

A list of layers to be displayed on the map.

Value is of type [`MapLayer`](/docs/reference/types/maplayer).

## Events[​](#events "Direct link to Events")

### `on_event`[​](#on_event "Direct link to on_event")

Fires when any map events occurs.

Event handler argument is of type [`MapEvent`](/docs/reference/types/mapevent).

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a hover event occurs.

Event handler argument is of type [`MapHoverEvent`](/docs/reference/types/maphoverevent).

### `on_init`[​](#on_init "Direct link to on_init")

Fires when the map is initialized.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when a long press event occurs.

Event handler argument is of type [`MapTapEvent`](/docs/reference/types/maptapevent).

### `on_position_change`[​](#on_position_change "Direct link to on_position_change")

Fires when the map position changes.

Event handler argument is of type [`MapPositionChangeEvent`](/docs/reference/types/mappositionchangeevent).

### `on_pointer_down`[​](#on_pointer_down "Direct link to on_pointer_down")

Fires when a pointer down event occurs.

Event handler argument is of type [`MapPointerEvent`](/docs/reference/types/mappointerevent).

### `on_pointer_cancel`[​](#on_pointer_cancel "Direct link to on_pointer_cancel")

Fires when a pointer cancel event occurs.

Event handler argument is of type [`MapPointerEvent`](/docs/reference/types/mappointerevent).

### `on_pointer_up`[​](#on_pointer_up "Direct link to on_pointer_up")

Fires when a pointer up event occurs.

Event handler argument is of type [`MapPointerEvent`](/docs/reference/types/mappointerevent).

### `on_secondary_tap`[​](#on_secondary_tap "Direct link to on_secondary_tap")

Fires when a secondary tap event occurs.

Event handler argument is of type [`MapTapEvent`](/docs/reference/types/maptapevent).

### `on_tap`[​](#on_tap "Direct link to on_tap")

Fires when a tap event occurs.

Event handler argument is of type [`MapTapEvent`](/docs/reference/types/maptapevent).

## Methods[​](#methods "Direct link to Methods")

### `rotate_from`[​](#rotate_from "Direct link to rotate_from")

Apply a rotation of `degree` to the current rotation.

It has the following arguments:

-   `animation_curve`: The curve of the zoom animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `degree`: The degree to rotate.

### `reset_rotation`[​](#reset_rotation "Direct link to reset_rotation")

Reset the rotation to 0 degrees.

It has the following arguments:

-   `animation_curve`: The curve of the zoom animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `animation_duration`: The duration of the zoom animation. Value is of type [`DurationValue`](/docs/reference/types/aliases#durationvalue) and defaults to `Map.animation_duration`.

### `zoom_in`[​](#zoom_in "Direct link to zoom_in")

Add one level to the current zoom level.

It has the following arguments:

-   `animation_curve`: The curve of the zoom animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `animation_duration`: The duration of the zoom animation. Value is of type [`DurationValue`](/docs/reference/types/aliases#durationvalue) and defaults to `Map.animation_duration`.

### `zoom_out`[​](#zoom_out "Direct link to zoom_out")

Subtract one level from the current zoom level.

It has the following arguments:

-   `animation_curve`: The curve of the zoom animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `animation_duration`: The duration of the zoom animation. Value is of type [`DurationValue`](/docs/reference/types/aliases#durationvalue) and defaults to `Map.animation_duration`.

### `zoom_to`[​](#zoom_to "Direct link to zoom_to")

Zoom to a specific level.

It has the following arguments:

-   `animation_curve`: The curve of the zoom animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `animation_duration`: The duration of the zoom animation. Value is of type [`DurationValue`](/docs/reference/types/aliases#durationvalue) and defaults to `Map.animation_duration`.
-   `zoom`: The zoom level to zoom to.

### `move_to`[​](#move_to "Direct link to move_to")

Move to a specific location.

It has the following arguments:

-   `animation_curve`: The curve of the move animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `animation_duration`: The duration of the move animation. Value is of type [`DurationValue`](/docs/reference/types/aliases#durationvalue) and defaults to `Map.animation_duration`.
-   `destination`: The destination point to move to. Value is of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).
-   `zoom`: The zoom level to move to.
-   `offset`: The offset to move to. Value is of type [`OffsetValue`](/docs/reference/types/aliases#offsetvalue).
-   `rotation`: The rotation to move to.

### `center_on`[​](#center_on "Direct link to center_on")

Center the map on a specific location.

It has the following arguments:

-   `animation_curve`: The curve of the move animation. Value is of type [`AnimationCurve`](/docs/reference/types/animationcurve) and defaults to `Map.animation_curve`.
-   `animation_duration`: The duration of the move animation. Value is of type [`DurationValue`](/docs/reference/types/aliases#durationvalue) and defaults to `Map.animation_duration`.
-   `point`: The point to center on. Value is of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).
-   `zoom`: The zoom level to move to.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/map.md)

[

Previous

Image

](/docs/controls/image)[

Next

CircleLayer

](/docs/controls/mapcirclelayer)

-   [Examples](#examples)
    -   [Example](#example)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`initial_center`](#initial_center)
    -   [`initial_rotation`](#initial_rotation)
    -   [`initial_zoom`](#initial_zoom)
    -   [`interaction_configuration`](#interaction_configuration)
    -   [`keep_alive`](#keep_alive)
    -   [`max_zoom`](#max_zoom)
    -   [`min_zoom`](#min_zoom)
    -   [`layers`](#layers)
-   [Events](#events)
    -   [`on_event`](#on_event)
    -   [`on_hover`](#on_hover)
    -   [`on_init`](#on_init)
    -   [`on_long_press`](#on_long_press)
    -   [`on_position_change`](#on_position_change)
    -   [`on_pointer_down`](#on_pointer_down)
    -   [`on_pointer_cancel`](#on_pointer_cancel)
    -   [`on_pointer_up`](#on_pointer_up)
    -   [`on_secondary_tap`](#on_secondary_tap)
    -   [`on_tap`](#on_tap)
-   [Methods](#methods)
    -   [`rotate_from`](#rotate_from)
    -   [`reset_rotation`](#reset_rotation)
    -   [`zoom_in`](#zoom_in)
    -   [`zoom_out`](#zoom_out)
    -   [`zoom_to`](#zoom_to)
    -   [`move_to`](#move_to)
    -   [`center_on`](#center_on)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CircleLayer | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/mapcirclelayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mapcirclelayer/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/mapcirclelayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mapcirclelayer/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   CircleLayer

On this page

# CircleLayer

A layer to display [`CircleMarker`](#circlemarker-properties)s.

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## `CircleLayer` Properties[​](#circlelayer-properties "Direct link to circlelayer-properties")

### `circles`[​](#circles "Direct link to circles")

A list of [`CircleMarker`](#circlemarker-properties)s to be displayed.

## `CircleMarker` Properties[​](#circlemarker-properties "Direct link to circlemarker-properties")

A circular marker displayed on the [`Map`](/docs/controls/map) through the [`CircleLayer`](/docs/controls/mapcirclelayer) at `coordinates`.

### `border_color`[​](#border_color "Direct link to border_color")

The border color of the circle border line. Requires `border_stroke_width > 0` inorder to be visible.

### `border_stroke_width`[​](#border_stroke_width "Direct link to border_stroke_width")

The border stroke width of the circle border.

Defaults to `0` - no border.

### `color`[​](#color "Direct link to color")

The [color](/docs/reference/colors) of the circle area.

### `coordinates`[​](#coordinates "Direct link to coordinates")

The center coordinates of the marker.

Value is of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).

### `radius`[​](#radius "Direct link to radius")

The radius of the circle.

### `use_radius_in_meter`[​](#use_radius_in_meter "Direct link to use_radius_in_meter")

A boolean value to indicate if the radius is in meters or pixels.

Defaults to `False` - pixels.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/mapcirclelayer.md)

[

Previous

Map

](/docs/controls/map)[

Next

MarkerLayer

](/docs/controls/mapmarkerlayer)

-   [Examples](#examples)
-   [`CircleLayer` Properties](#circlelayer-properties)
    -   [`circles`](#circles)
-   [`CircleMarker` Properties](#circlemarker-properties)
    -   [`border_color`](#border_color)
    -   [`border_stroke_width`](#border_stroke_width)
    -   [`color`](#color)
    -   [`coordinates`](#coordinates)
    -   [`radius`](#radius)
    -   [`use_radius_in_meter`](#use_radius_in_meter)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  MarkerLayer | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/mapmarkerlayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mapmarkerlayer/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/mapmarkerlayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mapmarkerlayer/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   MarkerLayer

On this page

# MarkerLayer

A layer to display `Marker`s.

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## `MarkerLayer` Properties[​](#markerlayer-properties "Direct link to markerlayer-properties")

### `alignment`[​](#alignment "Direct link to alignment")

Alignment of each marker relative to its normal center at `Marker.coordinates`.

Values is of type [`Alignment`](/docs/reference/types/alignment) and defaults to `ft.alignment.center`.

### `markers`[​](#markers "Direct link to markers")

A list of [`Marker`](#marker-properties)s to be displayed.

### `rotate`[​](#rotate "Direct link to rotate")

Whether to counter rotate markers to the map's rotation, to keep a fixed orientation.

## `Marker` Properties[​](#marker-properties "Direct link to marker-properties")

A container for a `content` control located at a geographic coordinate `coordinates`.

### `alignment`[​](#alignment-1 "Direct link to alignment-1")

Alignment of the marker relative to the normal center at `coordinates`.

Values is of type [`Alignment`](/docs/reference/types/alignment) and defaults to `alignment.center` if also unset by the parent `MarkerLayer`.

### `content`[​](#content "Direct link to content")

The content to be displayed at `coordinates`.

### `coordinates`[​](#coordinates "Direct link to coordinates")

The coordinates of the marker. This will be the center of the marker, if `alignment=ft.alignment.center`.

Value is of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).

### `height`[​](#height "Direct link to height")

The height of the `content` Control.

### `rotation`[​](#rotation "Direct link to rotation")

Whether to counter rotate this marker to the map's rotation, to keep a fixed orientation.

When `True`, this marker will always appear upright and vertical from the user's perspective.

Defaults to `False` if also unset by the parent `MarkerLayer`.

Note: this is not used to apply a custom rotation in degrees to the marker.

### `width`[​](#width "Direct link to width")

The width of the `content` Control.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/mapmarkerlayer.md)

[

Previous

CircleLayer

](/docs/controls/mapcirclelayer)[

Next

PolygonLayer

](/docs/controls/mappolygonlayer)

-   [Examples](#examples)
-   [`MarkerLayer` Properties](#markerlayer-properties)
    -   [`alignment`](#alignment)
    -   [`markers`](#markers)
    -   [`rotate`](#rotate)
-   [`Marker` Properties](#marker-properties)
    -   [`alignment`](#alignment-1)
    -   [`content`](#content)
    -   [`coordinates`](#coordinates)
    -   [`height`](#height)
    -   [`rotation`](#rotation)
    -   [`width`](#width)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  RichAttribution | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/maprichattribution/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/maprichattribution/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/maprichattribution/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/maprichattribution/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   RichAttribution

On this page

# RichAttribution

An animated and interactive attribution layer that supports both logos/images and text (displayed in a popup controlled by an icon button adjacent to the logos).

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## Properties[​](#properties "Direct link to Properties")

### `alignment`[​](#alignment "Direct link to alignment")

The alignment of the attribution.

Value is of type [`AttributionAlignment`](/docs/reference/types/attributionalignment).

### `attributions`[​](#attributions "Direct link to attributions")

A list of text source attributions.

Value is a list with items of type [`TextSourceAttribution`](/docs/controls/maptextsourceattribution).

### `permanent_height`[​](#permanent_height "Direct link to permanent_height")

The permanent height of the attribution layer.

Defaults to `24.0`.

### `popup_bgcolor`[​](#popup_bgcolor "Direct link to popup_bgcolor")

The background [color](/docs/reference/colors) of the popup box.

### `show_flutter_map_attribution`[​](#show_flutter_map_attribution "Direct link to show_flutter_map_attribution")

A boolean value indicating whether to show the Flutter map attribution.

Defaults to `True`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/maprichattribution.md)

[

Previous

PolylineLayer

](/docs/controls/mappolylinelayer)[

Next

SimpleAttribution

](/docs/controls/mapsimpleattribution)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`attributions`](#attributions)
    -   [`permanent_height`](#permanent_height)
    -   [`popup_bgcolor`](#popup_bgcolor)
    -   [`show_flutter_map_attribution`](#show_flutter_map_attribution)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  SimpleAttribution | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/mapsimpleattribution/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mapsimpleattribution/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/mapsimpleattribution/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mapsimpleattribution/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   SimpleAttribution

On this page

# SimpleAttribution

A simple attribution layer displayed on the [`Map`](/docs/controls/map).

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## Properties[​](#properties "Direct link to Properties")

### `alignment`[​](#alignment "Direct link to alignment")

The alignment of the attribution.

Value is of type [`Alignment`](/docs/reference/types/alignment) and defaults to `alignment.bottom_right`.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Color of the box containing the source text.

Defaults to the background color of the app Theme.

### `text`[​](#text "Direct link to text")

Attribution text, such as `"OpenStreetMap contributors"`.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when the `text` is clicked.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/mapsimpleattribution.md)

[

Previous

RichAttribution

](/docs/controls/maprichattribution)[

Next

TileLayer

](/docs/controls/maptilelayer)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`bgcolor`](#bgcolor)
    -   [`text`](#text)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  TileLayer | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/maptilelayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/maptilelayer/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/maptilelayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/maptilelayer/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   TileLayer

On this page

# TileLayer

The main layer of the map, displaying square raster images in a continuous grid.

## Examples[​](#examples "Direct link to Examples")

See [Map Control](/docs/controls/map).

## `TileLayer` Properties[​](#tilelayer-properties "Direct link to tilelayer-properties")

### `additional_options`[​](#additional_options "Direct link to additional_options")

A dictionary containing static information that should replace placeholders in the `url_template`. Applying API keys is a good example.

### `enable_retina_mode`[​](#enable_retina_mode "Direct link to enable_retina_mode")

A boolean indicating whether to enable retina mode.

### `enable_tms`[​](#enable_tms "Direct link to enable_tms")

Whether to enable [TMS](https://en.wikipedia.org/wiki/Tile_Map_Service)(Tile Map Service).

### `error_image_src`[​](#error_image_src "Direct link to error_image_src")

The source for an error image. Can be a URL or path to an image asset file.

### `evict_error_tile_strategy`[​](#evict_error_tile_strategy "Direct link to evict_error_tile_strategy")

The strategy for evicting error tiles. If a Tile was loaded with error and strategy isn't `None`, it will be evicted based on specified strategy.

### `fallback_url`[​](#fallback_url "Direct link to fallback_url")

A fallback URL to use if an error occurs when fetching tiles from the `url_template`.

### `keep_alive`[​](#keep_alive "Direct link to keep_alive")

A boolean indicating whether to keep the map alive.

### `keep_buffer`[​](#keep_buffer "Direct link to keep_buffer")

The number of rows and columns of tiles to keep (when panning the map) before unloading.

### `max_native_zoom`[​](#max_native_zoom "Direct link to max_native_zoom")

The maximum native zoom level.

### `max_zoom`[​](#max_zoom "Direct link to max_zoom")

The maximum zoom level.

### `min_native_zoom`[​](#min_native_zoom "Direct link to min_native_zoom")

The minimum native zoom level.

### `min_zoom`[​](#min_zoom "Direct link to min_zoom")

The minimum zoom level.

### `pan_buffer`[​](#pan_buffer "Direct link to pan_buffer")

When loading tiles only visible tiles are loaded by default. This option increases the loaded tiles by the given number on both axis which can help prevent the user from seeing loading tiles whilst panning.

Setting the pan buffer too high can impact performance, typically this is set to `0` or `1`.

### `subdomains`[​](#subdomains "Direct link to subdomains")

A list of subdomains for the tile server.

### `tile_bounds`[​](#tile_bounds "Direct link to tile_bounds")

The geographical bounds for the tiles. Meaning only tiles inside this bounds will be loaded.

Value is of type [`MapLatitudeLongitudeBounds`](/docs/reference/types/maplatitudelongitudebounds).

### `tile_size`[​](#tile_size "Direct link to tile_size")

The size of each tile.

Defaults to `256`.

### `url_template`[​](#url_template "Direct link to url_template")

The template URL for retrieving tile images. This is a string that contains placeholders, which, when filled in, create a URL/URI to a specific tile.

### `zoom_offset`[​](#zoom_offset "Direct link to zoom_offset")

The zoom number used in tile URLs will be offset with this value.

### `zoom_reverse`[​](#zoom_reverse "Direct link to zoom_reverse")

Whether to reverse the zoom number used in the tile URLs.

## Events[​](#events "Direct link to Events")

### `on_image_error`[​](#on_image_error "Direct link to on_image_error")

Event handler for image error events.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/maptilelayer.md)

[

Previous

SimpleAttribution

](/docs/controls/mapsimpleattribution)[

Next

TextSourceAttribution

](/docs/controls/maptextsourceattribution)

-   [Examples](#examples)
-   [`TileLayer` Properties](#tilelayer-properties)
    -   [`additional_options`](#additional_options)
    -   [`enable_retina_mode`](#enable_retina_mode)
    -   [`enable_tms`](#enable_tms)
    -   [`error_image_src`](#error_image_src)
    -   [`evict_error_tile_strategy`](#evict_error_tile_strategy)
    -   [`fallback_url`](#fallback_url)
    -   [`keep_alive`](#keep_alive)
    -   [`keep_buffer`](#keep_buffer)
    -   [`max_native_zoom`](#max_native_zoom)
    -   [`max_zoom`](#max_zoom)
    -   [`min_native_zoom`](#min_native_zoom)
    -   [`min_zoom`](#min_zoom)
    -   [`pan_buffer`](#pan_buffer)
    -   [`subdomains`](#subdomains)
    -   [`tile_bounds`](#tile_bounds)
    -   [`tile_size`](#tile_size)
    -   [`url_template`](#url_template)
    -   [`zoom_offset`](#zoom_offset)
    -   [`zoom_reverse`](#zoom_reverse)
-   [Events](#events)
    -   [`on_image_error`](#on_image_error)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoSegmentedButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinosegmentedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinosegmentedbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinosegmentedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinosegmentedbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoSegmentedButton

On this page

# CupertinoSegmentedButton

An iOS-style segmented button.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinosegmentedbutton)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page):    page.theme_mode = ft.ThemeMode.LIGHT    page.add(        ft.CupertinoSegmentedButton(            selected_index=1,            selected_color=ft.Colors.RED_400,            on_change=lambda e: print(f"selected_index: {e.data}"),            controls=[                ft.Text("One"),                ft.Container(                    padding=ft.padding.symmetric(0, 30),                    content=ft.Text("Two"),                ),                ft.Container(                    padding=ft.padding.symmetric(0, 10),                    content=ft.Text("Three"),                ),            ],        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinosegmentedbutton/img/docs/controls/cupertino-segmented-button/basic-cupertino-segmented-button.gif)

## Properties[​](#properties "Direct link to Properties")

### `border_color`[​](#border_color "Direct link to border_color")

The [color](/docs/reference/colors) of the button's border.

### `click_color`[​](#click_color "Direct link to click_color")

The [color](/docs/reference/colors) used to fill the background of this control when temporarily interacting with through a long press or drag.

Defaults to the `selected_color` with 20% opacity.

### `controls`[​](#controls "Direct link to controls")

A list of `Control`s to display as segments inside the CupertinoSegmentedButton.

### `padding`[​](#padding "Direct link to padding")

The button's padding. Padding value is an instance of [`Padding`](/docs/reference/types/padding) class.

### `selected_color`[​](#selected_color "Direct link to selected_color")

The [color](/docs/reference/colors) of the button when it is selected.

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index (starting from 0) of the selected segment in the `controls` list.

### `text`[​](#text "Direct link to text")

The text to be shown in the button. In case both `text` and `content` are provided, then `content` will be used.

### `trailing_icon`[​](#trailing_icon "Direct link to trailing_icon")

An optional icon to display at the right of the `text` or `content` control.

### `unselected_color`[​](#unselected_color "Direct link to unselected_color")

The [color](/docs/reference/colors) of the button when it is not selected.

## Events[​](#events "Direct link to Events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when the state of the button is changed - when one of the `controls` is clicked.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinosegmentedbutton.md)

[

Previous

CupertinoFilledButton

](/docs/controls/cupertinofilledbutton)[

Next

CupertinoSlidingSegmentedButton

](/docs/controls/cupertinoslidingsegmentedbutton)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`border_color`](#border_color)
    -   [`click_color`](#click_color)
    -   [`controls`](#controls)
    -   [`padding`](#padding)
    -   [`selected_color`](#selected_color)
    -   [`selected_index`](#selected_index)
    -   [`text`](#text)
    -   [`trailing_icon`](#trailing_icon)
    -   [`unselected_color`](#unselected_color)
-   [Events](#events)
    -   [`on_change`](#on_change)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoSlidingSegmentedButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinoslidingsegmentedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoslidingsegmentedbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinoslidingsegmentedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoslidingsegmentedbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoSlidingSegmentedButton

On this page

# CupertinoSlidingSegmentedButton

An iOS-13 style segmented control.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinoslidingsegmentedbutton)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page):    page.theme_mode = ft.ThemeMode.LIGHT    page.add(        ft.CupertinoSlidingSegmentedButton(            selected_index=1,            thumb_color=ft.Colors.BLUE_400,            on_change=lambda e: print(f"selected_index: {e.data}"),            padding=ft.padding.symmetric(0, 10),            controls=[                ft.Text("One"),                ft.Text("Two"),                ft.Text("Three"),            ],        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinoslidingsegmentedbutton/img/docs/controls/cupertino-sliding-segmented-button/basic-cupertino-sliding-segmented-button.gif)

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The background [color](/docs/reference/colors) of the button.

### `controls`[​](#controls "Direct link to controls")

A list of `Control`s to display as segments inside the CupertinoSegmentedButton. Must have at least 2 items.

### `padding`[​](#padding "Direct link to padding")

The button's padding. Padding value is an instance of [`Padding`](/docs/reference/types/padding) class.

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index (starting from 0) of the selected segment in the `controls` list.

### `thumb_color`[​](#thumb_color "Direct link to thumb_color")

The [color](/docs/reference/colors) of the button when it is not selected.

## Events[​](#events "Direct link to Events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when the state of the button is changed - when one of the `controls` is clicked.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinoslidingsegmentedbutton.md)

[

Previous

CupertinoSegmentedButton

](/docs/controls/cupertinosegmentedbutton)[

Next

ElevatedButton

](/docs/controls/elevatedbutton)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`controls`](#controls)
    -   [`padding`](#padding)
    -   [`selected_index`](#selected_index)
    -   [`thumb_color`](#thumb_color)
-   [Events](#events)
    -   [`on_change`](#on_change)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ElevatedButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/elevatedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/elevatedbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/elevatedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/elevatedbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   ElevatedButton

On this page

# ElevatedButton

Elevated buttons are essentially filled tonal buttons with a shadow. To prevent shadow creep, only use them when absolutely necessary, such as when the button requires visual separation from a patterned background. See [Material 3 buttons](https://m3.material.io/components/buttons/overview) for more info.

`ElevatedButton` has alias `Button` that can be used interchangebly.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/elevatedbutton)

### Basic elevated buttons[​](#basic-elevated-buttons "Direct link to Basic elevated buttons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Basic elevated buttons"    page.add(        ft.ElevatedButton(text="Elevated button"),        ft.Button("Disabled button", disabled=True),    )ft.app(main)
```

![](https://flet.dev/docs/controls/elevatedbutton/img/docs/controls/elevated-button/basic-elevated-buttons.png)

### Elevated buttons with icons[​](#elevated-buttons-with-icons "Direct link to Elevated buttons with icons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Elevated buttons with icons"    page.add(        ft.ElevatedButton("Button with icon", icon="chair_outlined"),        ft.ElevatedButton(            "Button with colorful icon",            icon="park_rounded",            icon_color="green400",        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/elevatedbutton/img/docs/controls/elevated-button/elevated-buttons-with-icons.png)

### Elevated button with `click` event[​](#elevated-button-with-click-event "Direct link to elevated-button-with-click-event")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Elevated button with 'click' event"    def button_clicked(e):        b.data += 1        t.value = f"Button clicked {b.data} time(s)"        page.update()    b = ft.ElevatedButton("Button with 'click' event", on_click=button_clicked, data=0)    t = ft.Text()    page.add(b, t)ft.app(main)
```

![](https://flet.dev/docs/controls/elevatedbutton/img/docs/controls/elevated-button/elevated-button-with-click-event.gif)

### Elevated button with custom content[​](#elevated-button-with-custom-content "Direct link to Elevated button with custom content")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Elevated buttons with custom content"    page.add(        ft.ElevatedButton(            width=150,            content=ft.Row(                [                    ft.Icon(name=ft.Icons.FAVORITE, color="pink"),                    ft.Icon(name=ft.Icons.AUDIOTRACK, color="green"),                    ft.Icon(name=ft.Icons.BEACH_ACCESS, color="blue"),                ],                alignment=ft.MainAxisAlignment.SPACE_AROUND,            ),        ),        ft.ElevatedButton(            content=ft.Container(                content=ft.Column(                    [                        ft.Text(value="Compound button", size=20),                        ft.Text(value="This is secondary text"),                    ],                    alignment=ft.MainAxisAlignment.CENTER,                    spacing=5,                ),                padding=ft.padding.all(10),            ),        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/elevatedbutton/img/docs/controls/elevated-button/elevated-buttons-with-custom-content.png)

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive button is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoButton`](/docs/controls/cupertinobutton) is created, which matches the functionality and presentation of this button. On other platforms, a Material `ElevatedButton` is created.

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Button's background [color](/docs/reference/colors). If both `bgcolor` and `style.bgcolor` are provided, `bgcolor` value will be used.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `color`[​](#color "Direct link to color")

Button's text [color](/docs/reference/colors). If both `color` and `style.color` are provided, `color` value will be used.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `elevation`[​](#elevation "Direct link to elevation")

Button's elevation. If both `elevation` and `style.elevation` are provided, `elevation` value will be used.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `style`[​](#style "Direct link to style")

The value is an instance of [`ButtonStyle`](/docs/reference/types/buttonstyle) class.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Methods[​](#methods "Direct link to Methods")

### `focus()`[​](#focus "Direct link to focus")

Moves focus to a button.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a mouse pointer enters or exists the button response area. `data` property of event object contains `true` (string) when cursor enters and `false` when it exits.

```
import flet as ftdef main(page: ft.Page):    def on_hover(e):        e.control.bgcolor = "orange" if e.data == "true" else "yellow"        e.control.update()    page.add(        ft.ElevatedButton(            "I'm changing color on hover", bgcolor="yellow", on_hover=on_hover        )    )ft.app(main)
```

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the button is long-pressed.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/elevatedbutton.md)

[

Previous

CupertinoSlidingSegmentedButton

](/docs/controls/cupertinoslidingsegmentedbutton)[

Next

FilledButton

](/docs/controls/filledbutton)

-   [Examples](#examples)
    -   [Basic elevated buttons](#basic-elevated-buttons)
    -   [Elevated buttons with icons](#elevated-buttons-with-icons)
    -   [Elevated button with `click` event](#elevated-button-with-click-event)
    -   [Elevated button with custom content](#elevated-button-with-custom-content)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`bgcolor`](#bgcolor)
    -   [`clip_behavior`](#clip_behavior)
    -   [`color`](#color)
    -   [`content`](#content)
    -   [`elevation`](#elevation)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`style`](#style)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Methods](#methods)
    -   [`focus()`](#focus)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)
    -   [`on_hover`](#on_hover)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  FloatingActionButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/floatingactionbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/floatingactionbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/floatingactionbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/floatingactionbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   FloatingActionButton

On this page

# FloatingActionButton

A material design floating action button. A floating action button is a circular icon button that hovers over content to promote a primary action in the application. Floating action button is usually set to `page.floating_action_button`, but can also be added as a regular control at any place on a page.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/floatingactionbutton)

### Basic FAB[​](#basic-fab "Direct link to Basic FAB")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Floating Action Button"    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.auto_scroll = True    page.scroll = ft.ScrollMode.HIDDEN    page.appbar = ft.AppBar(        title=ft.Text("Floating Action Button", weight=ft.FontWeight.BOLD, color=ft.Colors.BLACK87),        actions=[ft.IconButton(ft.Icons.MENU, tooltip="Menu", icon_color=ft.Colors.BLACK87)],        bgcolor=ft.Colors.BLUE,        center_title=True,        color=ft.Colors.WHITE,    )    # keeps track of the number of tiles already added    count = 0    def fab_pressed(e):        nonlocal count  # to modify the count variable found in the outer scope        page.add(            ft.ListTile(                title=ft.Text(f"Tile {count}"),                on_click=lambda x: print(x.control.title.value + " was clicked!"),            )        )        page.open(ft.SnackBar(ft.Text("Tile was added successfully!")))        count += 1    page.floating_action_button = ft.FloatingActionButton(icon=ft.Icons.ADD, on_click=fab_pressed, bgcolor=ft.Colors.LIME_300)    page.add(ft.Text("Press the FAB to add a tile!"))ft.app(main)
```

![](https://flet.dev/docs/controls/floatingactionbutton/img/docs/controls/floatingactionbutton/custom-fab.gif)

## Properties[​](#properties "Direct link to Properties")

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Button background [color](/docs/reference/colors).

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `disabled_elevation`[​](#disabled_elevation "Direct link to disabled_elevation")

The button's elevation when disabled.

Defaults to the same value as `elevation`.

### `elevation`[​](#elevation "Direct link to elevation")

The button's elevation.

Defaults to `6`.

### `enable_feedback`[​](#enable_feedback "Direct link to enable_feedback")

Whether detected gestures should provide acoustic and/or haptic feedback. On Android, for example, setting this to `True` will produce a click sound and a long-press will produce a short vibration.

Defaults to `True`.

### `focus_color`[​](#focus_color "Direct link to focus_color")

The [color](/docs/reference/colors) to use for filling the button when the button has input focus.

### `focus_elevation`[​](#focus_elevation "Direct link to focus_elevation")

The button's elevation when it has input focus.

Defaults to `8`.

### `foreground_color`[​](#foreground_color "Direct link to foreground_color")

The default foreground [color](/docs/reference/colors) for icons and text within the button.

### `highlight_elevation`[​](#highlight_elevation "Direct link to highlight_elevation")

The button's elevation when being touched.

Defaults to `12`.

### `hover_elevation`[​](#hover_elevation "Direct link to hover_elevation")

The button's elevation when it is enabled and being hovered.

Defaults to `8`.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `mini`[​](#mini "Direct link to mini")

Controls the size of this button.

By default, floating action buttons are non-mini and have a height and width of `56.0` logical pixels. Mini floating action buttons have a height and width of `40.0` logical pixels with a layout width and height of `48.0` logical pixels.

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor to be displayed when a mouse pointer enters or is hovering over this control.

Value is of type [`MouseCursor`](/docs/reference/types/mousecursor).

### `shape`[​](#shape "Direct link to shape")

The shape of the FAB's border.

The value is an instance of [`OutlinedBorder`](/docs/reference/types/outlinedborder) class.

### `splash_color`[​](#splash_color "Direct link to splash_color")

The [color](/docs/reference/colors) of the ripple shown when this button is pressed/clicked.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/floatingactionbutton.md)

[

Previous

FilledTonalButton

](/docs/controls/filledtonalbutton)[

Next

IconButton

](/docs/controls/iconbutton)

-   [Examples](#examples)
    -   [Basic FAB](#basic-fab)
-   [Properties](#properties)
    -   [`autofocus`](#autofocus)
    -   [`bgcolor`](#bgcolor)
    -   [`clip_behavior`](#clip_behavior)
    -   [`content`](#content)
    -   [`disabled_elevation`](#disabled_elevation)
    -   [`elevation`](#elevation)
    -   [`enable_feedback`](#enable_feedback)
    -   [`focus_color`](#focus_color)
    -   [`focus_elevation`](#focus_elevation)
    -   [`foreground_color`](#foreground_color)
    -   [`highlight_elevation`](#highlight_elevation)
    -   [`hover_elevation`](#hover_elevation)
    -   [`icon`](#icon)
    -   [`mini`](#mini)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`shape`](#shape)
    -   [`splash_color`](#splash_color)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  IconButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/iconbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/iconbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/iconbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/iconbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   IconButton

On this page

# IconButton

An icon button is a round button with an icon in the middle that reacts to touches by filling with color (ink).

Icon buttons are commonly used in the toolbars, but they can be used in many other places as well.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/iconbutton)

### Icon buttons[​](#icon-buttons "Direct link to Icon buttons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Icon buttons"    page.add(        ft.Row(            [                ft.IconButton(                    icon=ft.Icons.PAUSE_CIRCLE_FILLED_ROUNDED,                    icon_color="blue400",                    icon_size=20,                    tooltip="Pause record",                ),                ft.IconButton(                    icon=ft.Icons.DELETE_FOREVER_ROUNDED,                    icon_color="pink600",                    icon_size=40,                    tooltip="Delete record",                ),            ]        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/iconbutton/img/docs/controls/icon-button/icon-buttons.gif)

### Icon button with `click` event[​](#icon-button-with-click-event "Direct link to icon-button-with-click-event")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Icon button with 'click' event"    def button_clicked(e):        b.data += 1        t.value = f"Button clicked {b.data} time(s)"        page.update()    b = ft.IconButton(        icon=ft.Icons.PLAY_CIRCLE_FILL_OUTLINED, on_click=button_clicked, data=0    )    t = ft.Text()    page.add(b, t)ft.app(main)
```

![](https://flet.dev/docs/controls/iconbutton/img/docs/controls/icon-button/icon-button-with-click-event.gif)

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive button is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoButton`](/docs/controls/cupertinobutton) is created, which matches the functionality and presentation of this button. On other platforms, a Material `IconButton` is created.

Defaults to `False`.

### `alignment`[​](#alignment "Direct link to alignment")

Defines how the icon is positioned within the IconButton. Alignment is an instance of [`Alignment`](/docs/reference/types/alignment) class.

Defaults to `alignment.center`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `disabled_color`[​](#disabled_color "Direct link to disabled_color")

The [color](/docs/reference/colors) to use for the icon inside the button when disabled.

### `enable_feedback`[​](#enable_feedback "Direct link to enable_feedback")

Whether detected gestures should provide acoustic and/or haptic feedback. On Android, for example, setting this to `True` produce a click sound and a long-press will produce a short vibration.

Defaults to `True`.

### `focus_color`[​](#focus_color "Direct link to focus_color")

The button's [color](/docs/reference/colors) when in focus.

### `highlight_color`[​](#highlight_color "Direct link to highlight_color")

The button's [color](/docs/reference/colors) when the button is pressed. The highlight fades in quickly as the button is held down.

### `hover_color`[​](#hover_color "Direct link to hover_color")

The button's [color](/docs/reference/colors) when hovered.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `icon_size`[​](#icon_size "Direct link to icon_size")

Icon size in virtual pixels.

Defaults to `24`.

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor to be displayed when a mouse pointer enters or is hovering over this control.

Value is of type [`MouseCursor`](/docs/reference/types/mousecursor).

### `padding`[​](#padding "Direct link to padding")

Defines the padding around this button. The entire padded icon will react to input gestures.

Value is of type [`Padding`](/docs/reference/types/padding) and defaults to `padding.all(8)`.

### `selected`[​](#selected "Direct link to selected")

Turns icon button to a toggle button: `True` - the button is in selected state, `False` - in normal.

### `selected_icon`[​](#selected_icon "Direct link to selected_icon")

Icon shown in the button in selected state.

### `selected_icon_color`[​](#selected_icon_color "Direct link to selected_icon_color")

Icon [color](/docs/reference/colors) for the selected state.

An example of icon toggle button:

![](https://flet.dev/docs/controls/iconbutton/img/blog/gradients/toggle-icon-button.gif)

```
import flet as ftdef main(page: ft.Page):    def toggle_icon_button(e):        e.control.selected = not e.control.selected        e.control.update()    page.add(        ft.IconButton(            icon=ft.Icons.BATTERY_1_BAR,            selected_icon=ft.Icons.BATTERY_FULL,            on_click=toggle_icon_button,            selected=False,            style=ft.ButtonStyle(color={"selected": ft.Colors.GREEN, "": ft.Colors.RED}),        )    )ft.app(main)
```

### `splash_color`[​](#splash_color "Direct link to splash_color")

The primary [color](/docs/reference/colors) of the button when the button is in the down (pressed) state.

### `splash_radius`[​](#splash_radius "Direct link to splash_radius")

The splash radius. Honoured only when in Material 2.

### `style`[​](#style "Direct link to style")

Value is of type [`ButtonStyle`](/docs/reference/types/buttonstyle).

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

### `visual_density`[​](#visual_density "Direct link to visual_density")

Defines how compact the control's layout will be.

Value is of type [`VisualDensity`](/docs/reference/types/visualdensity).

## Methods[​](#methods "Direct link to Methods")

### `focus()`[​](#focus "Direct link to focus")

Moves focus to a button.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/iconbutton.md)

[

Previous

FloatingActionButton

](/docs/controls/floatingactionbutton)[

Next

MenuItemButton

](/docs/controls/menuitembutton)

-   [Examples](#examples)
    -   [Icon buttons](#icon-buttons)
    -   [Icon button with `click` event](#icon-button-with-click-event)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`alignment`](#alignment)
    -   [`autofocus`](#autofocus)
    -   [`content`](#content)
    -   [`disabled_color`](#disabled_color)
    -   [`enable_feedback`](#enable_feedback)
    -   [`focus_color`](#focus_color)
    -   [`highlight_color`](#highlight_color)
    -   [`hover_color`](#hover_color)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`icon_size`](#icon_size)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`padding`](#padding)
    -   [`selected`](#selected)
    -   [`selected_icon`](#selected_icon)
    -   [`selected_icon_color`](#selected_icon_color)
    -   [`splash_color`](#splash_color)
    -   [`splash_radius`](#splash_radius)
    -   [`style`](#style)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
    -   [`visual_density`](#visual_density)
-   [Methods](#methods)
    -   [`focus()`](#focus)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  MenuItemButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/menuitembutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/menuitembutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/menuitembutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/menuitembutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   MenuItemButton

On this page

# MenuItemButton

A button for use in a [MenuBar](/docs/controls/menubar) or on its own, that can be activated by click or keyboard navigation.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/menuitembutton)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.padding = 0    page.spacing = 0    bg_container = ft.Ref[ft.Container]()    def handle_color_click(e):        color = e.control.content.value        print(f"{color}.on_click")        bg_container.current.content.value = f"{color} background color"        bg_container.current.bgcolor = color.lower()        page.update()    def handle_on_hover(e):        print(f"{e.control.content.value}.on_hover")    menubar = ft.MenuBar(        expand=True,        controls=[            ft.SubmenuButton(                content=ft.Text("BgColors"),                controls=[                    ft.MenuItemButton(                        content=ft.Text("Blue"),                        leading=ft.Icon(ft.Icons.COLORIZE),                        style=ft.ButtonStyle(bgcolor={ft.ControlState.HOVERED: ft.Colors.BLUE}),                        on_click=handle_color_click,                        on_hover=handle_on_hover,                    ),                    ft.MenuItemButton(                        content=ft.Text("Green"),                        leading=ft.Icon(ft.Icons.COLORIZE),                        style=ft.ButtonStyle(bgcolor={ft.ControlState.HOVERED: ft.Colors.GREEN}),                        on_click=handle_color_click,                        on_hover=handle_on_hover,                    ),                    ft.MenuItemButton(                        content=ft.Text("Red"),                        leading=ft.Icon(ft.Icons.COLORIZE),                        style=ft.ButtonStyle(bgcolor={ft.ControlState.HOVERED: ft.Colors.RED}),                        on_click=handle_color_click,                        on_hover=handle_on_hover,                    )                ]            ),        ]    )    page.add(        ft.Row([menubar]),        ft.Container(            ref=bg_container,            expand=True,            bgcolor=ft.Colors.SURFACE,            content=ft.Text("Choose a bgcolor from the menu", style=ft.TextThemeStyle.HEADLINE_LARGE),            alignment=ft.alignment.center,        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/menuitembutton/img/docs/controls/menu-item-button/menu-item-button.gif)

## Properties[​](#properties "Direct link to Properties")

### `autofocus`[​](#autofocus "Direct link to autofocus")

Whether this button should automatically request focus.

Defaults to `False`.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

Whether to clip the content of this control or not.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `close_on_click`[​](#close_on_click "Direct link to close_on_click")

Defines if the menu will be closed when the `MenuItemButton` is clicked.

Defaults to `True`.

### `content`[​](#content "Direct link to content")

The child control to be displayed in the center of this button.

Typically this is the button's label, using a `Text` control.

### `focus_on_hover`[​](#focus_on_hover "Direct link to focus_on_hover")

Determine if hovering can request focus.

Defaults to `True`.

### `leading`[​](#leading "Direct link to leading")

An optional control to display before the `content`.

Typically an [`Icon`](/docs/controls/icon) control.

### `overflow_axis`[​](#overflow_axis "Direct link to overflow_axis")

The direction in which the menu item expands.

If the menu item button is a descendent of `MenuBar`, then this property is ignored.

Value is of type [`Axis`](/docs/reference/types/axis).

### `semantic_label`[​](#semantic_label "Direct link to semantic_label")

A string that describes the button's action to assistive technologies.

### `style`[​](#style "Direct link to style")

Customizes this button's appearance.

Value is of type [`ButtonStyle`](/docs/reference/types/buttonstyle).

### `trailing`[​](#trailing "Direct link to trailing")

An optional control to display after the `content`.

Typically an [`Icon`](/docs/controls/icon) control.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fired when this button loses focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fired when the button is clicked.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fired when the button receives focus.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fired when the button is hovered.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/menuitembutton.md)

[

Previous

IconButton

](/docs/controls/iconbutton)[

Next

OutlinedButton

](/docs/controls/outlinedbutton)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`autofocus`](#autofocus)
    -   [`clip_behavior`](#clip_behavior)
    -   [`close_on_click`](#close_on_click)
    -   [`content`](#content)
    -   [`focus_on_hover`](#focus_on_hover)
    -   [`leading`](#leading)
    -   [`overflow_axis`](#overflow_axis)
    -   [`semantic_label`](#semantic_label)
    -   [`style`](#style)
    -   [`trailing`](#trailing)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)
    -   [`on_hover`](#on_hover)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  OutlinedButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/outlinedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/outlinedbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/outlinedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/outlinedbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   OutlinedButton

On this page

# OutlinedButton

Outlined buttons are medium-emphasis buttons. They contain actions that are important, but aren’t the primary action in an app. Outlined buttons pair well with filled buttons to indicate an alternative, secondary action. See [Material 3 buttons](https://m3.material.io/components/buttons/overview) for more info.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/outlinedbutton)

### Basic outlined buttons[​](#basic-outlined-buttons "Direct link to Basic outlined buttons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Basic outlined buttons"    page.add(        ft.OutlinedButton(text="Outlined button"),        ft.OutlinedButton("Disabled button", disabled=True),    )ft.app(main)
```

![](https://flet.dev/docs/controls/outlinedbutton/img/docs/controls/outlined-button/basic-outlined-buttons.png)

### Outlined buttons with icons[​](#outlined-buttons-with-icons "Direct link to Outlined buttons with icons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Outlined buttons with icons"    page.add(        ft.OutlinedButton("Button with icon", icon="chair_outlined"),        ft.OutlinedButton(            "Button with colorful icon",            icon="park_rounded",            icon_color="green400",        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/outlinedbutton/img/docs/controls/outlined-button/outlined-buttons-with-icons.png)

### Outlined button with `click` event[​](#outlined-button-with-click-event "Direct link to outlined-button-with-click-event")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Outlined button with 'click' event"    def button_clicked(e):        b.data += 1        t.value = f"Button clicked {b.data} time(s)"        page.update()    b = ft.OutlinedButton("Button with 'click' event", on_click=button_clicked, data=0)    t = ft.Text()    page.add(b, t)ft.app(main)
```

![](https://flet.dev/docs/controls/outlinedbutton/img/docs/controls/outlined-button/outlined-button-with-click-event.gif)

### Outlined button with custom content[​](#outlined-button-with-custom-content "Direct link to Outlined button with custom content")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Outlined buttons with custom content"    page.add(        ft.OutlinedButton(            width=150,            content=ft.Row(                [                    ft.Icon(name=ft.Icons.FAVORITE, color="pink"),                    ft.Icon(name=ft.Icons.AUDIOTRACK, color="green"),                    ft.Icon(name=ft.Icons.BEACH_ACCESS, color="blue"),                ],                alignment=ft.MainAxisAlignment.SPACE_AROUND,            ),        ),        ft.OutlinedButton(            content=ft.Container(                content=ft.Column(                    [                        ft.Text(value="Compound button", size=20),                        ft.Text(value="This is secondary text"),                    ],                    alignment=ft.MainAxisAlignment.CENTER,                    spacing=5,                ),                padding=ft.padding.all(10),            ),        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/outlinedbutton/img/docs/controls/outlined-button/outlined-buttons-with-custom-content.png)

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive button is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoButton`](/docs/controls/cupertinobutton) is created, which matches the functionality and presentation of this button. On other platforms, a Material `ElevatedButton` is created.

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `style`[​](#style "Direct link to style")

The value is an instance of [`ButtonStyle`](/docs/reference/types/buttonstyle) class.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Methods[​](#methods "Direct link to Methods")

### `focus()`[​](#focus "Direct link to focus")

Moves focus to a button.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a mouse pointer enters or exists the button response area. `data` property of event object contains `true` (string) when cursor enters and `false` when it exits.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the button is long-pressed.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/outlinedbutton.md)

[

Previous

MenuItemButton

](/docs/controls/menuitembutton)[

Next

PopupMenuButton

](/docs/controls/popupmenubutton)

-   [Examples](#examples)
    -   [Basic outlined buttons](#basic-outlined-buttons)
    -   [Outlined buttons with icons](#outlined-buttons-with-icons)
    -   [Outlined button with `click` event](#outlined-button-with-click-event)
    -   [Outlined button with custom content](#outlined-button-with-custom-content)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`clip_behavior`](#clip_behavior)
    -   [`content`](#content)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`style`](#style)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Methods](#methods)
    -   [`focus()`](#focus)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)
    -   [`on_hover`](#on_hover)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  PopupMenuButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/popupmenubutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/popupmenubutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/popupmenubutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/popupmenubutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   PopupMenuButton

On this page

# PopupMenuButton

An icon button which displays a menu when clicked.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/popupmenubutton)

### PopupMenuButton[​](#popupmenubutton "Direct link to PopupMenuButton")

-   Python

```
import flet as ftdef main(page: ft.Page):    def check_item_clicked(e):        e.control.checked = not e.control.checked        page.update()    pb = ft.PopupMenuButton(        items=[            ft.PopupMenuItem(text="Item 1"),            ft.PopupMenuItem(icon=ft.Icons.POWER_INPUT, text="Check power"),            ft.PopupMenuItem(                content=ft.Row(                    [                        ft.Icon(ft.Icons.HOURGLASS_TOP_OUTLINED),                        ft.Text("Item with a custom content"),                    ]                ),                on_click=lambda _: print("Button with a custom content clicked!"),            ),            ft.PopupMenuItem(),  # divider            ft.PopupMenuItem(                text="Checked item", checked=False, on_click=check_item_clicked            ),        ]    )    page.add(pb)ft.app(main)
```

![](https://flet.dev/docs/controls/popupmenubutton/img/docs/controls/popup-menu-button/popup-menu-button-with-custom-content.gif)

## `PopupMenuButton` Properties[​](#popupmenubutton-properties "Direct link to popupmenubutton-properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The menu's background [color](/docs/reference/colors).

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The `content` will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `content`[​](#content "Direct link to content")

A `Control` that will be displayed instead of "more" icon.

### `elevation`[​](#elevation "Direct link to elevation")

The menu's elevation when opened.

Defaults to `8`.

### `enable_feedback`[​](#enable_feedback "Direct link to enable_feedback")

Whether detected gestures should provide acoustic and/or haptic feedback. On Android, for example, setting this to `True` produce a click sound and a long-press will produce a short vibration.

Defaults to `True`.

### `icon`[​](#icon "Direct link to icon")

If provided, an icon to draw on the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

The `icon`'s [color](/docs/reference/colors).

### `icon_size`[​](#icon_size "Direct link to icon_size")

The `icon`'s size.

### `items`[​](#items "Direct link to items")

A collection of `PopupMenuItem` controls to display in a dropdown menu.

### `menu_position`[​](#menu_position "Direct link to menu_position")

Defines position of the popup menu relative to the button.

Value is of type [`PopupMenuPosition`](/docs/reference/types/popupmenuposition) and defaults to `PopupMenuPosition.OVER`.

### `padding`[​](#padding "Direct link to padding")

Value is of type [`Padding`](/docs/reference/types/padding) and defaults to `padding.all(8.0)`.

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) used to paint the shadow below the menu.

### `shape`[​](#shape "Direct link to shape")

The menu's shape.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder) and defaults to `CircleBorder(radius=10.0)`.

### `splash_radius`[​](#splash_radius "Direct link to splash_radius")

The splash radius.

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The [color](/docs/reference/colors) used as an overlay on color to indicate elevation.

## `PopupMenuButton` Events[​](#popupmenubutton-events "Direct link to popupmenubutton-events")

### `on_cancel`[​](#on_cancel "Direct link to on_cancel")

Called when the user dismisses/cancels the popup menu without selecting an item.

### `on_open`[​](#on_open "Direct link to on_open")

Called when the popup menu is shown.

## `PopupMenuItem` Properties[​](#popupmenuitem-properties "Direct link to popupmenuitem-properties")

### `check`[​](#check "Direct link to check")

If set to `True` or `False` a menu item draws a checkmark.

### `content`[​](#content-1 "Direct link to content-1")

A `Control` representing custom content of this menu item. If specified, then both `icon` and `text` properties are ignored.

### `height`[​](#height "Direct link to height")

The minimum height of this menu item.

Defaults to `40`.

### `icon`[​](#icon-1 "Direct link to icon-1")

An icon to draw before the text label of this menu item.

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor to be displayed when a mouse pointer enters or is hovering over this control.

Value is of type [`MouseCursor`](/docs/reference/types/mousecursor).

### `padding`[​](#padding-1 "Direct link to padding-1")

The padding of this menu item. Note that the `height` value of this menu item may influence the applied padding. For example, If a `height` greater than the height of the sum of the padding and a `content` is provided, then the padding's effect will not be visible.

Padding value is an instance of [`Padding`](/docs/reference/types/padding) class.

Defaults to `padding.symmetric(horizontal=12)`.

### `text`[​](#text "Direct link to text")

The text label of this menu item.

## `PopupMenuItem` Events[​](#popupmenuitem-events "Direct link to popupmenuitem-events")

### `on_click`[​](#on_click "Direct link to on_click")

Called when a user clicks a this menu item.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/popupmenubutton.md)

[

Previous

OutlinedButton

](/docs/controls/outlinedbutton)[

Next

SegmentedButton

](/docs/controls/segmentedbutton)

-   [Examples](#examples)
    -   [PopupMenuButton](#popupmenubutton)
-   [`PopupMenuButton` Properties](#popupmenubutton-properties)
    -   [`bgcolor`](#bgcolor)
    -   [`clip_behavior`](#clip_behavior)
    -   [`content`](#content)
    -   [`elevation`](#elevation)
    -   [`enable_feedback`](#enable_feedback)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`icon_size`](#icon_size)
    -   [`items`](#items)
    -   [`menu_position`](#menu_position)
    -   [`padding`](#padding)
    -   [`shadow_color`](#shadow_color)
    -   [`shape`](#shape)
    -   [`splash_radius`](#splash_radius)
    -   [`surface_tint_color`](#surface_tint_color)
-   [`PopupMenuButton` Events](#popupmenubutton-events)
    -   [`on_cancel`](#on_cancel)
    -   [`on_open`](#on_open)
-   [`PopupMenuItem` Properties](#popupmenuitem-properties)
    -   [`check`](#check)
    -   [`content`](#content-1)
    -   [`height`](#height)
    -   [`icon`](#icon-1)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`padding`](#padding-1)
    -   [`text`](#text)
-   [`PopupMenuItem` Events](#popupmenuitem-events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Input and Selections | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/input-and-selections/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/input-and-selections/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/input-and-selections/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/input-and-selections/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   Input and Selections

# Input and Selections

[

## 📄️ AutoComplete

Helps the user make a selection by entering some text and choosing from among a list of suggestions.

](/docs/controls/autocomplete)

[

## 📄️ AutofillGroup

Groups autofillable controls such as TextField

](/docs/controls/autofillgroup)

[

## 📄️ Checkbox

Checkbox allows to select one or more items from a group, or switch between two mutually exclusive options (checked or unchecked, on or off).

](/docs/controls/checkbox)

[

## 📄️ Chip

Chips are compact elements that represent an attribute, text, entity, or action.

](/docs/controls/chip)

[

## 📄️ CupertinoCheckbox

A macOS style checkbox. Checkbox allows to select one or more items from a group, or switch between two mutually exclusive options (checked or unchecked, on or off).

](/docs/controls/cupertinocheckbox)

[

## 📄️ CupertinoRadio

A macOS style radio button. Radio buttons let people select a single option from two or more choices.

](/docs/controls/cupertinoradio)

[

## 📄️ CupertinoSlider

An macOS style slider. It provides a visual indication of adjustable content, as well as the current setting in the total range of content.

](/docs/controls/cupertinoslider)

[

## 📄️ CupertinoSwitch

An iOS-style switch.

](/docs/controls/cupertinoswitch)

[

## 📄️ CupertinoTextField

An iOS-style text field.

](/docs/controls/cupertinotextfield)

[

## 📄️ Dropdown

Dropdown is used to help people make a choice from a menu and put the selected item into the text input field. It's also possible to filter the list based on the text input or search one item in the menu list.

](/docs/controls/dropdown)

[

## 📄️ DropdownM2

A material design button for selecting from a list of items.

](/docs/controls/dropdownm2)

[

## 📄️ Radio

Radio buttons let people select a single option from two or more choices.

](/docs/controls/radio)

[

## 📄️ RangeSlider

A Material Design range slider. Used to select a range from a range of values.

](/docs/controls/rangeslider)

[

## 📄️ SearchBar

A Material Design search bar. It visually looks like a TextField.

](/docs/controls/searchbar)

[

## 📄️ Slider

A slider provides a visual indication of adjustable content, as well as the current setting in the total range of content.

](/docs/controls/slider)

[

## 📄️ Switch

A toggle represents a physical switch that allows someone to choose between two mutually exclusive options.

](/docs/controls/switch)

[

## 📄️ TextField

A material design text field.

](/docs/controls/textfield)

[

Previous

TextButton

](/docs/controls/textbutton)[

Next

AutoComplete

](/docs/controls/autocomplete)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  AutoComplete | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/autocomplete/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/autocomplete/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/autocomplete/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/autocomplete/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Input and Selections](/docs/controls/input-and-selections)
-   AutoComplete

On this page

# AutoComplete

Helps the user make a selection by entering some text and choosing from among a list of suggestions.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/input/autocomplete)

### Basic example[​](#basic-example "Direct link to Basic example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.AutoComplete(            suggestions=[                ft.AutoCompleteSuggestion(key="one 1", value="One"),                ft.AutoCompleteSuggestion(key="two 2", value="Two"),                ft.AutoCompleteSuggestion(key="three 3", value="Three"),            ],            on_select=lambda e: print(e.control.selected_index, e.selection),        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/autocomplete/img/docs/controls/autocomplete/autocomplete-example.gif)

## Properties[​](#properties "Direct link to Properties")

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index of the selected suggestion in the list of `suggestions`.

This property is read-only and `None` at initialization, until a suggestion is selected for the first time.

Valule is of type `int`.

### `suggestions`[​](#suggestions "Direct link to suggestions")

A list of [`AutoCompleteSuggestion`](/docs/reference/types/autocompletesuggestion) controls representing the suggestions to be displayed.

**Note:**

-   The internal filtration process of the suggestions (based on their `key`s) with respect to the user's input is case-insensitive because the comparison is done in lowercase.
-   A valid `AutoCompleteSuggestion` must have at least a `key` or `value` specified, else it will be ignored. If only `key` is provided, `value` will be set to `key` as fallback and vice versa.

### `suggestions_max_height`[​](#suggestions_max_height "Direct link to suggestions_max_height")

The maximum - visual - height of the suggestions list.

Value is of type [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber) and defaults to `200`.

## Events[​](#events "Direct link to Events")

### `on_select`[​](#on_select "Direct link to on_select")

Fires when a suggestion is selected.

Event handler is of type [`AutoCompleteSelectEvent`](/docs/reference/types/autocompleteselectevent).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/autocomplete.md)

[

Previous

Input and Selections

](/docs/controls/input-and-selections)[

Next

AutofillGroup

](/docs/controls/autofillgroup)

-   [Examples](#examples)
    -   [Basic example](#basic-example)
-   [Properties](#properties)
    -   [`selected_index`](#selected_index)
    -   [`suggestions`](#suggestions)
    -   [`suggestions_max_height`](#suggestions_max_height)
-   [Events](#events)
    -   [`on_select`](#on_select)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  AutofillGroup | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/autofillgroup/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/autofillgroup/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/autofillgroup/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/autofillgroup/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Input and Selections](/docs/controls/input-and-selections)
-   AutofillGroup

On this page

# AutofillGroup

Groups autofillable controls such as [`TextField`](/docs/controls/textfield) or [`CupertinoTextField`](/docs/controls/cupertinotextfield).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/input/autofillgroup)

### Basic example[​](#basic-example "Direct link to Basic example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.AutofillGroup(            ft.Column(                controls=[                    ft.TextField(                        label="Name",                        autofill_hints=ft.AutofillHint.NAME,                    ),                    ft.TextField(                        label="Email",                        autofill_hints=[ft.AutofillHint.EMAIL],                    ),                    ft.TextField(                        label="Phone Number",                        autofill_hints=[ft.AutofillHint.TELEPHONE_NUMBER],                    ),                    ft.TextField(                        label="Street Address",                        autofill_hints=ft.AutofillHint.FULL_STREET_ADDRESS,                    ),                    ft.TextField(                        label="Postal Code",                        autofill_hints=ft.AutofillHint.POSTAL_CODE,                    ),                ]            )        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/autofillgroup/img/docs/controls/autofillgroup/autofillgroup-example.gif)

## Properties[​](#properties "Direct link to Properties")

### `content`[​](#content "Direct link to content")

The content control of this group.

Value is of type `Control`.

### `dispose_action`[​](#dispose_action "Direct link to dispose_action")

The action to be run when this `AutofillGroup` is the topmost `AutofillGroup` and it's being disposed, in order to clean up the current autofill context.

Value is of type [`AutofillGroupDisposeAction`](/docs/reference/types/autofillgroupdisposeaction) and defaults to `AutofillGroupDisposeAction.COMMIT`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/autofillgroup.md)

[

Previous

AutoComplete

](/docs/controls/autocomplete)[

Next

Checkbox

](/docs/controls/checkbox)

-   [Examples](#examples)
    -   [Basic example](#basic-example)
-   [Properties](#properties)
    -   [`content`](#content)
    -   [`dispose_action`](#dispose_action)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Checkbox | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/checkbox/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/checkbox/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/checkbox/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/checkbox/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Input and Selections](/docs/controls/input-and-selections)
-   Checkbox

On this page

# Checkbox

Checkbox allows to select one or more items from a group, or switch between two mutually exclusive options (checked or unchecked, on or off).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/input/checkbox)

### Basic checkboxes[​](#basic-checkboxes "Direct link to Basic checkboxes")

-   Python

```
import flet as ftdef main(page):    def button_clicked(e):        t.value = (            f"Checkboxes values are:  {c1.value}, {c2.value}, {c3.value}, {c4.value}, {c5.value}."        )        page.update()    t = ft.Text()    c1 = ft.Checkbox(label="Unchecked by default checkbox", value=False)    c2 = ft.Checkbox(label="Undefined by default tristate checkbox", tristate=True)    c3 = ft.Checkbox(label="Checked by default checkbox", value=True)    c4 = ft.Checkbox(label="Disabled checkbox", disabled=True)    c5 = ft.Checkbox(        label="Checkbox with rendered label_position='left'", label_position=ft.LabelPosition.LEFT    )    b = ft.ElevatedButton(text="Submit", on_click=button_clicked)    page.add(c1, c2, c3, c4, c5, b, t)ft.app(main)
```

![](https://flet.dev/docs/controls/checkbox/img/docs/controls/checkbox/basic-checkbox.gif)

### Checkbox with `on_change` event[​](#checkbox-with-on_change-event "Direct link to checkbox-with-on_change-event")

-   Python

```
import flet as ftdef main(page):  def checkbox_changed(e):    t.value = f"Checkbox value changed to {c.value}"     t.update()  c = ft.Checkbox(label="Checkbox with 'change' event", on_change=checkbox_changed)  t = ft.Text()  page.add(c, t)ft.app(main)
```

![](https://flet.dev/docs/controls/checkbox/img/docs/controls/checkbox/checkbox-with-change-event.gif)

## Properties[​](#properties "Direct link to Properties")

### `active_color`[​](#active_color "Direct link to active_color")

The [color](/docs/reference/colors) to use when this checkbox is checked.

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive Checkbox is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoCheckbox`](/docs/controls/cupertinocheckbox) is created, which has matching functionality and presentation as `Checkbox`, and the graphics as expected on iOS. On other platforms, a Material Checkbox is created.

See the example of usage [here](/docs/controls/cupertinocheckbox#cupertinocheckbox-and-adaptive-checkbox-example).

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `border`[​](#border "Direct link to border")

The color and width of the checkbox's border to be rendered when the checkbox's `value` is `False`.

### `check_color`[​](#check_color "Direct link to check_color")

The [color](/docs/reference/colors) to use for the check icon when this checkbox is checked.

### `fill_color`[​](#fill_color "Direct link to fill_color")

The [color](/docs/reference/colors) that fills the checkbox in various [`ControlState`](/docs/reference/types/controlstate) states.

### `hover_color`[​](#hover_color "Direct link to hover_color")

The [color](/docs/reference/colors) to use when this checkbox is hovered.

### `is_error`[​](#is_error "Direct link to is_error")

Whether this checkbox wants to show an error state. When `True` this checkbox will have a different default container color and check color. Defaults to `False`.

### `label`[​](#label "Direct link to label")

The clickable label to display on the right of a checkbox.

### `label_style`[​](#label_style "Direct link to label_style")

The label's style. An instance of type [`TextStyle`](/docs/reference/types/textstyle).

### `label_position`[​](#label_position "Direct link to label_position")

Defines on which side of the checkbox the `label` should be shown.

Value is of type [`LabelPosition`](/docs/reference/types/labelposition) and defaults to `LabelPosition.RIGHT`.

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor to be displayed when a mouse pointer enters or is hovering over this control.

Value is of type [`MouseCursor`](/docs/reference/types/mousecursor).

### `overlay_color`[​](#overlay_color "Direct link to overlay_color")

The [color](/docs/reference/colors) of the checkbox's overlay in various [`ControlState`](/docs/reference/types/controlstate) states.

This property supports the following `ControlState` values: `PRESSED`, `SELECTED`, `HOVERED` and `FOCUSED`.

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

The semantic label for the checkbox that is not shown in the UI, but will be announced by screen readers in accessibility modes (e.g TalkBack/VoiceOver).

### `shape`[​](#shape "Direct link to shape")

The shape of the checkbox. The value is an instance of [`OutlinedBorder`](/docs/reference/types/outlinedborder) class.

Defaults to `RoundedRectangleBorder(radius=2)`.

### `splash_radius`[​](#splash_radius "Direct link to splash_radius")

The radius of the circular Material ink response (ripple) in logical pixels.

Defaults to `20.0`.

### `tristate`[​](#tristate "Direct link to tristate")

If `True` the checkboxes value can be `True`, `False`, or `None`.

Checkbox displays a dash when its value is `None`.

### `value`[​](#value "Direct link to value")

Current value of the checkbox.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_change`[​](#on_change "Direct link to on_change")

Fires when the state of the Checkbox is changed.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/checkbox.md)

[

Previous

AutofillGroup

](/docs/controls/autofillgroup)[

Next

Chip

](/docs/controls/chip)

-   [Examples](#examples)
    -   [Basic checkboxes](#basic-checkboxes)
    -   [Checkbox with `on_change` event](#checkbox-with-on_change-event)
-   [Properties](#properties)
    -   [`active_color`](#active_color)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`border`](#border)
    -   [`check_color`](#check_color)
    -   [`fill_color`](#fill_color)
    -   [`hover_color`](#hover_color)
    -   [`is_error`](#is_error)
    -   [`label`](#label)
    -   [`label_style`](#label_style)
    -   [`label_position`](#label_position)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`overlay_color`](#overlay_color)
    -   [`semantics_label`](#semantics_label)
    -   [`shape`](#shape)
    -   [`splash_radius`](#splash_radius)
    -   [`tristate`](#tristate)
    -   [`value`](#value)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_change`](#on_change)
    -   [`on_focus`](#on_focus)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Testing Flet app on Android | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/testing-on-android/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/testing-on-android/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/testing-on-android/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/testing-on-android/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Testing on Android

# Testing Flet app on Android

Start building awesome mobile apps in Python using just your computer and mobile phone!

Install [Flet](https://play.google.com/store/apps/details?id=com.appveyor.flet) app to your Android device. You will be using this app to see how your Flet project is working on Android device.

[![Get it on Google Play](https://flet.dev/docs/getting-started/testing-on-android/img/docs/getting-started/testing-on-android/google-play-badge.png)](https://play.google.com/store/apps/details?id=com.appveyor.flet)

To get started on your computer you need Python 3.9 or greater installed.

Important

Your Android device and computer must be connected to the same Wi-Fi or local network.

It's recommended to start with the creation of a new virtual environment:

-   macOS
-   Linux
-   Windows

```
python3 -m venv .venvsource .venv/bin/activate
```

```
python3 -m venv .venvsource .venv/bin/activate
```

```
python.exe -m venv .venv.venv\Scripts\activate.bat
```

Next, install the latest `flet` package:

```
pip install flet --upgrade
```

Ensure that Flet has successfully installed and Flet CLI is available in `PATH` by running:

```
flet --version
```

Create a new Flet project:

```
flet create my-appcd my-app
```

Run the following command to start Flet development server with your app:

```
flet run --android
```

A QR code with encoded project URL will be displayed in the terminal:

![](https://flet.dev/docs/getting-started/testing-on-android/img/docs/getting-started/testing-on-android/app-qr-code.png)

Open **Camera** app on your Android device, point to a QR code and click URL to open it in Flet app.

Try updating `main.py` (for example, replace a greeting of `Text` control) - the app will be instantly refreshed on your Android device.

You can try more complex Flet example from [Introduction](/docs/#flet-app-example).

To return to "Home" tab either:

-   Long-press anywhere on the screen with 3 fingers or
-   Shake your Android device.

You can also "manually" add a new project by clicking **"+"** button and typing its URL.

Quick test

There is "Counter" Flet project hosted on the internet that you can add to Flet app to make sure everything works:

```
https://flet-counter-test-ios.fly.dev
```

Check "Gallery" tab for some great examples of what kind of projects could be done with Flet.

Explore [Flet examples](https://github.com/flet-dev/examples/tree/main/python) for even more examples.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/testing-on-android.md)

[

Previous

Testing on iOS

](/docs/getting-started/testing-on-ios)[

Next

Async apps

](/docs/getting-started/async-apps)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Async apps | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/getting-started/async-apps/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/async-apps/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/getting-started/async-apps/img/logo.svg)![Flet Logo](https://flet.dev/docs/getting-started/async-apps/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
    -   [Create a new Flet app](/docs/getting-started/create-flet-app)
    -   [Running Flet app](/docs/getting-started/running-app)
    -   [Flet controls](/docs/getting-started/flet-controls)
    -   [Custom controls](/docs/getting-started/custom-controls)
    -   [Adaptive apps](/docs/getting-started/adaptive-apps)
    -   [Navigation and routing](/docs/getting-started/navigation-and-routing)
    -   [Testing on iOS](/docs/getting-started/testing-on-ios)
    -   [Testing on Android](/docs/getting-started/testing-on-android)
    -   [Async apps](/docs/getting-started/async-apps)
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Getting started](/docs/getting-started/)
-   Async apps

On this page

# Async apps

Flet app can be written as an async app and use `asyncio` and other Python async libraries. Calling coroutines is naturally supported in Flet, so you don't need to wrap them to run synchronously.

By default, Flet executes control event handlers in separate threads, but sometimes that could be an ineffective usage of CPU or it does nothing while waiting for a HTTP response or executing `sleep()`.

Asyncio, on the other hand, allows implementing concurrency in a single thread by switching execution context between "coroutines". This is especially important for apps that are going to be [published as static websites](/docs/publish/web/static-website) using [Pyodide](https://pyodide.org/en/stable/). Pyodide is a Python runtime built as a WebAssembly (WASM) and running in the browser. At the time of writing it doesn't support [threading](https://github.com/pyodide/pyodide/issues/237) yet.

## Getting started with async[​](#getting-started-with-async "Direct link to Getting started with async")

You could mark `main()` method of Flet app as `async` and then use any asyncio API inside it:

```
import flet as ftasync def main(page: ft.Page):    await asyncio.sleep(1)    page.add(ft.Text("Hello, async world!"))ft.app(main)
```

You can use `await ft.app_async(main)` if Flet app is part of a larger app and called from `async` code.

## Control event handlers[​](#control-event-handlers "Direct link to Control event handlers")

Control event handlers could be both sync and `async`.

If a handler does not call any async methods it could be a regular sync method:

```
def page_resize(e):    print("New page size:", page.window.width, page.window.height)page.on_resize = page_resize
```

However, if a handler calls async logic it must be async too:

```
async def main(page: ft.Page):    async def button_click(e):        await some_async_method()        page.add(ft.Text("Hello!"))    page.add(ft.ElevatedButton("Say hello!", on_click=button_click))ft.app(main)
```

### Async lambdas[​](#async-lambdas "Direct link to Async lambdas")

There are no async lambdas in Python. It's perfectly fine to have a lambda event handler in async app for simple things:

```
page.on_error = lambda e: print("Page error:", e.data)
```

but you can't have an async lambda, so an async event handler must be used.

## Sleeping[​](#sleeping "Direct link to Sleeping")

To delay code execution in async Flet app you should use [`asyncio.sleep()`](https://docs.python.org/3/library/asyncio-task.html#asyncio.sleep) instead of `time.sleep()`, for example:

```
import asyncioimport flet as ftdef main(page: ft.Page):    async def button_click(e):        await asyncio.sleep(1)        page.add(ft.Text("Hello!"))    page.add(        ft.ElevatedButton("Say hello with delay!", on_click=button_click)    )ft.app(main)
```

## Threading[​](#threading "Direct link to Threading")

To run something in the background use [`page.run_task()`](/docs/controls/page#run_taskhandler-args-kwargs). For example, "Countdown" custom control which is self-updating on background could be implemented as following:

```
import asyncioimport flet as ftclass Countdown(ft.Text):    def __init__(self, seconds):        super().__init__()        self.seconds = seconds    def did_mount(self):        self.running = True        self.page.run_task(self.update_timer)    def will_unmount(self):        self.running = False    async def update_timer(self):        while self.seconds and self.running:            mins, secs = divmod(self.seconds, 60)            self.value = "{:02d}:{:02d}".format(mins, secs)            self.update()            await asyncio.sleep(1)            self.seconds -= 1def main(page: ft.Page):    page.add(Countdown(120), Countdown(60))ft.app(main)
```

![](https://flet.dev/docs/getting-started/async-apps/img/docs/getting-started/user-control-countdown.gif)

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/getting-started/async-apps.md)

[

Previous

Testing on Android

](/docs/getting-started/testing-on-android)[

Next

Publishing Flet app to multiple platforms

](/docs/publish)

-   [Getting started with async](#getting-started-with-async)
-   [Control event handlers](#control-event-handlers)
    -   [Async lambdas](#async-lambdas)
-   [Sleeping](#sleeping)
-   [Threading](#threading)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Publishing Flet app to multiple platforms | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   Publishing Flet app

On this page

# Publishing Flet app to multiple platforms

## Introduction[​](#introduction "Direct link to Introduction")

Flet CLI provides `flet build` command that allows packaging Flet app into a standalone executable or install package for distribution.

## Platform matrix[​](#platform-matrix "Direct link to Platform matrix")

The following matrix shows which OS you should run `flet build` command on in order to build a package for specific platform:

Run on / `flet build`

`apk/aab`

`ipa`

`macos`

`linux`

`windows`

`web`

macOS

✅

✅

✅

✅

Windows

✅

✅ (WSL)

✅

✅

Linux

✅

✅

✅

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

### Flutter SDK[​](#flutter-sdk "Direct link to Flutter SDK")

If the correct version of the Flutter SDK is not found in the `PATH`, it will be automatically installed during the first run when building a Flet app for any platform.

Flutter SDK is installed into `$HOME/flutter/{version}` directory.

## Project structure[​](#project-structure "Direct link to Project structure")

`flet build` command assumes the following minimal Flet project structure:

```
├── README.md├── pyproject.toml└── src    ├── assets    │   └── icon.png    └── main.py
```

`main.py` is the entry point of your Flet application with `ft.app(main)` at the end. A different entry point could be specified with `--module-name` argument.

`assets` is an optional directory that contains application assets (images, sound, text and other files required by your app) as well as images used for package icons and splash screens.

If only `icon.png` (or other supported format such as `.bmp`, `.jpg`, `.webp`) is provided it will be used as a source image to generate all icons and splash screens for all platforms. See section below for more information about icons and splashes.

`pyproject.toml` contains the application metadata, lists its dependencies and controls build process. The list of project dependencies should contain at least `flet` package:

pyproject.toml

```
[project]name = "myapp"version = "0.1.0"description = ""readme = "README.md"requires-python = ">=3.9"authors = [    { name = "Flet developer", email = "you@example.com" }]dependencies = [  "flet"][tool.flet]org = "com.mycompany"product = "MyApp"company = "My Company"copyright = "Copyright (C) 2025 by My Company"[tool.flet.app]path = "src"
```

note

Though `requirements.txt` can also be used to list app requirements Flet recommends using `pyproject.toml` for new projects. If both `pyproject.toml` and `requirements.txt` exist the latter will be ignored.

No pip freeze

Do not use `pip freeze > requirements.txt` command to create `requirements.txt` for the app that will be running on mobile. As you run `pip freeze` command on a desktop `requirements.txt` will have dependencies that are not intended to work on a mobile device, such as `watchdog`.

Hand-pick `requirements.txt` to have only direct dependencies required by your app, plus `flet`.

The easiest way to start with the right project structure is to use `flet create` command:

```
flet create myapp
```

where `myapp` is a target directory.

## How it works[​](#how-it-works "Direct link to How it works")

`flet build <target_platform>` command could be run from the root of Flet app directory:

```
<flet_app_directory> % flet build <target_platform>
```

where `<target_platform>` could be one of the following: `apk`, `aab`, `ipa`, `web`, `macos`, `windows`, `linux`.

When running from a different directory you can provide the path to a directory with Flet app:

```
flet build <target_platform> <path_to_python_app>
```

Build results are copied to `<python_app_directory>/build/<target_platform>`. You can specify a custom output directory with `--output` option:

```
flet build <target_platform> --output <path-to-output-dir>
```

`flet build` uses Flutter SDK and the number of Flutter packages to build a distribution package from your Flet app.

When you run `flet build <target_platform>` command it:

-   Creates a new Flutter project in `{flet_app_directory}/build/flutter` directory from [https://github.com/flet-dev/flet-build-template](https://github.com/flet-dev/flet-build-template) template. Flutter app will contain a packaged Python app in the assets and use `flet` and `serious_python` packages to run Python app and render its UI respectively. The project is ephemeral and deleted upon completion.
-   Copies custom icons and splash images (see below) from `assets` directory into a Flutter project.
-   Generates icons for all platforms using [`flutter_launcher_icons`](https://pub.dev/packages/flutter_launcher_icons) package.
-   Generates splash screens for web, iOS and Android targets using [`flutter_native_splash`](https://pub.dev/packages/flutter_native_splash) package.
-   Packages Python app using `package` command of [`serious_python`](https://pub.dev/packages/serious_python) package. `package` command installs pure and binary Python packages from [https://pypi.org](https://pypi.org) and [https://pypi.flet.dev](https://pypi.flet.dev) for selected platform. If configured, `.py` files of installed packages and/or application will be compiled to `.pyc` files. All files, except `build` directory will be added to a package asset.
-   Runs `flutter build <target_platform>` command to produce an executable or an install package.
-   Copies build results to `{flet_app_directory}/build/<target_platform>` directory.

## Including optional controls[​](#including-optional-controls "Direct link to Including optional controls")

If your app uses the following controls their packages must be added to a build command:

-   Ad controls (`BannerAd` and `InterstitialAd`) implemented in `flet_ads` package.
-   [`Audio`](/docs/controls/audio) control implemented in `flet_audio` package.
-   [`AudioRecorder`](/docs/controls/audiorecorder) control implemented in `flet_audio_recorder` package.
-   [`Flashlight`](/docs/controls/flashlight) control implemented in `flet_flashlight` package.
-   [`Geolocator`](/docs/controls/geolocator) control implemented in `flet_geolocator` package.
-   [`Lottie`](/docs/controls/lottie) control implemented in `flet_lottie` package.
-   [`Map`](/docs/controls/map) control implemented in `flet_map` package.
-   [`PermissionHandler`](/docs/controls/permissionhandler) control implemented in `flet_permission_handler` package.
-   [`Rive`](/docs/controls/rive) control implemented in `flet_rive` package.
-   [`Video`](/docs/controls/video) control implemented in `flet_video` package.
-   [`WebView`](/docs/controls/webview) control implemented in `flet_webview` package.

Use `--include-packages <package_1> <package_2> ...` option to add Flutter packages with optional Flet controls or use `tool.flet.flutter.dependencies` section in `pyproject.toml`.

For example, to build your Flet app with `Video` and `Audio` controls add `--include-packages flet_video flet_audio` to your `flet build` command:

```
flet build apk --include-packages flet_video flet_audio
```

or the same in `pyproject.toml`:

```
flutter.dependencies = ["flet_video", "flet_audio"]
```

or an alternative syntax with versions:

```
[tool.flet.flutter.dependencies]flet_video = "1.0.0"flet_audio = "2.0.0"
```

or with path to the package on your disk:

```
[tool.flet.flutter.dependencies.my_package]path = "/path/to/my_package"
```

## Icons[​](#icons "Direct link to Icons")

You can customize app icons for all platforms (excluding Linux) with images in `assets` directory of your Flet app.

If only `icon.png` (or other supported format such as `.bmp`, `.jpg`, `.webp`) is provided it will be used as a source image to generate all icons.

-   **iOS** - `icon_ios.png` (or any supported image format). Recommended minimum image size is 1024 px. Image should not be transparent (have alpha channel). Defaults to `icon.png` with alpha-channel automatically removed.
-   **Android** - `icon_android.png` (or any supported image format). Recommended minimum image size is 192 px. Defaults to `icon.png`.
-   **Web** - `icon_web.png` (or any supported image format). Recommended minimum image size is 512 px. Defaults to `icon.png`.
-   **Windows** - `icon_windows.png` (or any supported image format). ICO will be produced of 256 px size. Defaults to `icon.png`. If `icon_windows.ico` file is provided it will be just copied to `windows/runner/resources/app_icon.ico` unmodified.
-   **macOS** - `icon_macos.png` (or any supported image format). Recommended minimum image size is 1024 px. Defaults to `icon.png`.

## Splash screen[​](#splash-screen "Direct link to Splash screen")

You can customize splash screens for iOS, Android and web applications with images in `assets` directory of your Flet app.

If only `splash.png` or `icon.png` (or other supported format such as `.bmp`, `.jpg`, `.webp`) is provided it will be used as a source image to generate all splash screen.

-   **iOS (light)** - `splash_ios.png` (or any supported image format). Defaults to `splash.png` and then `icon.png`.
-   **iOS (dark)** - `splash_dark_ios.png` (or any supported image format). Defaults to light iOS splash, then to `splash_dark.png`, then to `splash.png` and then `icon.png`.
-   **Android (light)** - `splash_android.png` (or any supported image format). Defaults to `splash.png` and then `icon.png`.
-   **Android (dark)** - `splash_dark_android.png` (or any supported image format). Defaults to light Android splash, then to `splash_dark.png`, then to `splash.png` and then `icon.png`.
-   **Web (light)** - `splash_web.png` (or any supported image format). Defaults to `splash.png` and then `icon.png`.
-   **Web (dark)** - `splash_dark_web.png` (or any supported image format). Defaults to light web splash, then `splash_dark.png`, then to `splash.png` and then `icon.png`.

`--splash-color` option specifies background color for a splash screen in light mode. Defaults to `#ffffff`.

`--splash-dark-color` option specifies background color for a splash screen in dark mode. Defaults to `#333333`.

Configuring splash settings in `pyproject.toml`:

```
[tool.flet.splash]color = "#FFFF00" # --splash-colordark_color = "#8B8000" # --splash-dark-colorweb = false # --no-web-splashios = false # --no-ios-splashandroid = false # --no-android-splash
```

## Entry point[​](#entry-point "Direct link to Entry point")

By default, `flet build` command assumes `main.py` as the entry point of your Flet application, i.e. the file with `ft.app(main)` at the end. A different entry point could be specified with `--module-name` argument or in `pyproject.toml`:

```
[tool.flet]app.module = "main"
```

## Compilation and cleanup[​](#compilation-and-cleanup "Direct link to Compilation and cleanup")

`flet build` command is not compiling app `.py` files into `.pyc` by default which allows you to avoid (or defer?) discovery of any syntax errors in your app and successfully complete the packaging.

You can enable the compilation and cleanup with the following new options:

-   `--compile-app` - compile app's `.py` files.
-   `--compile-packages` - compile installed packages' `.py` files.
-   `--cleanup-on-compile` - remove unnecessary files upon successful compilation.

Configuring compilation in `pyproject.toml`:

```
[tool.flet]compile.app = true # --compile-appcompile.packages = true # --compile-packagescompile.cleanup = true # --cleanup-on-compile
```

## Permissions[​](#permissions "Direct link to Permissions")

`flet build` command allows granular control over permissions, features and entitlements embedded into `AndroidManifest.xml`, `Info.plist` and `.entitlements` files.

See platform guides for setting specific [iOS](/docs/publish/ios), [Android](/docs/publish/android) and [macOS](/docs/publish/macos) permissions.

### Cross-platform permissions[​](#cross-platform-permissions "Direct link to Cross-platform permissions")

There are pre-defined permissions that mapped to `Info.plist`, `*.entitlements` and `AndroidManifest.xml` for respective platforms.

Setting cross-platform permissions:

```
flet build --permissions permission_1 permission_2 ...
```

Supported permissions:

-   `location`
-   `camera`
-   `microphone`
-   `photo_library`

#### iOS mapping to `Info.plist` entries[​](#ios-mapping-to-infoplist-entries "Direct link to ios-mapping-to-infoplist-entries")

-   `location`
    -   `NSLocationWhenInUseUsageDescription = This app uses location service when in use.`
    -   `NSLocationAlwaysAndWhenInUseUsageDescription = This app uses location service.`
-   `camera`
    -   `NSCameraUsageDescription = This app uses the camera to capture photos and videos.`
-   `microphone`
    -   `NSMicrophoneUsageDescription = This app uses microphone to record sounds.`
-   `photo_library`
    -   `NSPhotoLibraryUsageDescription = This app saves photos and videos to the photo library.`

#### macOS mapping to entitlements[​](#macos-mapping-to-entitlements "Direct link to macOS mapping to entitlements")

-   `location`
    -   `com.apple.security.personal-information.location = True`
-   `camera`
    -   `com.apple.security.device.camera = True`
-   `microphone`
    -   `com.apple.security.device.audio-input = True`
-   `photo_library`
    -   `com.apple.security.personal-information.photos-library = True`

#### Android mappings[​](#android-mappings "Direct link to Android mappings")

-   `location`
    -   permissions:
        -   `android.permission.ACCESS_FINE_LOCATION": True`
        -   `android.permission.ACCESS_COARSE_LOCATION": True`
        -   `android.permission.ACCESS_BACKGROUND_LOCATION": True`
    -   features:
        -   `android.hardware.location.network": False`
        -   `android.hardware.location.gps": False`
-   `camera`
    -   permissions:
        -   `android.permission.CAMERA": True`
    -   features:
        -   `android.hardware.camera": False`
        -   `android.hardware.camera.any": False`
        -   `android.hardware.camera.front": False`
        -   `android.hardware.camera.external": False`
        -   `android.hardware.camera.autofocus": False`
-   `microphone`
    -   permissions:
        -   `android.permission.RECORD_AUDIO": True`
        -   `android.permission.WRITE_EXTERNAL_STORAGE": True`
        -   `android.permission.READ_EXTERNAL_STORAGE": True`
-   `photo_library`
    -   permissions:
        -   `android.permission.READ_MEDIA_VISUAL_USER_SELECTED": True`

Configuring cross-platform permissions in `pyproject.toml`:

```
[tool.flet]permissions = ["camera", "microphone"]
```

## Versioning[​](#versioning "Direct link to Versioning")

You can provide a version information for built executable or package with `--build-number` and `--build-version` arguments. This is the information that is used to distinguish one build/release from another in App Store and Google Play and is shown to the user in about dialogs.

`--build-number` - an integer number (defaults to `1`), an identifier used as an internal version number. Each build must have a unique identifier to differentiate it from previous builds. It is used to determine whether one build is more recent than another, with higher numbers indicating more recent build.

`--build-version` - a "x.y.z" string (defaults to `1.0.0`) used as the version number shown to users. For each new version of your app, you will provide a version number to differentiate it from previous versions.

Configuring display version and version number in `pyproject.toml`:

```
[project]name = "my_app"version = "1.0.0"description = "My Flet app"authors = [  {name = "John Smith", email = "john@email.com"}]dependencies = ["flet==0.25.0"][tool.flet]build_number = 1
```

## Customizing packaging template[​](#customizing-packaging-template "Direct link to Customizing packaging template")

To create a temporary Flutter project `flet build` uses [cookiecutter](https://cookiecutter.readthedocs.io/en/stable/) template stored in [https://github.com/flet-dev/flet-build-template](https://github.com/flet-dev/flet-build-template) repository.

You can customize that template to suit your specific needs and then use it with `flet build`.

`--template` option can be used to provide the URL to the repository or path to a directory with your own template. Use `gh:` prefix for GitHub repos, e.g. `gh:{my-org}/{my-repo}` or provide a full path to a Git repository, e.g. `https://github.com/{my-org}/{my-repo}.git`.

For Git repositories you can checkout specific branch/tag/commit with `--template-ref` option.

`--template-dir` option specifies a relative path to a cookiecutter template in a repository given by `--template` option. When `--template` option is not used, this option specifies path relative to the `<user-directory>/.cookiecutters/flet-build-template`.

Configuring template in `pyproject.toml`:

```
[tool.flet.template]path = "gh:some-github/repo" # --templatedir = "" # --template-dirref = "" # --template-ref
```

## Extra args to `flutter build` command[​](#extra-args-to-flutter-build-command "Direct link to extra-args-to-flutter-build-command")

`--flutter-build-args` option allows passing extra arguments to `flutter build` command called during the build process. The option can be used multiple times.

For example, if you want to add `--no-tree-shake-icons` option:

```
flet build macos --flutter-build-args=--no-tree-shake-icons
```

To pass an option with a value:

```
flet build ipa --flutter-build-args=--export-method --flutter-build-args=development
```

Configuring Flutter build extra args:

```
[tool.flet]flutter.build_args = [    "--some-flutter-arg-1",    "--some-flutter-arg-2"]
```

## Verbose logging[​](#verbose-logging "Direct link to Verbose logging")

`--verbose` or `-vv` option allows to see the output of all commands during `flet build` run. We might ask for a detailed log if you need support.

## Console output[​](#console-output "Direct link to Console output")

All Flet apps output to `stdout` and `stderr` (e.g. all `print()` statements or `sys.stdout.write()` calls, Python `logging` library) is now redirected to `console.log` file with a full path to it stored in `FLET_APP_CONSOLE` environment variable.

Writes to that file are unbuffered, so you can retrieve a log in your Python program at any moment with a simple:

```
with open(os.getenv("FLET_APP_CONSOLE"), "r") as f:    log = f.read()
```

`AlertDialog` or any other control can be used to display the value of `log` variable.

When the program is terminated by calling `sys.exit()` with exit code `100` (magic code) the entire log will be displayed in a scrollable window.

```
import syssys.exit(100)
```

Calling `sys.exit()` with any other exit code will terminate (close) the app without displaying a log.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/index.md)

[

Previous

Async apps

](/docs/getting-started/async-apps)[

Next

Android

](/docs/publish/android)

-   [Introduction](#introduction)
-   [Platform matrix](#platform-matrix)
-   [Prerequisites](#prerequisites)
    -   [Flutter SDK](#flutter-sdk)
-   [Project structure](#project-structure)
-   [How it works](#how-it-works)
-   [Including optional controls](#including-optional-controls)
-   [Icons](#icons)
-   [Splash screen](#splash-screen)
-   [Entry point](#entry-point)
-   [Compilation and cleanup](#compilation-and-cleanup)
-   [Permissions](#permissions)
    -   [Cross-platform permissions](#cross-platform-permissions)
-   [Versioning](#versioning)
-   [Customizing packaging template](#customizing-packaging-template)
-   [Extra args to `flutter build` command](#extra-args-to-flutter-build-command)
-   [Verbose logging](#verbose-logging)
-   [Console output](#console-output)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Packaging app for Android | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/android/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/android/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/android/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/android/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Publishing Flet app](/docs/publish)
-   Android

On this page

# Packaging app for Android

## Introduction[​](#introduction "Direct link to Introduction")

Flet CLI provides `flet build apk` and `flet build aab` commands that allow packaging Flet app into Android APK and Android App Bundle (AAB) respectively.

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

### Android SDK[​](#android-sdk "Direct link to Android SDK")

Java (JDK) and Android SDK will be automatically installed on the first run of `flet build` command.

JDK is installed into `$HOME/java/{version}` directory.

If you have Android Studio installed Flet CLI will locate and use Android SDK coming with the studio; otherwise Android SDK will be installed to `$HOME/Android/sdk` directory.

### Android wheels for binary Python packages[​](#android-wheels-for-binary-python-packages "Direct link to Android wheels for binary Python packages")

Binary Python packages (vs "pure" Python packages written in Python only) are packages that partially written in C, Rust or other languages producing native code. Example packages are `numpy`, `cryptography`, or `pydantic-core`.

Make sure all non-pure (binary) packages used in your Flet app have [pre-built wheels for Android](/docs/reference/binary-packages-android-ios).

## `flet build apk`[​](#flet-build-apk "Direct link to flet-build-apk")

Build an Android APK file from your app.

This command builds release version. 'release' builds don't support debugging and are suitable for deploying to app stores. If you are deploying the app to the Play Store, it's recommended to use Android App Bundles (AAB) or split the APK to reduce the APK size.

-   [https://developer.android.com/guide/app-bundle](https://developer.android.com/guide/app-bundle)
-   [https://developer.android.com/studio/build/configure-apk-splits#configure-abi-split](https://developer.android.com/studio/build/configure-apk-splits#configure-abi-split)

### Building platform-specific APKs[​](#building-platform-specific-apks "Direct link to Building platform-specific APKs")

By default, Flet builds "fat" APK which includes binaries for both `arm64-v8a` and `armeabi-v7a` architectures.

You can configure Flet to split fat APK into smaller APKs for each platformby using `--split-per-abi` option or by setting `split_per_abi` in `pyproject.toml`:

```
[tool.flet.android]split_per_abi = true
```

### Installing APK to a device[​](#installing-apk-to-a-device "Direct link to Installing APK to a device")

The easiest way to install APK to your device is to use `adb` (Android Debug Bridge) tool.

`adb` is a part of Android SDK. For example, on macOS, if Android SDK was installed with Android Studio the location of `adb` tool will be at `~/Library/Android/sdk/platform-tools/adb`.

[Check this article](https://www.makeuseof.com/install-apps-via-adb-android/) for more information about installing and using `adb` tool on various platforms.

To install APK to a device run the following command:

```
adb install <path-to-your.apk>
```

If more than one device is connected to your computer (say, emulator and a physical phone) you can use `-s` option to specify which device you want to install `.apk` on:

```
adb -s <device> install <path-to-your.apk>
```

where `<device>` can be found with `adb devices` command.

## `flet build aab`[​](#flet-build-aab "Direct link to flet-build-aab")

Build an Android App Bundle (AAB) file from your app.

This command builds release version. 'release' builds don't support debugging and are suitable for deploying to app stores. App bundle is the recommended way to publish to the Play Store as it improves your app size.

## Signing Android bundle[​](#signing-android-bundle "Direct link to Signing Android bundle")

TBD

```
[tool.flet.android.signing]# store and key passwords can be passed with `--android-signing-key-store-password`# and `--android-signing-key-password` options or# FLET_ANDROID_SIGNING_KEY_STORE_PASSWORD# and FLET_ANDROID_SIGNING_KEY_PASSWORD environment variables.key_store = "path/to/store.jks" # --android-signing-key-storekey_alias = "upload"
```

## Splash screen[​](#splash-screen "Direct link to Splash screen")

By default, generated Android app will be showing a splash screen with an image from `assets` directory (see below) or Flet logo. You can disable splash screen for Android app with `--no-android-splash` option.

Configuring splash in `pyproject.toml`:

```
[tool.flet.splash]android = false
```

## Permissions[​](#permissions "Direct link to Permissions")

Configuring Android permissions and features to be written into `AndroidManifest.xml`:

```
flet build --android-permissions permission=True|False ... --android-features feature_name=True|False
```

For example:

```
flet build \    --android-permissions android.permission.READ_EXTERNAL_STORAGE=True \      android.permission.WRITE_EXTERNAL_STORAGE=True \    --android-features android.hardware.location.network=False
```

Default Android permissions:

-   `android.permission.INTERNET`

Default permissions can be disabled with `--android-permissions` option and `False` value, for example:

```
flet build --android-permissions android.permission.INTERNET=False
```

Default Android features:

-   `android.software.leanback=False` (`False` means it's written in manifest as `android:required="false"`)
-   `android.hardware.touchscreen=False`

Configuring permissions and features in `pyproject.toml` (notice quotes `"` around key names):

```
[tool.flet.android.permission] # --android-permissions"android.permission.CAMERA" = true"android.permission.CAMERA" = true[tool.flet.android.feature] # --android-features"android.hardware.camera" = false
```

## Meta-data[​](#meta-data "Direct link to Meta-data")

Configuring Android app meta-data to be written into `AndroidManifest.xml`:

```
flet build --android-meta-data name_1=value_1 name_2=value_2 ...
```

Default Android meta-data:

-   `io.flutter.embedding.android.EnableImpeller=false`

Configuring meta-data in `pyproject.toml` (notice quotes `"` around key names):

```
[tool.flet.android.meta_data]"com.google.android.gms.ads.APPLICATION_ID" = "ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy"
```

## Deep linking[​](#deep-linking "Direct link to Deep linking")

You can configure deep-linking settings for Android app with the following `flet build` options:

-   `--deep-linking-scheme` - deep linking URL scheme to configure for Android builds, i.g. "https" or "myapp".
-   `--deep-linking-host` - deep linking URL host.

The same can be configured in `pyproject.toml`:

```
[tool.flet.android.deep_linking]scheme = "https"host = "mydomain.com"
```

See [Deep linking](https://docs.flutter.dev/ui/navigation/deep-linking) section in Flutter docs for more information and complete setup guide.

## Troubleshooting Android[​](#troubleshooting-android "Direct link to Troubleshooting Android")

To run interactive commands inside simulator or device:

```
adb shell
```

To overcome "permissions denied" error while trying to browse file system in interactive Android shell:

```
su
```

To download a file from a device to your local computer:

```
adb pull <device-path> <local-path>
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/android.md)

[

Previous

Publishing Flet app to multiple platforms

](/docs/publish)[

Next

iOS

](/docs/publish/ios)

-   [Introduction](#introduction)
-   [Prerequisites](#prerequisites)
    -   [Android SDK](#android-sdk)
    -   [Android wheels for binary Python packages](#android-wheels-for-binary-python-packages)
-   [`flet build apk`](#flet-build-apk)
    -   [Building platform-specific APKs](#building-platform-specific-apks)
    -   [Installing APK to a device](#installing-apk-to-a-device)
-   [`flet build aab`](#flet-build-aab)
-   [Signing Android bundle](#signing-android-bundle)
-   [Splash screen](#splash-screen)
-   [Permissions](#permissions)
-   [Meta-data](#meta-data)
-   [Deep linking](#deep-linking)
-   [Troubleshooting Android](#troubleshooting-android)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Packaging app for macOS | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/macos/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/macos/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/macos/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/macos/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Publishing Flet app](/docs/publish)
-   macOS

On this page

# Packaging app for macOS

Flet CLI provides `flet build macos` command that allows packaging Flet app into a macOS application bundle.

note

The command can be run on macOS only.

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

## Prerequisites[​](#prerequisites-1 "Direct link to Prerequisites")

### Rosetta 2[​](#rosetta-2 "Direct link to Rosetta 2")

Flutter requires [Rosetta 2](https://support.apple.com/en-us/HT211861) on Apple silicon:

```
sudo softwareupdate --install-rosetta --agree-to-license
```

### Xcode[​](#xcode "Direct link to Xcode")

[Xcode](https://developer.apple.com/xcode/) 15 or later to compile native Swift or ObjectiveC code.

### CocoaPods[​](#cocoapods "Direct link to CocoaPods")

[CocoaPods](https://cocoapods.org/) 1.16 to compile and enable Flutter plugins.

## `flet build macos`[​](#flet-build-macos "Direct link to flet-build-macos")

Creates a macOS application bundle from your Flet app.

## Bundle architecture[​](#bundle-architecture "Direct link to Bundle architecture")

By default, `flet build macos` command builds universal app bundle that works on both Apple Silicon and older Intel processors. Therefore, packaging utility will try to download Python binary wheels for both `arm64` and `x86_64` platforms. Recent releases of some popular packages do not include `x86_64` wheels anymore, so the entire packaging operation will fail.

You can limit the build command to a specific architecture only, by using `--arch` option. For example, to build macOS app bundle that works on Apple Silicon only use the following command:

```
flet build macos --arch arm64
```

The same can be configured in `pyproject.toml`:

```
[tool.flet.macos]build_arch = "arm64"
```

## Permissions[​](#permissions "Direct link to Permissions")

Setting macOS entitlements which are written and `.entitlements` files:

```
flet build --macos-entitlements name_1=True|False name_2=True|False ...
```

Default macOS entitlements:

-   `com.apple.security.app-sandbox = False`
-   `com.apple.security.cs.allow-jit = True`
-   `com.apple.security.network.client = True`
-   `com.apple.security.network.server" = True`

Configuring macOS app entitlements in `pyproject.toml` (notice `"` around entitlement name):

```
[tool.flet.macos]entitlement."com.apple.security.personal-information.photos-library" = true
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/macos.md)

[

Previous

iOS

](/docs/publish/ios)[

Next

Linux

](/docs/publish/linux)

-   [Prerequisites](#prerequisites)
-   [Prerequisites](#prerequisites-1)
    -   [Rosetta 2](#rosetta-2)
    -   [Xcode](#xcode)
    -   [CocoaPods](#cocoapods)
-   [`flet build macos`](#flet-build-macos)
-   [Bundle architecture](#bundle-architecture)
-   [Permissions](#permissions)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Flet   

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/linux/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/linux/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/linux/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/linux/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Publishing Flet app](/docs/publish)
-   Linux

On this page

# Packaging app for Linux

Flet CLI provides `flet build linux` command that allows packaging Flet app into a Linux application.

note

The command can be run on Linux only.

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

### GStreamer for `Audio`[​](#gstreamer-for-audio "Direct link to gstreamer-for-audio")

[GStreamer](https://gstreamer.freedesktop.org/) libraries must be installed if your Flet app uses `Audio` control.

To install minimal set of GStreamer libs on Ubuntu/Debian run the following commands:

```
apt install libgtk-3-dev libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev
```

To install full set of GStreamer libs:

```
apt install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-doc gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio
```

See [this guide](https://gstreamer.freedesktop.org/documentation/installing/on-linux.html?gi-language=c) for installing on other Linux distributives.

To build your Flet app that uses `Audio` control add `--include-packages flet_audio` to `flet build` command, for example:

```
flet build apk --include-packages flet_audio
```

### MPV for `Video`[​](#mpv-for-video "Direct link to mpv-for-video")

[libmpv](https://mpv.io/) libraries must be installed if your Flet app uses `Video` control. On Ubuntu/Debian you can install it with:

```
sudo apt install libmpv-dev mpv
```

To build your Flet app that uses `Video` control add `--include-packages flet_video` to `flet build` command, for example:

```
flet build apk --include-packages flet_video
```

## `flet build linux`[​](#flet-build-linux "Direct link to flet-build-linux")

Creates a Linux application from your Flet app.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/linux.md)

[

Previous

macOS

](/docs/publish/macos)[

Next

Windows

](/docs/publish/windows)

-   [Prerequisites](#prerequisites)
    -   [GStreamer for `Audio`](#gstreamer-for-audio)
    -   [MPV for `Video`](#mpv-for-video)
-   [`flet build linux`](#flet-build-linux)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Packaging app for Windows | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/windows/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/windows/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/windows/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/windows/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Publishing Flet app](/docs/publish)
-   Windows

On this page

# Packaging app for Windows

Flet CLI provides `flet build windows` command that allows packaging Flet app into a Windows application.

note

The command can be run on Windows only.

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

### Visual Studio 2022[​](#visual-studio-2022 "Direct link to Visual Studio 2022")

Building Flet app for Windows desktop requires [Visual Studio 2022](https://learn.microsoft.com/visualstudio/install/install-visual-studio?view=vs-2022) with **Desktop development with C++** workload installed.

[Follow this medium article](https://medium.com/@teamcode20233/a-guide-to-install-desktop-development-with-c-workload-542bb92cfe90) for the instructions on downloading & installing correct Visual Studio components for Flutter desktop development.

### Enable Developer Mode[​](#enable-developer-mode "Direct link to Enable Developer Mode")

While running `flet build` on Windows you may get the following error:

```
Building with plugins requires symlink support.Please enable Developer Mode in your system settings. Run  start ms-settings:developersto open settings.
```

[Follow this SO answer](https://stackoverflow.com/a/70994092/1435891) for the instructions on how to enable developer mode in Windows 11.

## `flet build windows`[​](#flet-build-windows "Direct link to flet-build-windows")

Creates a Windows application from your Flet app.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/windows.md)

[

Previous

Linux

](/docs/publish/linux)[

Next

Web

](/docs/publish/web)

-   [Prerequisites](#prerequisites)
    -   [Visual Studio 2022](#visual-studio-2022)
    -   [Enable Developer Mode](#enable-developer-mode)
-   [`flet build windows`](#flet-build-windows)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Publishing Flet app to web | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/web/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/web/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/web/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/web/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
        -   [Static website](/docs/publish/web/static-website)
            
        -   [Dynamic website](/docs/publish/web/dynamic-website)
            
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Publishing Flet app](/docs/publish)
-   Web

# Publishing Flet app to web

Flet allows publishing your app as a **static** or **dynamic** website.

**Static website** - content is not changing and delivered exactly as it's stored. Python code is running in the web browser.

**Dynamic website** - content is dynamically generated for each user. Python code is running on the server.

Here is a table comparing Flet app running as a static vs dynamic website:

[Static website](/docs/publish/web/static-website)

[Dynamic website](/docs/publish/web/dynamic-website)

**Loading time**

⬇️ Slower - Python runtime (Pyodide) along with app's Python code and all its dependencies must be loaded into the browser. Pyodide initialization takes time too.

✅ Faster - the app stays and runs on the server.

**Python compatibility**

⬇️ Not every program that works with native Python [can be run with Pyodide](https://pyodide.org/en/stable/usage/wasm-constraints.html)

✅ Any Python package can be used.

**Responsiveness**

✅ Zero latency between user-generated events (clicks, text field changes, drags) and page updates.

⬇️ Non-zero latency - user-generated events are communicated to a server via WebSockets. UI updates are communicated back.

**Performance**

⬇️ Slower - Pyodide is currently 3x-5x slower than native Python because of WASM

✅ Faster - the code is running on the server by native Python.

**Code protection**

⬇️ Low - app's code is loaded into a web browser and can be inspected by a user.

✅ High - the app is running on the server.

**Hosting**

✅ Cheap/Free - no code is running on the server and thus the app can be hosted anywhere: GitHub Pages, Cloudflare Pages, Replit, Vercel, a shared hosting or your own VPS.

⬇️ Paid - the app requires Python code to run on the server and communicate with a web browser via WebSockets.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/web/index.md)

[

Previous

Windows

](/docs/publish/windows)[

Next

Static website

](/docs/publish/web/static-website)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Layout | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/layout/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/layout/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/layout/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/layout/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   Layout

# Layout

[

## 📄️ Card

A material design card: a panel with slightly rounded corners and an elevation shadow.

](/docs/controls/card)

[

## 📄️ Column

A control that displays its children in a vertical array.

](/docs/controls/column)

[

## 📄️ Container

Container allows to decorate a control with background color and border and position it with padding, margin and alignment.

](/docs/controls/container)

[

## 📄️ CupertinoListTile

An iOS-style list tile. The CupertinoListTile is a Cupertino equivalent of Material ListTile.

](/docs/controls/cupertinolisttile)

[

## 📄️ DataTable

A Material Design data table.

](/docs/controls/datatable)

[

## 📄️ Dismissible

A control that can be dismissed by dragging in the indicated dismiss\_direction.

](/docs/controls/dismissible)

[

## 📄️ Divider

A thin horizontal line, with padding on either side.

](/docs/controls/divider)

[

## 📄️ ExpansionPanelList

A material expansion panel list that lays out its children and animates expansions.

](/docs/controls/expansionpanel)

[

## 📄️ ExpansionTile

A single-line ListTile with an expansion arrow icon that expands or collapses the tile to reveal or hide its children.

](/docs/controls/expansiontile)

[

## 📄️ GridView

A scrollable, 2D array of controls.

](/docs/controls/gridview)

[

## 📄️ ListTile

A single fixed-height row that typically contains some text as well as a leading or trailing icon.

](/docs/controls/listtile)

[

## 📄️ ListView

A scrollable list of controls arranged linearly.

](/docs/controls/listview)

[

## 📄️ Page

Page is a container for View controls.

](/docs/controls/page)

[

## 📄️ Pagelet

Pagelet implements the basic Material Design visual layout structure.

](/docs/controls/pagelet)

[

## 📄️ Placeholder

A control that draws a box that represents where other widgets will one day be added.

](/docs/controls/placeholder)

[

## 📄️ ReorderableListView

A control that allows the user to reorder its children by dragging a handle.

](/docs/controls/reorderablelistview)

[

## 📄️ ResponsiveRow

ResponsiveRow borrows the idea of grid layout from Bootstrap web framework.

](/docs/controls/responsiverow)

[

## 📄️ Row

A control that displays its children in a horizontal array.

](/docs/controls/row)

[

## 📄️ SafeArea

A control that insets its content by sufficient padding to avoid intrusions by the operating system.

](/docs/controls/safearea)

[

## 📄️ Stack

A control that positions its children on top of each other.

](/docs/controls/stack)

[

## 📄️ Tabs

The Tabs control is used for navigating frequently accessed, distinct content categories. Tabs allow for navigation between two or more content views and relies on text headers to articulate the different sections of content.

](/docs/controls/tabs)

[

## 📄️ VerticalDivider

A thin vertical line, with padding on either side.

](/docs/controls/verticaldivider)

[

## 📄️ View

View is the top most container for all other controls.

](/docs/controls/view)

[

Previous

Controls reference

](/docs/controls)[

Next

Card

](/docs/controls/card)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  TextSourceAttribution | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/maptextsourceattribution/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/maptextsourceattribution/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/maptextsourceattribution/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/maptextsourceattribution/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   TextSourceAttribution

On this page

# TextSourceAttribution

A text source attribution displayed on the Map.

Can be used in [`RichAttribution.attributions`](/docs/controls/maprichattribution) list.

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## Properties[​](#properties "Direct link to Properties")

### `prepend_copyright`[​](#prepend_copyright "Direct link to prepend_copyright")

Whether to add the '©' character to the start of the `text`.

Defaults to `True`.

### `text`[​](#text "Direct link to text")

The text of the source attribution styled with `text_style`.

### `text_style`[​](#text_style "Direct link to text_style")

The style of the text.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when the attribution source is clicked or tapped.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/maptextsourceattribution.md)

[

Previous

TileLayer

](/docs/controls/maptilelayer)[

Next

Markdown

](/docs/controls/markdown)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`prepend_copyright`](#prepend_copyright)
    -   [`text`](#text)
    -   [`text_style`](#text_style)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Markdown | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/markdown/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/markdown/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/markdown/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/markdown/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Markdown

On this page

# Markdown

Control for rendering text in markdown format.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/markdown)

### Markdown with GitHubWeb extensions and clickable links[​](#markdown-with-githubweb-extensions-and-clickable-links "Direct link to Markdown with GitHubWeb extensions and clickable links")

-   Python

```
import flet as ftmd1 = """# Markdown ExampleMarkdown allows you to easily include formatted text, images, and even formatted Dart code in your app.## TitlesSetext-styleThis is an H1=============This is an H2-------------Atx-style# This is an H1## This is an H2###### This is an H6Select the valid headers:- [x] `# hello`- [ ] `#hello`## Links[inline-style](https://www.google.com)## Images![Image from Flet assets](https://flet.dev/docs/controls/markdown/icons/icon-192.png)![Test image](https://picsum.photos/200/300)## Tables|Syntax                                 |Result                               ||---------------------------------------|-------------------------------------||`*italic 1*`                           |*italic 1*                           ||`_italic 2_`                           | _italic 2_                          ||`**bold 1**`                           |**bold 1**                           ||`__bold 2__`                           |__bold 2__                           ||`This is a ~~strikethrough~~`          |This is a ~~strikethrough~~          ||`***italic bold 1***`                  |***italic bold 1***                  ||`___italic bold 2___`                  |___italic bold 2___                  ||`***~~italic bold strikethrough 1~~***`|***~~italic bold strikethrough 1~~***||`~~***italic bold strikethrough 2***~~`|~~***italic bold strikethrough 2***~~|## StylingStyle text as _italic_, __bold__, ~~strikethrough~~, or `inline code`.- Use bulleted lists- To better clarify- Your points## Code blocksFormatted Dart code looks really pretty too:```void main() {  runApp(MaterialApp(    home: Scaffold(      body: ft.Markdown(data: markdownData),    ),  ));}```"""def main(page: ft.Page):    page.scroll = "auto"    page.add(        ft.Markdown(            md1,            selectable=True,            extension_set=ft.MarkdownExtensionSet.GITHUB_WEB,            on_tap_link=lambda e: page.launch_url(e.data),        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/markdown/img/docs/controls/markdown/custom-markdown.gif)

### Markdown with code syntax highlight[​](#markdown-with-code-syntax-highlight "Direct link to Markdown with code syntax highlight")

[Source code](https://github.com/flet-dev/examples/blob/main/python/controls/markdown/markdown-code-highlight.py)

![](https://flet.dev/docs/controls/markdown/img/docs/controls/markdown/markdown-highlight.png)

## Properties[​](#properties "Direct link to Properties")

### `auto_follow_links`[​](#auto_follow_links "Direct link to auto_follow_links")

Automatically open URLs in the document. Default is `False`. If registered, `on_tap_link` event is fired after that.

### `auto_follow_links_target`[​](#auto_follow_links_target "Direct link to auto_follow_links_target")

Where to open URL in the web mode

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.SELF`.

### `code_style_sheet`[​](#code_style_sheet "Direct link to code_style_sheet")

The styles to use when displaying the code blocks.

Value is of type [`MarkdownStyleSheet`](/docs/reference/types/markdownstylesheet).

### `code_theme`[​](#code_theme "Direct link to code_theme")

A syntax highlighting theme for code blocks.

Value is of type [`MarkdownCodeTheme`](/docs/reference/types/markdowncodetheme) and defaults to `MarkdownCodeTheme.GITHUB`.

### `extension_set`[​](#extension_set "Direct link to extension_set")

The extensions to use when rendering the markdown content.

Value is of type [`MarkdownExtensionSet`](/docs/reference/types/markdownextensionset) and defaults to `MarkdownExtensionSet.NONE`.

### `fit_content`[​](#fit_content "Direct link to fit_content")

Whether to allow the widget to fit the child content.

Value is of type `bool` and defaults to `True`.

### `img_error_content`[​](#img_error_content "Direct link to img_error_content")

The `Control` to display when an image fails to load.

### `md_style_sheet`[​](#md_style_sheet "Direct link to md_style_sheet")

The styles to use when displaying the markdown.

Value is of type [`MarkdownStyleSheet`](/docs/reference/types/markdownstylesheet).

### `selectable`[​](#selectable "Direct link to selectable")

Whether rendered text is selectable or not.

### `shrink_wrap`[​](#shrink_wrap "Direct link to shrink_wrap")

Whether the extent of the scroll view in the scroll direction should be determined by the contents being viewed.

Value is of type `bool` and defaults to `True`.

### `soft_line_break`[​](#soft_line_break "Direct link to soft_line_break")

The soft line break is used to identify the spaces at the end of aline of text and the leading spaces in the immediately following the line of text.

Value is of type `bool` and defaults to `False`.

### `value`[​](#value "Direct link to value")

Markdown content to render.

## Events[​](#events "Direct link to Events")

### `on_tap_link`[​](#on_tap_link "Direct link to on_tap_link")

Fires when a link within Markdown document is clicked/tapped. `data` property of event contains URL.

The following example opens markdown URLs in a new window:

```
import flet as ftdef main(page: ft.Page):    def open_url(e):        page.launch_url(e.data)    page.add(        ft.Markdown(            "[inline-style](https://www.google.com)",            extension_set="gitHubWeb",            on_tap_link=open_url,            expand=True,        ),    )ft.app(main)
```

### `on_selection_change`[​](#on_selection_change "Direct link to on_selection_change")

Fires when the text selection changes.

Event handler argument is of type [`MarkdownSelectionChangeEvent`](/docs/reference/types/markdownselectionchangeevent).

### `on_tap_text`[​](#on_tap_text "Direct link to on_tap_text")

Fires when some text is clicked/tapped.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/markdown.md)

[

Previous

TextSourceAttribution

](/docs/controls/maptextsourceattribution)[

Next

Text

](/docs/controls/text)

-   [Examples](#examples)
    -   [Markdown with GitHubWeb extensions and clickable links](#markdown-with-githubweb-extensions-and-clickable-links)
    -   [Markdown with code syntax highlight](#markdown-with-code-syntax-highlight)
-   [Properties](#properties)
    -   [`auto_follow_links`](#auto_follow_links)
    -   [`auto_follow_links_target`](#auto_follow_links_target)
    -   [`code_style_sheet`](#code_style_sheet)
    -   [`code_theme`](#code_theme)
    -   [`extension_set`](#extension_set)
    -   [`fit_content`](#fit_content)
    -   [`img_error_content`](#img_error_content)
    -   [`md_style_sheet`](#md_style_sheet)
    -   [`selectable`](#selectable)
    -   [`shrink_wrap`](#shrink_wrap)
    -   [`soft_line_break`](#soft_line_break)
    -   [`value`](#value)
-   [Events](#events)
    -   [`on_tap_link`](#on_tap_link)
    -   [`on_selection_change`](#on_selection_change)
    -   [`on_tap_text`](#on_tap_text)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Text | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/text/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/text/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/text/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/text/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Text

On this page

# Text

Text is a control for displaying text.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/text)

### Custom text styles[​](#custom-text-styles "Direct link to Custom text styles")

![](https://flet.dev/docs/controls/text/img/docs/controls/text/custom-text-styles.gif)

```
import flet as ftdef main(page: ft.Page):    page.title = "Text custom styles"    page.scroll = "adaptive"    page.add(        ft.Text("Size 10", size=10),        ft.Text("Size 30, Italic", size=30, color="pink600", italic=True),        ft.Text(            "Size 40, w100",            size=40,            color=ft.Colors.WHITE,            bgcolor=ft.Colors.BLUE_600,            weight=ft.FontWeight.W_100,        ),        ft.Text(            "Size 50, Normal",            size=50,            color=ft.Colors.WHITE,            bgcolor=ft.Colors.ORANGE_800,            weight=ft.FontWeight.NORMAL,        ),        ft.Text(            "Size 60, Bold, Italic",            size=50,            color=ft.Colors.WHITE,            bgcolor=ft.Colors.GREEN_700,            weight=ft.FontWeight.BOLD,            italic=True,        ),        ft.Text("Size 70, w900, selectable", size=70, weight=ft.FontWeight.W_900, selectable=True),        ft.Text("Limit long text to 1 line with ellipsis", theme_style=ft.TextThemeStyle.HEADLINE_SMALL),        ft.Text(            "Proin rutrum, purus sit amet elementum volutpat, nunc lacus vulputate orci, cursus ultrices neque dui quis purus. Ut ultricies purus nec nibh bibendum, eget vestibulum metus various. Duis convallis maximus justo, eu rutrum libero maximus id. Donec ullamcorper arcu in sapien molestie, non pellentesque tellus pellentesque. Nulla nec tristique ex. Maecenas euismod nisl enim, a convallis arcu laoreet at. Ut at tortor finibus, rutrum massa sit amet, pulvinar velit. Phasellus diam lorem, viverra vitae leo vitae, consequat suscipit lorem.",            max_lines=1,            overflow=ft.TextOverflow.ELLIPSIS,        ),        ft.Text("Limit long text to 2 lines and fading", theme_style=ft.TextThemeStyle.HEADLINE_SMALL),        ft.Text(            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur quis nibh vitae purus consectetur facilisis sed vitae ipsum. Quisque faucibus sed nulla placerat sagittis. Phasellus condimentum risus vitae nulla vestibulum auctor. Curabitur scelerisque, nibh eget imperdiet consequat, odio ante tempus diam, sed volutpat nisl erat eget turpis. Sed viverra, diam sit amet blandit vulputate, mi tellus dapibus lorem, vitae vehicula diam mauris placerat diam. Morbi sit amet pretium turpis, et consequat ligula. Nulla velit sem, suscipit sit amet dictum non, tincidunt sed nulla. Aenean pellentesque odio porttitor sagittis aliquam. Name various at metus vitae vulputate. Praesent faucibus nibh lorem, eu pretium dolor dictum nec. Phasellus eget dui laoreet, viverra magna vitae, pellentesque diam.",            max_lines=2,        ),        ft.Text("Limit the width and height of long text", theme_style=ft.TextThemeStyle.HEADLINE_SMALL),        ft.Text(            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur quis nibh vitae purus consectetur facilisis sed vitae ipsum. Quisque faucibus sed nulla placerat sagittis. Phasellus condimentum risus vitae nulla vestibulum auctor. Curabitur scelerisque, nibh eget imperdiet consequat, odio ante tempus diam, sed volutpat nisl erat eget turpis. Sed viverra, diam sit amet blandit vulputate, mi tellus dapibus lorem, vitae vehicula diam mauris placerat diam. Morbi sit amet pretium turpis, et consequat ligula. Nulla velit sem, suscipit sit amet dictum non, tincidunt sed nulla. Aenean pellentesque odio porttitor sagittis aliquam. Name various at metus vitae vulputate. Praesent faucibus nibh lorem, eu pretium dolor dictum nec. Phasellus eget dui laoreet, viverra magna vitae, pellentesque diam.",            width=700,            height=100,        ),    )ft.app(main)
```

### Pre-defined theme text styles[​](#pre-defined-theme-text-styles "Direct link to Pre-defined theme text styles")

![](https://flet.dev/docs/controls/text/img/docs/controls/text/predefined-text-styles.png)

```
import flet as ftdef main(page: ft.Page):    page.title = "Text theme styles"    page.scroll = "adaptive"    page.add(        ft.Text("Display Large", theme_style=ft.TextThemeStyle.DISPLAY_LARGE),        ft.Text("Display Medium", theme_style=ft.TextThemeStyle.DISPLAY_MEDIUM),        ft.Text("Display Small", theme_style=ft.TextThemeStyle.DISPLAY_SMALL),        ft.Text("Headline Large", theme_style=ft.TextThemeStyle.HEADLINE_LARGE),        ft.Text("Headline Medium", theme_style=ft.TextThemeStyle.HEADLINE_MEDIUM),        ft.Text("Headline Small", theme_style=ft.TextThemeStyle.HEADLINE_SMALL),        ft.Text("Title Large", theme_style=ft.TextThemeStyle.TITLE_LARGE),        ft.Text("Title Medium", theme_style=ft.TextThemeStyle.TITLE_MEDIUM),        ft.Text("Title Small", theme_style=ft.TextThemeStyle.TITLE_SMALL),        ft.Text("Label Large", theme_style=ft.TextThemeStyle.LABEL_LARGE),        ft.Text("Label Medium", theme_style=ft.TextThemeStyle.LABEL_MEDIUM),        ft.Text("Label Small", theme_style=ft.TextThemeStyle.LABEL_SMALL),        ft.Text("Body Large", theme_style=ft.TextThemeStyle.BODY_LARGE),        ft.Text("Body Medium", theme_style=ft.TextThemeStyle.BODY_MEDIUM),        ft.Text("Body Small", theme_style=ft.TextThemeStyle.BODY_SMALL),    )ft.app(main)
```

### Font with variable weight[​](#font-with-variable-weight "Direct link to Font with variable weight")

![](https://flet.dev/docs/controls/text/img/docs/controls/text/variable-weight-font.gif)

```
import flet as ftdef main(page: ft.Page):    page.fonts = {        "RobotoSlab": "https://github.com/google/fonts/raw/main/apache/robotoslab/RobotoSlab%5Bwght%5D.ttf"    }    t = ft.Text(        "This is rendered with Roboto Slab",        size=30,        font_family="RobotoSlab",        weight=ft.FontWeight.W_100,    )    def width_changed(e):        t.weight = f"w{int(e.control.value)}"        t.update()    page.add(        t,        ft.Slider(            min=100,            max=900,            divisions=8,            label="{value}",            width=500,            on_change=width_changed,        ),    )ft.app(main)
```

### Rich text basics[​](#rich-text-basics "Direct link to Rich text basics")

![](https://flet.dev/docs/controls/text/img/docs/controls/text/richtext.png)

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Text("Plain text with default style"),        ft.Text(            "Some text",            size=30,            spans=[                ft.TextSpan(                    "here goes italic",                    ft.TextStyle(italic=True, size=20, color=ft.Colors.GREEN),                    spans=[                        ft.TextSpan(                            "bold and italic",                            ft.TextStyle(weight=ft.FontWeight.BOLD),                        ),                        ft.TextSpan(                            "just italic",                            spans=[                                ft.TextSpan("smaller italic", ft.TextStyle(size=15))                            ],                        ),                    ],                )            ],        ),        ft.Text(            disabled=False,            spans=[                ft.TextSpan(                    "underlined and clickable",                    ft.TextStyle(decoration=ft.TextDecoration.UNDERLINE),                    on_click=lambda e: print(f"Clicked span: {e.control.uid}"),                    on_enter=lambda e: print(f"Entered span: {e.control.uid}"),                    on_exit=lambda e: print(f"Exited span: {e.control.uid}"),                ),                ft.TextSpan(" "),                ft.TextSpan(                    "underlined red wavy",                    ft.TextStyle(                        decoration=ft.TextDecoration.UNDERLINE,                        decoration_color=ft.Colors.RED,                        decoration_style=ft.TextDecorationStyle.WAVY,                    ),                    on_enter=lambda e: print(f"Entered span: {e.control.uid}"),                    on_exit=lambda e: print(f"Exited span: {e.control.uid}"),                ),                ft.TextSpan(" "),                ft.TextSpan(                    "overlined blue",                    ft.TextStyle(                        decoration=ft.TextDecoration.OVERLINE, decoration_color="blue"                    ),                ),                ft.TextSpan(" "),                ft.TextSpan(                    "overlined and underlined",                    ft.TextStyle(                        decoration=ft.TextDecoration.OVERLINE                        | ft.TextDecoration.UNDERLINE                    ),                ),                ft.TextSpan(" "),                ft.TextSpan(                    "line through thick",                    ft.TextStyle(                        decoration=ft.TextDecoration.LINE_THROUGH,                        decoration_thickness=3,                    ),                ),            ],        ),    )    def highlight_link(e):        e.control.style.color = ft.Colors.BLUE        e.control.update()    def unhighlight_link(e):        e.control.style.color = None        e.control.update()    page.add(        ft.Text(            disabled=False,            spans=[                ft.TextSpan("AwesomeApp 1.0 "),                ft.TextSpan(                    "Visit our website",                    ft.TextStyle(decoration=ft.TextDecoration.UNDERLINE),                    url="https://google.com",                    on_enter=highlight_link,                    on_exit=unhighlight_link,                ),                ft.TextSpan(" All rights reserved. "),                ft.TextSpan(                    "Documentation",                    ft.TextStyle(decoration=ft.TextDecoration.UNDERLINE),                    url="https://google.com",                    on_enter=highlight_link,                    on_exit=unhighlight_link,                ),            ],        ),    )ft.app(main)
```

### Rich text with borders and stroke[​](#rich-text-with-borders-and-stroke "Direct link to Rich text with borders and stroke")

![](https://flet.dev/docs/controls/text/img/docs/controls/text/richtext-borders-stroke.png)

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Stack(            [                ft.Text(                    spans=[                        ft.TextSpan(                            "Greetings, planet!",                            ft.TextStyle(                                size=40,                                weight=ft.FontWeight.BOLD,                                foreground=ft.Paint(                                    color=ft.Colors.BLUE_700,                                    stroke_width=6,                                    stroke_join=ft.StrokeJoin.ROUND,                                    style=ft.PaintingStyle.STROKE,                                ),                            ),                        ),                    ],                ),                ft.Text(                    spans=[                        ft.TextSpan(                            "Greetings, planet!",                            ft.TextStyle(                                size=40,                                weight=ft.FontWeight.BOLD,                                color=ft.Colors.GREY_300,                            ),                        ),                    ],                ),            ]        )    )ft.app(main)
```

### Rich text with gradient[​](#rich-text-with-gradient "Direct link to Rich text with gradient")

![](https://flet.dev/docs/controls/text/img/docs/controls/text/richtext-gradient.png)

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Text(            spans=[                ft.TextSpan(                    "Greetings, planet!",                    ft.TextStyle(                        size=40,                        weight=ft.FontWeight.BOLD,                        foreground=ft.Paint(                            gradient=ft.PaintLinearGradient(                                (0, 20), (150, 20), [ft.Colors.RED, ft.Colors.YELLOW]                            )                        ),                    ),                ),            ],        )    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Text background [color](/docs/reference/colors).

### `color`[​](#color "Direct link to color")

Text foreground [color](/docs/reference/colors).

### `font_family`[​](#font_family "Direct link to font_family")

System or custom font family to render text with. See [`Fonts`](/docs/controls/page#fonts) cookbook guide for instructions on how to import and use custom fonts in your application.

### `italic`[​](#italic "Direct link to italic")

`True` to use italic typeface.

Value is of type `bool` and defaults to `False`.

### `max_lines`[​](#max_lines "Direct link to max_lines")

An optional maximum number of lines for the text to span, wrapping if necessary. If the text exceeds the given number of lines, it will be truncated according to `overflow`.

If this is 1, text will not wrap. Otherwise, text will be wrapped at the edge of the box.

### `no_wrap`[​](#no_wrap "Direct link to no_wrap")

If `False` (default) the text should break at soft line breaks.

If `True`, the glyphs in the text will be positioned as if there was unlimited horizontal space.

Value is of type `bool` and defaults to `False`.

### `overflow`[​](#overflow "Direct link to overflow")

Controls how text overflows.

Value is of type [`TextOverflow`](/docs/reference/types/textoverflow) and defaults to `TextOverflow.FADE`.

### `rtl`[​](#rtl "Direct link to rtl")

`True` to set text direction to right-to-left.

Defaults to `False`.

### `selectable`[​](#selectable "Direct link to selectable")

Whether the text should be selectable.

Defaults to `False`.

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

An alternative semantics label for this text.

If present, the semantics of this control will contain this value instead of the actual text. This will overwrite any of the `TextSpan.semantics_label`s.

This is useful for replacing abbreviations or shorthands with the full text value:

Value is of type `str`.

```
ft.Text("$$", semantics_label="Double dollars")
```

### `size`[​](#size "Direct link to size")

Text size in virtual pixels.

Value is of type `OptionalNumber` and defaults to `14`.

### `spans`[​](#spans "Direct link to spans")

The list of [`TextSpan`](/docs/reference/types/textspan) objects to build a rich text paragraph.

### `style`[​](#style "Direct link to style")

The text's style.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

### `text_align`[​](#text_align "Direct link to text_align")

Text horizontal align.

Value is of type [`TextAlign`](/docs/reference/types/textalign) and defaults to `TextAlign.LEFT`.

### `theme_style`[​](#theme_style "Direct link to theme_style")

Pre-defined text style.

Value is of type [`TextThemeStyle`](/docs/reference/types/textthemestyle).

### `value`[​](#value "Direct link to value")

The text displayed.

Value is of type `str`.

### `weight`[​](#weight "Direct link to weight")

Font weight.

Value is of type [`FontWeight`](/docs/reference/types/fontweight) and defaults to `FontWeight.NORMAL`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/text.md)

[

Previous

Markdown

](/docs/controls/markdown)[

Next

ProgressBar

](/docs/controls/progressbar)

-   [Examples](#examples)
    -   [Custom text styles](#custom-text-styles)
    -   [Pre-defined theme text styles](#pre-defined-theme-text-styles)
    -   [Font with variable weight](#font-with-variable-weight)
    -   [Rich text basics](#rich-text-basics)
    -   [Rich text with borders and stroke](#rich-text-with-borders-and-stroke)
    -   [Rich text with gradient](#rich-text-with-gradient)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`font_family`](#font_family)
    -   [`italic`](#italic)
    -   [`max_lines`](#max_lines)
    -   [`no_wrap`](#no_wrap)
    -   [`overflow`](#overflow)
    -   [`rtl`](#rtl)
    -   [`selectable`](#selectable)
    -   [`semantics_label`](#semantics_label)
    -   [`size`](#size)
    -   [`spans`](#spans)
    -   [`style`](#style)
    -   [`text_align`](#text_align)
    -   [`theme_style`](#theme_style)
    -   [`value`](#value)
    -   [`weight`](#weight)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ProgressBar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/progressbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/progressbar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/progressbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/progressbar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   ProgressBar

On this page

# ProgressBar

A material design linear progress indicator, also known as a progress bar.

A control that shows progress along a line.

There are two kinds of linear progress indicators:

-   *Determinate*. Determinate progress indicators have a specific value at each point in time, and the value should increase monotonically from `0.0` to `1.0`, at which time the indicator is complete. To create a determinate progress indicator, use a non-null value between `0.0` and `1.0`.
-   *Indeterminate*. Indeterminate progress indicators do not have a specific value at each point in time and instead indicate that progress is being made without indicating how much progress remains. To create an indeterminate progress indicator, use a null value.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/progressbar)

-   Python

```
from time import sleepimport flet as ftdef main(page: ft.Page):    pb = ft.ProgressBar(width=400)    page.add(        ft.Text("Linear progress indicator", style="headlineSmall"),        ft.Column([ ft.Text("Doing something..."), pb]),        ft.Text("Indeterminate progress bar", style="headlineSmall"),        ft.ProgressBar(width=400, color="amber", bgcolor="#eeeeee"),    )    for i in range(0, 101):        pb.value = i * 0.01        sleep(0.1)        page.update()ft.app(main)
```

![](https://flet.dev/docs/controls/progressbar/img/docs/controls/progress-bar/custom-progress-bars.gif)

## Properties[​](#properties "Direct link to Properties")

### `value`[​](#value "Direct link to value")

The value of this progress indicator. A value of `0.0` means no progress and `1.0` means that progress is complete. The value will be clamped to be in the range `0.0` - `1.0`.

Defaults to `None`, meaning that this progress indicator is indeterminate - displays a predetermined animation that does not indicate how much actual progress is being made.

### `bar_height`[​](#bar_height "Direct link to bar_height")

The minimum height of the line used to draw the linear indicator.

Defaults to `4`.

### `border_radius`[​](#border_radius "Direct link to border_radius")

The border radius of both the indicator and the track. Border radius is an instance of [`BorderRadius`](/docs/reference/types/borderradius) class.

Defaults to `border_radius.all(0)` - rectangular shape.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

[Color](/docs/reference/colors) of the track being filled by the linear indicator.

### `color`[​](#color "Direct link to color")

The progress indicator's [color](/docs/reference/colors).

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

The [`Semantics.label`](/docs/controls/semantics#label) for this progress indicator.

### `semantics_value`[​](#semantics_value "Direct link to semantics_value")

The [`Semantics.value`](/docs/controls/semantics#value) for this progress indicator.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the control.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/progressbar.md)

[

Previous

Text

](/docs/controls/text)[

Next

ProgressRing

](/docs/controls/progressring)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`value`](#value)
    -   [`bar_height`](#bar_height)
    -   [`border_radius`](#border_radius)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`semantics_label`](#semantics_label)
    -   [`semantics_value`](#semantics_value)
    -   [`tooltip`](#tooltip)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ProgressRing | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/progressring/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/progressring/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/progressring/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/progressring/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   ProgressRing

On this page

# ProgressRing

A material design circular progress indicator, which spins to indicate that the application is busy.

A control that shows progress along a circle.

There are two kinds of circular progress indicators:

-   *Determinate*. Determinate progress indicators have a specific value at each point in time, and the value should increase monotonically from `0.0` to `1.0`, at which time the indicator is complete. To create a determinate progress indicator, use a non-null value between `0.0` and `1.0`.
-   *Indeterminate*. Indeterminate progress indicators do not have a specific value at each point in time and instead indicate that progress is being made without indicating how much progress remains. To create an indeterminate progress indicator, use a null value.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/progressring)

-   Python

```
from time import sleepimport flet as ftdef main(page: ft.Page):    pr = ft.ProgressRing(width=16, height=16, stroke_width = 2)    page.add(        ft.Text("Circular progress indicator", style="headlineSmall"),        ft.Row([pr, ft.Text("Wait for the completion...")]),        ft.Text("Indeterminate cicrular progress", style="headlineSmall"),        ft.Column(            [ft.ProgressRing(), ft.Text("I'm going to run for ages...")],            horizontal_alignment=ft.CrossAxisAlignment.CENTER,        ),    )    for i in range(0, 101):        pr.value = i * 0.01        sleep(0.1)        page.update()ft.app(main)
```

![](https://flet.dev/docs/controls/progressring/img/docs/controls/progress-ring/custom-progress-rings.gif)

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

[Color](/docs/reference/colors) of the circular track being filled by the circular indicator.

### `color`[​](#color "Direct link to color")

The progress indicator's [color](/docs/reference/colors).

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

The `Semantics.label` for this progress indicator.

### `semantics_value`[​](#semantics_value "Direct link to semantics_value")

The `Semantics.value` for this progress indicator.

### `stroke_align`[​](#stroke_align "Direct link to stroke_align")

The relative position of the stroke. Value typically ranges be `-1.0` (inside stroke) and `1.0` (outside stroke).

Defaults to `0` - centered.

### `stroke_cap`[​](#stroke_cap "Direct link to stroke_cap")

The progress indicator's line ending.

Value is of type [`StrokeCap`](/docs/reference/types/strokecap).

### `stroke_width`[​](#stroke_width "Direct link to stroke_width")

The width of the line used to draw the circle.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the control.

### `value`[​](#value "Direct link to value")

The value of this progress indicator. A value of `0.0` means no progress and `1.0` means that progress is complete. The value will be clamped to be in the range `0.0` - `1.0`. If `None`, this progress indicator is indeterminate, which means the indicator displays a predetermined animation that does not indicate how much actual progress is being made.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/progressring.md)

[

Previous

ProgressBar

](/docs/controls/progressbar)[

Next

WebView

](/docs/controls/webview)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`semantics_label`](#semantics_label)
    -   [`semantics_value`](#semantics_value)
    -   [`stroke_align`](#stroke_align)
    -   [`stroke_cap`](#stroke_cap)
    -   [`stroke_width`](#stroke_width)
    -   [`tooltip`](#tooltip)
    -   [`value`](#value)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoDialogAction | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinodialogaction/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinodialogaction/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinodialogaction/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinodialogaction/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoDialogAction

On this page

# CupertinoDialogAction

A button typically used in a [CupertinoAlertDialog](/docs/controls/cupertinoalertdialog).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinodialogaction)

### CupertinoAlertDialog example[​](#cupertinoalertdialog-example "Direct link to CupertinoAlertDialog example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    def dialog_dismissed(e):        page.add(ft.Text("Dialog dismissed"))    def handle_action_click(e):        page.add(ft.Text(f"Action clicked: {e.control.text}"))        page.close(cupertino_alert_dialog)    cupertino_alert_dialog = ft.CupertinoAlertDialog(        title=ft.Text("Cupertino Alert Dialog"),        content=ft.Text("Do you want to delete this file?"),        on_dismiss=dialog_dismissed,        actions=[            ft.CupertinoDialogAction(                text="Yes",                is_destructive_action=True,                on_click=handle_action_click,            ),            ft.CupertinoDialogAction(                text="No",                 is_default_action=True,                 on_click=handle_action_click            ),        ],    )    page.add(        ft.CupertinoFilledButton(            text="Open CupertinoAlertDialog",            on_click=lambda e: page.open(cupertino_alert_dialog),        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinodialogaction/img/docs/controls/cupertinodialogaction/cupertinoalertdialog.png)

## Properties[​](#properties "Direct link to Properties")

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `is_default_action`[​](#is_default_action "Direct link to is_default_action")

If set to True, the button will have bold text. More than one action can have this property set to True in CupertinoAlertDialog.

Defaults to `False`.

### `is_destructive_action`[​](#is_destructive_action "Direct link to is_destructive_action")

If set to True, the button's text color will be red. Use it for actions that destroy objects, such as an delete that deletes an email etc.

Defaults to `False`.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `text_style`[​](#text_style "Direct link to text_style")

The text style to use for text on the button.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinodialogaction.md)

[

Previous

CupertinoContextMenuAction

](/docs/controls/cupertinocontextmenuaction)[

Next

CupertinoFilledButton

](/docs/controls/cupertinofilledbutton)

-   [Examples](#examples)
    -   [CupertinoAlertDialog example](#cupertinoalertdialog-example)
-   [Properties](#properties)
    -   [`content`](#content)
    -   [`is_default_action`](#is_default_action)
    -   [`is_destructive_action`](#is_destructive_action)
    -   [`text`](#text)
    -   [`text_style`](#text_style)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoFilledButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinofilledbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinofilledbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinofilledbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinofilledbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoFilledButton

On this page

# CupertinoFilledButton

An iOS-style button with filled with background color.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinofilledbutton)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.CupertinoFilledButton(            content=ft.Text("CupertinoFilled"),            opacity_on_click=0.3,            on_click=lambda e: print("CupertinoFilledButton clicked!"),        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinofilledbutton/img/docs/controls/cupertino-filled-button/cupertino-filled-button.png)

## Properties[​](#properties "Direct link to Properties")

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `disabled_bgcolor`[​](#disabled_bgcolor "Direct link to disabled_bgcolor")

The background [color](/docs/reference/colors) of the button when it is disabled.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `min_size`[​](#min_size "Direct link to min_size")

The minimum size of the button.

Defaults to `44.0`.

### `opacity_on_click`[​](#opacity_on_click "Direct link to opacity_on_click")

Defines the opacity of the button when it is clicked.

Defaults to `0.4`. The button will have an opacity of `1.0` when it is not pressed.

### `padding`[​](#padding "Direct link to padding")

The amount of space to surround the `content` control inside the bounds of the button.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the button loses focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the button receives focus.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when a user long-presses the button.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinofilledbutton.md)

[

Previous

CupertinoDialogAction

](/docs/controls/cupertinodialogaction)[

Next

CupertinoSegmentedButton

](/docs/controls/cupertinosegmentedbutton)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`content`](#content)
    -   [`disabled_bgcolor`](#disabled_bgcolor)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`min_size`](#min_size)
    -   [`opacity_on_click`](#opacity_on_click)
    -   [`padding`](#padding)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  FilledButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/filledbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/filledbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/filledbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/filledbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   FilledButton

On this page

# FilledButton

Filled buttons have the most visual impact after the [`FloatingActionButton`](/docs/controls/floatingactionbutton), and should be used for important, final actions that complete a flow, like **Save**, **Join now**, or **Confirm**. See [Material 3 buttons](https://m3.material.io/components/buttons/overview) for more info.

![](https://flet.dev/docs/controls/filledbutton/img/docs/controls/filled-button/basic-filled-buttons.png)

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/filledbutton)

### Filled button[​](#filled-button "Direct link to Filled button")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Basic filled buttons"    page.add(        ft.FilledButton(text="Filled button"),        ft.FilledButton("Disabled button", disabled=True),        ft.FilledButton("Button with icon", icon="add"),    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive Button is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoButton`](/docs/controls/cupertinofilledbutton) is created, which matches the functionality and presentation of this button. On other platforms, a Material `FilledButton` is created.

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Button's background [color](/docs/reference/colors). If both `bgcolor` and `style.bgcolor` are provided, `bgcolor` value will be used.

### `color`[​](#color "Direct link to color")

Button's text [color](/docs/reference/colors). If both `color` and `style.color` are provided, `color` value will be used.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `elevation`[​](#elevation "Direct link to elevation")

Button's elevation. If both `elevation` and `style.elevation` are provided, `elevation` value will be used.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `style`[​](#style "Direct link to style")

The value is an instance of [`ButtonStyle`](/docs/reference/types/buttonstyle) class.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a mouse pointer enters or exists the button response area. `data` property of event object contains `true` (string) when cursor enters and `false` when it exits.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the button is long-pressed.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/filledbutton.md)

[

Previous

ElevatedButton

](/docs/controls/elevatedbutton)[

Next

FilledTonalButton

](/docs/controls/filledtonalbutton)

-   [Examples](#examples)
    -   [Filled button](#filled-button)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`content`](#content)
    -   [`elevation`](#elevation)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`style`](#style)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_click`](#on_click)
    -   [`on_hover`](#on_hover)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  FilledTonalButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/filledtonalbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/filledtonalbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/filledtonalbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/filledtonalbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   FilledTonalButton

On this page

# FilledTonalButton

A filled tonal button is an alternative middle ground between [`FilledButton`](/docs/controls/filledbutton) and [`OutlinedButton`](/docs/controls/outlinedbutton) buttons. They’re useful in contexts where a lower-priority button requires slightly more emphasis than an outline would give, such as "Next" in an onboarding flow. Tonal buttons use the secondary color mapping. See [Material 3 buttons](https://m3.material.io/components/buttons/overview) for more info.

![](https://flet.dev/docs/controls/filledtonalbutton/img/docs/controls/filled-tonal-button/basic-filled-tonal-buttons.png)

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/filledtonalbutton)

### Filled tonal button[​](#filled-tonal-button "Direct link to Filled tonal button")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Basic filled tonal buttons"    page.add(        ft.FilledTonalButton(text="Filled tonal button"),        ft.FilledTonalButton("Disabled button", disabled=True),        ft.FilledTonalButton("Button with icon", icon="add"),    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive Button is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoButton`](/docs/controls/cupertinobutton) is created, which matches the functionality and presentation of this button. On other platforms, a Material `FilledTonalButton` is created.

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Button's background [color](/docs/reference/colors). If both `bgcolor` and `style.bgcolor` are provided, `bgcolor` value will be used.

### `color`[​](#color "Direct link to color")

Button's text [color](/docs/reference/colors). If both `color` and `style.color` are provided, `color` value will be used.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `elevation`[​](#elevation "Direct link to elevation")

Button's elevation. If both `elevation` and `style.elevation` are provided, `elevation` value will be used.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `style`[​](#style "Direct link to style")

The value is an instance of [`ButtonStyle`](/docs/reference/types/buttonstyle) class.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a mouse pointer enters or exists the button response area. `data` property of event object contains `true` (string) when cursor enters and `false` when it exits.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the button is long-pressed.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/filledtonalbutton.md)

[

Previous

FilledButton

](/docs/controls/filledbutton)[

Next

FloatingActionButton

](/docs/controls/floatingactionbutton)

-   [Examples](#examples)
    -   [Filled tonal button](#filled-tonal-button)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`content`](#content)
    -   [`elevation`](#elevation)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`style`](#style)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_click`](#on_click)
    -   [`on_hover`](#on_hover)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  SegmentedButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/segmentedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/segmentedbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/segmentedbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/segmentedbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   SegmentedButton

On this page

# SegmentedButton

A Material button that allows the user to select from limited set of options and are typically used in cases where there are only 2-5 options.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/segmentedbutton)

-   Python

```
import flet as ftdef main(page: ft.Page):    def handle_change(e):        print("on_change data : " + str(e.data))    page.add(        ft.SegmentedButton(            on_change=handle_change,            selected_icon=ft.Icon(ft.Icons.ONETWOTHREE),            selected={"1", "4"},            allow_multiple_selection=True,            segments=[                ft.Segment(                    value="1",                    label=ft.Text("1"),                    icon=ft.Icon(ft.Icons.LOOKS_ONE),                ),                ft.Segment(                    value="2",                    label=ft.Text("2"),                    icon=ft.Icon(ft.Icons.LOOKS_TWO),                ),                ft.Segment(                    value="3",                    label=ft.Text("3"),                    icon=ft.Icon(ft.Icons.LOOKS_3),                ),                ft.Segment(                    value="4",                    label=ft.Text("4"),                    icon=ft.Icon(ft.Icons.LOOKS_4),                ),            ],        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/segmentedbutton/img/docs/controls/segmented-button/segmented-button.png)

## `SegmentedButton` Properties[​](#segmentedbutton-properties "Direct link to segmentedbutton-properties")

### `allow_empty_selection`[​](#allow_empty_selection "Direct link to allow_empty_selection")

A boolean value that indicates if having no selected segments is allowed.

If `True`, then it is acceptable for none of the segments to be selected and also that `selected` can be empty.

If `False` (the default), there must be at least one segment selected. If the user taps on the only selected segment it will not be deselected, and `on_change` will not be called.

### `allow_multiple_selection`[​](#allow_multiple_selection "Direct link to allow_multiple_selection")

A boolean value that indicates if multiple segments can be selected at one time.

If `True`, more than one segment can be selected. When selecting a segment, the other `selected` segments will stay selected. Selecting an already selected segment will unselect it.

If `False`(the default), only one segment may be selected at a time. When a segment is selected, any previously selected segment will be unselected.

### `direction`[​](#direction "Direct link to direction")

The orientation of the button's `segments`.

Value is of type [`Axis`](/docs/reference/types/axis) and defaults to `Axis.HORIZONTAL`.

### `padding`[​](#padding "Direct link to padding")

Defines the button's size and padding. If specified, the button expands to fill its parent's space with this padding.

When `None`, the button adopts its intrinsic content size.

Value is of type [`PaddingValue`](/docs/reference/types/aliases#paddingvalue).

### `segments`[​](#segments "Direct link to segments")

A required parameter that describes the segments in the button. It's a list of `Segment` objects.

### `selected`[​](#selected "Direct link to selected")

A set of `Segment.value`s that indicate which segments are selected. It is updated when the user (un)selects a segment.

### `selected_icon`[​](#selected_icon "Direct link to selected_icon")

An `Icon` control that is used to indicate a segment is selected.

If `show_selected_icon` is `True` then for `selected` segments this icon will be shown before the `Segment.label`, replacing the `Segment.icon` if it is specified.

Defaults to an `Icon` with the `CHECK` icon.

### `show_selected_icon`[​](#show_selected_icon "Direct link to show_selected_icon")

A boolean value that indicates if the `selected_icon` is displayed on the `selected` segments.

If `True`, the `selected_icon` will be displayed at the start of the `selected` segments.

If `False`, then the `selected_icon` is not used and will not be displayed on `selected` segments.

### `style`[​](#style "Direct link to style")

Customizes this button's appearance.

Value is of type [`ButtonStyle`](/docs/reference/types/buttonstyle).

## Events[​](#events "Direct link to Events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when the selection changes.

## `Segment` Properties[​](#segment-properties "Direct link to segment-properties")

### `disabled`[​](#disabled "Direct link to disabled")

Determines if the segment is available for selection.

### `icon`[​](#icon "Direct link to icon")

The icon (typically an [`Icon`](/docs/controls/icon)) to be displayed in the segment.

### `label`[​](#label "Direct link to label")

The label (usually a [`Text`](/docs/controls/text)) to be displayed in the segment.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The tooltip for the segment.

### `value`[​](#value "Direct link to value")

Used to identify the `Segment`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/segmentedbutton.md)

[

Previous

PopupMenuButton

](/docs/controls/popupmenubutton)[

Next

SubmenuButton

](/docs/controls/submenubutton)

-   [Examples](#examples)
-   [`SegmentedButton` Properties](#segmentedbutton-properties)
    -   [`allow_empty_selection`](#allow_empty_selection)
    -   [`allow_multiple_selection`](#allow_multiple_selection)
    -   [`direction`](#direction)
    -   [`padding`](#padding)
    -   [`segments`](#segments)
    -   [`selected`](#selected)
    -   [`selected_icon`](#selected_icon)
    -   [`show_selected_icon`](#show_selected_icon)
    -   [`style`](#style)
-   [Events](#events)
    -   [`on_change`](#on_change)
-   [`Segment` Properties](#segment-properties)
    -   [`disabled`](#disabled)
    -   [`icon`](#icon)
    -   [`label`](#label)
    -   [`tooltip`](#tooltip)
    -   [`value`](#value)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  SubmenuButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/submenubutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/submenubutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/submenubutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/submenubutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   SubmenuButton

On this page

# SubmenuButton

A menu button that displays a cascading menu.

It can be used as part of a [MenuBar](/docs/controls/menubar), or as a standalone control.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/submenubutton)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.padding = 0    page.spacing = 0    bg_container = ft.Ref[ft.Container]()    def handle_color_click(e):        color = e.control.content.value        print(f"{color}.on_click")        bg_container.current.content.value = f"{color} background color"        bg_container.current.bgcolor = color.lower()        page.update()    def handle_on_hover(e):        print(f"{e.control.content.value}.on_hover")    menubar = ft.MenuBar(        expand=True,        controls=[            ft.SubmenuButton(                content=ft.Text("BgColors"),                controls=[                    ft.SubmenuButton(                        content=ft.Text("B"),                        leading=ft.Icon(ft.Icons.COLORIZE),                        controls=[                            ft.MenuItemButton(                                content=ft.Text("Blue"),                                style=ft.ButtonStyle(bgcolor={ft.ControlState.HOVERED: ft.Colors.BLUE}),                                on_click=handle_color_click,                                on_hover=handle_on_hover,                            )                        ]                    ),                    ft.SubmenuButton(                        content=ft.Text("G"),                        leading=ft.Icon(ft.Icons.COLORIZE),                        controls=[                            ft.MenuItemButton(                                content=ft.Text("Green"),                                style=ft.ButtonStyle(bgcolor={ft.ControlState.HOVERED: ft.Colors.GREEN}),                                on_click=handle_color_click,                                on_hover=handle_on_hover,                            )                        ]                    ),                    ft.SubmenuButton(                        content=ft.Text("R"),                        leading=ft.Icon(ft.Icons.COLORIZE),                        controls=[                            ft.MenuItemButton(                                content=ft.Text("Red"),                                style=ft.ButtonStyle(bgcolor={ft.ControlState.HOVERED: ft.Colors.RED}),                                on_click=handle_color_click,                                on_hover=handle_on_hover,                            )                        ]                    )                ]            )        ]    )    page.add(        ft.Row([menubar]),        ft.Container(            ref=bg_container,            expand=True,            bgcolor=ft.Colors.SURFACE,            content=ft.Text("Choose a bgcolor from the menu", style=ft.TextThemeStyle.HEADLINE_LARGE),            alignment=ft.alignment.center,        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/submenubutton/img/docs/controls/submenu-button/submenu-button.gif)

## Properties[​](#properties "Direct link to Properties")

### `alignment_offset`[​](#alignment_offset "Direct link to alignment_offset")

The offset of the menu relative to the alignment origin determined by `MenuStyle.alignment` on the `style` attribute.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

Whether to clip the content of this control or not.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.HARD_EDGE`.

### `content`[​](#content "Direct link to content")

The child control to be displayed in the middle portion of this button.

Typically this is the button's label, using a `Text` control.

### `controls`[​](#controls "Direct link to controls")

A list of controls that appear in the menu when it is opened.

Typically either `MenuItemButton` or `SubMenuButton` controls.

If this list is empty, then the button for this menu item will be disabled.

### `leading`[​](#leading "Direct link to leading")

An optional control to display before the `content`.

Typically an [`Icon`](/docs/controls/icon) control.

### `menu_style`[​](#menu_style "Direct link to menu_style")

Customizes this menu's appearance.

Value is of type [`MenuStyle`](/docs/reference/types/menustyle).

### `style`[​](#style "Direct link to style")

Customizes this button's appearance.

Value is of type [`ButtonStyle`](/docs/reference/types/buttonstyle).

### `trailing`[​](#trailing "Direct link to trailing")

An optional control to display after the `content`.

Typically an [`Icon`](/docs/controls/icon) control.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fired when this button loses focus.

### `on_close`[​](#on_close "Direct link to on_close")

Fired when the menu is closed.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fired when the button receives focus.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fired when the button is hovered.

### `on_open`[​](#on_open "Direct link to on_open")

Fired when the menu is opened.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/submenubutton.md)

[

Previous

SegmentedButton

](/docs/controls/segmentedbutton)[

Next

TextButton

](/docs/controls/textbutton)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`alignment_offset`](#alignment_offset)
    -   [`clip_behavior`](#clip_behavior)
    -   [`content`](#content)
    -   [`controls`](#controls)
    -   [`leading`](#leading)
    -   [`menu_style`](#menu_style)
    -   [`style`](#style)
    -   [`trailing`](#trailing)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_close`](#on_close)
    -   [`on_focus`](#on_focus)
    -   [`on_hover`](#on_hover)
    -   [`on_open`](#on_open)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  TextButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/textbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/textbutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/textbutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/textbutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   TextButton

On this page

# TextButton

Text buttons are used for the lowest priority actions, especially when presenting multiple options. Text buttons can be placed on a variety of backgrounds. Until the button is interacted with, its container isn’t visible. See [Material 3 buttons](https://m3.material.io/components/buttons/overview) for more info.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/textbutton)

### Basic text buttons[​](#basic-text-buttons "Direct link to Basic text buttons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Basic text buttons"    page.add(        ft.TextButton(text="Text button"),        ft.TextButton("Disabled button", disabled=True),    )ft.app(main)
```

![](https://flet.dev/docs/controls/textbutton/img/docs/controls/text-button/basic-text-buttons.png)

### Text buttons with icons[​](#text-buttons-with-icons "Direct link to Text buttons with icons")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Text buttons with icons"    page.add(        ft.TextButton("Button with icon", icon="chair_outlined"),        ft.TextButton(            "Button with colorful icon",            icon="park_rounded",            icon_color="green400",        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/textbutton/img/docs/controls/text-button/text-buttons-with-icons.png)

### Text button with `click` event[​](#text-button-with-click-event "Direct link to text-button-with-click-event")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Text button with 'click' event"    def button_clicked(e):        b.data += 1        t.value = f"Button clicked {b.data} time(s)"        page.update()    b = ft.TextButton("Button with 'click' event", on_click=button_clicked, data=0)    t = ft.Text()    page.add(b, t)ft.app(main)
```

![](https://flet.dev/docs/controls/textbutton/img/docs/controls/text-button/text-button-with-click-event.gif)

### Text button with custom content[​](#text-button-with-custom-content "Direct link to Text button with custom content")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Text buttons with custom content"    page.add(        ft.TextButton(            width=150,            content=ft.Row(                [                    ft.Icon(name=ft.Icons.FAVORITE, color="pink"),                    ft.Icon(name=ft.Icons.AUDIOTRACK, color="green"),                    ft.Icon(name=ft.Icons.BEACH_ACCESS, color="blue"),                ],                alignment=ft.MainAxisAlignment.SPACE_AROUND,            ),        ),        ft.TextButton(            content=ft.Container(                content=ft.Column(                    [                        ft.Text(value="Compound button", size=20),                        ft.Text(value="This is secondary text"),                    ],                    alignment=ft.MainAxisAlignment.CENTER,                    spacing=5,                ),                padding=ft.padding.all(10),            ),        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/textbutton/img/docs/controls/text-button/text-buttons-with-custom-content.png)

## Properties[​](#properties "Direct link to Properties")

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive Button is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoButton`](/docs/controls/cupertinobutton) is created, which matches the functionality and presentation of this button. On other platforms, a Material `TextButton` is created.

Defaults to `False`.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.HARD_EDGE`.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `style`[​](#style "Direct link to style")

Value is of type [`ButtonStyle`](/docs/reference/types/buttonstyle).

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode. Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Methods[​](#methods "Direct link to Methods")

### `focus()`[​](#focus "Direct link to focus")

Moves focus to a button.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a mouse pointer enters or exists the button response area. `data` property of event object contains `true` (string) when cursor enters and `false` when it exits.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the button is long-pressed.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/textbutton.md)

[

Previous

SubmenuButton

](/docs/controls/submenubutton)[

Next

Input and Selections

](/docs/controls/input-and-selections)

-   [Examples](#examples)
    -   [Basic text buttons](#basic-text-buttons)
    -   [Text buttons with icons](#text-buttons-with-icons)
    -   [Text button with `click` event](#text-button-with-click-event)
    -   [Text button with custom content](#text-button-with-custom-content)
-   [Properties](#properties)
    -   [`adaptive`](#adaptive)
    -   [`autofocus`](#autofocus)
    -   [`content`](#content)
    -   [`clip_behavior`](#clip_behavior)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`style`](#style)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Methods](#methods)
    -   [`focus()`](#focus)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)
    -   [`on_hover`](#on_hover)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Chip | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/chip/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/chip/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/chip/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/chip/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Input and Selections](/docs/controls/input-and-selections)
-   Chip

On this page

# Chip

Chips are compact elements that represent an attribute, text, entity, or action.

Chips help people enter information, make selections, filter content, or trigger actions. Use chips to show options for a specific context.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/input/chip)

### Assist chips[​](#assist-chips "Direct link to Assist chips")

Assist chips are chips with `leading` icon and `on_click` event specified. They represent smart or automated actions that appear dynamically and contextually in a UI.

An alternative to assist chips are buttons, which should appear persistently and consistently.

-   Python

```
import flet as ftdef main(page: ft.Page):    def save_to_favorites_clicked(e):        e.control.label.value = "Saved to favorites"        e.control.leading = ft.Icon(ft.Icons.FAVORITE_OUTLINED)        e.control.disabled = True        page.update()    def open_google_maps(e):        page.launch_url("https://maps.google.com")        page.update()    save_to_favourites = ft.Chip(        label=ft.Text("Save to favourites"),        leading=ft.Icon(ft.Icons.FAVORITE_BORDER_OUTLINED),        bgcolor=ft.Colors.GREEN_200,        disabled_color=ft.Colors.GREEN_100,        autofocus=True,        on_click=save_to_favorites_clicked,    )    open_in_maps = ft.Chip(        label=ft.Text("9 min walk"),        leading=ft.Icon(ft.Icons.MAP_SHARP),        bgcolor=ft.Colors.GREEN_200,        on_click=open_google_maps,    )    page.add(ft.Row([save_to_favourites, open_in_maps]))ft.app(main)
```

![](https://flet.dev/docs/controls/chip/img/docs/controls/chip/assist-chips.png)

### Filter chips[​](#filter-chips "Direct link to Filter chips")

Filter chips are chips with `on_select` event specified. They use tags or descriptive words provided in the `label` to filter content. They can be a good alternative to switches or checkboxes.

-   Python

```
import flet as ftdef main(page: ft.Page):    def amenity_selected(e):        page.update()    title = ft.Row([ft.Icon(ft.Icons.HOTEL_CLASS), ft.Text("Amenities")])    amenities = ["Washer / Dryer", "Ramp access", "Dogs OK", "Cats OK", "Smoke-free"]    amenity_chips = []    for amenity in amenities:        amenity_chips.append(            ft.Chip(                label=ft.Text(amenity),                bgcolor=ft.Colors.GREEN_200,                disabled_color=ft.Colors.GREEN_100,                autofocus=True,                on_select=amenity_selected,            )        )    page.add(title, ft.Row(amenity_chips))ft.app(main)
```

![](https://flet.dev/docs/controls/chip/img/docs/controls/chip/filter-chips.png)

## Properties[​](#properties "Direct link to Properties")

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

[Color](/docs/reference/colors) to be used for the unselected, enabled chip's background.

### `border_side`[​](#border_side "Direct link to border_side")

Defines the color and weight of the chip's outline.

Value is of type [`BorderSide`](/docs/reference/types/borderside).

### `check_color`[​](#check_color "Direct link to check_color")

[Color](/docs/reference/colors) of the chip's check mark when a check mark is visible.

### `click_elevation`[​](#click_elevation "Direct link to click_elevation")

A non-negative value which defines the elevation of the chip when clicked/pressed.

Defaults to `8.0`.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `color`[​](#color "Direct link to color")

The [color](/docs/reference/colors) that fills the chip in various [`ControlState`](/docs/reference/types/controlstate)s.

### `delete_drawer_animation_style`[​](#delete_drawer_animation_style "Direct link to delete_drawer_animation_style")

The animation style for the `delete_icon`'s animations.

Value is of type [`AnimationStyle`](/docs/reference/types/animationstyle).

### `delete_icon_tooltip`[​](#delete_icon_tooltip "Direct link to delete_icon_tooltip")

The text to be used for the chip's `delete_icon` tooltip. If not provided or provided with an empty string, the tooltip of the delete icon will not be displayed.

### `delete_icon`[​](#delete_icon "Direct link to delete_icon")

A `Control` to display to the right of the chip's `label` in case `on_delete` event is specified.

Defaults to an [`Icon(icons.CANCEL)`](/docs/controls/icon).

### `delete_icon_color`[​](#delete_icon_color "Direct link to delete_icon_color")

[Color](/docs/reference/colors) of the `delete_icon`.

### `delete_icon_size_constraints`[​](#delete_icon_size_constraints "Direct link to delete_icon_size_constraints")

The size constraints for the `delete_icon` control. When unspecified, it defaults to a minimum size of chip height or label height (whichever is greater) and a padding of 8.0 pixels on all sides.

Value is of type [`BoxConstraints`](/docs/reference/types/boxconstraints).

### `disabled_color`[​](#disabled_color "Direct link to disabled_color")

The [color](/docs/reference/colors) used for the chip's background if it is disabled.

### `elevation`[​](#elevation "Direct link to elevation")

A non-negative value which defines the size of the shadow below the chip.

Defaults to `0`.

### `enable_animation_style`[​](#enable_animation_style "Direct link to enable_animation_style")

The animation style for the enable and disable animations.

Value is of type [`AnimationStyle`](/docs/reference/types/animationstyle).

### `label`[​](#label "Direct link to label")

A `Control` that represents primary content of the chip, typically a [`Text`](/docs/controls/text). Label is a required property.

### `label_padding`[​](#label_padding "Direct link to label_padding")

Padding around the `label`.

The value is an instance of [`padding.Padding`](/docs/reference/types/padding) class or a number.

By default, this is 4 logical pixels at the beginning and the end of the label, and zero on top and bottom.

### `label_style`[​](#label_style "Direct link to label_style")

The style to be applied to the chip's `label`.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

### `leading`[​](#leading "Direct link to leading")

A `Control` to display to the left of the chip's `label`.

Typically the leading control is an [`Icon`](/docs/controls/icon) or a [`CircleAvatar`](/docs/controls/circleavatar).

### `leading_drawer_animation_style`[​](#leading_drawer_animation_style "Direct link to leading_drawer_animation_style")

The animation style for the `leading` control's animations.

Value is of type [`AnimationStyle`](/docs/reference/types/animationstyle).

### `leading_size_constraints`[​](#leading_size_constraints "Direct link to leading_size_constraints")

The size constraints for the `leading` control. When unspecified, it defaults to a minimum size of chip height or label height (whichever is greater) and a padding of 8.0 pixels on all sides.

Value is of type [`BoxConstraints`](/docs/reference/types/boxconstraints).

### `padding`[​](#padding "Direct link to padding")

The padding between the `label` and the outside shape.

The value is an instance of [`Padding`](/docs/reference/types/padding) class or a number.

By default, this is 4 logical pixels on all sides.

### `selected`[​](#selected "Direct link to selected")

If `on_select` event is specified, `selected` property is used to determine whether the chip is selected or not.

Defaults to `False`.

### `select_animation_style`[​](#select_animation_style "Direct link to select_animation_style")

The animation style for the select and unselect animations.

Value is of type [`AnimationStyle`](/docs/reference/types/animationstyle).

### `selected_color`[​](#selected_color "Direct link to selected_color")

The [color](/docs/reference/colors) used for the chip's background when it is selected.

### `selected_shadow_color`[​](#selected_shadow_color "Direct link to selected_shadow_color")

The [color](/docs/reference/colors) used for the chip's background when the elevation is greater than `0` and the chip is selected.

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) used for the chip's background when the elevation is greater than `0` and the chip is not selected.

### `shape`[​](#shape "Direct link to shape")

The shape of the border around the chip.

The value is an instance of [`OutlinedBorder`](/docs/reference/types/outlinedborder) class.

The default shape is a `StadiumBorder`.

### `show_checkmark`[​](#show_checkmark "Direct link to show_checkmark")

If `on_select` event is specified and chip is selected, `show_checkmark` is used to determine whether or not to show a checkmark.

Defaults to `True`.

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The [color](/docs/reference/colors) used as an overlay on `bgcolor` to indicate elevation.

### `visual_density`[​](#visual_density "Direct link to visual_density")

Defines how compact the control's layout will be.

Value is of type [`VisualDensity`](/docs/reference/types/visualdensity).

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when the user clicks on the chip. Cannot be specified together with `on_select` event.

### `on_delete`[​](#on_delete "Direct link to on_delete")

Fires when the user clicks on the `delete_icon`.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

### `on_select`[​](#on_select "Direct link to on_select")

Fires when the user clicks on the chip. Changes `selected` property to the opposite value. Cannot be specified together with `on_click` event.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/chip.md)

[

Previous

Checkbox

](/docs/controls/checkbox)[

Next

CupertinoCheckbox

](/docs/controls/cupertinocheckbox)

-   [Examples](#examples)
    -   [Assist chips](#assist-chips)
    -   [Filter chips](#filter-chips)
-   [Properties](#properties)
    -   [`autofocus`](#autofocus)
    -   [`bgcolor`](#bgcolor)
    -   [`border_side`](#border_side)
    -   [`check_color`](#check_color)
    -   [`click_elevation`](#click_elevation)
    -   [`clip_behavior`](#clip_behavior)
    -   [`color`](#color)
    -   [`delete_drawer_animation_style`](#delete_drawer_animation_style)
    -   [`delete_icon_tooltip`](#delete_icon_tooltip)
    -   [`delete_icon`](#delete_icon)
    -   [`delete_icon_color`](#delete_icon_color)
    -   [`delete_icon_size_constraints`](#delete_icon_size_constraints)
    -   [`disabled_color`](#disabled_color)
    -   [`elevation`](#elevation)
    -   [`enable_animation_style`](#enable_animation_style)
    -   [`label`](#label)
    -   [`label_padding`](#label_padding)
    -   [`label_style`](#label_style)
    -   [`leading`](#leading)
    -   [`leading_drawer_animation_style`](#leading_drawer_animation_style)
    -   [`leading_size_constraints`](#leading_size_constraints)
    -   [`padding`](#padding)
    -   [`selected`](#selected)
    -   [`select_animation_style`](#select_animation_style)
    -   [`selected_color`](#selected_color)
    -   [`selected_shadow_color`](#selected_shadow_color)
    -   [`shadow_color`](#shadow_color)
    -   [`shape`](#shape)
    -   [`show_checkmark`](#show_checkmark)
    -   [`surface_tint_color`](#surface_tint_color)
    -   [`visual_density`](#visual_density)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_delete`](#on_delete)
    -   [`on_focus`](#on_focus)
    -   [`on_select`](#on_select)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoCheckbox | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinocheckbox/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinocheckbox/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinocheckbox/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinocheckbox/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Input and Selections](/docs/controls/input-and-selections)
-   CupertinoCheckbox

On this page

# CupertinoCheckbox

A macOS style checkbox. Checkbox allows to select one or more items from a group, or switch between two mutually exclusive options (checked or unchecked, on or off).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/input/cupertinocheckbox)

### CupertinoCheckbox and adaptive CheckBox example[​](#cupertinocheckbox-and-adaptive-checkbox-example "Direct link to CupertinoCheckbox and adaptive CheckBox example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.CupertinoCheckbox(label="Cupertino Checkbox", value=True),        ft.Checkbox(label="Material Checkbox", value=True),        ft.Container(height=20),        ft.Text(            "Adaptive Checkbox shows as CupertinoCheckbox on macOS and iOS and as Checkbox on other platforms:"        ),        ft.Checkbox(adaptive=True, label="Adaptive Checkbox", value=True),    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinocheckbox/img/docs/controls/cupertinocheckbox/cupertinocheckbox.png)

## Properties[​](#properties "Direct link to Properties")

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `active_color`[​](#active_color "Direct link to active_color")

The [color](/docs/reference/colors) used to fill checkbox when it is checked/selected.

If `fill_color` returns a non-null color in the `SELECTED` state, it will be used instead of this color.

Defaults to `Colors.PRIMARY`.

### `border_side`[​](#border_side "Direct link to border_side")

Defines the checkbox's border sides in all or specific [`ControlState`](/docs/reference/types/controlstate) states.

The following states are supported: `DEFAULT`, `PRESSED`, `SELECTED`, `HOVERED`, `FOCUSED`, `DISABLED` and `ERROR`.

### `check_color`[​](#check_color "Direct link to check_color")

The [color](/docs/reference/colors) to use for the check icon when this checkbox is checked.

### `fill_color`[​](#fill_color "Direct link to fill_color")

The [color](/docs/reference/colors) used to fill the checkbox in all or specific [`ControlState`](/docs/reference/types/controlstate) states.

The following states are supported: `DEFAULT`, `SELECTED`, `HOVERED`, `FOCUSED`, and `DISABLED`.

`active_color` is used as fallback color when the checkbox is in the `SELECTED` state, `CupertinoColors.WHITE` at 50% opacity is used as fallback color when the checkbox is in the `DISABLED` state, and `CupertinoColors.WHITE` otherwise.

### `focus_color`[​](#focus_color "Direct link to focus_color")

The [color](/docs/reference/colors) used for the checkbox's border shadow when it has the input focus.

### `label`[​](#label "Direct link to label")

The clickable label to display on the right of a checkbox.

### `label_position`[​](#label_position "Direct link to label_position")

Defines on which side of the checkbox the `label` should be shown.

Value is of type [`LabelPosition`](/docs/reference/types/labelposition) and defaults to `RIGHT`.

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor for a mouse pointer entering or hovering over this control.

Value is of type [`MouseCursor`](/docs/reference/types/mousecursor).

### `semantics_label`[​](#semantics_label "Direct link to semantics_label")

The semantic label for the checkbox that will be announced by screen readers.

This is announced by assistive technologies (e.g TalkBack/VoiceOver) and not shown on the UI.

### `shape`[​](#shape "Direct link to shape")

The shape of the checkbox.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder) and defaults to `RoundedRectangleBorder(radius=4)`.

### `tristate`[​](#tristate "Direct link to tristate")

If `True` the checkbox's value can be `True`, `False`, or `None`.

Checkbox displays a dash when its value is null.

### `value`[​](#value "Direct link to value")

Current value of the checkbox.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_change`[​](#on_change "Direct link to on_change")

Fires when the state of the Checkbox is changed.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinocheckbox.md)

[

Previous

Chip

](/docs/controls/chip)[

Next

CupertinoRadio

](/docs/controls/cupertinoradio)

-   [Examples](#examples)
    -   [CupertinoCheckbox and adaptive CheckBox example](#cupertinocheckbox-and-adaptive-checkbox-example)
-   [Properties](#properties)
    -   [`autofocus`](#autofocus)
    -   [`active_color`](#active_color)
    -   [`border_side`](#border_side)
    -   [`check_color`](#check_color)
    -   [`fill_color`](#fill_color)
    -   [`focus_color`](#focus_color)
    -   [`label`](#label)
    -   [`label_position`](#label_position)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`semantics_label`](#semantics_label)
    -   [`shape`](#shape)
    -   [`tristate`](#tristate)
    -   [`value`](#value)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_change`](#on_change)
    -   [`on_focus`](#on_focus)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoRadio | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinoradio/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoradio/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinoradio/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoradio/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
        -   [AutoComplete](/docs/controls/autocomplete)
        -   [AutofillGroup](/docs/controls/autofillgroup)
        -   [Checkbox](/docs/controls/checkbox)
        -   [Chip](/docs/controls/chip)
        -   [CupertinoCheckbox](/docs/controls/cupertinocheckbox)
        -   [CupertinoRadio](/docs/controls/cupertinoradio)
        -   [CupertinoSlider](/docs/controls/cupertinoslider)
        -   [CupertinoSwitch](/docs/controls/cupertinoswitch)
        -   [CupertinoTextField](/docs/controls/cupertinotextfield)
        -   [Dropdown](/docs/controls/dropdown)
        -   [DropdownM2](/docs/controls/dropdownm2)
        -   [Radio](/docs/controls/radio)
        -   [RangeSlider](/docs/controls/rangeslider)
        -   [SearchBar](/docs/controls/searchbar)
        -   [Slider](/docs/controls/slider)
        -   [Switch](/docs/controls/switch)
        -   [TextField](/docs/controls/textfield)
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Input and Selections](/docs/controls/input-and-selections)
-   CupertinoRadio

On this page

# CupertinoRadio

A macOS style radio button. Radio buttons let people select a single option from two or more choices.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/input/cupertinoradio)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page):    def button_clicked(e):        t.value = f"Your favorite color is:  {cg.value}"        page.update()    t = ft.Text()    b = ft.ElevatedButton(text="Submit", on_click=button_clicked)    cg = ft.RadioGroup(        content=ft.Column(            [                ft.CupertinoRadio(value="red", label="Red - Cupertino Radio", active_color=ft.Colors.RED, inactive_color=ft.Colors.RED),                ft.Radio(value="green", label="Green - Material Radio", fill_color=ft.Colors.GREEN),                ft.Radio(value="blue", label="Blue - Adaptive Radio", adaptive=True, active_color=ft.Colors.BLUE),            ]        )    )    page.add(ft.Text("Select your favorite color:"), cg, b, t)ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinoradio/img/docs/controls/cupertinoradio/cupertino-radio-basic.png)

## `RadioGroup` properties[​](#radiogroup-properties "Direct link to radiogroup-properties")

### `value`[​](#value "Direct link to value")

Current value of the RadioGroup.

## `RadioGroup` events[​](#radiogroup-events "Direct link to radiogroup-events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when the state of the RadioGroup is changed.

## `CupertinoRadio` properties[​](#cupertinoradio-properties "Direct link to cupertinoradio-properties")

### `active_color`[​](#active_color "Direct link to active_color")

The [color](/docs/reference/colors) used to fill this radio when it is selected.

### `autofocus`[​](#autofocus "Direct link to autofocus")

True if the control will be selected as the initial focus. If there is more than one control on a page with autofocus set, then the first one added to the page will get focus.

### `fill_color`[​](#fill_color "Direct link to fill_color")

The [color](/docs/reference/colors) that fills the radio.

### `focus_color`[​](#focus_color "Direct link to focus_color")

The [color](/docs/reference/colors) for the radio's border when it has the input focus.

### `inactive_color`[​](#inactive_color "Direct link to inactive_color")

The [color](/docs/reference/colors) used to fill this radio when it is not selected.

Defaults to `colors.WHITE`.

### `label`[​](#label "Direct link to label")

The clickable label to display on the right of a Radio.

### `label_position`[​](#label_position "Direct link to label_position")

The position of the label relative to the radio.

Value is of type [`LabelPosition`](/docs/reference/types/labelposition) and defaults to `LabelPosition.RIGHT`.

### `toggleable`[​](#toggleable "Direct link to toggleable")

Set to `True` if this radio button is allowed to be returned to an indeterminate state by selecting it again when selected.

Defaults to `False`.

### `use_checkmark_style`[​](#use_checkmark_style "Direct link to use_checkmark_style")

Defines whether the radio displays in a checkbox style or the default radio style.

Defaults to `False`.

### `value`[​](#value-1 "Direct link to value-1")

The value to set to containing `RadioGroup` when the radio is selected.

## `CupertinoRadio` events[​](#cupertinoradio-events "Direct link to cupertinoradio-events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the control has lost focus.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the control has received focus.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinoradio.md)

[

Previous

CupertinoCheckbox

](/docs/controls/cupertinocheckbox)[

Next

CupertinoSlider

](/docs/controls/cupertinoslider)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [`RadioGroup` properties](#radiogroup-properties)
    -   [`value`](#value)
-   [`RadioGroup` events](#radiogroup-events)
    -   [`on_change`](#on_change)
-   [`CupertinoRadio` properties](#cupertinoradio-properties)
    -   [`active_color`](#active_color)
    -   [`autofocus`](#autofocus)
    -   [`fill_color`](#fill_color)
    -   [`focus_color`](#focus_color)
    -   [`inactive_color`](#inactive_color)
    -   [`label`](#label)
    -   [`label_position`](#label_position)
    -   [`toggleable`](#toggleable)
    -   [`use_checkmark_style`](#use_checkmark_style)
    -   [`value`](#value-1)
-   [`CupertinoRadio` events](#cupertinoradio-events)
    -   [`on_blur`](#on_blur)
    -   [`on_focus`](#on_focus)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Packaging app for iOS | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/publish/ios/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/ios/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/publish/ios/img/logo.svg)![Flet Logo](https://flet.dev/docs/publish/ios/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
    -   [Android](/docs/publish/android)
    -   [iOS](/docs/publish/ios)
    -   [macOS](/docs/publish/macos)
    -   [Linux](/docs/publish/linux)
    -   [Windows](/docs/publish/windows)
    -   [Web](/docs/publish/web)
        
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Publishing Flet app](/docs/publish)
-   iOS

On this page

# Packaging app for iOS

## Introduction[​](#introduction "Direct link to Introduction")

Flet CLI provides `flet build ipa` command that allows packaging Flet app into an iOS archive bundle and IPA for distribution.

note

The command can be run on macOS only.

## Prerequisites[​](#prerequisites "Direct link to Prerequisites")

### Rosetta 2[​](#rosetta-2 "Direct link to Rosetta 2")

Flutter requires [Rosetta 2](https://support.apple.com/en-us/HT211861) on Apple silicon:

```
sudo softwareupdate --install-rosetta --agree-to-license
```

### Xcode[​](#xcode "Direct link to Xcode")

[Xcode](https://developer.apple.com/xcode/) 15 or later to compile native Swift or ObjectiveC code.

### CocoaPods[​](#cocoapods "Direct link to CocoaPods")

[CocoaPods](https://cocoapods.org/) 1.16 to compile and enable Flutter plugins.

### iOS wheels for binary Python packages[​](#ios-wheels-for-binary-python-packages "Direct link to iOS wheels for binary Python packages")

Binary Python packages (vs "pure" Python packages written in Python only) are packages that partially written in C, Rust or other languages producing native code. Example packages are `numpy`, `cryptography`, or `pydantic-core`.

Make sure all non-pure (binary) packages used in your Flet app have [pre-built wheels for iOS](/docs/reference/binary-packages-android-ios).

## `flet build ipa`[​](#flet-build-ipa "Direct link to flet-build-ipa")

Build an iOS app archive (`.ipa`) for testing and distribution (macOS host only).

To generate an `.ipa` file for testing on your device or uploading to App Store Connect for distribution, you will need:

-   **Apple Developer Program** subscription with access to App Store Connect.
-   **Application Indentifier**.
-   **Signing Certificate**.
-   **Provisioning Profile**.

## Application Identifier[​](#application-identifier "Direct link to Application Identifier")

An **Application Identifier (App ID)** is a unique string that identifies your app within the Apple ecosystem. It is required to sign and distribute an iOS app and is used for various services like **Push Notifications, App Groups, iCloud, and In-App Purchases**.

An App ID consists of two parts:

1.  **Team ID** – A unique 10-character string assigned by Apple to your developer account.
2.  **Bundle ID** – A reverse domain-style identifier for your app (e.g., `com.example.myapp`).

Example of a full App ID:

```
TeamID.com.example.myapp
```

### Creating a new App ID[​](#creating-a-new-app-id "Direct link to Creating a new App ID")

1.  Visit [Apple Developer Portal](https://developer.apple.com/account/resources/identifiers/list).
2.  Sign in with your **Apple Developer Account**.
3.  Click the **"+"** button to add a new identifier.
4.  Select **"App IDs"** and click **Continue**.
5.  **Enter a Description** – This is just for reference (e.g., "MyApp Identifier").
6.  **Choose the App ID Type:**
    -   Select **"App"** for a standard iOS/macOS app.
    -   If you need an identifier for services like Apple Pay or Passbook, select the appropriate option.
7.  **Bundle ID** – Choose:
    -   **Explicit Bundle ID** (`com.example.myapp`) – Recommended for most apps.
    -   **Wildcard Bundle ID** (`com.example.*`) – Allows multiple apps to use the same identifier (rarely used).
8.  **Enable App Services** – Check the boxes for any services your app needs (e.g., Push Notifications, Sign in with Apple, etc.).
9.  Click **Continue** and **Register**.

Now you have **Bundle ID** and **Team ID** that must be used to sign iOS bundle.

The next step is creating a **Certificate** and a **Provisioning Profile** to install and distribute your app.

## Signing Certificate[​](#signing-certificate "Direct link to Signing Certificate")

### Generating a Certificate Signing Request (CSR)[​](#generating-a-certificate-signing-request-csr "Direct link to Generating a Certificate Signing Request (CSR)")

Before creating a development or distribution certificate, you need a **CSR (Certificate Signing Request)**.

1.  **Open Keychain Access** on your Mac (`Command ⌘ + Space`, then search for "Keychain Access").
2.  In the top menu, go to **Keychain Access → Certificate Assistant → Request a Certificate From a Certificate Authority…**
3.  Fill in:
    -   **User Email Address:** Your Apple Developer email.
    -   **Common Name:** A descriptive name (e.g., "My App Distribution").
    -   **CA Email Address:** Leave this blank.
    -   **Request is for:** Select "**Saved to disk**".
4.  Click **Continue**, choose a location to save the `.certSigningRequest` file, and click **Save**.

### Creating a Certificate in Apple Developer Portal[​](#creating-a-certificate-in-apple-developer-portal "Direct link to Creating a Certificate in Apple Developer Portal")

1.  Go to [Apple Developer Certificates Page](https://developer.apple.com/account/resources/certificates/list).
2.  Click the **"+"** button to create a new certificate.
3.  Select **"Apple Distribution"** (for App Store & Ad Hoc) or **"Apple Development"** (for development) and click **Continue**.
4.  Upload the **CSR file** you created earlier and click **Continue**.
5.  Apple will generate the certificate. Click **Download** to get the `.cer` file.
6.  Double-click the downloaded `.cer` file to install it in **Keychain Access**.
7.  Open **Keychain Access** app and ensure the certificate is installed under **"login"** keychain. The name of development certificate usually starts with **"Apple development:"** and the name of distribution certificate starts with **"Apple distribution:"**.

## Provisioning Profile[​](#provisioning-profile "Direct link to Provisioning Profile")

A **Provisioning Profile** is a file that allows an iOS app to run on physical devices and be distributed through the App Store or internally. It links your **App ID**, **Developer/Distribution Certificate**, and **Registered Devices**.

There are different types of provisioning profiles:

-   **Development Profile** – Used for testing on physical devices.
-   **Ad Hoc Profile** – Used for distributing an app outside the App Store to specific devices.
-   **App Store Profile** – Used for submitting an app to the App Store.
-   **Enterprise Profile** – Used for internal distribution within an organization.

### Creating a new Provisioning Profile[​](#creating-a-new-provisioning-profile "Direct link to Creating a new Provisioning Profile")

**Step 1: Go to Apple Developer Portal**

1.  Visit [Apple Developer Portal](https://developer.apple.com/account/resources/profiles/list).
2.  Sign in with your **Apple Developer Account**.

**Step 2: Create a New Provisioning Profile**

1.  Click the **"+"** button to add a new provisioning profile.
2.  Choose the **type of profile**:
    -   Select **"iOS App Development"** for testing on devices.
    -   Select **"Ad Hoc"** for distributing to specific devices.
    -   Select **"App Store"** for submitting an app to the App Store.
    -   Select **"In-House"** (Enterprise accounts only) for internal distribution.
3.  Click **Continue**.

**Step 3: Select an App ID**

1.  Choose the **App ID** that matches your app.
2.  Click **Continue**.

**Step 4: Select a Distribution Certificate**

1.  Choose the **iOS Distribution Certificate** or **Development Certificate** (depending on the profile type).
2.  Click **Continue**.

**Step 5: Select Registered Devices (For Development & Ad Hoc)**

1.  If you selected **Development** or **Ad Hoc**, choose the devices that can run the app.
2.  Click **Continue**.

**Step 6: Name and Generate the Profile**

1.  Enter a **Profile Name** (e.g., "MyApp Development Profile").
2.  Click **Generate**.
3.  Click **Download** to get the `.mobileprovision` file.

### Installing Provisioning Profile[​](#installing-provisioning-profile "Direct link to Installing Provisioning Profile")

Provisioning profiles are stored in `~/Library/MobileDevice/Provisioning Profiles` directory.

To install downloaded provisioning profile just copy it to `~/Library/MobileDevice/Provisioning\ Profiles` directory with a new `{UUID}.mobileprovision` name.

Run the following command to get profile UUID:

```
profile_uuid=$(security cms -D -i ~/Downloads/{profile-name}.mobileprovision | xmllint --xpath "string(//key[.='UUID']/following-sibling::string[1])" -)echo $profile_uuid
```

Run this command to copy profile to `~/Library/MobileDevice/Provisioning Profiles` with a new name `{UUID}.mobileprovision`:

```
cp ~/Downloads/{profile-name}.mobileprovision ~/Library/MobileDevice/Provisioning\ Profiles/${profile_uuid}.mobileprovision
```

warning

If the copied profile disappears from the `~/Library/MobileDevice/Provisioning Profiles` directory, ensure that the Xcode process is not running in the background.

Finally, you can use this command to list all installed provisioning profiles, with their names and UUIDs:

```
for profile in ~/Library/MobileDevice/Provisioning\ Profiles/*.mobileprovision; do security cms -D -i "$profile" | grep -E -A1 '<key>(Name|UUID)</key>' | sed -n 's/.*<string>\(.*\)<\/string>/\1/p' | paste -d ' | ' - -; done
```

## Configuring build[​](#configuring-build "Direct link to Configuring build")

To can either pass .ipa build options via `flet build` command line or configure in `pyproject.toml`.

### Command line[​](#command-line "Direct link to Command line")

To successfully generate "runnable" IPA you should provide correct values for the following arguments:

-   `--ios-export-method` - specifies how the app should be packaged when exporting an `.ipa` file. Default is `debugging`. Can be one of the following:
    -   `debugging` (or deprecated `development`) - used for debugging and testing on development devices.
    -   `release-testing` (or deprecated `ad-hoc`) - used for distributing the app outside the App Store to specific registered devices.
    -   `app-store-connect` (or deprecated `app-store`) - used for submitting the app to the App Store.
    -   `enterprise` - used for internal distribution within an organization (requires an enterprise account).
-   `--ios-provisioning-profile` - provisioning profile name or UUID that used to sign and export an iOS app.
-   `--ios-signing-certificate` - certificate name, SHA-1 hash, or automatic selector to use for signing iOS app bundle. Automatic selectors allow Xcode to pick the newest installed certificate of a particular type. The available automatic selectors are "Apple Development", "Apple Distribution", "Developer ID Application", "iOS Developer", "iOS Distribution", "Mac App Distribution", and "Mac Developer".
-   `--ios-team-id` - developer team ID to export iOS app.
-   `--bundle-id` - bundle ID for the application, e.g. "com.mycompany.app-name" - used as an iOS, Android, macOS and Linux bundle ID.
-   `--org` - organization name in reverse domain name notation, e.g. `com.mycompany` (defaults to `com.flet`). The value is combined with `--project` and used as an iOS and Android bundle ID.
-   `--project` - project name in C-style identifier format (lowercase alphanumerics with underscores) used to build bundle ID and as a name for bundle executable. By default, it's the name of Flet app directory.

Development package

To build `.ipa` for testing on your developer device you need to provide `--ios-provisioning-profile` option only. `flet build` will assume `debugging` as an export method and automatically choose the most recent "Apple Development" certificate in your keychain. Team ID is not required.

Bundle ID or Org?

You can specify either `--bundle-id`, `--org`, or both.

-   If only the `--bundle-id` is provided and "--org" is not, the organization name is derived from the bundle ID by extracting the part before the last dot.
-   If only `--org` is specified and the "--bundle-id" is not, the bundle ID is generated as `{org}.{project_name}`.

### `pyproject.toml`[​](#pyprojecttoml "Direct link to pyprojecttoml")

You can also configure package export and signing settings in `pyproject.toml`.

Project name and org:

```
[project]name = "my-app"[tool.flet]org = "com.mycompany"
```

or bundle ID:

```
[tool.flet]bundle_id = "com.mycompany.example-app"
```

Both `org` and `bundle_id` could be platform-specific, for example:

```
[tool.flet.ios]bundle_id = "com.mycompany.example-app-ios"[tool.flet.android]bundle_id = "com.mycompany.example-app-android"
```

To configure iOS signing settings that will be globally applied to all export methods:

```
[tool.flet.ios]provisioning_profile = "release-testing com.mycompany.example-app"signing_certificate = "Apple Distribution"team_id = "ABCDEFE234"export_options = { uploadSymbols = false }
```

To configure signing settings per export methods:

```
[tool.flet.ios.export_methods."debugging"]provisioning_profile = "debugging com.mycompany.example-app"signing_certificate = "Apple Development"[tool.flet.ios.export_methods."release-testing"]provisioning_profile = "release-testing com.mycompany.example-app"team_id = "ABCDEFE234"signing_certificate = "Apple Distribution"export_options = { uploadSymbols = false }[tool.flet.ios.export_methods."app-store-connect"]provisioning_profile = "app-store-connect com.mycompany.example-app"team_id = "ABCDEFE234"signing_certificate = "Apple Distribution"export_options = { uploadSymbols = true }
```

With the settings above you can run `flet build` command with just `--ios-export-method` provided, for example:

```
flet build ipa --ios-export-method release-testing
```

## Deploying app to an Apple device for testing[​](#deploying-app-to-an-apple-device-for-testing "Direct link to Deploying app to an Apple device for testing")

Apple Configurator for macOS allows you to install `.ipa` files on iOS devices without using the App Store.

Follow these steps to deploy an `.ipa` file to your device:

**Step 1: Install Apple Configurator**

1.  Install [Apple Configurator](https://apps.apple.com/ca/app/apple-configurator/id1037126344?mt=12) from App Store.

**Step 2: Connect the iOS Device**

1.  Connect the **iPhone** or **iPad** to your Mac using a USB cable.
2.  Unlock the device and **Trust** the computer if prompted.

**Step 3: Open Apple Configurator**

1.  Launch **Apple Configurator** on your Mac.
2.  The connected device should appear in the main window.

**Step 4: Add the `.ipa` File**

1.  Drag and drop the `.ipa` file onto the connected device in Apple Configurator.
2.  Alternatively, click **Add → Apps**, then choose the `.ipa` file from your Mac.

**Step 5: Install the App**

1.  Click **Prepare** or **Install** to begin the deployment.
2.  Apple Configurator will install the app on the device.

**Step 6: Trust the Developer Profile (For Ad Hoc or Enterprise Apps)**

If the `.ipa` is installed from an **Ad Hoc or Enterprise profile**, you may need to manually trust the developer:

1.  On the iOS device, go to **Settings → General → VPN & Device Management**.
2.  Under **Developer App**, select your **Developer Profile**.
3.  Tap **Trust** and confirm.

## Uploading app to App Store Connect for distribution[​](#uploading-app-to-app-store-connect-for-distribution "Direct link to Uploading app to App Store Connect for distribution")

**Transporter** is a macOS app that allows you to upload `.ipa` files to **App Store Connect** for distribution.

**Step 1: Install Transporter**

1.  Install [Transporter](https://apps.apple.com/us/app/transporter/id1450874784) from App Store.

**Step 2: Prepare the `.ipa` File**

1.  Ensure your `.ipa` file is built with either **app-store-connect** or **release-testing** export methods.

**Step 3: Open Transporter and Sign In**

1.  Launch **Transporter** on your Mac.
2.  Sign in with your **Apple Developer Account** (the same one used for App Store Connect).

**Step 4: Upload the `.ipa` File**

1.  Drag and drop the `.ipa` file into the Transporter window.
2.  Alternatively, click **Add App**, then choose the `.ipa` file from your Mac.
3.  Click `...` button next to "Deliver" and choose "Verify".
4.  Wait for Transporter to **verify** the file.
5.  Click **"Deliver"** to start the upload.

**Step 5: Check Upload Status**

1.  Once the upload is complete, Transporter will display a **success message**.
2.  If there are errors, review them and correct any issues before retrying the upload.

**Step 6: Confirm in App Store Connect**

1.  Go to [App Store Connect](https://appstoreconnect.apple.com/).
2.  Navigate to **Apps → Your App → TestFlight or App Store Version**.
3.  The uploaded build should appear under **Processing** (this may take a few minutes to an hour).
4.  Once processing is complete, you can **submit the app for review**.

## Permissions[​](#permissions "Direct link to Permissions")

Setting iOS permissions which are written into `Info.plist` file:

```
flet build --info-plist permission_1=True|False|description permission_2=True|False|description ...
```

For example:

```
flet build --info-plist NSLocationWhenInUseUsageDescription="This app uses location service when in use."
```

Configuring iOS permissions in `pyproject.toml`:

```
[tool.flet.ios.info] # --info-plistNSCameraUsageDescription = "This app uses the camera to ..."
```

## Deep linking[​](#deep-linking "Direct link to Deep linking")

You can configure deep-linking settings for iOS bundle with the following `flet build` options:

-   `--deep-linking-scheme` - deep linking URL scheme to configure for iOS and Android builds, i.g. "https" or "myapp".
-   `--deep-linking-host` - deep linking URL host.

The same can be configured in `pyproject.toml`:

```
[tool.flet.ios.deep_linking]scheme = "https"host = "mydomain.com"
```

See [Deep linking](https://docs.flutter.dev/ui/navigation/deep-linking) section in Flutter docs for more information and complete setup guide.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/publish/ios.md)

[

Previous

Android

](/docs/publish/android)[

Next

macOS

](/docs/publish/macos)

-   [Introduction](#introduction)
-   [Prerequisites](#prerequisites)
    -   [Rosetta 2](#rosetta-2)
    -   [Xcode](#xcode)
    -   [CocoaPods](#cocoapods)
    -   [iOS wheels for binary Python packages](#ios-wheels-for-binary-python-packages)
-   [`flet build ipa`](#flet-build-ipa)
-   [Application Identifier](#application-identifier)
    -   [Creating a new App ID](#creating-a-new-app-id)
-   [Signing Certificate](#signing-certificate)
    -   [Generating a Certificate Signing Request (CSR)](#generating-a-certificate-signing-request-csr)
    -   [Creating a Certificate in Apple Developer Portal](#creating-a-certificate-in-apple-developer-portal)
-   [Provisioning Profile](#provisioning-profile)
    -   [Creating a new Provisioning Profile](#creating-a-new-provisioning-profile)
    -   [Installing Provisioning Profile](#installing-provisioning-profile)
-   [Configuring build](#configuring-build)
    -   [Command line](#command-line)
    -   [`pyproject.toml`](#pyprojecttoml)
-   [Deploying app to an Apple device for testing](#deploying-app-to-an-apple-device-for-testing)
-   [Uploading app to App Store Connect for distribution](#uploading-app-to-app-store-connect-for-distribution)
-   [Permissions](#permissions)
-   [Deep linking](#deep-linking)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Built-in Flet extensions | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/extend/built-in-extensions/img/logo.svg)![Flet Logo](https://flet.dev/docs/extend/built-in-extensions/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/extend/built-in-extensions/img/logo.svg)![Flet Logo](https://flet.dev/docs/extend/built-in-extensions/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
    -   [Built-in extensions](/docs/extend/built-in-extensions)
    -   [User extensions](/docs/extend/user-extensions)
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   Extending Flet
-   Built-in extensions

# Built-in Flet extensions

Flet controls based on 3rd-party Flutter packages that used to be a part of Flet repository, now have been moved to separate repos and published on pypi:

-   [flet-ads](https://pypi.org/project/flet-ads/)
-   [flet-audio](https://pypi.org/project/flet-audio/)
-   [flet-audio-recorder](https://pypi.org/project/flet-audio-recorder/)
-   [flet-flashlight](https://pypi.org/project/flet-flashlight/)
-   [flet-geolocator](https://pypi.org/project/flet-geolocator/)
-   [flet-lottie](https://pypi.org/project/flet-lottie/)
-   [flet-map](https://pypi.org/project/flet-map/)
-   [flet-permission-handler](https://pypi.org/project/flet-permission-handler/)
-   [flet-rive](https://pypi.org/project/flet-rive/)
-   [flet-video](https://pypi.org/project/flet-video/)
-   [flet-webview](https://pypi.org/project/flet-webview/)

To use a built-in Flet extension in your project, add it to the `dependencies` section of your `pyproject.toml` file, for example:

```
dependencies = [  "flet-audio",  "flet>=0.26.0",]
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/extend/built-in-extensions.md)

[

Previous

Self Hosting

](/docs/publish/web/dynamic-website/hosting/self-hosting)[

Next

User extensions

](/docs/extend/user-extensions)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Creating Flet extension for existing Flutter package | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/extend/user-extensions/img/logo.svg)![Flet Logo](https://flet.dev/docs/extend/user-extensions/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/extend/user-extensions/img/logo.svg)![Flet Logo](https://flet.dev/docs/extend/user-extensions/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
    -   [Built-in extensions](/docs/extend/built-in-extensions)
    -   [User extensions](/docs/extend/user-extensions)
-   [Controls](/docs/controls)
    
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   Extending Flet
-   User extensions

On this page

# Creating Flet extension for existing Flutter package

## Introduction[​](#introduction "Direct link to Introduction")

While Flet controls leverage many built-in Flutter widgets, enabling the creation of complex applications, not all Flutter widgets or third-party packages can be directly supported by the Flet team or included within the core Flet framework.

To address this, the Flet framework provides an extensibility mechanism. This allows you to incorporate widgets and APIs from your own custom Flutter packages or [third-party libraries](https://pub.dev/packages?sort=popularity) directly into your Flet application.

In this guide, you will learn how to create Flet extension from template and then customize it to integrate 3rd-party Flutter package into your Flet app.

### Prerequisites[​](#prerequisites "Direct link to Prerequisites")

To integrate custom Flutter package into Flet you need to have basic understanding of how to create Flutter apps and packages in Dart language and have Flutter development environment configured. See [Flutter Getting Started](https://docs.flutter.dev/get-started/install) for more information about Flutter and Dart.

## Create Flet extension from template[​](#create-flet-extension-from-template "Direct link to Create Flet extension from template")

Flet now makes it easy to create and build projects with your custom controls based on Flutter widgets or Flutter 3rd-party packages. In the example below, we will be creating a custom Flet extension based on the [flutter\_spinkit](https://pub.dev/packages/flutter_spinkit) package.

1.  Create new virtual enviroment and [install Flet](/docs/getting-started/#virtual-environment) there.
    
2.  Create new Flet extension project from template:
    

```
flet create --template extension --project-name flet-spinkit
```

A project with new FletSpinkit control will be created. The control is just a Flutter Text widget with text property, which we will customize later.

3.  Build your app.

Flet project created from extension template has `examples/flet_spinkit_example` folder with the example app.

When in the folder where your `pyproject.toml` for the app is (`examples/flet_spinkit_example`), run `flet build` command, for example, for macos:

```
flet build macos -v
```

Open the app and see the new custom Flet Control:

```
open build/macos/flet-spinkit-example.app
```

![](https://flet.dev/docs/extend/user-extensions/img/docs/extending-flet/example.png)

4.  Change your app.

Once the project was built for desktop once, you can make changes to your python files and run it without re-building.

First, install dependencies from pyproject.toml:

```
pip install .
```

Now you can make changes to your example app main.py:

```
import flet as ftfrom flet_spinkit import FletSpinkitdef main(page: ft.Page):    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.add(        ft.Container(            height=150,            width=300,            alignment=ft.alignment.center,            bgcolor=ft.Colors.PINK_200,            content=FletSpinkit(                tooltip="My new PINK FletSpinkit Control tooltip",                value="My new PINK FletSpinkit Flet Control",            ),        ),    )ft.app(main)
```

and run:

```
flet run
```

![](https://flet.dev/docs/extend/user-extensions/img/docs/extending-flet/example-pink.png)

5.  Re-build your app.

Known issue

There is a [known issue](https://github.com/flet-dev/flet/issues/4754) that Flet would build with cached files and your changes will not be included. As a temporary solution, you need to clear cache before re-building:

```
pip cache purge
```

When you make any changes to your package, you need to re-build:

```
pip cache purgeflet build macos -v
```

If you need to debug, run this command:

```
build/macos/flet-spinkit-example.app/Contents/MacOS/flet-spinkit-example --debug
```

## Integrate 3rd-party Flutter package[​](#integrate-3rd-party-flutter-package "Direct link to Integrate 3rd-party Flutter package")

For the example purposes we will be integrating [flutter\_spinkit](https://pub.dev/packages/flutter_spinkit) package into our Flet app.

1.  Add dependency.

Go to `src/flutter/flet_spinkit` folder and run this command to add dependency to `flutter_spinkit` to `pubspec.yaml`:

```
flutter pub add flutter_spinkit
```

Read more information about using Flutter packages [here](https://docs.flutter.dev/packages-and-plugins/using-packages).

2.  Modify `dart` file.

In the `src/flutter/flet_spinkit/lib/src/flet_spinkit.dart` file, add import statement and replace Text widget with `SpinKitRotatingCircle` widget:

```
import 'package:flet/flet.dart';import 'package:flutter/material.dart';import 'package:flutter_spinkit/flutter_spinkit.dart';class FletSpinkitControl extends StatelessWidget {  final Control? parent;  final Control control;  const FletSpinkitControl({    super.key,    required this.parent,    required this.control,  });  @override  Widget build(BuildContext context) {    Widget myControl = SpinKitRotatingCircle(      color: Colors.red,      size: 100.0,    );    return constrainedControl(context, myControl, parent, control);  }}
```

3.  Rebuild your example app.

Go to `examples/flet_spinkit_example`, clear cache and rebuild your app:

```
pip cache purgeflet build macos -v
```

4.  Run your app:

![](https://flet.dev/docs/extend/user-extensions/img/docs/extending-flet/spinkit1.gif)

## Flet extension structure[​](#flet-extension-structure "Direct link to Flet extension structure")

After creating new Flet project from extension template, you will see the following folder structure:

```
├── LICENSE├── README.md├── examples│   └── flet_spinkit_example│       ├── README.md│       ├── pyproject.toml│       └── src│           └── main.py├── pyproject.toml└── src    ├── flet_spinkit    │   ├── __init__.py    │   └── flet_spinkit.py    └── flutter        └── flet_spinkit            ├── CHANGELOG.md            ├── LICENSE            ├── README.md            ├── lib            │   ├── flet_spinkit.dart            │   └── src            │       ├── create_control.dart            │       └── flet_spinkit.dart            └── pubspec.yaml
```

Flet extension consists of:

-   **package**, located in `src` folder
-   **example app**, located in `examples/flet-spinkit_example` folder

### Package[​](#package "Direct link to Package")

Package is the component that will be used in your app. It contists of two parts: Python and Flutter.

#### Python[​](#python "Direct link to Python")

##### flet\_spinkit.py[​](#flet_spinkitpy "Direct link to flet_spinkit.py")

Here you create Flet Python control - a Python class that you use in your Flet app.

The minumal requirements for this class is that it has to be inherited from Flet `Control` and it has to have `_get_control_name` method that will return the control name. This name should be the same as `args.control.type` we check in the `create_control.dart` file.

#### Flutter[​](#flutter "Direct link to Flutter")

##### pubspec.yaml[​](#pubspecyaml "Direct link to pubspec.yaml")

A yaml file containing metadata that specifies the package's dependencies.

There is already a dependency to `flet` created from template. You need to add there a dependency to Flutter package for which you are creating your extension.

##### flet\_spinkit.dart[​](#flet_spinkitdart "Direct link to flet_spinkit.dart")

Two methods are exported:

-   `createControl` - called to create a widget that corresponds to a control on Python side.
-   `ensureInitialized` - called once on Flet program start.

##### src/create\_control.dart[​](#srccreate_controldart "Direct link to src/create_control.dart")

Creates Flutter widget based on control names returned by the Control's `_get_control_name()` function. This mechanism iterates through all third-party packages and returns the first matching widget.

##### src/flet\_spinkit.dart[​](#srcflet_spinkitdart "Direct link to src/flet_spinkit.dart")

Here you create Flutter "wrapper" widget that will build Flutter widget or API that you want to use in your Flet app.

Wrapper widget passes the state of Python control down to a Flutter widget, that will be displayed on a page, and provides an API to route events from Flutter widget back to Python control.

### Example app[​](#example-app "Direct link to Example app")

##### src/main.py[​](#srcmainpy "Direct link to src/main.py")

Python program that uses Flet Python control.

##### pyproject.toml[​](#pyprojecttoml "Direct link to pyproject.toml")

Here you specify dependency to your package, which can be:

-   **Path dependency**

Absolute path to your Flet extension folder, for example:

```
dependencies = [  "flet-spinkit @ file:///Users/user-name/projects/flet-spinkit",  "flet>=0.26.0",]
```

-   **Git dependency**

Link to git repository, for example:

```
dependencies = [  "flet-ads @ git+https://github.com/flet-dev/flet-ads.git",  "flet>=0.26.0",]
```

-   **PyPi dependency**

Name of the package published on pypi.org, for example:

```
dependencies = [  "flet-ads",  "flet>=0.26.0",]
```

## Customize properties[​](#customize-properties "Direct link to Customize properties")

In the example above, Spinkit control creates a hardcoded Flutter widget. Now let's customize its properties.

### Common properties[​](#common-properties "Direct link to Common properties")

Generally, there are two types of controls in Flet:

1.  Visual controls that are added to the app/page surface, such as FletSpinkit.
    
2.  Non-visual controls that can be:
    
    -   popup controls (dialogs, pickers, panels etc.).
        
    -   services that are added to `overlay`, such as Video or Audio.
        

Flet `Control` class has properties common for all controls such as `visible`, `opacity` and `tooltip`, to name a few.

Flet `ConstrainedControl` class is inherited from `Control` and has many additional properties such as `top` and `left` for its position within Stack and a bunch of animation properties.

When creating non-visual control, your Python control should be inherited from ['Control](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet/src/flet/core/control.py). Then, to be able to use `Control` properties in your app, you need to add them to the constructor of your Python Control. In its dart counterpart (`src/flet_spinkit.dart`) use `baseControl()` to wrap your Flutter widget.

When creating visual control, your Python control should be inherited from [`ConstrainedControl`](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet/src/flet/core/constrained_control.py). In its dart counterpart (`src/flet_spinkit.dart`) use `constrainedControl()` to wrap your Flutter widget.

Then, to be able to use `Control` and `ConstrainedControl` properties in your app, you need to add them to the constructor of your Python Control.

See reference for the common Control properties [here](https://flet.dev/docs/controls).

If you have created your extension project from Flet extension template, your Python Control is already inherited from `ConstrainedControl` and you can use its properties in your example app:

```
import flet as ftfrom flet_spinkit import FletSpinkitdef main(page: ft.Page):    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.add(        ft.Stack(            [                ft.Container(height=200, width=200, bgcolor=ft.Colors.BLUE_100),                FletSpinkit(opacity=0.5, tooltip="Spinkit tooltip", top=0, left=0),            ]        )    )ft.app(main)
```

![](https://flet.dev/docs/extend/user-extensions/img/docs/extending-flet/spinkit2.gif)

### Control-specific properties[​](#control-specific-properties "Direct link to Control-specific properties")

Now that you have taken full advantage of the properties Flet `Control` and `ConstrainedControl` offer, let's define the properties that are specific to the new Control you are building.

In the FletSpinkit example, let's define its `color` and `size`.

In Python class, define new `color` and `size` properties:

```
from enum import Enumfrom typing import Any, Optionalfrom flet.core.constrained_control import ConstrainedControlfrom flet.core.control import OptionalNumberfrom flet.core.types import ColorEnums, ColorValueclass FletSpinkit(ConstrainedControl):    """    FletSpinkit Control.    """    def __init__(        self,        #        # Control        #        opacity: OptionalNumber = None,        tooltip: Optional[str] = None,        visible: Optional[bool] = None,        data: Any = None,        #        # ConstrainedControl        #        left: OptionalNumber = None,        top: OptionalNumber = None,        right: OptionalNumber = None,        bottom: OptionalNumber = None,        #        # FletSpinkit specific        #        color: Optional[ColorValue] = None,        size: OptionalNumber = None,    ):        ConstrainedControl.__init__(            self,            tooltip=tooltip,            opacity=opacity,            visible=visible,            data=data,            left=left,            top=top,            right=right,            bottom=bottom,        )        self.color = color        self.size = size    def _get_control_name(self):        return "flet_spinkit"    # color    @property    def color(self) -> Optional[ColorValue]:        return self.__color    @color.setter    def color(self, value: Optional[ColorValue]):        self.__color = value        self._set_enum_attr("color", value, ColorEnums)    # size    @property    def size(self):        return self._get_attr("size")    @size.setter    def size(self, value):        self._set_attr("size", value)
```

In `src/flet_spinkit.dart` file, use helper methods `attrColor` and `attrDouble` to access color and size values:

```
import 'package:flet/flet.dart';import 'package:flutter/material.dart';import 'package:flutter_spinkit/flutter_spinkit.dart';class FletSpinkitControl extends StatelessWidget {  final Control? parent;  final Control control;  const FletSpinkitControl({    super.key,    required this.parent,    required this.control,  });  @override  Widget build(BuildContext context) {    var color = control.attrColor("color", context);    var size = control.attrDouble("size");    Widget myControl = SpinKitRotatingCircle(      color: color,      size: size ?? 100,    );    return constrainedControl(context, myControl, parent, control);  }}
```

Use `color` and `size` properties in your app:

```
import flet as ftfrom flet_spinkit import FletSpinkitdef main(page: ft.Page):    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.add(        ft.Stack(            [                ft.Container(height=200, width=200, bgcolor=ft.Colors.BLUE_100),                FletSpinkit(                    opacity=0.5,                    tooltip="Spinkit tooltip",                    top=0,                    left=0,                    color=ft.Colors.YELLOW,                    size=150,                ),            ]        )    )ft.app(main)
```

Re-build and run:

![](https://flet.dev/docs/extend/user-extensions/img/docs/extending-flet/spinkit3.gif)

You can find source code for this example [here](https://github.com/flet-dev/flet-spinkit).

#### Examples for different types of properties and events[​](#examples-for-different-types-of-properties-and-events "Direct link to Examples for different types of properties and events")

##### Enum properties[​](#enum-properties "Direct link to Enum properties")

For example, `clip_behaviour` for `AppBar`.

In [Python](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet/src/flet/core/app_bar.py):

```
# clip_behavior@propertydef clip_behavior(self) -> Optional[ClipBehavior]:    return self._get_attr("clipBehavior")@clip_behavior.setterdef clip_behavior(self, value: Optional[ClipBehavior]):    self._set_attr(        "clipBehavior",        value.value if isinstance(value, ClipBehavior) else value,    )
```

In [Dart](https://github.com/flet-dev/flet/blob/main/packages/flet/lib/src/controls/app_bar.dart):

```
var clipBehavior = Clip.values.firstWhere(    (e) =>        e.name.toLowerCase() ==        widget.control.attrString("clipBehavior", "")!.toLowerCase(),    orElse: () => Clip.none);
```

##### Json properties[​](#json-properties "Direct link to Json properties")

For example, `shape` property for `Card`.

In [Python](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet/src/flet/core/card.py):

```
def before_update(self):    super().before_update()    self._set_attr_json("shape", self.__shape)# shape@propertydef shape(self) -> Optional[OutlinedBorder]:    return self.__shape@shape.setterdef shape(self, value: Optional[OutlinedBorder]):    self.__shape = value
```

In [Dart](https://github.com/flet-dev/flet/blob/main/packages/flet/lib/src/controls/card.dart):

```
var shape = parseOutlinedBorder(control, "shape")
```

##### Children[​](#children "Direct link to Children")

For example, `content` for `AlertDialog`:

In [Python](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet/src/flet/core/alert_dialog.py):

```
    def _get_children(self):        children = []        if self.__content:            self.__content._set_attr_internal("n", "content")            children.append(self.__content)        return children
```

In [Dart](https://github.com/flet-dev/flet/blob/main/packages/flet/lib/src/controls/alert_dialog.dart):

```
    var contentCtrls =        widget.children.where((c) => c.name == "content" && c.isVisible);
```

##### Events[​](#events "Direct link to Events")

For example, `on_click` event for `ElevatedButton`.

In [Python](https://github.com/flet-dev/flet/blob/main/sdk/python/packages/flet/src/flet/core/elevated_button.py):

```
# on_click@propertydef on_click(self):    return self._get_event_handler("click")@on_click.setterdef on_click(self, handler):    self._add_event_handler("click", handler)
```

In [Dart](https://github.com/flet-dev/flet/blob/main/packages/flet/lib/src/controls/elevated_button.dart):

```
Function()? onPressed = !disabled    ? () {        debugPrint("Button ${widget.control.id} clicked!");        if (url != "") {        openWebBrowser(url,            webWindowName: widget.control.attrString("urlTarget"));        }        widget.backend.triggerControlEvent(widget.control.id, "click");    }    : null;
```

## Examples[​](#examples "Direct link to Examples")

Flet has controls that are implemented as [built-in extensions](/docs/extend/built-in-extensions) and could serve as a starting point for your own controls.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/extend/user-extensions.md)

[

Previous

Built-in extensions

](/docs/extend/built-in-extensions)[

Next

Controls reference

](/docs/controls)

-   [Introduction](#introduction)
    -   [Prerequisites](#prerequisites)
-   [Create Flet extension from template](#create-flet-extension-from-template)
-   [Integrate 3rd-party Flutter package](#integrate-3rd-party-flutter-package)
-   [Flet extension structure](#flet-extension-structure)
    -   [Package](#package)
    -   [Example app](#example-app)
-   [Customize properties](#customize-properties)
    -   [Common properties](#common-properties)
    -   [Control-specific properties](#control-specific-properties)
-   [Examples](#examples)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Controls reference | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   Controls

On this page

# Controls reference

Flet UI is built of controls. Controls are organized into hierarchy, or a tree, where each control has a parent (except [Page](/docs/controls/page)) and container controls like [Column](/docs/controls/column), [Dropdown](/docs/controls/dropdown) can contain child controls, for example:

```
Page ├─ TextField ├─ Dropdown │   ├─ Option │   └─ Option └─ Row     ├─ ElevatedButton     └─ ElevatedButton
```

[Control gallery live demo](https://flet-controls-gallery.fly.dev/layout)

## Controls by categories[​](#controls-by-categories "Direct link to Controls by categories")

[

## 🗃️ Layout

23 items

](/docs/controls/layout)

[

## 🗃️ Navigation

8 items

](/docs/controls/app-structure-navigation)

[

## 🗃️ Information Displays

12 items

](/docs/controls/information-displays)

[

## 🗃️ Buttons

18 items

](/docs/controls/buttons)

[

## 🗃️ Input and Selections

17 items

](/docs/controls/input-and-selections)

[

## 🗃️ Dialogs, Alerts and Panels

13 items

](/docs/controls/dialogs-alerts-panels)

[

## 🗃️ Charts

5 items

](/docs/controls/charts)

[

## 🗃️ Animations

3 items

](/docs/controls/animations)

[

## 🗃️ Utility

22 items

](/docs/controls/utility)

## Common control properties[​](#common-control-properties "Direct link to Common control properties")

Flet controls have the following properties:

### `adaptive`[​](#adaptive "Direct link to adaptive")

`adaptive` property can be specified for a control in the following cases:

-   A control has matching Cupertino control with similar functionality/presentation and graphics as expected on iOS/macOS. In this case, if `adaptive` is `True`, either Material or Cupertino control will be created depending on the target platform.
    
    These controls have their Cupertino analogs and `adaptive` property:
    
    -   [`AlertDialog`](/docs/controls/alertdialog)
    -   [`AppBar`](/docs/controls/appbar)
    -   [`Checkbox`](/docs/controls/checkbox)
    -   [`ListTile`](/docs/controls/listtile)
    -   [`NavigationBar`](/docs/controls/navigationbar)
    -   [`Radio`](/docs/controls/radio)
    -   [`Slider`](/docs/controls/slider)
    -   [`Switch`](/docs/controls/switch)
-   A control has child controls. In this case `adaptive` property value is passed on to its children that don't have their `adaptive` property set.
    
    The following container controls have `adaptive` property:
    
    -   [`Card`](/docs/controls/card)
    -   [`Column`](/docs/controls/column)
    -   [`Container`](/docs/controls/container)
    -   [`Dismissible`](/docs/controls/dismissible)
    -   [`ExpansionPanel`](/docs/controls/expansionpanel)
    -   [`FletApp`](/docs/controls/fletapp)
    -   [`GestureDetector`](/docs/controls/gesturedetector)
    -   [`GridView`](/docs/controls/gridview)
    -   [`ListView`](/docs/controls/listview)
    -   [`Page`](/docs/controls/page)
    -   [`Row`](/docs/controls/row)
    -   [`SafeArea`](/docs/controls/safearea)
    -   [`Stack`](/docs/controls/stack)
    -   [`Tabs`](/docs/controls/tabs)
    -   [`View`](/docs/controls/view)

### `badge`[​](#badge "Direct link to badge")

The `badge` property (available in almost all controls) supports both strings and [`Badge`](/docs/reference/types/badge) objects.

### `bottom`[​](#bottom "Direct link to bottom")

Effective inside [`Stack`](/docs/controls/stack) only. The distance that the child's bottom edge is inset from the bottom of the stack.

### `data`[​](#data "Direct link to data")

Arbitrary data that can be attached to a control.

### `disabled`[​](#disabled "Direct link to disabled")

Every control has `disabled` property which is `False` by default - control and all its children are enabled. `disabled` property is mostly used with data entry controls like `TextField`, `Dropdown`, `Checkbox`, buttons. However, `disabled` could be set to a parent control and its value will be propagated down to all children recursively.

For example, if you have a form with multiple entry controls you can disable them all together by disabling container:

```
c = ft.Column(controls=[    ft.TextField(),    ft.TextField()])c.disabled = Truepage.add(c)
```

### `expand`[​](#expand "Direct link to expand")

When a child Control is placed into a [`Column`](/docs/controls/column) or a [`Row`](/docs/controls/row) you can "expand" it to fill the available space. `expand` property could be a boolean value (`True` - expand control to fill all available space) or an integer - an "expand factor" specifying how to divide a free space with other expanded child controls.

For more information and examples about `expand` property see "Expanding children" sections in [`Column`](/docs/controls/column#expanding-children) or [`Row`](/docs/controls/row#expanding-children).

Here is an example of expand being used in action for both [`Column`](/docs/controls/column) and [`Row`](/docs/controls/row):

```
import flet as ftdef main(page: ft.Page):    page.spacing = 0    page.padding = 0    page.add(        ft.Column(            controls=[                ft.Row(                    [                        ft.Card(                            content=ft.Text("Card_1"),                            color=ft.Colors.ORANGE_300,                            expand=True,                            height=page.height,                            margin=0,                        ),                        ft.Card(                            content=ft.Text("Card_2"),                            color=ft.Colors.GREEN_100,                            expand=True,                            height=page.height,                            margin=0,                        ),                    ],                    expand=True,                    spacing=0,                ),            ],            expand=True,            spacing=0,        ),    )ft.app(main)
```

### `expand_loose`[​](#expand_loose "Direct link to expand_loose")

Effective only if `expand` is `True`.

If `expand_loose` is `True`, the child control of a [`Column`](/docs/controls/column) or a [`Row`](/docs/controls/row) will be given the flexibility to expand to fill the available space in the main axis (e.g., horizontally for a Row or vertically for a Column), but will not be required to fill the available space.

The default value is `False`.

Here is the example of Containers placed in Rows with `expand_loose = True`:

```
import flet as ftclass Message(ft.Container):    def __init__(self, author, body):        super().__init__()        self.content = ft.Column(            controls=[                ft.Text(author, weight=ft.FontWeight.BOLD),                ft.Text(body),            ],        )        self.border = ft.border.all(1, ft.Colors.BLACK)        self.border_radius = ft.border_radius.all(10)        self.bgcolor = ft.Colors.GREEN_200        self.padding = 10        self.expand = True        self.expand_loose = Truedef main(page: ft.Page):    chat = ft.ListView(        padding=10,        spacing=10,        controls=[            ft.Row(                alignment=ft.MainAxisAlignment.START,                controls=[                    Message(                        author="John",                        body="Hi, how are you?",                    ),                ],            ),            ft.Row(                alignment=ft.MainAxisAlignment.END,                controls=[                    Message(                        author="Jake",                        body="Hi I am good thanks, how about you?",                    ),                ],            ),            ft.Row(                alignment=ft.MainAxisAlignment.START,                controls=[                    Message(                        author="John",                        body="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",                    ),                ],            ),            ft.Row(                alignment=ft.MainAxisAlignment.END,                controls=[                    Message(                        author="Jake",                        body="Thank you!",                    ),                ],            ),        ],    )    page.window.width = 393    page.window.height = 600    page.window.always_on_top = False    page.add(chat)ft.app(main)
```

![](https://flet.dev/docs/controls/img/docs/controls/overview/expand = True, expand_loose = True.png)

### `height`[​](#height "Direct link to height")

Imposed Control height in virtual pixels.

### `left`[​](#left "Direct link to left")

Effective inside [`Stack`](/docs/controls/stack) only. The distance that the child's left edge is inset from the left of the stack.

### `parent`[​](#parent "Direct link to parent")

Points to the direct ancestor(parent) of this control.

It defaults to `None` and will only have a value when this control is mounted (added to the page tree).

The `Page` control (which is the root of the tree) is an exception - it always has `parent=None`.

### `right`[​](#right "Direct link to right")

Effective inside [`Stack`](/docs/controls/stack) only. The distance that the child's right edge is inset from the right of the stack.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The `tooltip` property (available in almost all controls) now supports both strings and [`Tooltip`](/docs/reference/types/tooltip) objects.

### `top`[​](#top "Direct link to top")

Effective inside [`Stack`](/docs/controls/stack) only. The distance that the child's top edge is inset from the top of the stack.

### `visible`[​](#visible "Direct link to visible")

Every control has `visible` property which is `True` by default - control is rendered on the page. Setting `visible` to `False` completely prevents control (and all its children if any) from rendering on a page canvas. Hidden controls cannot be focused or selected with a keyboard or mouse and they do not emit any events.

### `width`[​](#width "Direct link to width")

Imposed Control width in virtual pixels.

## Transformations[​](#transformations "Direct link to Transformations")

### `offset`[​](#offset "Direct link to offset")

Applies a translation transformation before painting the control.

The translation is expressed as a `transform.Offset` scaled to the control's size. For example, an `Offset` with a `x` of `0.25` will result in a horizontal translation of one quarter the width of the control.

The following example displays container at `0, 0` top left corner of a stack as transform applies `-1 * 100, -1 * 100` (`offset * control_size`) horizontal and vertical translations to the control:

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Stack(            [                ft.Container(                    bgcolor="red",                    width=100,                    height=100,                    left=100,                    top=100,                    offset=ft.transform.Offset(-1, -1),                )            ],            width=1000,            height=1000,        )    )ft.app(main)
```

### `opacity`[​](#opacity "Direct link to opacity")

Defines the transparency of the control.

Value ranges from `0.0` (completely transparent) to `1.0` (completely opaque without any transparency) and defaults to `1.0`.

### `rotate`[​](#rotate "Direct link to rotate")

Transforms control using a rotation around the center.

The value of `rotate` property could be one of the following types:

-   `number` - a rotation in clockwise radians. Full circle `360°` is `math.pi * 2` radians, `90°` is `pi / 2`, `45°` is `pi / 4`, etc.
-   `transform.Rotate` - allows to specify rotation `angle` as well as `alignment` - the location of rotation center.

For example:

```
ft.Image(    src="https://picsum.photos/100/100",    width=100,    height=100,    border_radius=5,    rotate=Rotate(angle=0.25 * pi, alignment=ft.alignment.center_left))
```

### `scale`[​](#scale "Direct link to scale")

Scale control along the 2D plane. Default scale factor is `1.0` - control is not scaled. `0.5` - the control is twice smaller, `2.0` - the control is twice larger.

Different scale multipliers can be specified for `x` and `y` axis, but setting `Control.scale` property to an instance of `transform.Scale` class:

```
from dataclasses import fieldclass Scale:    scale: float = field(default=None)    scale_x: float = field(default=None)    scale_y: float = field(default=None)    alignment: Alignment = field(default=None)
```

Either `scale` or `scale_x` and `scale_y` could be specified, but not all of them, for example:

```
ft.Image(    src="https://picsum.photos/100/100",    width=100,    height=100,    border_radius=5,    scale=Scale(scale_x=2, scale_y=0.5))
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/overview.md)

[

Previous

User extensions

](/docs/extend/user-extensions)[

Next

Layout

](/docs/controls/layout)

-   [Controls by categories](#controls-by-categories)
-   [Common control properties](#common-control-properties)
    -   [`adaptive`](#adaptive)
    -   [`badge`](#badge)
    -   [`bottom`](#bottom)
    -   [`data`](#data)
    -   [`disabled`](#disabled)
    -   [`expand`](#expand)
    -   [`expand_loose`](#expand_loose)
    -   [`height`](#height)
    -   [`left`](#left)
    -   [`parent`](#parent)
    -   [`right`](#right)
    -   [`tooltip`](#tooltip)
    -   [`top`](#top)
    -   [`visible`](#visible)
    -   [`width`](#width)
-   [Transformations](#transformations)
    -   [`offset`](#offset)
    -   [`opacity`](#opacity)
    -   [`rotate`](#rotate)
    -   [`scale`](#scale)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Card | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/card/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/card/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/card/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/card/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Card

On this page

# Card

A material design card: a panel with slightly rounded corners and an elevation shadow.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/card)

-   Python

```
import flet as ftdef main(page):    page.title = "Card Example"    page.add(        ft.Card(            content=ft.Container(                content=ft.Column(                    [                        ft.ListTile(                            leading=ft.Icon(ft.Icons.ALBUM),                            title=ft.Text("The Enchanted Nightingale"),                            subtitle=ft.Text(                                "Music by Julie Gable. Lyrics by Sidney Stein."                            ),                        ),                        ft.Row(                            [ft.TextButton("Buy tickets"), ft.TextButton("Listen")],                            alignment=ft.MainAxisAlignment.END,                        ),                    ]                ),                width=400,                padding=10,            )        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/card/img/docs/controls/card/card.gif)

## Properties[​](#properties "Direct link to Properties")

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The `content` will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `color`[​](#color "Direct link to color")

The card's background [color](/docs/reference/colors).

### `content`[​](#content "Direct link to content")

The `Control` that should be displayed inside the card.

This control can only have one child. To lay out multiple children, let this control's child be a control such as [`Row`](/docs/controls/row), [`Column`](/docs/controls/column), or [`Stack`](/docs/controls/stack), which have a children property, and then provide the children to that control.

### `elevation`[​](#elevation "Direct link to elevation")

Controls the size of the shadow below the card. Default value is `1.0`.

### `is_semantic_container`[​](#is_semantic_container "Direct link to is_semantic_container")

Set to `True` (default) if this card represents a single semantic container, or to `False` if it instead represents a collection of individual semantic nodes (different types of content).

### `margin`[​](#margin "Direct link to margin")

The empty space that surrounds the card.

Value can be one of the following types: `int`, `float`, or [`Margin`](/docs/reference/types/margin).

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) to paint the shadow below the card.

### `shape`[​](#shape "Direct link to shape")

The shape of the card.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder) and defaults to `RoundedRectangleBorder(radius=4.0)`.

### `show_border_on_foreground`[​](#show_border_on_foreground "Direct link to show_border_on_foreground")

Whether the shape of the border should be painted in front of the `content` or behind.

Defaults to `True`.

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The [color](/docs/reference/colors) used as an overlay on `color` to indicate elevation.

If this is `None`, no overlay will be applied. Otherwise this color will be composited on top of `color` with an opacity related to `elevation` and used to paint the background of the card.

Defaults to `None`.

### `variant`[​](#variant "Direct link to variant")

Defines the card variant to be used.

Value is of type [`CardVariant`](/docs/reference/types/cardvariant) and defaults to `CardVariant.ELEVATED`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/card.md)

[

Previous

Layout

](/docs/controls/layout)[

Next

Column

](/docs/controls/column)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`clip_behavior`](#clip_behavior)
    -   [`color`](#color)
    -   [`content`](#content)
    -   [`elevation`](#elevation)
    -   [`is_semantic_container`](#is_semantic_container)
    -   [`margin`](#margin)
    -   [`shadow_color`](#shadow_color)
    -   [`shape`](#shape)
    -   [`show_border_on_foreground`](#show_border_on_foreground)
    -   [`surface_tint_color`](#surface_tint_color)
    -   [`variant`](#variant)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Column | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/column/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/column/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/column/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/column/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Column

On this page

# Column

A control that displays its children in a vertical array.

To cause a child control to expand and fill the available vertical space set its `expand` property.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/column)

### Column spacing[​](#column-spacing "Direct link to Column spacing")

![](https://flet.dev/docs/controls/column/img/docs/controls/column/column-spacing.gif)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER,                    border_radius=ft.border_radius.all(5),                )            )        return items    def spacing_slider_change(e):        col.spacing = int(e.control.value)        col.update()    gap_slider = ft.Slider(        min=0,        max=100,        divisions=10,        value=0,        label="{value}",        width=500,        on_change=spacing_slider_change,    )    col = ft.Column(spacing=0, controls=items(5))    page.add(ft.Column([ ft.Text("Spacing between items"), gap_slider]), col)ft.app(main)
```

### Column wrapping[​](#column-wrapping "Direct link to Column wrapping")

![](https://flet.dev/docs/controls/column/img/docs/controls/column/column-wrapping.gif)

-   Python

```
import flet as ftHEIGHT = 400def main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=30,                    height=30,                    bgcolor=ft.Colors.AMBER,                    border_radius=ft.border_radius.all(5),                )            )        return items    def slider_change(e):        col.height = float(e.control.value)        col.update()    width_slider = ft.Slider(        min=0,        max=HEIGHT,        divisions=20,        value=HEIGHT,        label="{value}",        width=500,        on_change=slider_change,    )    col = ft.Column(        wrap=True,        spacing=10,        run_spacing=10,        controls=items(10),        height=HEIGHT,    )    page.add(        ft.Column(            [                ft.Text(                    "Change the column height to see how child items wrap onto multiple columns:"                ),                width_slider,            ]        ),        ft.Container(content=col, bgcolor=ft.Colors.AMBER_100),    )ft.app(main)
```

### Column vertical alignments[​](#column-vertical-alignments "Direct link to Column vertical alignments")

![](https://flet.dev/docs/controls/column/img/docs/controls/column/column-alignment.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER_500,                )            )        return items    def column_with_alignment(align: ft.MainAxisAlignment):        return ft.Column(            [                ft.Text(str(align), size=10),                ft.Container(                    content=ft.Column(items(3), alignment=align),                    bgcolor=ft.Colors.AMBER_100,                    height=400,                ),            ]        )    page.add(        ft.Row(            [                column_with_alignment(ft.MainAxisAlignment.START),                column_with_alignment(ft.MainAxisAlignment.CENTER),                column_with_alignment(ft.MainAxisAlignment.END),                column_with_alignment(ft.MainAxisAlignment.SPACE_BETWEEN),                column_with_alignment(ft.MainAxisAlignment.SPACE_AROUND),                column_with_alignment(ft.MainAxisAlignment.SPACE_EVENLY),            ],            spacing=30,            alignment=ft.MainAxisAlignment.START,        )    )ft.app(main)
```

### Column horizontal alignments[​](#column-horizontal-alignments "Direct link to Column horizontal alignments")

![](https://flet.dev/docs/controls/column/img/docs/controls/column/column-horiz-alignment.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    def items(count):        items = []        for i in range(1, count + 1):            items.append(                ft.Container(                    content=ft.Text(value=str(i)),                    alignment=ft.alignment.center,                    width=50,                    height=50,                    bgcolor=ft.Colors.AMBER_500,                )            )        return items    def column_with_horiz_alignment(align: ft.CrossAxisAlignment):        return ft.Column(            [                ft.Text(str(align), size=16),                ft.Container(                    content=ft.Column(                        items(3),                        alignment=ft.MainAxisAlignment.START,                        horizontal_alignment=align,                    ),                    bgcolor=ft.Colors.AMBER_100,                    width=100,                ),            ]        )    page.add(        ft.Row(            [                column_with_horiz_alignment(ft.CrossAxisAlignment.START),                column_with_horiz_alignment(ft.CrossAxisAlignment.CENTER),                column_with_horiz_alignment(ft.CrossAxisAlignment.END),            ],            spacing=30,            alignment=ft.MainAxisAlignment.START,        )    )ft.app(main)
```

### Infinite scroll list[​](#infinite-scroll-list "Direct link to Infinite scroll list")

The following example demonstrates adding of list items on-the-fly, as user scroll to the bottom, creating the illusion of infinite list:

```
import threadingimport flet as ftclass State:    i = 0s = State()sem = threading.Semaphore()def main(page: ft.Page):    def on_scroll(e: ft.OnScrollEvent):        if e.pixels >= e.max_scroll_extent - 100:            if sem.acquire(blocking=False):                try:                    for i in range(0, 10):                        cl.controls.append(ft.Text(f"Text line {s.i}", key=str(s.i)))                        s.i += 1                    cl.update()                finally:                    sem.release()    cl = ft.Column(        spacing=10,        height=200,        width=200,        scroll=ft.ScrollMode.ALWAYS,        on_scroll_interval=0,        on_scroll=on_scroll,    )    for i in range(0, 50):        cl.controls.append(ft.Text(f"Text line {s.i}", key=str(s.i)))        s.i += 1    page.add(ft.Container(cl, border=ft.border.all(1)))ft.app(main)
```

### Scrolling column programmatically[​](#scrolling-column-programmatically "Direct link to Scrolling column programmatically")

![](https://flet.dev/docs/controls/column/img/docs/controls/column/column-scroll-to.png)

The following example demonstrates various `scroll_to()` options as well as defines a custom scrollbar theme:

```
import flet as ftdef main(page: ft.Page):    page.theme = ft.Theme(        scrollbar_theme=ft.ScrollbarTheme(            track_color={                ft.ControlState.HOVERED: ft.Colors.AMBER,                ft.ControlState.DEFAULT: ft.Colors.TRANSPARENT,            },            track_visibility=True,            track_border_color=ft.Colors.BLUE,            thumb_visibility=True,            thumb_color={                ft.ControlState.HOVERED: ft.Colors.RED,                ft.ControlState.DEFAULT: ft.Colors.GREY_300,            },            thickness=30,            radius=15,            main_axis_margin=5,            cross_axis_margin=10,            # interactive=False,        )    )    cl = ft.Column(        spacing=10,        height=200,        width=float("inf"),        scroll=ft.ScrollMode.ALWAYS,    )    for i in range(0, 100):        cl.controls.append(ft.Text(f"Text line {i}", key=str(i)))    def scroll_to_offset(e):        cl.scroll_to(offset=100, duration=1000)    def scroll_to_start(e):        cl.scroll_to(offset=0, duration=1000)    def scroll_to_end(e):        cl.scroll_to(offset=-1, duration=2000, curve=ft.AnimationCurve.EASE_IN_OUT)    def scroll_to_key(e):        cl.scroll_to(key="20", duration=1000)    def scroll_to_delta(e):        cl.scroll_to(delta=40, duration=200)    def scroll_to_minus_delta(e):        cl.scroll_to(delta=-40, duration=200)    page.add(        ft.Container(cl, border=ft.border.all(1)),        ft.ElevatedButton("Scroll to offset 100", on_click=scroll_to_offset),        ft.Row(            [                ft.ElevatedButton("Scroll to start", on_click=scroll_to_start),                ft.ElevatedButton("Scroll to end", on_click=scroll_to_end),            ]        ),        ft.ElevatedButton("Scroll to key '20'", on_click=scroll_to_key),        ft.Row(            [                ft.ElevatedButton("Scroll -40", on_click=scroll_to_minus_delta),                ft.ElevatedButton("Scroll +40", on_click=scroll_to_delta),            ]        ),    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `alignment`[​](#alignment "Direct link to alignment")

How the child Controls should be placed vertically.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment).

### `auto_scroll`[​](#auto_scroll "Direct link to auto_scroll")

`True` if scrollbar should automatically move its position to the end when children updated. Must be `False` for `scroll_to()` method to work.

### `controls`[​](#controls "Direct link to controls")

A list of Controls to display inside the Column.

### `horizontal_alignment`[​](#horizontal_alignment "Direct link to horizontal_alignment")

How the child Controls should be placed horizontally.

Value is of type [`CrossAxisAlignment`](/docs/reference/types/crossaxisalignment) and defaults to `CrossAxisAlignment.START`.

### `on_scroll_interval`[​](#on_scroll_interval "Direct link to on_scroll_interval")

Throttling in milliseconds for `on_scroll` event.

Defaults to `10`.

### `rtl`[​](#rtl "Direct link to rtl")

`True` to set text direction to right-to-left.

Defaults to `False`.

### `run_alignment`[​](#run_alignment "Direct link to run_alignment")

How the runs should be placed in the cross-axis when `wrap=True`.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment) and defaults to `MainAxisAlignment.START`.

### `run_spacing`[​](#run_spacing "Direct link to run_spacing")

Spacing between runs when `wrap=True`. Default value is 10.

### `scroll`[​](#scroll "Direct link to scroll")

Enables a vertical scrolling for the Column to prevent its content overflow.

Value is of type [`ScrollMode`](/docs/reference/types/scrollmode) and defaults to `ScrollMode.None`.

### `spacing`[​](#spacing "Direct link to spacing")

Spacing between the `controls`. It is applied only when `alignment` is set to `MainAxisAlignment.START`, `MainAxisAlignment.END` or `MainAxisAlignment.CENTER`.

Default value is `10` virtual pixels.

### `tight`[​](#tight "Direct link to tight")

Specifies how much space should be occupied vertically.

Defaults to `False` - allocate all space to children.

### `wrap`[​](#wrap "Direct link to wrap")

When set to `True` the Column will put child controls into additional columns (runs) if they don't fit a single column.

## Methods[​](#methods "Direct link to Methods")

### `scroll_to(offset, delta, key, duration, curve)`[​](#scroll_tooffset-delta-key-duration-curve "Direct link to scroll_tooffset-delta-key-duration-curve")

Moves scroll position to either absolute `offset`, relative `delta` or jump to the control with specified `key`.

`offset` is an absolute value between minimum and maximum extents of a scrollable control, for example:

```
products.scroll_to(offset=100, duration=1000)
```

`offset` could be a negative to scroll from the end of a scrollable. For example, to scroll to the very end:

```
products.scroll_to(offset=-1, duration=1000)
```

`delta` allows moving scroll relatively to the current position. Use positive `delta` to scroll forward and negative `delta` to scroll backward. For example, to move scroll on 50 pixels forward:

```
products.scroll_to(delta=50)
```

`key` allows moving scroll position to a control with specified `key`. Most of Flet controls have `key` property which is translated to Flutter as "global key". `key` must be unique for the entire page/view. For example:

```
import flet as ftdef main(page: ft.Page):    cl = ft.Column(        spacing=10,        height=200,        width=200,        scroll=ft.ScrollMode.ALWAYS,    )    for i in range(0, 50):        cl.controls.append(ft.Text(f"Text line {i}", key=str(i)))    def scroll_to_key(e):        cl.scroll_to(key="20", duration=1000)    page.add(        ft.Container(cl, border=ft.border.all(1)),        ft.ElevatedButton("Scroll to key '20'", on_click=scroll_to_key),    )ft.app(main)
```

note

`scroll_to()` method won't work with `ListView` and `GridView` controls building their items dynamically.

`duration` is scrolling animation duration in milliseconds. Defaults to `0` - no animation.

`curve` configures animation curve. Property value is [`AnimationCurve`](/docs/reference/types/animationcurve) enum. Defaults to `AnimationCurve.EASE`.

## Events[​](#events "Direct link to Events")

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when scroll position is changed by a user.

Event handler argument is an instance of [`OnScrollEvent`](/docs/reference/types/onscrollevent) class.

## Expanding children[​](#expanding-children "Direct link to Expanding children")

When a child Control is placed into a Column you can "expand" it to fill the available space. Every Control has `expand` property that can have either a boolean value (`True` - expand control to fill all available space) or an integer - an "expand factor" specifying how to divide a free space with other expanded child controls. For example, this code creates a column with a Container taking all available space and a Text control at the bottom serving as a status bar:

```
r = ft.Column([  ft.Container(expand=True, content=ft.Text("Here is search results")),  ft.Text("Records found: 10")])
```

The following example with numeric expand factors creates a Column with 3 containers in it and having heights of `20% (1/5)`, `60% (3/5)` and `20% (1/5)` respectively:

```
r = ft.Column([  ft.Container(expand=1, content=ft.Text("Header")),  ft.Container(expand=3, content=ft.Text("Body")),  ft.Container(expand=1, content=ft.Text("Footer"))])
```

In general, the resulting height of a child in percents is calculated as `expand / sum(all expands) * 100%`.

If you need to give the child Control of the Column the flexibility to expand to fill the available space vertically but not require it to fill the available space, set its `expand_loose` property to `True`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/column.md)

[

Previous

Card

](/docs/controls/card)[

Next

Container

](/docs/controls/container)

-   [Examples](#examples)
    -   [Column spacing](#column-spacing)
    -   [Column wrapping](#column-wrapping)
    -   [Column vertical alignments](#column-vertical-alignments)
    -   [Column horizontal alignments](#column-horizontal-alignments)
    -   [Infinite scroll list](#infinite-scroll-list)
    -   [Scrolling column programmatically](#scrolling-column-programmatically)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`auto_scroll`](#auto_scroll)
    -   [`controls`](#controls)
    -   [`horizontal_alignment`](#horizontal_alignment)
    -   [`on_scroll_interval`](#on_scroll_interval)
    -   [`rtl`](#rtl)
    -   [`run_alignment`](#run_alignment)
    -   [`run_spacing`](#run_spacing)
    -   [`scroll`](#scroll)
    -   [`spacing`](#spacing)
    -   [`tight`](#tight)
    -   [`wrap`](#wrap)
-   [Methods](#methods)
    -   [`scroll_to(offset, delta, key, duration, curve)`](#scroll_tooffset-delta-key-duration-curve)
-   [Events](#events)
    -   [`on_scroll`](#on_scroll)
-   [Expanding children](#expanding-children)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Container | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/container/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/container/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/container/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/container/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Container

On this page

# Container

Container allows to decorate a control with background color and border and position it with padding, margin and alignment.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/container)

### Clickable container[​](#clickable-container "Direct link to Clickable container")

![](https://flet.dev/docs/controls/container/img/docs/controls/container/clickable-container.gif)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "Containers - clickable and not"    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.add(        ft.Row(            [                ft.Container(                    content=ft.Text("Non clickable"),                    margin=10,                    padding=10,                    alignment=ft.alignment.center,                    bgcolor=ft.Colors.AMBER,                    width=150,                    height=150,                    border_radius=10,                ),                ft.Container(                    content=ft.Text("Clickable without Ink"),                    margin=10,                    padding=10,                    alignment=ft.alignment.center,                    bgcolor=ft.Colors.GREEN_200,                    width=150,                    height=150,                    border_radius=10,                    on_click=lambda e: print("Clickable without Ink clicked!"),                ),                ft.Container(                    content=ft.Text("Clickable with Ink"),                    margin=10,                    padding=10,                    alignment=ft.alignment.center,                    bgcolor=ft.Colors.CYAN_200,                    width=150,                    height=150,                    border_radius=10,                    ink=True,                    on_click=lambda e: print("Clickable with Ink clicked!"),                ),                ft.Container(                    content=ft.Text("Clickable transparent with Ink"),                    margin=10,                    padding=10,                    alignment=ft.alignment.center,                    width=150,                    height=150,                    border_radius=10,                    ink=True,                    on_click=lambda e: print("Clickable transparent with Ink clicked!"),                ),            ],            alignment=ft.MainAxisAlignment.CENTER,        ),    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

![](https://flet.dev/docs/controls/container/img/docs/controls/container/container-diagram.png)

### `alignment`[​](#alignment "Direct link to alignment")

Align the child control within the container.

Value is of type [`Alignment`](/docs/reference/types/alignment).

### `animate`[​](#animate "Direct link to animate")

Enables container "implicit" animation that gradually changes its values over a period of time.

Value is of type [`AnimationValue`](/docs/reference/types/animationvalue).

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Defines the background [color](/docs/reference/colors) of the container.

### `blend_mode`[​](#blend_mode "Direct link to blend_mode")

The blend mode applied to the `color` or `gradient` background of the container.

Value is of type [`BlendMode`](/docs/reference/types/blendmode) and defaults to `BlendMode.MODULATE`.

### `blur`[​](#blur "Direct link to blur")

Applies Gaussian blur effect under the container.

The value of this property could be one of the following:

-   **a number** - specifies the same value for horizontal and vertical sigmas, e.g. `10`.
-   **a tuple** - specifies separate values for horizontal and vertical sigmas, e.g. `(10, 1)`.
-   **an instance of [`Blur`](/docs/reference/types/blur)**

For example:

```
ft.Stack(    [        ft.Container(            content=ft.Text("Hello"),            image_src="https://picsum.photos/100/100",            width=100,            height=100,        ),        ft.Container(            width=50,            height=50,            blur=10,            bgcolor="#44CCCC00",        ),        ft.Container(            width=50,            height=50,            left=10,            top=60,            blur=(0, 10),        ),        ft.Container(            top=10,            left=60,            blur=ft.Blur(10, 0, ft.BlurTileMode.MIRROR),            width=50,            height=50,            bgcolor="#44CCCCCC",            border=ft.border.all(2, ft.Colors.BLACK),        ),    ])
```

![](https://flet.dev/docs/controls/container/img/docs/controls/container/blur-container.PNG)

### `border`[​](#border "Direct link to border")

A border to draw above the background color.

Value is of type [`Border`](/docs/reference/types/border).

### `border_radius`[​](#border_radius "Direct link to border_radius")

If specified, the corners of the container are rounded by this radius.

Value is of type [`BorderRadius`](/docs/reference/types/borderradius).

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.ANTI_ALIAS` if `border_radius` is not `None`; otherwise `ClipBehavior.NONE`.

### `color_filter`[​](#color_filter "Direct link to color_filter")

Applies a color filter to the container.

Value is of type [`ColorFilter`](/docs/reference/types/colorfilter).

### `content`[​](#content "Direct link to content")

A child Control contained by the container.

### `dark_theme`[​](#dark_theme "Direct link to dark_theme")

Allows setting a nested `theme` to be used when in dark theme mode for all controls inside the container and down the tree.

Value is of type [`Theme`](/docs/cookbook/theming).

### `foreground_decoration`[​](#foreground_decoration "Direct link to foreground_decoration")

The foreground decoration.

Value is of type [`BoxDecoration`](/docs/reference/types/boxdecoration).

### `gradient`[​](#gradient "Direct link to gradient")

Defines the gradient background of the container.

Value is of type [`Gradient`](/docs/reference/types/gradient).

### `ignore_interactions`[​](#ignore_interactions "Direct link to ignore_interactions")

Whether to ignore all interactions with this container and its descendants.

Defaults to `False`.

### `image`[​](#image "Direct link to image")

An image to paint above the `bgcolor` or `gradient`. If `shape=BoxShape.CIRCLE` then this image is clipped to the circle's boundary; if `border_radius` is not `None`then the image is clipped to the given radii.

Value is of type [`DecorationImage`](/docs/reference/types/decorationimage).

### `ink`[​](#ink "Direct link to ink")

`True` to produce ink ripples effect when user clicks the container.

Defaults to `False`.

### `ink_color`[​](#ink_color "Direct link to ink_color")

The splash [color](/docs/reference/colors) of the ink response.

### `margin`[​](#margin "Direct link to margin")

Empty space to surround the decoration and child control.

Value is of type [`Margin`](/docs/reference/types/margin) class or a number.

### `padding`[​](#padding "Direct link to padding")

Empty space to inscribe inside a container decoration (background, border). The child control is placed inside this padding.

Value is of type [`Padding`](/docs/reference/types/padding) or a number.

### `rtl`[​](#rtl "Direct link to rtl")

`True` to set text direction to right-to-left.

Defaults to `False`.

### `shadow`[​](#shadow "Direct link to shadow")

Shadows cast by the container.

Value is of type [`BoxShadow`](/docs/reference/types/boxshadow) or a `List[BoxShadow]`.

### `shape`[​](#shape "Direct link to shape")

Sets the shape of the container.

Value is of type [`BoxShape`](/docs/reference/types/boxshape) and defaults to `BoxShape.RECTANGLE`.

### `theme_mode`[​](#theme_mode "Direct link to theme_mode")

Setting `theme_mode` "resets" parent theme and creates a new, unique scheme for all controls inside the container. Otherwise the styles defined in container's `theme` property override corresponding styles from the parent, inherited theme.

Value is of type [`ThemeMode`](/docs/reference/types/thememode) and defaults to `ThemeMode.SYSTEM`.

### `theme`[​](#theme "Direct link to theme")

Allows setting a nested `theme` for all controls inside the container and down the tree.

Value is of type [`Theme`](/docs/cookbook/theming).

**Usage example**

```
import flet as ftdef main(page: ft.Page):    # Yellow page theme with SYSTEM (default) mode    page.theme = ft.Theme(        color_scheme_seed=ft.Colors.YELLOW,    )    page.add(        # Page theme        ft.Container(            content=ft.ElevatedButton("Page theme button"),            bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST,            padding=20,            width=300,        ),        # Inherited theme with primary color overridden        ft.Container(            theme=ft.Theme(color_scheme=ft.ColorScheme(primary=ft.Colors.PINK)),            content=ft.ElevatedButton("Inherited theme button"),            bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST,            padding=20,            width=300,        ),                # Unique always DARK theme        ft.Container(            theme=ft.Theme(color_scheme_seed=ft.Colors.INDIGO),            theme_mode=ft.ThemeMode.DARK,            content=ft.ElevatedButton("Unique theme button"),            bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST,            padding=20,            width=300,        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/container/img/blog/theme-scrolling/nested-themes.png)

### `url`[​](#url "Direct link to url")

The URL to open when the container is clicked. If provided, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the container. Will not be fired on long press.

### `on_hover`[​](#on_hover "Direct link to on_hover")

Fires when a mouse pointer enters or exists the container area. `data` property of event object contains `true` (string) when cursor enters and `false` when it exits.

A simple example of a container changing its background color on mouse hover:

```
import flet as ftdef main(page: ft.Page):    def on_hover(e):        e.control.bgcolor = "blue" if e.data == "true" else "red"        e.control.update()    page.add(        ft.Container(width=100, height=100, bgcolor="red", ink=False, on_hover=on_hover)    )ft.app(main)
```

![](https://flet.dev/docs/controls/container/img/docs/controls/container/hover-container.gif)

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the container is long-pressed.

### `on_tap_down`[​](#on_tap_down "Direct link to on_tap_down")

Fires when a user clicks the container with or without a long press.

Event handler argument is of type [`ContainerTapEvent`](/docs/reference/types/containertapevent).

info

If `ink` is `True`, `e` will be plain `ControlEvent` with empty `data` instead of `ContainerTapEvent`.

A simple usage example:

```
import flet as ftdef main(page: ft.Page):    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    def on_long_press(e):        print("on long press")        page.add(ft.Text("on_long_press triggered"))    def on_click(e):        print("on click")        page.add(ft.Text("on_click triggered"))    def on_tap_down(e: ft.ContainerTapEvent):        print("on tap down", e.local_x, e.local_y)        page.add(ft.Text("on_tap_down triggered"))    c = ft.Container(        bgcolor=ft.Colors.RED,        content=ft.Text("Test Long Press"),        height=100,        width=100,        on_click=on_click,        on_long_press=on_long_press,        on_tap_down=on_tap_down,    )        page.add(c)ft.app(main)
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/container.md)

[

Previous

Column

](/docs/controls/column)[

Next

CupertinoListTile

](/docs/controls/cupertinolisttile)

-   [Examples](#examples)
    -   [Clickable container](#clickable-container)
-   [Properties](#properties)
    -   [`alignment`](#alignment)
    -   [`animate`](#animate)
    -   [`bgcolor`](#bgcolor)
    -   [`blend_mode`](#blend_mode)
    -   [`blur`](#blur)
    -   [`border`](#border)
    -   [`border_radius`](#border_radius)
    -   [`clip_behavior`](#clip_behavior)
    -   [`color_filter`](#color_filter)
    -   [`content`](#content)
    -   [`dark_theme`](#dark_theme)
    -   [`foreground_decoration`](#foreground_decoration)
    -   [`gradient`](#gradient)
    -   [`ignore_interactions`](#ignore_interactions)
    -   [`image`](#image)
    -   [`ink`](#ink)
    -   [`ink_color`](#ink_color)
    -   [`margin`](#margin)
    -   [`padding`](#padding)
    -   [`rtl`](#rtl)
    -   [`shadow`](#shadow)
    -   [`shape`](#shape)
    -   [`theme_mode`](#theme_mode)
    -   [`theme`](#theme)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_click`](#on_click)
    -   [`on_hover`](#on_hover)
    -   [`on_long_press`](#on_long_press)
    -   [`on_tap_down`](#on_tap_down)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoListTile | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinolisttile/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinolisttile/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinolisttile/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinolisttile/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   CupertinoListTile

On this page

# CupertinoListTile

An iOS-style list tile. The CupertinoListTile is a Cupertino equivalent of Material [ListTile](/docs/controls/listtile).

It comes in two forms, an old-fashioned edge-to-edge variant known from iOS Settings app and in a new, "Inset Grouped" form, known from either iOS Notes or Reminders app. The first form is created if `notched` property is `False` (default value) and the second form is created is [`notched`](/docs/controls/cupertinolisttile#notched) is `True`.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/cupertinolisttile)

-   Python

```
import flet as ftdef main(page: ft.Page):    def tile_clicked(e):        print("Tile clicked")    page.add(        ft.CupertinoListTile(            additional_info=ft.Text("Wed Jan 24"),            bgcolor_activated=ft.Colors.AMBER_ACCENT,            leading=ft.Icon(name=ft.cupertino_icons.GAME_CONTROLLER),            title=ft.Text("CupertinoListTile not notched"),            subtitle=ft.Text("Subtitle"),            trailing=ft.Icon(name=ft.cupertino_icons.ALARM),            on_click=tile_clicked,        ),        ft.CupertinoListTile(            notched=True,            additional_info=ft.Text("Thu Jan 25"),            leading=ft.Icon(name=ft.cupertino_icons.GAME_CONTROLLER),            title=ft.Text("CupertinoListTile notched"),            subtitle=ft.Text("Subtitle"),            trailing=ft.Icon(name=ft.cupertino_icons.ALARM),            on_click=tile_clicked,        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinolisttile/img/docs/controls/cupertinolisttile/cupertinolisttile-example.png)

## Properties[​](#properties "Direct link to Properties")

### `additional_info`[​](#additional_info "Direct link to additional_info")

A `Control` to display on the right of the list tile, before `trailing`. Similar to `subtitle`, an `additional_info` is used to display additional information. Usually a [`Text`](/docs/controls/text) control.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The list tile's background [color](/docs/reference/colors).

### `bgcolor_activated`[​](#bgcolor_activated "Direct link to bgcolor_activated")

The list tile's background [color](/docs/reference/colors) after the tile was tapped.

### `leading`[​](#leading "Direct link to leading")

A `Control` to display before the `title`.

### `leading_size`[​](#leading_size "Direct link to leading_size")

Used to constrain the width and height of `leading` control.

Defaults to `30.0`, if `notched=True`, else `28.0`.

### `leading_to_title`[​](#leading_to_title "Direct link to leading_to_title")

The horizontal space between `leading` and `title`.

Defaults to `12.0`, if `notched=True`, else `16.0`.

### `notched`[​](#notched "Direct link to notched")

If `True`, list tile will be created in an "Inset Grouped" form, known from either iOS Notes or Reminders app.

Defaults to `False`.

### `padding`[​](#padding "Direct link to padding")

The tile's internal padding. Insets a CupertinoListTile's contents: its `leading`, `title`, `subtitle`, `additional_info` and `trailing` controls.

Padding is an instance of [`Padding`](/docs/reference/types/padding) class.

### `subtitle`[​](#subtitle "Direct link to subtitle")

Additional content displayed below the title.

Typically a [`Text`](/docs/controls/text) control.

### `title`[​](#title "Direct link to title")

A `Control` to display as primary content of the list tile.

Typically a [`Text`](/docs/controls/text) control.

### `toggle_inputs`[​](#toggle_inputs "Direct link to toggle_inputs")

Whether clicking on a list tile should toggle the state of `Radio`, `Checkbox` or `Switch` inside the tile. Default is `False`.

### `trailing`[​](#trailing "Direct link to trailing")

A `Control` to display after the title.

Typically an [`Icon`](/docs/controls/icon) control.

### `url`[​](#url "Direct link to url")

The URL to open when the list tile is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks or taps the list tile.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinolisttile.md)

[

Previous

Container

](/docs/controls/container)[

Next

DataTable

](/docs/controls/datatable)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`additional_info`](#additional_info)
    -   [`bgcolor`](#bgcolor)
    -   [`bgcolor_activated`](#bgcolor_activated)
    -   [`leading`](#leading)
    -   [`leading_size`](#leading_size)
    -   [`leading_to_title`](#leading_to_title)
    -   [`notched`](#notched)
    -   [`padding`](#padding)
    -   [`subtitle`](#subtitle)
    -   [`title`](#title)
    -   [`toggle_inputs`](#toggle_inputs)
    -   [`trailing`](#trailing)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  DataTable | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/datatable/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/datatable/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/datatable/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/datatable/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   DataTable

On this page

# DataTable

A Material Design data table.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/datatable)

### A simple DataTable[​](#a-simple-datatable "Direct link to A simple DataTable")

![](https://flet.dev/docs/controls/datatable/img/docs/controls/datatable/datatable-minimal.png)

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.DataTable(            columns=[                ft.DataColumn(ft.Text("First name")),                ft.DataColumn(ft.Text("Last name")),                ft.DataColumn(ft.Text("Age"), numeric=True),            ],            rows=[                ft.DataRow(                    cells=[                        ft.DataCell(ft.Text("John")),                        ft.DataCell(ft.Text("Smith")),                        ft.DataCell(ft.Text("43")),                    ],                ),                ft.DataRow(                    cells=[                        ft.DataCell(ft.Text("Jack")),                        ft.DataCell(ft.Text("Brown")),                        ft.DataCell(ft.Text("19")),                    ],                ),                ft.DataRow(                    cells=[                        ft.DataCell(ft.Text("Alice")),                        ft.DataCell(ft.Text("Wong")),                        ft.DataCell(ft.Text("25")),                    ],                ),            ],        ),    )ft.app(main)
```

### A styled DataTable[​](#a-styled-datatable "Direct link to A styled DataTable")

![](https://flet.dev/docs/controls/datatable/img/docs/controls/datatable/datatable-styled.png)

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.DataTable(            width=700,            bgcolor="yellow",            border=ft.border.all(2, "red"),            border_radius=10,            vertical_lines=ft.BorderSide(3, "blue"),            horizontal_lines=ft.BorderSide(1, "green"),            sort_column_index=0,            sort_ascending=True,            heading_row_color=ft.Colors.BLACK12,            heading_row_height=100,            data_row_color={ft.ControlState.HOVERED: "0x30FF0000"},            show_checkbox_column=True,            divider_thickness=0,            column_spacing=200,            columns=[                ft.DataColumn(                    ft.Text("Column 1"),                    on_sort=lambda e: print(f"{e.column_index}, {e.ascending}"),                ),                ft.DataColumn(                    ft.Text("Column 2"),                    tooltip="This is a second column",                    numeric=True,                    on_sort=lambda e: print(f"{e.column_index}, {e.ascending}"),                ),            ],            rows=[                ft.DataRow(                    [ft.DataCell(ft.Text("A")), ft.DataCell(ft.Text("1"))],                    selected=True,                    on_select_changed=lambda e: print(f"row select changed: {e.data}"),                ),                ft.DataRow([ft.DataCell(ft.Text("B")), ft.DataCell(ft.Text("2"))]),            ],        ),    )ft.app(main)
```

## `DataTable` properties[​](#datatable-properties "Direct link to datatable-properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The background [color](/docs/reference/colors) for the table.

### `border`[​](#border "Direct link to border")

The border around the table.

The value is an instance of [`Border`](/docs/reference/types/border) class.

### `border_radius`[​](#border_radius "Direct link to border_radius")

Border corners.

Border radius is an instance of [`BorderRadius`](/docs/reference/types/borderradius) class.

### `checkbox_horizontal_margin`[​](#checkbox_horizontal_margin "Direct link to checkbox_horizontal_margin")

Horizontal margin around the checkbox, if it is displayed.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.ANTI_ALIAS` if `border_radius!=None`; otherwise `ClipBehavior.HARD_EDGE`.

### `column_spacing`[​](#column_spacing "Direct link to column_spacing")

The horizontal margin between the contents of each data column.

### `columns`[​](#columns "Direct link to columns")

A list of [`DataColumn`](#datacolumn) controls describing table columns.

### `data_row_color`[​](#data_row_color "Direct link to data_row_color")

The background [color](/docs/reference/colors) for the data rows.

The effective background color can be made to depend on the [`ControlState`](/docs/reference/types/controlstate) state, i.e. if the row is selected, pressed, hovered, focused, disabled or enabled. The color is painted as an overlay to the row. To make sure that the row's InkWell is visible (when pressed, hovered and focused), it is recommended to use a translucent background color.

### `data_row_min_height`[​](#data_row_min_height "Direct link to data_row_min_height")

The minimum height of each row (excluding the row that contains column headings).

Defaults to `48.0` and must be less than or equal to `data_row_max_height`.

### `data_row_max_height`[​](#data_row_max_height "Direct link to data_row_max_height")

The maximum height of each row (excluding the row that contains column headings). Set to `float("inf")` for the height of each row to adjust automatically with its content.

Defaults to `48.0` and must be greater than or equal to `data_row_min_height`.

### `data_text_style`[​](#data_text_style "Direct link to data_text_style")

The text style for data rows. An instance of [`TextStyle`](/docs/reference/types/textstyle) class.

### `divider_thickness`[​](#divider_thickness "Direct link to divider_thickness")

The width of the divider that appears between `TableRow`s. Must be greater than or equal to zero.

Defaults to 1.0.

### `gradient`[​](#gradient "Direct link to gradient")

The background gradient for the table.

Value is of type [`Gradient`](/docs/reference/types/gradient).

### `heading_row_alignment`[​](#heading_row_alignment "Direct link to heading_row_alignment")

The alignment of the heading row.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment).

### `heading_row_color`[​](#heading_row_color "Direct link to heading_row_color")

The background [color](/docs/reference/colors) for the heading row.

The effective background color can be made to depend on the [`ControlState`](/docs/reference/types/controlstate) state, i.e. if the row is pressed, hovered, focused when sorted. The color is painted as an overlay to the row. To make sure that the row's InkWell is visible (when pressed, hovered and focused), it is recommended to use a translucent color.

### `heading_row_height`[​](#heading_row_height "Direct link to heading_row_height")

The height of the heading row.

### `heading_text_style`[​](#heading_text_style "Direct link to heading_text_style")

The text style for the heading row. An instance of [`TextStyle`](/docs/reference/types/textstyle) class.

### `horizontal_lines`[​](#horizontal_lines "Direct link to horizontal_lines")

Set the [color](/docs/reference/colors) and width of horizontal lines between rows. An instance of [`BorderSide`](/docs/reference/types/borderside) class.

### `horizontal_margin`[​](#horizontal_margin "Direct link to horizontal_margin")

The horizontal margin between the edges of the table and the content in the first and last cells of each row.

When a checkbox is displayed, it is also the margin between the checkbox the content in the first data column.

### `rows`[​](#rows "Direct link to rows")

A list of [`DataRow`](#datarow) controls defining table rows.

### `show_bottom_border`[​](#show_bottom_border "Direct link to show_bottom_border")

Whether a border at the bottom of the table is displayed.

By default, a border is not shown at the bottom to allow for a border around the table defined by decoration.

### `show_checkbox_column`[​](#show_checkbox_column "Direct link to show_checkbox_column")

Whether the control should display checkboxes for selectable rows.

If `True`, a `Checkbox` will be placed at the beginning of each row that is selectable. However, if `DataRow.on_select_changed` is not set for any row, checkboxes will not be placed, even if this value is `True`.

If `False`, all rows will not display a `Checkbox`.

### `sort_ascending`[​](#sort_ascending "Direct link to sort_ascending")

Whether the column mentioned in `sort_column_index`, if any, is sorted in ascending order.

If `True`, the order is ascending (meaning the rows with the smallest values for the current sort column are first in the table).

If `False`, the order is descending (meaning the rows with the smallest values for the current sort column are last in the table).

### `sort_column_index`[​](#sort_column_index "Direct link to sort_column_index")

The current primary sort key's column.

If specified, indicates that the indicated column is the column by which the data is sorted. The number must correspond to the index of the relevant column in `columns`.

Setting this will cause the relevant column to have a sort indicator displayed.

When this is `None`, it implies that the table's sort order does not correspond to any of the columns.

### `vertical_lines`[​](#vertical_lines "Direct link to vertical_lines")

Set the [color](/docs/reference/colors) and width of vertical lines between columns.

Value is of type [`BorderSide`](/docs/reference/types/borderside).

## `DataTable` events[​](#datatable-events "Direct link to datatable-events")

### `on_select_all`[​](#on_select_all "Direct link to on_select_all")

Invoked when the user selects or unselects every row, using the checkbox in the heading row.

If this is `None`, then the `DataRow.on_select_changed` callback of every row in the table is invoked appropriately instead.

To control whether a particular row is selectable or not, see `DataRow.on_select_changed`. This callback is only relevant if any row is selectable.

## `DataColumn`[​](#datacolumn "Direct link to datacolumn")

Column configuration for a `DataTable`.

One column configuration must be provided for each column to display in the table.

### `label`[​](#label "Direct link to label")

The column heading.

Typically, this will be a `Text` control. It could also be an `Icon` (typically using size 18), or a `Row` with an icon and some text.

### `numeric`[​](#numeric "Direct link to numeric")

Whether this column represents numeric data or not.

The contents of cells of columns containing numeric data are right-aligned.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The column heading's tooltip.

This is a longer description of the column heading, for cases where the heading might have been abbreviated to keep the column width to a reasonable size.

## `DataColumn` events[​](#datacolumn-events "Direct link to datacolumn-events")

### `on_sort`[​](#on_sort "Direct link to on_sort")

Called when the user asks to sort the table using this column.

If not set, the column will not be considered sortable.

## `DataRow`[​](#datarow "Direct link to datarow")

Row configuration and cell data for a DataTable.

One row configuration must be provided for each row to display in the table.

The data for this row of the table is provided in the `cells` property of the `DataRow` object.

### `cells`[​](#cells "Direct link to cells")

The data for this row - a list of [`DataCell`](#datacell) controls.

There must be exactly as many cells as there are columns in the table.

### `color`[​](#color "Direct link to color")

The [color](/docs/reference/colors) for the row.

By default, the color is transparent unless selected. Selected rows has a grey translucent color.

The effective color can depend on the [`ControlState`](/docs/reference/types/controlstate) state, if the row is selected, pressed, hovered, focused, disabled or enabled. The color is painted as an overlay to the row. To make sure that the row's InkWell is visible (when pressed, hovered and focused), it is recommended to use a translucent color.

### `selected`[​](#selected "Direct link to selected")

Whether the row is selected.

If `on_select_changed` is non-null for any row in the table, then a checkbox is shown at the start of each row. If the row is selected (`True`), the checkbox will be checked and the row will be highlighted.

Otherwise, the checkbox, if present, will not be checked.

## `DataRow` events[​](#datarow-events "Direct link to datarow-events")

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Called if the row is long-pressed.

If a `DataCell` in the row has its `DataCell.on_tap`, `DataCell.on_double_tap`, `DataCell.on_long_press`, `DataCell.on_tap_cancel` or `DataCell.on_tap_down` callback defined, that callback behavior overrides the gesture behavior of the row for that particular cell.

### `on_select_changed`[​](#on_select_changed "Direct link to on_select_changed")

Called when the user selects or unselects a selectable row.

If this is not null, then the row is selectable. The current selection state of the row is given by selected.

If any row is selectable, then the table's heading row will have a checkbox that can be checked to select all selectable rows (and which is checked if all the rows are selected), and each subsequent row will have a checkbox to toggle just that row.

A row whose `on_select_changed` callback is null is ignored for the purposes of determining the state of the "all" checkbox, and its checkbox is disabled.

If a `DataCell` in the row has its `DataCell.on_tap` callback defined, that callback behavior overrides the gesture behavior of the row for that particular cell.

## `DataCell`[​](#datacell "Direct link to datacell")

The data for a cell of a `DataTable`.

One list of DataCell objects must be provided for each `DataRow` in the `DataTable`.

### `content`[​](#content "Direct link to content")

The data for the row.

Typically a `Text` control or a `Dropdown` control.

If the cell has no data, then a `Text` widget with placeholder text should be provided instead, and `placeholder` should be set to `True`.

This control can only have one child. To lay out multiple children, let this control's child be a widget such as `Row`, `Column`, or `Stack`, which have `controls` property, and then provide the children to that widget.

### `placeholder`[​](#placeholder "Direct link to placeholder")

Whether the child is actually a placeholder.

If this is `True`, the default text style for the cell is changed to be appropriate for placeholder text.

### `show_edit_icon`[​](#show_edit_icon "Direct link to show_edit_icon")

Whether to show an edit icon at the end of the cell.

This does not make the cell actually editable; the caller must implement editing behavior if desired (initiated from the `on_tap` callback).

If this is set, `on_tap` should also be set, otherwise tapping the icon will have no effect.

## `DataCell` events[​](#datacell-events "Direct link to datacell-events")

### `on_double_tap`[​](#on_double_tap "Direct link to on_double_tap")

Called when the cell is double tapped.

If specified, tapping the cell will call this callback, else (tapping the cell will attempt to select the row ( if `DataRow.on_select_changed` is provided).

### `on_long_press`[​](#on_long_press-1 "Direct link to on_long_press-1")

Called if the cell is long-pressed.

If specified, tapping the cell will invoke this callback, else tapping the cell will attempt to select the row ( if `DataRow.on_select_changed` is provided).

### `on_tap`[​](#on_tap "Direct link to on_tap")

Called if the cell is tapped.

If specified, tapping the cell will call this callback, else tapping the cell will attempt to select the row ( if `DataRow.on_select_changed` is provided).

### `on_tap_cancel`[​](#on_tap_cancel "Direct link to on_tap_cancel")

Called if the user cancels a tap was started on cell.

If specified, cancelling the tap gesture will invoke this callback, else tapping the cell will attempt to select the row (if `DataRow.on_select_changed` is provided).

### `on_tap_down`[​](#on_tap_down "Direct link to on_tap_down")

Called if the cell is tapped down.

If specified, tapping the cell will call this callback, else tapping the cell will attempt to select the row ( if `DataRow.on_select_changed` is provided).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/datatable.md)

[

Previous

CupertinoListTile

](/docs/controls/cupertinolisttile)[

Next

Dismissible

](/docs/controls/dismissible)

-   [Examples](#examples)
    -   [A simple DataTable](#a-simple-datatable)
    -   [A styled DataTable](#a-styled-datatable)
-   [`DataTable` properties](#datatable-properties)
    -   [`bgcolor`](#bgcolor)
    -   [`border`](#border)
    -   [`border_radius`](#border_radius)
    -   [`checkbox_horizontal_margin`](#checkbox_horizontal_margin)
    -   [`clip_behavior`](#clip_behavior)
    -   [`column_spacing`](#column_spacing)
    -   [`columns`](#columns)
    -   [`data_row_color`](#data_row_color)
    -   [`data_row_min_height`](#data_row_min_height)
    -   [`data_row_max_height`](#data_row_max_height)
    -   [`data_text_style`](#data_text_style)
    -   [`divider_thickness`](#divider_thickness)
    -   [`gradient`](#gradient)
    -   [`heading_row_alignment`](#heading_row_alignment)
    -   [`heading_row_color`](#heading_row_color)
    -   [`heading_row_height`](#heading_row_height)
    -   [`heading_text_style`](#heading_text_style)
    -   [`horizontal_lines`](#horizontal_lines)
    -   [`horizontal_margin`](#horizontal_margin)
    -   [`rows`](#rows)
    -   [`show_bottom_border`](#show_bottom_border)
    -   [`show_checkbox_column`](#show_checkbox_column)
    -   [`sort_ascending`](#sort_ascending)
    -   [`sort_column_index`](#sort_column_index)
    -   [`vertical_lines`](#vertical_lines)
-   [`DataTable` events](#datatable-events)
    -   [`on_select_all`](#on_select_all)
-   [`DataColumn`](#datacolumn)
    -   [`label`](#label)
    -   [`numeric`](#numeric)
    -   [`tooltip`](#tooltip)
-   [`DataColumn` events](#datacolumn-events)
    -   [`on_sort`](#on_sort)
-   [`DataRow`](#datarow)
    -   [`cells`](#cells)
    -   [`color`](#color)
    -   [`selected`](#selected)
-   [`DataRow` events](#datarow-events)
    -   [`on_long_press`](#on_long_press)
    -   [`on_select_changed`](#on_select_changed)
-   [`DataCell`](#datacell)
    -   [`content`](#content)
    -   [`placeholder`](#placeholder)
    -   [`show_edit_icon`](#show_edit_icon)
-   [`DataCell` events](#datacell-events)
    -   [`on_double_tap`](#on_double_tap)
    -   [`on_long_press`](#on_long_press-1)
    -   [`on_tap`](#on_tap)
    -   [`on_tap_cancel`](#on_tap_cancel)
    -   [`on_tap_down`](#on_tap_down)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Dismissible | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/dismissible/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/dismissible/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/dismissible/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/dismissible/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Dismissible

On this page

# Dismissible

A control that can be dismissed by dragging in the indicated `dismiss_direction`. When dragged or flung in the specified `dismiss_direction`, it's content smoothly slides out of view.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/dismissible)

### Dismissible ListView Tiles[​](#dismissible-listview-tiles "Direct link to Dismissible ListView Tiles")

-   Python

```
import flet as ftdef main(page):    def handle_dlg_action_clicked(e):        page.close(dlg)        dlg.data.confirm_dismiss(e.control.data)    dlg = ft.AlertDialog(        modal=True,        title=ft.Text("Please confirm"),        content=ft.Text("Do you really want to delete this item?"),        actions=[            ft.TextButton("Yes", data=True, on_click=handle_dlg_action_clicked),            ft.TextButton("No", data=False, on_click=handle_dlg_action_clicked),        ],        actions_alignment=ft.MainAxisAlignment.CENTER,    )    def handle_confirm_dismiss(e: ft.DismissibleDismissEvent):        if e.direction == ft.DismissDirection.END_TO_START:  # right-to-left slide            # save current dismissible to dialog's data, for confirmation in handle_dlg_action_clicked            dlg.data = e.control            page.open(dlg)        else:  # left-to-right slide            e.control.confirm_dismiss(True)    def handle_dismiss(e):        e.control.parent.controls.remove(e.control)        page.update()    def handle_update(e: ft.DismissibleUpdateEvent):        print(            f"Update - direction: {e.direction}, progress: {e.progress}, reached: {e.reached}, previous_reached: {e.previous_reached}"        )    page.add(        ft.ListView(            expand=True,            controls=[                ft.Dismissible(                    content=ft.ListTile(title=ft.Text(f"Item {i}")),                    dismiss_direction=ft.DismissDirection.HORIZONTAL,                    background=ft.Container(bgcolor=ft.Colors.GREEN),                    secondary_background=ft.Container(bgcolor=ft.Colors.RED),                    on_dismiss=handle_dismiss,                    on_update=handle_update,                    on_confirm_dismiss=handle_confirm_dismiss,                    dismiss_thresholds={                        ft.DismissDirection.END_TO_START: 0.2,                        ft.DismissDirection.START_TO_END: 0.2,                    },                )                for i in range(10)            ],        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/dismissible/img/docs/controls/dismissible/dismissible-listview.gif)

## Properties[​](#properties "Direct link to Properties")

### `background`[​](#background "Direct link to background")

A Control that is stacked behind the `content`.

If `secondary_background` is also specified, then this control only appears when the content has been dragged down or to the right.

### `content`[​](#content "Direct link to content")

A child Control contained by the Dismissible.

### `cross_axis_end_offset`[​](#cross_axis_end_offset "Direct link to cross_axis_end_offset")

Specifies the end offset along the main axis once the card has been dismissed.

If non-zero value is given then widget moves in cross direction depending on whether it is positive or negative.

### `dismiss_direction`[​](#dismiss_direction "Direct link to dismiss_direction")

The direction in which the control can be dismissed.

Value is of type [`DismissDirection`](/docs/reference/types/dismissdirection).

### `dismiss_thresholds`[​](#dismiss_thresholds "Direct link to dismiss_thresholds")

The offset threshold the item has to be dragged in order to be considered dismissed.

Ex: a threshold of `0.4` (the default) means that the item has to be dragged *at least* 40% in order for it to be dismissed.

It is specified as a dictionary where the key is of type [`DismissDirection`](/docs/reference/types/dismissdirection) and the value is the threshold(fractional/decimal value between `0.0` and `1.0`):

```
ft.Dismissible(    # ...    dismiss_thresholds={        ft.DismissDirection.VERTICAL: 0.1,        ft.DismissDirection.START_TO_END: 0.7    })
```

### `movement_duration`[​](#movement_duration "Direct link to movement_duration")

The duration for card to dismiss or to come back to original position if not dismissed.

### `resize_duration`[​](#resize_duration "Direct link to resize_duration")

The amount of time the control will spend contracting before `on_dismiss` is called.

### `secondary_background`[​](#secondary_background "Direct link to secondary_background")

A control that is stacked behind the `content` and is exposed when the `content` has been dragged up or to the left.

Has no effect if `background` is not specified.

## Events[​](#events "Direct link to Events")

### `on_confirm_dismiss`[​](#on_confirm_dismiss "Direct link to on_confirm_dismiss")

Gives the app an opportunity to confirm or veto a pending dismissal. The widget cannot be dragged again until the returned this pending dismissal is resolved.

To resolve the pending dismissal, call the `confirm_dismiss(dismiss)` method passing it a boolean representing the decision. If `True`, then the control will be dismissed, otherwise it will be moved back to its original location.

See the example at the top of this page for a possible implementation.

### `on_dismiss`[​](#on_dismiss "Direct link to on_dismiss")

Fires when this control has been dismissed, after finishing resizing.

### `on_resize`[​](#on_resize "Direct link to on_resize")

Fires when this control changes size, for example, when contracting before being dismissed.

### `on_update`[​](#on_update "Direct link to on_update")

Fires when this control has been dragged.

## Methods[​](#methods "Direct link to Methods")

### `confirm_dismiss(dismiss: bool)`[​](#confirm_dismissdismiss-bool "Direct link to confirm_dismissdismiss-bool")

Resolves the pending dismissal. To be called while handling the `on_confirm_dismiss` event.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/dismissible.md)

[

Previous

DataTable

](/docs/controls/datatable)[

Next

Divider

](/docs/controls/divider)

-   [Examples](#examples)
    -   [Dismissible ListView Tiles](#dismissible-listview-tiles)
-   [Properties](#properties)
    -   [`background`](#background)
    -   [`content`](#content)
    -   [`cross_axis_end_offset`](#cross_axis_end_offset)
    -   [`dismiss_direction`](#dismiss_direction)
    -   [`dismiss_thresholds`](#dismiss_thresholds)
    -   [`movement_duration`](#movement_duration)
    -   [`resize_duration`](#resize_duration)
    -   [`secondary_background`](#secondary_background)
-   [Events](#events)
    -   [`on_confirm_dismiss`](#on_confirm_dismiss)
    -   [`on_dismiss`](#on_dismiss)
    -   [`on_resize`](#on_resize)
    -   [`on_update`](#on_update)
-   [Methods](#methods)
    -   [`confirm_dismiss(dismiss: bool)`](#confirm_dismissdismiss-bool)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  View | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/view/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/view/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/view/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/view/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   View

On this page

# View

View is the top most container for all other controls.

A root view is automatically created when a new user session started. From layout perspective the View represents a [`Column`](/docs/controls/column) control, so it has a similar behavior and shares same properties.

## Properties[​](#properties "Direct link to Properties")

### `appbar`[​](#appbar "Direct link to appbar")

A [`AppBar`](/docs/controls/appbar) control to display at the top of the Page.

### `auto_scroll`[​](#auto_scroll "Direct link to auto_scroll")

`True` if scrollbar should automatically move its position to the end when children updated. Must be `False` for `scroll_to()` to work.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Background [color](/docs/reference/colors) of the view.

### `controls`[​](#controls "Direct link to controls")

A list of `Control`s to display on the Page.

For example, to add a new control to a page:

-   Python

```
page.controls.append(ft.Text("Hello!"))page.update()
```

or to get the same result as above using `page.add()` shortcut method:

-   Python

```
page.add(ft.Text("Hello!"))
```

To remove the top most control on the page:

-   Python

```
page.controls.pop()page.update()
```

Value is of a list of `Control`s.

### `decoration`[​](#decoration "Direct link to decoration")

The background decoration.

Value is of type [`BoxDecoration`](/docs/reference/types/boxdecoration).

### `drawer`[​](#drawer "Direct link to drawer")

A [`NavigationDrawer`](/docs/controls/navigationdrawer) control to display as a panel sliding from the start edge of the view.

### `end_drawer`[​](#end_drawer "Direct link to end_drawer")

A [`NavigationDrawer`](/docs/controls/navigationdrawer) control to display as a panel sliding from the end edge of the view.

### `floating_action_button`[​](#floating_action_button "Direct link to floating_action_button")

A [`FloatingActionButton`](/docs/controls/floatingactionbutton) control to display on top of Page content.

### `floating_action_button_location`[​](#floating_action_button_location "Direct link to floating_action_button_location")

Describes position of [`floating_action_button`](#floating_action_button)

Value is of type [`FloatingActionButtonLocation`](/docs/controls/floatingactionbutton)

### `foreground_decoration`[​](#foreground_decoration "Direct link to foreground_decoration")

The foreground decoration.

Value is of type [`BoxDecoration`](/docs/reference/types/boxdecoration).

### `fullscreen_dialog`[​](#fullscreen_dialog "Direct link to fullscreen_dialog")

Whether this view is a full-screen dialog.

In Material and Cupertino, being fullscreen has the effects of making the app bars have a close button instead of a back button. On iOS, dialogs transitions animate differently and are also not closeable with the back swipe gesture.

Value is of type `bool` and defaults to `False`.

### `horizontal_alignment`[​](#horizontal_alignment "Direct link to horizontal_alignment")

How the child Controls should be placed horizontally.

Value is of type [`CrossAxisAlignment`](/docs/reference/types/crossaxisalignment) and defaults to `CrossAxisAlignment.START`.

### `on_scroll_interval`[​](#on_scroll_interval "Direct link to on_scroll_interval")

Throttling in milliseconds for `on_scroll` event.

Value is of type `int` and defaults to `10`.

### `padding`[​](#padding "Direct link to padding")

A space between page contents and its edges.

Value is of type [`PaddingValue`](/docs/reference/types/aliases#paddingvalue) and defaults to `padding.all(10)`.

### `route`[​](#route "Direct link to route")

View's route - not currently used by Flet framework, but can be used in a user program to update [`page.route`](/docs/controls/page#route) when a view popped.

Value is of type `str`

### `scroll`[​](#scroll "Direct link to scroll")

Enables a vertical scrolling for the Page to prevent its content overflow.

Value is of type [`ScrollMode`](/docs/reference/types/scrollmode).

### `spacing`[​](#spacing "Direct link to spacing")

Vertical spacing between controls on the Page. Default value is 10 virtual pixels. Spacing is applied only when `vertical_alignment` is set to `MainAxisAlignment.START`, `MainAxisAlignment.END` or `MainAxisAlignment.CENTER`.

Value is of type \[`OptionalNumber`\] and defaults to `10`

### `vertical_alignment`[​](#vertical_alignment "Direct link to vertical_alignment")

How the child Controls should be placed vertically.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment) and defaults to `MainAxisAlignment.START`.

## Methods[​](#methods "Direct link to Methods")

### `scroll_to(offset, delta, key, duration, curve)`[​](#scroll_tooffset-delta-key-duration-curve "Direct link to scroll_tooffset-delta-key-duration-curve")

Moves scroll position to either absolute `offset`, relative `delta` or jump to the control with specified `key`.

See [`Column.scroll_to()`](/docs/controls/column#scroll_tooffset-delta-key-duration-curve) for method details and examples.

## Events[​](#events "Direct link to Events")

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when scroll position is changed by a user.

Event handler argument is of type [`OnScrollEvent`](/docs/reference/types/onscrollevent).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/view.md)

[

Previous

VerticalDivider

](/docs/controls/verticaldivider)[

Next

Navigation

](/docs/controls/app-structure-navigation)

-   [Properties](#properties)
    -   [`appbar`](#appbar)
    -   [`auto_scroll`](#auto_scroll)
    -   [`bgcolor`](#bgcolor)
    -   [`controls`](#controls)
    -   [`decoration`](#decoration)
    -   [`drawer`](#drawer)
    -   [`end_drawer`](#end_drawer)
    -   [`floating_action_button`](#floating_action_button)
    -   [`floating_action_button_location`](#floating_action_button_location)
    -   [`foreground_decoration`](#foreground_decoration)
    -   [`fullscreen_dialog`](#fullscreen_dialog)
    -   [`horizontal_alignment`](#horizontal_alignment)
    -   [`on_scroll_interval`](#on_scroll_interval)
    -   [`padding`](#padding)
    -   [`route`](#route)
    -   [`scroll`](#scroll)
    -   [`spacing`](#spacing)
    -   [`vertical_alignment`](#vertical_alignment)
-   [Methods](#methods)
    -   [`scroll_to(offset, delta, key, duration, curve)`](#scroll_tooffset-delta-key-duration-curve)
-   [Events](#events)
    -   [`on_scroll`](#on_scroll)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  BannerAd | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/bannerad/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/bannerad/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/bannerad/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/bannerad/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
            -   [BannerAd](/docs/controls/bannerad)
            -   [InterstitialAd](/docs/controls/interstitialad)
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Ads](/docs/controls/ads)
-   BannerAd

On this page

# BannerAd

Rectangular ads that appear at the top or bottom of the device screen. Banner ads stay on screen while users are interacting with the app, and can refresh automatically after a certain period of time.

See [this](/docs/controls/ads) for more information.

note

For enhanced app performance, it is recommended dispose (remove from the controls tree) any `BannerAd` control after it is no longer needed.

On iOS, make sure you place this ad in a control with a fixed width and height, otherwise your ad may not be displayed. See [this](https://developers.google.com/admob/flutter/banner/fixed-size) for more information on standard banner sizes.

## Properties[​](#properties "Direct link to Properties")

### `unit_id`[​](#unit_id "Direct link to unit_id")

The ad unit ID to be used for the ad.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when the ad is clicked.

### `on_close`[​](#on_close "Direct link to on_close")

Fires when the full screen view has been closed.

You can resume anything paused while handling `on_open`.

### `on_error`[​](#on_error "Direct link to on_error")

Fires when an error occurs on the ad.

### `on_impression`[​](#on_impression "Direct link to on_impression")

Fires when an impression occurs on the ad.

### `on_load`[​](#on_load "Direct link to on_load")

Fires when the ad is loaded.

### `on_open`[​](#on_open "Direct link to on_open")

Fires when the ad is clicked. A full screen view/overlay (e.g. a browser window) is presented in response to the user clicking on an ad.

You may want to pause animations and time sensitive interactions.

### `on_will_dismiss`[​](#on_will_dismiss "Direct link to on_will_dismiss")

Fires before dismissing a full screen view. iOS only.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/bannerad.md)

[

Previous

Ads

](/docs/controls/ads)[

Next

InterstitialAd

](/docs/controls/interstitialad)

-   [Properties](#properties)
    -   [`unit_id`](#unit_id)
-   [Events](#events)
    -   [`on_click`](#on_click)
    -   [`on_close`](#on_close)
    -   [`on_error`](#on_error)
    -   [`on_impression`](#on_impression)
    -   [`on_load`](#on_load)
    -   [`on_open`](#on_open)
    -   [`on_will_dismiss`](#on_will_dismiss)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  InterstitialAd | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/interstitialad/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/interstitialad/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/interstitialad/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/interstitialad/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
            -   [BannerAd](/docs/controls/bannerad)
            -   [InterstitialAd](/docs/controls/interstitialad)
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Ads](/docs/controls/ads)
-   InterstitialAd

On this page

# InterstitialAd

Full-screen ads that cover the interface of an app until closed by the user. They're best used at natural pauses in the flow of an app's execution, such as in between levels of a game or just after completing a task.

See [this](/docs/controls/ads) for more information.

## Properties[​](#properties "Direct link to Properties")

### `unit_id`[​](#unit_id "Direct link to unit_id")

The ad unit ID to be used for the ad.

## Methods[​](#methods "Direct link to Methods")

### `show()`[​](#show "Direct link to show")

Shows the interstitial ad. The interstitial ad must be added to the [`page.overlay`](/docs/controls/page#overlay) before calling this method.

note

Interstitial ads require user input to be dismissed. They can't be dismissed programmatically.

Also, interstitial ads can only be shown once. Subsequent calls to show will trigger `on_error`. To show an `InterstitialAd` again, you need to create a new instance. ([example](/docs/controls/ads#examples))

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when the ad is clicked.

### `on_close`[​](#on_close "Direct link to on_close")

Fires when the full screen view has been closed.

You can resume anything paused while handling `on_open`.

### `on_error`[​](#on_error "Direct link to on_error")

Fires when an error occurs on the ad.

### `on_impression`[​](#on_impression "Direct link to on_impression")

Fires when an impression occurs on the ad.

### `on_load`[​](#on_load "Direct link to on_load")

Fires when the ad is loaded.

### `on_open`[​](#on_open "Direct link to on_open")

Fires when the ad is clicked. A full screen view/overlay (e.g. a browser window) is presented in response to the user clicking on an ad.

You may want to pause animations and time sensitive interactions.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/interstitialad.md)

[

Previous

BannerAd

](/docs/controls/bannerad)[

Next

Canvas

](/docs/controls/canvas)

-   [Properties](#properties)
    -   [`unit_id`](#unit_id)
-   [Methods](#methods)
    -   [`show()`](#show)
-   [Events](#events)
    -   [`on_click`](#on_click)
    -   [`on_close`](#on_close)
    -   [`on_error`](#on_error)
    -   [`on_impression`](#on_impression)
    -   [`on_load`](#on_load)
    -   [`on_open`](#on_open)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CircleAvatar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/circleavatar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/circleavatar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/circleavatar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/circleavatar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   CircleAvatar

On this page

# CircleAvatar

A circle that represents a user.

Typically used with a user's profile image, or, in the absence of such an image, the user's initials. A given user's initials should always be paired with the same background color, for consistency.

If `foreground_image_src` fails then `background_image_src` is used. If `background_image_src` fails too, `bgcolor` is used.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/displays/circleavatar)

-   Python

```
import flet as ftdef main(page):    # a "normal" avatar with background image    a1 = ft.CircleAvatar(        foreground_image_src="https://avatars.githubusercontent.com/u/5041459?s=88&v=4",        content=ft.Text("FF"),    )    # avatar with failing foreground image and fallback text    a2 = ft.CircleAvatar(        foreground_image_src="https://avatars.githubusercontent.com/u/_5041459?s=88&v=4",        content=ft.Text("FF"),    )    # avatar with icon, aka icon with inverse background    a3 = ft.CircleAvatar(        content=ft.Icon(ft.Icons.ABC),    )    # avatar with icon and custom colors    a4 = ft.CircleAvatar(        content=ft.Icon(ft.Icons.WARNING_ROUNDED),        color=ft.Colors.YELLOW_200,        bgcolor=ft.Colors.AMBER_700,    )    # avatar with online status    a5 = ft.Stack(        [            ft.CircleAvatar(                foreground_image_src="https://avatars.githubusercontent.com/u/5041459?s=88&v=4"            ),            ft.Container(                content=ft.CircleAvatar(bgcolor=ft.Colors.GREEN, radius=5),                alignment=ft.alignment.bottom_left,            ),        ],        width=40,        height=40,    )    page.add(a1, a2, a3, a4, a5)ft.app(main)
```

![](https://flet.dev/docs/controls/circleavatar/img/docs/controls/circle-avatar/circle-avatar.png)

## Properties[​](#properties "Direct link to Properties")

### `background_image_src`[​](#background_image_src "Direct link to background_image_src")

The source (local asset file or URL) of the background image in the circle. Changing the background image will cause the avatar to animate to the new image. Typically used as a fallback image for `foreground_image_src`. If the CircleAvatar is to have the user's initials, use `content` instead.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The [color](/docs/reference/colors) with which to fill the circle. Changing the background color will cause the avatar to animate to the new color.

### `color`[​](#color "Direct link to color")

The default text [color](/docs/reference/colors) for text in the circle. Defaults to the primary text theme color if no `bgcolor` is specified.

### `content`[​](#content "Direct link to content")

Typically a `Text` control. If the CircleAvatar is to have an image, use `background_image_src` instead.

### `foreground_image_src`[​](#foreground_image_src "Direct link to foreground_image_src")

The source (local asset file or URL) of the foreground image in the circle. Typically used as profile image. For fallback use `background_image_src`.

### `max_radius`[​](#max_radius "Direct link to max_radius")

The maximum size of the avatar, expressed as the radius (half the diameter). If maxRadius is specified, then radius must not also be specified. Defaults to "infinity".

### `min_radius`[​](#min_radius "Direct link to min_radius")

The minimum size of the avatar, expressed as the radius (half the diameter). If minRadius is specified, then radius must not also be specified. Defaults to zero.

### `radius`[​](#radius "Direct link to radius")

The size of the avatar, expressed as the radius (half the diameter). If radius is specified, then neither minRadius nor maxRadius may be specified.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

## Events[​](#events "Direct link to Events")

### `on_image_error`[​](#on_image_error "Direct link to on_image_error")

Fires when an error occurs while loading the `background_image_src` or `foreground_image_src`.

The event data (`e.data`) is a string whose value is either `"background"` or `"foreground"` indicating the error's origin.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/circleavatar.md)

[

Previous

Canvas

](/docs/controls/canvas)[

Next

CupertinoActivityIndicator

](/docs/controls/cupertinoactivityindicator)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`background_image_src`](#background_image_src)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`content`](#content)
    -   [`foreground_image_src`](#foreground_image_src)
    -   [`max_radius`](#max_radius)
    -   [`min_radius`](#min_radius)
    -   [`radius`](#radius)
    -   [`tooltip`](#tooltip)
-   [Events](#events)
    -   [`on_image_error`](#on_image_error)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  PolygonLayer | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/mappolygonlayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mappolygonlayer/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/mappolygonlayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mappolygonlayer/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   PolygonLayer

On this page

# PolygonLayer

A layer to display `PolygonMarker`s.

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## `PolygonLayer` Properties[​](#polygonlayer-properties "Direct link to polygonlayer-properties")

### `draw_labels_last`[​](#draw_labels_last "Direct link to draw_labels_last")

A boolean value indicating whether to draw labels last.

Defaults to `False`.

### `polygon_culling`[​](#polygon_culling "Direct link to polygon_culling")

A boolean value indicating whether to use polygon culling.

Defaults to `False`.

### `polygon_labels`[​](#polygon_labels "Direct link to polygon_labels")

A boolean value indicating whether to display polygon labels.

Defaults to `True`.

### `polygons`[​](#polygons "Direct link to polygons")

A list of [`PolygonMarker`](#polygonmarker-properties)s to be displayed.

### `simplification_tolerance`[​](#simplification_tolerance "Direct link to simplification_tolerance")

The distance between two neighboring polygon points, in logical pixels scaled to floored zoom.

Defaults to `0.5`.

### `use_alternative_rendering`[​](#use_alternative_rendering "Direct link to use_alternative_rendering")

Whether to use an alternative rendering pathway to draw polygons onto the underlying Canvas, which can be more performant in some circumstances.

Defaults to `False`.

## `PolygonMarker` Properties[​](#polygonmarker-properties "Direct link to polygonmarker-properties")

A marker for the `PolygonLayer`.

### `border_color`[​](#border_color "Direct link to border_color")

The border color of the polygon outline.

### `border_stroke_width`[​](#border_stroke_width "Direct link to border_stroke_width")

The border stroke width of the polygon outline.

### `color`[​](#color "Direct link to color")

The fill color of the polygon.

### `coordinates`[​](#coordinates "Direct link to coordinates")

The list of coordinates (latitude and longitude) defining the polygon marker.

Value is of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).

### `disable_holes_border`[​](#disable_holes_border "Direct link to disable_holes_border")

Whether to holes should have borders.

Defaults to `False`.

### `label`[​](#label "Direct link to label")

The label of the polygon.

### `label_text_style`[​](#label_text_style "Direct link to label_text_style")

The style of the `label`.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

### `rotate_label`[​](#rotate_label "Direct link to rotate_label")

Whether to rotate the label counter to the camera's rotation, to ensure it remains upright.

Defaults to `False`.

### `stroke_cap`[​](#stroke_cap "Direct link to stroke_cap")

The stroke cap style of the polygon.

Value is of type [`StrokeCap`](/docs/reference/types/strokecap).

### `stroke_join`[​](#stroke_join "Direct link to stroke_join")

The stroke join style of the polygon.

Value is of type [`StrokeJoin`](/docs/reference/types/strokejoin).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/mappolygonlayer.md)

[

Previous

MarkerLayer

](/docs/controls/mapmarkerlayer)[

Next

PolylineLayer

](/docs/controls/mappolylinelayer)

-   [Examples](#examples)
-   [`PolygonLayer` Properties](#polygonlayer-properties)
    -   [`draw_labels_last`](#draw_labels_last)
    -   [`polygon_culling`](#polygon_culling)
    -   [`polygon_labels`](#polygon_labels)
    -   [`polygons`](#polygons)
    -   [`simplification_tolerance`](#simplification_tolerance)
    -   [`use_alternative_rendering`](#use_alternative_rendering)
-   [`PolygonMarker` Properties](#polygonmarker-properties)
    -   [`border_color`](#border_color)
    -   [`border_stroke_width`](#border_stroke_width)
    -   [`color`](#color)
    -   [`coordinates`](#coordinates)
    -   [`disable_holes_border`](#disable_holes_border)
    -   [`label`](#label)
    -   [`label_text_style`](#label_text_style)
    -   [`rotate_label`](#rotate_label)
    -   [`stroke_cap`](#stroke_cap)
    -   [`stroke_join`](#stroke_join)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Divider | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/divider/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/divider/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/divider/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/divider/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Divider

On this page

# Divider

A thin horizontal line, with padding on either side.

In the material design language, this represents a divider.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/divider)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Column(            [                ft.Container(                    bgcolor=ft.Colors.AMBER,                    alignment=ft.alignment.center,                    expand=True,                ),                ft.Divider(),                ft.Container(bgcolor=ft.Colors.PINK, alignment=ft.alignment.center, expand=True),                ft.Divider(height=1, color="white"),                ft.Container(                    bgcolor=ft.Colors.BLUE_300,                    alignment=ft.alignment.center,                    expand=True,                ),                ft.Divider(height=9, thickness=3),                ft.Container(                    bgcolor=ft.Colors.DEEP_PURPLE_200,                    alignment=ft.alignment.center,                    expand=True,                ),            ],            spacing=0,            expand=True,        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/divider/img/docs/controls/divider/divider.png)

## Properties[​](#properties "Direct link to Properties")

### `color`[​](#color "Direct link to color")

The [color](/docs/reference/colors) to use when painting the line.

### `height`[​](#height "Direct link to height")

The divider's height extent. The divider itself is always drawn as a horizontal line that is centered within the height specified by this value.

Defaults to `16.0`.

### `leading_indent`[​](#leading_indent "Direct link to leading_indent")

The amount of empty space to the leading edge of the divider.

Defaults to `0.0`.

### `thickness`[​](#thickness "Direct link to thickness")

The thickness of the line drawn within the divider. A divider with a thickness of `0.0` is always drawn as a line with a height of exactly one device pixel.

Defaults to `0.0`.

### `trailing_indent`[​](#trailing_indent "Direct link to trailing_indent")

The amount of empty space to the trailing edge of the divider.

Defaults to `0.0`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/divider.md)

[

Previous

Dismissible

](/docs/controls/dismissible)[

Next

ExpansionPanelList

](/docs/controls/expansionpanel)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`color`](#color)
    -   [`height`](#height)
    -   [`leading_indent`](#leading_indent)
    -   [`thickness`](#thickness)
    -   [`trailing_indent`](#trailing_indent)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ExpansionPanelList | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/expansionpanel/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/expansionpanel/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/expansionpanel/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/expansionpanel/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   ExpansionPanelList

On this page

# ExpansionPanelList

A material expansion panel list that lays out its children and animates expansions.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/expansionpanellist)

### Simple Example[​](#simple-example "Direct link to Simple Example")

-   Python

```
import flet as ftdef main(page: ft.Page):    def handle_change(e: ft.ControlEvent):        print(f"change on panel with index {e.data}")    def handle_delete(e: ft.ControlEvent):        panel.controls.remove(e.control.data)        page.update()    panel = ft.ExpansionPanelList(        expand_icon_color=ft.Colors.AMBER,        elevation=8,        divider_color=ft.Colors.AMBER,        on_change=handle_change,        controls=[            ft.ExpansionPanel(                # has no header and content - placeholders will be used                bgcolor=ft.Colors.BLUE_400,                expanded=True,            )        ]    )    colors = [        ft.Colors.GREEN_500,        ft.Colors.BLUE_800,        ft.Colors.RED_800,    ]        for i in range(3):        exp = ft.ExpansionPanel(            bgcolor=colors[i % len(colors)],            header=ft.ListTile(title=ft.Text(f"Panel {i}")),        )        exp.content = ft.ListTile(            title=ft.Text(f"This is in Panel {i}"),            subtitle=ft.Text(f"Press the icon to delete panel {i}"),            trailing=ft.IconButton(ft.Icons.DELETE, on_click=handle_delete, data=exp),        )        panel.controls.append(exp)    page.add(panel)ft.app(main)
```

![](https://flet.dev/docs/controls/expansionpanel/img/docs/controls/expansion-panel/expansion-panel.gif)

## `ExpansionPanelList` Properties[​](#expansionpanellist-properties "Direct link to expansionpanellist-properties")

### `controls`[​](#controls "Direct link to controls")

A list of `ExpansionPanel`s to display inside `ExpansionPanelList`.

### `divider_color`[​](#divider_color "Direct link to divider_color")

The [color](/docs/reference/colors) of the divider when `ExpansionPanel.expanded` is `False`.

### `elevation`[​](#elevation "Direct link to elevation")

Defines the elevation of the children controls (`ExpansionPanel`s), while it is expanded. Default value is `2`.

### `expanded_header_padding`[​](#expanded_header_padding "Direct link to expanded_header_padding")

Defines the padding around the header when expanded.

Padding value is an instance of [`Padding`](/docs/reference/types/padding) class. Default value is `padding.symmetric(vertical=16.0)`.

### `expanded_icon_color`[​](#expanded_icon_color "Direct link to expanded_icon_color")

The [color](/docs/reference/colors) of the icon. Defaults to `colors.BLACK_54` in light theme mode and `colors.WHITE_60` in dark theme mode.

### `spacing`[​](#spacing "Direct link to spacing")

The size of the gap between the `ExpansionPanel`s when expanded.

## Events[​](#events "Direct link to Events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when an `ExpansionPanel` is expanded or collapsed. The event's data (`e.data`), contains the index of the `ExpansionPanel` which triggered this event.

## `ExpansionPanel` properties[​](#expansionpanel-properties "Direct link to expansionpanel-properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The background [color](/docs/reference/colors) of the panel.

### `content`[​](#content "Direct link to content")

The control to be found in the body of the `ExpansionPanel`. It is displayed below the `header` when the panel is expanded.

If this property is `None`, the `ExpansionPanel` will have a placeholder `Text` as content.

### `can_tap_header`[​](#can_tap_header "Direct link to can_tap_header")

If `True`, tapping on the panel's `header` will expand or collapse it. Defaults to `False`.

### `expanded`[​](#expanded "Direct link to expanded")

Whether expanded(`True`) or collapsed(`False`). Defaults to `False`.

### `header`[​](#header "Direct link to header")

The control to be found in the header of the `ExpansionPanel`. If `can_tap_header` is `True`, tapping on the header will expand or collapse the panel.

If this property is `None`, the `ExpansionPanel` will have a placeholder `Text` as header.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/expansionpanel.md)

[

Previous

Divider

](/docs/controls/divider)[

Next

ExpansionTile

](/docs/controls/expansiontile)

-   [Examples](#examples)
    -   [Simple Example](#simple-example)
-   [`ExpansionPanelList` Properties](#expansionpanellist-properties)
    -   [`controls`](#controls)
    -   [`divider_color`](#divider_color)
    -   [`elevation`](#elevation)
    -   [`expanded_header_padding`](#expanded_header_padding)
    -   [`expanded_icon_color`](#expanded_icon_color)
    -   [`spacing`](#spacing)
-   [Events](#events)
    -   [`on_change`](#on_change)
-   [`ExpansionPanel` properties](#expansionpanel-properties)
    -   [`bgcolor`](#bgcolor)
    -   [`content`](#content)
    -   [`can_tap_header`](#can_tap_header)
    -   [`expanded`](#expanded)
    -   [`header`](#header)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  ExpansionTile | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/expansiontile/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/expansiontile/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/expansiontile/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/expansiontile/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   ExpansionTile

On this page

# ExpansionTile

A single-line ListTile with an expansion arrow icon that expands or collapses the tile to reveal or hide its children.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/expansiontile)

![](https://flet.dev/docs/controls/expansiontile/img/docs/controls/expansion-tile/expansion-tile.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.spacing = 0    page.padding = 0    def handle_expansion_tile_change(e):        page.open(            ft.SnackBar(                ft.Text(f"ExpansionTile was {'expanded' if e.data=='true' else 'collapsed'}"),                duration=1000,            )        )        if e.control.trailing:            e.control.trailing.name = (                ft.Icons.ARROW_DROP_DOWN                if e.control.trailing.name == ft.Icons.ARROW_DROP_DOWN_CIRCLE                else ft.Icons.ARROW_DROP_DOWN_CIRCLE            )            page.update()    page.add(        ft.ExpansionTile(            title=ft.Text("ExpansionTile 1"),            subtitle=ft.Text("Trailing expansion arrow icon"),            affinity=ft.TileAffinity.PLATFORM,            maintain_state=True,            collapsed_text_color=ft.Colors.RED,            text_color=ft.Colors.RED,            controls=[ft.ListTile(title=ft.Text("This is sub-tile number 1"))],        ),        ft.ExpansionTile(            title=ft.Text("ExpansionTile 2"),            subtitle=ft.Text("Custom expansion arrow icon"),            trailing=ft.Icon(ft.Icons.ARROW_DROP_DOWN),            collapsed_text_color=ft.Colors.GREEN,            text_color=ft.Colors.GREEN,            on_change=handle_expansion_tile_change,            controls=[ft.ListTile(title=ft.Text("This is sub-tile number 2"))],        ),        ft.ExpansionTile(            title=ft.Text("ExpansionTile 3"),            subtitle=ft.Text("Leading expansion arrow icon"),            affinity=ft.TileAffinity.LEADING,            initially_expanded=True,            collapsed_text_color=ft.Colors.BLUE,            text_color=ft.Colors.BLUE,            controls=[                ft.ListTile(title=ft.Text("This is sub-tile number 3")),                ft.ListTile(title=ft.Text("This is sub-tile number 4")),                ft.ListTile(title=ft.Text("This is sub-tile number 5")),            ],        ),    )ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `affinity`[​](#affinity "Direct link to affinity")

Typically used to force the expansion arrow icon to the tile's `leading` or `trailing` edge.

Value is of type [`TileAffinity`](/docs/reference/types/tileaffinity) and defaults to `TileAffinity.PLATFORM`.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The [color](/docs/reference/colors) to display behind the sublist when expanded.

### `controls`[​](#controls "Direct link to controls")

The controls to be displayed when the tile expands.

Typically a list of [`ListTile`](/docs/controls/listtile) controls.

### `controls_padding`[​](#controls_padding "Direct link to controls_padding")

Defines the padding around the `controls`.

Padding value is an instance of [`Padding`](/docs/reference/types/padding).

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `collapsed_bgcolor`[​](#collapsed_bgcolor "Direct link to collapsed_bgcolor")

Defines the background [color](/docs/reference/colors) of tile when the sublist is collapsed.

### `collapsed_icon_color`[​](#collapsed_icon_color "Direct link to collapsed_icon_color")

The icon [color](/docs/reference/colors) of tile's expansion arrow icon when the sublist is collapsed.

### `collapsed_shape`[​](#collapsed_shape "Direct link to collapsed_shape")

The tile's border shape when the sublist is collapsed. The value is an instance of [`OutlinedBorder`](/docs/reference/types/outlinedborder).

### `collapsed_text_color`[​](#collapsed_text_color "Direct link to collapsed_text_color")

The [color](/docs/reference/colors) of the tile's titles when the sublist is collapsed.

### `dense`[​](#dense "Direct link to dense")

Whether this list tile is part of a vertically dense list. Dense list tiles default to a smaller height.

It is not recommended to set this property to `True` when in Material3.

Defaults to `False`.

### `enable_feedback`[​](#enable_feedback "Direct link to enable_feedback")

Whether detected gestures should provide acoustic and/or haptic feedback. For example, on Android a tap will produce a clicking sound and a long-press will produce a short vibration, when feedback is enabled.

Defaults to `True`.

### `expanded_alignment`[​](#expanded_alignment "Direct link to expanded_alignment")

Defines the alignment of children, which are arranged in a column when the tile is expanded.

Value is of type [`Alignment`](/docs/reference/types/alignment).

### `expanded_cross_axis_alignment`[​](#expanded_cross_axis_alignment "Direct link to expanded_cross_axis_alignment")

Defines the alignment of each child control within `controls` when the tile is expanded.

Value is of type [`CrossAxisAlignment`](/docs/reference/types/crossaxisalignment) and defaults to `CrossAxisAlignment.CENTER`.

### `icon_color`[​](#icon_color "Direct link to icon_color")

The icon [color](/docs/reference/colors) of tile's expansion arrow icon when the sublist is expanded.

### `initially_expanded`[​](#initially_expanded "Direct link to initially_expanded")

A boolean value which defines whether the tile is initially expanded or collapsed.

Defaults to `False`.

### `leading`[​](#leading "Direct link to leading")

A `Control` to display before the title.

### `maintain_state`[​](#maintain_state "Direct link to maintain_state")

A boolean value which defines whether the state of the `controls` is maintained when the tile expands and collapses.

Defaults to `False`.

### `min_tile_height`[​](#min_tile_height "Direct link to min_tile_height")

The minimum height of the tile.

### `shape`[​](#shape "Direct link to shape")

The tile's border shape when the sublist is expanded.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder).

### `show_trailing_icon`[​](#show_trailing_icon "Direct link to show_trailing_icon")

Whether to show the trailing icon (be it the default icon or the custom `trailing`, if specified and visible).

Defaults to `True`.

### `subtitle`[​](#subtitle "Direct link to subtitle")

Additional content displayed below the title.

Typically a [`Text`](/docs/controls/text) control.

### `text_color`[​](#text_color "Direct link to text_color")

The [color](/docs/reference/colors) of the tile's titles when the sublist is expanded.

### `tile_padding`[​](#tile_padding "Direct link to tile_padding")

Defines the tile's padding. Default value is `padding.symmetric(horizontal=16.0)`.

Padding value is an instance of [`Padding`](/docs/reference/types/padding) class.

### `title`[​](#title "Direct link to title")

A `Control` to display as primary content of the tile.

Typically a [`Text`](/docs/controls/text) control.

### `trailing`[​](#trailing "Direct link to trailing")

A `Control` to display after the title.

Typically an [`Icon`](/docs/controls/icon) control.

### `visual_density`[​](#visual_density "Direct link to visual_density")

Defines how compact the control's layout will be.

Value is of type [`VisualDensity`](/docs/reference/types/visualdensity).

## Events[​](#events "Direct link to Events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when a user clicks or taps the list tile.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when the user long-presses on this list tile.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/expansiontile.md)

[

Previous

ExpansionPanelList

](/docs/controls/expansionpanel)[

Next

GridView

](/docs/controls/gridview)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`affinity`](#affinity)
    -   [`bgcolor`](#bgcolor)
    -   [`controls`](#controls)
    -   [`controls_padding`](#controls_padding)
    -   [`clip_behavior`](#clip_behavior)
    -   [`collapsed_bgcolor`](#collapsed_bgcolor)
    -   [`collapsed_icon_color`](#collapsed_icon_color)
    -   [`collapsed_shape`](#collapsed_shape)
    -   [`collapsed_text_color`](#collapsed_text_color)
    -   [`dense`](#dense)
    -   [`enable_feedback`](#enable_feedback)
    -   [`expanded_alignment`](#expanded_alignment)
    -   [`expanded_cross_axis_alignment`](#expanded_cross_axis_alignment)
    -   [`icon_color`](#icon_color)
    -   [`initially_expanded`](#initially_expanded)
    -   [`leading`](#leading)
    -   [`maintain_state`](#maintain_state)
    -   [`min_tile_height`](#min_tile_height)
    -   [`shape`](#shape)
    -   [`show_trailing_icon`](#show_trailing_icon)
    -   [`subtitle`](#subtitle)
    -   [`text_color`](#text_color)
    -   [`tile_padding`](#tile_padding)
    -   [`title`](#title)
    -   [`trailing`](#trailing)
    -   [`visual_density`](#visual_density)
-   [Events](#events)
    -   [`on_change`](#on_change)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  GridView | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/gridview/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/gridview/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/gridview/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/gridview/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   GridView

On this page

# GridView

A scrollable, 2D array of controls.

info

GridView is very effective for large lists (thousands of items). Prefer it over wrapping [`Column`](/docs/controls/column) or [`Row`](/docs/controls/row) for smooth scrolling. See [Flet Icons Browser](https://github.com/flet-dev/examples/blob/main/python/apps/icons-browser/main.py) for GridView usage example.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/gridview)

### Photo gallery[​](#photo-gallery "Direct link to Photo gallery")

![](https://flet.dev/docs/controls/gridview/img/docs/controls/gridview/photo-gallery.png)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.title = "GridView Example"    page.theme_mode = ft.ThemeMode.DARK    page.padding = 50    page.update()    images = ft.GridView(        expand=1,        runs_count=5,        max_extent=150,        child_aspect_ratio=1.0,        spacing=5,        run_spacing=5,    )    page.add(images)    for i in range(0, 60):        images.controls.append(            ft.Image(                src=f"https://picsum.photos/150/150?{i}",                fit=ft.ImageFit.NONE,                repeat=ft.ImageRepeat.NO_REPEAT,                border_radius=ft.border_radius.all(10),            )        )    page.update()ft.app(main, view=ft.AppView.WEB_BROWSER)
```

## Properties[​](#properties "Direct link to Properties")

### `auto_scroll`[​](#auto_scroll "Direct link to auto_scroll")

`True` if scrollbar should automatically move its position to the end when children updated. Must be `False` for `scroll_to()` method to work.

### `cache_extent`[​](#cache_extent "Direct link to cache_extent")

Items that fall in the cache area (area before or after the visible area that are about to become visible when the user scrolls) are laid out even though they are not (yet) visible on screen. The cacheExtent describes how many pixels the cache area extends before the leading edge and after the trailing edge of the viewport.

The total extent, which the viewport will try to cover with `controls`, is `cache_extent` before the leading edge + extent of the main axis + `cache_extent` after the trailing edge.

### `child_aspect_ratio`[​](#child_aspect_ratio "Direct link to child_aspect_ratio")

The ratio of the cross-axis to the main-axis extent of each child.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.HARD_EDGE`.

### `controls`[​](#controls "Direct link to controls")

A list of `Control`s to display inside GridView.

### `horizontal`[​](#horizontal "Direct link to horizontal")

`True` to layout GridView items horizontally.

### `max_extent`[​](#max_extent "Direct link to max_extent")

The maximum width or height of the grid item.

### `on_scroll_interval`[​](#on_scroll_interval "Direct link to on_scroll_interval")

Throttling in milliseconds for `on_scroll` event.

Defaults to `10`.

### `padding`[​](#padding "Direct link to padding")

The amount of space by which to inset the children.

Padding is an instance of [`Padding`](/docs/reference/types/padding).

### `reverse`[​](#reverse "Direct link to reverse")

Defines whether the scroll view scrolls in the reading direction.

Defaults to `False`.

### `run_spacing`[​](#run_spacing "Direct link to run_spacing")

The number of logical pixels between each child along the cross axis.

### `runs_count`[​](#runs_count "Direct link to runs_count")

The number of children in the cross axis.

### `semantic_child_count`[​](#semantic_child_count "Direct link to semantic_child_count")

The number of children that will contribute semantic information.

### `spacing`[​](#spacing "Direct link to spacing")

The number of logical pixels between each child along the main axis.

## Methods[​](#methods "Direct link to Methods")

### `scroll_to(offset, delta, key, duration, curve)`[​](#scroll_tooffset-delta-key-duration-curve "Direct link to scroll_tooffset-delta-key-duration-curve")

Moves scroll position to either absolute `offset`, relative `delta` or jump to the control with specified `key`.

See [`Column.scroll_to()`](/docs/controls/column#scroll_tooffset-delta-key-duration-curve) for method details and examples.

## Events[​](#events "Direct link to Events")

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when scroll position is changed by a user.

Event handler argument is an instance of [`OnScrollEvent`](/docs/reference/types/onscrollevent) class.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/gridview.md)

[

Previous

ExpansionTile

](/docs/controls/expansiontile)[

Next

ListTile

](/docs/controls/listtile)

-   [Examples](#examples)
    -   [Photo gallery](#photo-gallery)
-   [Properties](#properties)
    -   [`auto_scroll`](#auto_scroll)
    -   [`cache_extent`](#cache_extent)
    -   [`child_aspect_ratio`](#child_aspect_ratio)
    -   [`clip_behavior`](#clip_behavior)
    -   [`controls`](#controls)
    -   [`horizontal`](#horizontal)
    -   [`max_extent`](#max_extent)
    -   [`on_scroll_interval`](#on_scroll_interval)
    -   [`padding`](#padding)
    -   [`reverse`](#reverse)
    -   [`run_spacing`](#run_spacing)
    -   [`runs_count`](#runs_count)
    -   [`semantic_child_count`](#semantic_child_count)
    -   [`spacing`](#spacing)
-   [Methods](#methods)
    -   [`scroll_to(offset, delta, key, duration, curve)`](#scroll_tooffset-delta-key-duration-curve)
-   [Events](#events)
    -   [`on_scroll`](#on_scroll)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Page | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/page/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/page/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/page/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/page/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Page

On this page

# Page

Page is a container for [`View`](/docs/controls/view) controls.

A page instance and the root view are automatically created when a new user session started.

## Properties[​](#properties "Direct link to Properties")

### `auto_scroll`[​](#auto_scroll "Direct link to auto_scroll")

`True` if scrollbar should automatically move its position to the end when children updated. Must be `False` for `scroll_to()` method to work.

### `appbar`[​](#appbar "Direct link to appbar")

An [`AppBar`](/docs/controls/appbar) control to display at the top of the Page.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Background color of the Page.

A color value could be a hex value in `#ARGB` format (e.g. `#FFCC0000`), `#RGB` format (e.g. `#CC0000`) or a named color from `flet.colors` module.

### `bottom_appbar`[​](#bottom_appbar "Direct link to bottom_appbar")

[`BottomAppBar`](/docs/controls/bottomappbar) control to display at the bottom of the Page. If both [`bottom_appbar`](#bottom_appbar) and [`navigation_bar`](#navigation_bar) properties are provided, `NavigationBar` will be displayed.

### `browser_context_menu`[​](#browser_context_menu "Direct link to browser_context_menu")

Used to enable or disable the context menu that appears when the user right-clicks on the web page.

Value is of type [`BrowserContextMenu`](/docs/reference/types/browsercontextmenu).

🌎 Web only.

### `client_ip`[​](#client_ip "Direct link to client_ip")

IP address of the connected user.

🌎 Web only.

### `client_user_agent`[​](#client_user_agent "Direct link to client_user_agent")

Browser details of the connected user.

🌎 Web only.

### `controls`[​](#controls "Direct link to controls")

A list of Controls to display on the Page.

For example, to add a new control to a page:

-   Python

```
page.controls.append(ft.Text("Hello!"))page.update()
```

or to get the same result as above using [`page.add()`](#addcontrols) method

To remove the top most control on the page:

-   Python

```
page.controls.pop()page.update()
```

### `dark_theme`[​](#dark_theme "Direct link to dark_theme")

Customizes the theme of the application when in dark theme mode.

Value is an instance of the `Theme()` class - more information in the [theming](/docs/cookbook/theming) guide.

### `debug`[​](#debug "Direct link to debug")

`True` if Flutter client of Flet app is running in debug mode.

### `decoration`[​](#decoration "Direct link to decoration")

The background decoration.

Value is of type [`BoxDecoration`](/docs/reference/types/boxdecoration).

### `design`[​](#design "Direct link to design")

Reserved for future use.

### `drawer`[​](#drawer "Direct link to drawer")

A [`NavigationDrawer`](/docs/controls/navigationdrawer) control to display as a panel sliding from the start edge of the page.

### `end_drawer`[​](#end_drawer "Direct link to end_drawer")

A [`NavigationDrawer`](/docs/controls/navigationdrawer) control to display as a panel sliding from the end edge of the page.

### `floating_action_button`[​](#floating_action_button "Direct link to floating_action_button")

A [`FloatingActionButton`](/docs/controls/floatingactionbutton) control to display on top of Page content.

### `floating_action_button_location`[​](#floating_action_button_location "Direct link to floating_action_button_location")

Defines a position for the `FloatingActionButton`.

Value is of type [`FloatingActionButtonLocation`](/docs/reference/types/floatingactionbuttonlocation) enum. Default is `FloatingActionButtonLocation.END_FLOAT`.

### `fonts`[​](#fonts "Direct link to fonts")

Defines the custom fonts to be used in the application.

Value is a dictionary, in which the keys represent the font family name used for reference and the values

-   **Key**: The font family name used for reference.
-   **Value**: The font source, either an absolute URL or a relative path to a local asset. The following font file formats are supported `.ttc`, `.ttf` and `.otf`.

Usage example [here](/docs/cookbook/fonts#importing-fonts).

### `height`[​](#height "Direct link to height")

A height of a web page or content area of a native OS window containing Flet app. This property is read-only. It's usually being used inside [`page.on_resized`](#on_resized) handler.

### `horizontal_alignment`[​](#horizontal_alignment "Direct link to horizontal_alignment")

How the child Controls should be placed horizontally.

Property value is [`CrossAxisAlignment`](/docs/reference/types/crossaxisalignment) enum. Default is `START`.

### `locale_configuration`[​](#locale_configuration "Direct link to locale_configuration")

A locale configuration for the app.

Value is of type [`LocaleConfiguration`](/docs/reference/types/localeconfiguration).

### `media`[​](#media "Direct link to media")

Provides details about app media (screen, window). See [MediaQueryData](https://api.flutter.dev/flutter/widgets/MediaQueryData-class.html) in Flutter docs for more info.

Value is of type [`PageMediaData`](/docs/reference/types/pagemediadata).

note

In most cases you should be fine by wrapping your content into [`SafeArea`](/docs/controls/safearea) control.

### `name`[​](#name "Direct link to name")

Page name as specified in `ft.app()` call. Page name is set when Flet app is running as web app. This is a portion of the URL after host name.

### `navigation_bar`[​](#navigation_bar "Direct link to navigation_bar")

[`NavigationBar`](/docs/controls/navigationbar) control to display at the bottom of the page. If both [`bottom_appbar`](#bottom_appbar) and [`navigation_bar`](#navigation_bar) properties are provided, `NavigationBar` will be displayed.

### `on_scroll_interval`[​](#on_scroll_interval "Direct link to on_scroll_interval")

Throttling in milliseconds for `on_scroll` event.

Defaults to `10`.

### `overlay`[​](#overlay "Direct link to overlay")

A list of `Control`s displayed as a stack on top of main page contents.

### `padding`[​](#padding "Direct link to padding")

A space between page contents and its edges. Default value is 10 pixels from each side. To set zero padding:

-   Python

```
page.padding = 0page.update()
```

Value is of type [`Padding`](/docs/reference/types/padding).

### `platform`[​](#platform "Direct link to platform")

Operating system the application is running on.

Value is of type [`PagePlatform`](/docs/reference/types/pageplatform).

This property can be used to create adaptive UI with different controls depending on the operating system:

```
def main(page: ft.Page):    if page.platform == ft.PagePlatform.MACOS:        page.add(ft.CupertinoDialogAction("Cupertino Button"))    else:        page.add(ft.TextButton("Material Button"))
```

You can also set this property for testing purposes:

```
import flet as ftdef main(page):    def set_android(e):        page.platform = ft.PagePlatform.ANDROID        page.update()        print("New platform:", page.platform)    def set_ios(e):        page.platform = "ios"        page.update()        print("New platform:", page.platform)    page.add(        ft.Switch(label="Switch A", adaptive=True),        ft.ElevatedButton("Set Android", on_click=set_android),        ft.ElevatedButton("Set iOS", on_click=set_ios),    )    print("Default platform:", page.platform)ft.app(main)
```

### `platform_brightness`[​](#platform_brightness "Direct link to platform_brightness")

The current brightness mode of the host platform.

Value is read-only and of type [`Brightness`](/docs/reference/types/brightness).

### `pubsub`[​](#pubsub "Direct link to pubsub")

A simple PubSub implementation for passing messages between app sessions.

#### `subscribe(handler)`[​](#subscribehandler "Direct link to subscribehandler")

Subscribe current app session for broadcast (no topic) messages. `handler` is a function or method with a single `message` argument, for example:

```
def main(page: ft.Page):    def on_broadcast_message(message):        print(message)    page.pubsub.subscribe(on_broadcast_message)
```

#### `subscribe_topic(topic, handler)`[​](#subscribe_topictopic-handler "Direct link to subscribe_topictopic-handler")

Subscribe current app session to a specific topic. `handler` is a function or method with two arguments: `topic` and `message`, for example:

```
def main(page: ft.Page):    def on_message(topic, message):        print(topic, message)    page.pubsub.subscribe_topic("general", on_message)
```

#### `send_all(message)`[​](#send_allmessage "Direct link to send_allmessage")

Broadcast message to all subscribers. `message` could be anything: a simple literal or a class instance, for example:

```
@dataclassclass Message:    user: str    text: strdef main(page: ft.Page):    def on_broadcast_message(message):        page.add(ft.Text(f"{message.user}: {message.text}"))    page.pubsub.subscribe(on_broadcast_message)    def on_send_click(e):        page.pubsub.send_all(Message("John", "Hello, all!"))    page.add(ft.ElevatedButton(text="Send message", on_click=on_send_click))
```

#### `send_all_on_topic(topic, message)`[​](#send_all_on_topictopic-message "Direct link to send_all_on_topictopic-message")

Send message to all subscribers on specific topic.

#### `send_others(message)`[​](#send_othersmessage "Direct link to send_othersmessage")

Broadcast message to all subscribers except sender.

#### `send_others_on_topic(topic, message)`[​](#send_others_on_topictopic-message "Direct link to send_others_on_topictopic-message")

Send message to all subscribers on specific topic except sender.

#### `unsubscribe()`[​](#unsubscribe "Direct link to unsubscribe")

Unsubscribe current app session from broadcast messages, for example:

```
@dataclassclass Message:    user: str    text: strdef main(page: ft.Page):    def on_leave_click(e):        page.pubsub.unsubscribe()    page.add(ft.ElevatedButton(text="Leave chat", on_click=on_leave_click))
```

#### `unsubscribe_topic(topic)`[​](#unsubscribe_topictopic "Direct link to unsubscribe_topictopic")

Unsubscribe current app session from specific topic.

#### `unsubscribe_all()`[​](#unsubscribe_all "Direct link to unsubscribe_all")

Unsubscribe current app session from broadcast messages and all topics, for example:

```
def main(page: ft.Page):    def client_exited(e):        page.pubsub.unsubscribe_all()    page.on_close = client_exited
```

### `pwa`[​](#pwa "Direct link to pwa")

`True` if the application is running as Progressive Web App (PWA).

Value is read-only.

### `query`[​](#query "Direct link to query")

A part of app URL after `?`. The value is an instance of `QueryString` with helper methods for fetching query parameters.

### `route`[​](#route "Direct link to route")

Get or sets page's navigation route. See [Navigation and routing](/docs/getting-started/navigation-and-routing) section for more information and examples.

### `rtl`[​](#rtl "Direct link to rtl")

`True` to set text direction to right-to-left.

Defaults to `False`.

### `scroll`[​](#scroll "Direct link to scroll")

Enables a vertical scrolling for the Page to prevent its content overflow.

Value is of type [`ScrollMode`](/docs/reference/types/scrollmode).

### `session`[​](#session "Direct link to session")

A simple key-value storage for session data.

### `session_id`[​](#session_id "Direct link to session_id")

A unique ID of user's session. This property is read-only.

### `spacing`[​](#spacing "Direct link to spacing")

Vertical spacing between controls on the Page. Default value is 10 virtual pixels. Spacing is applied only when `alignment` is set to `start`, `end` or `center`.

### `show_semantics_debugger`[​](#show_semantics_debugger "Direct link to show_semantics_debugger")

`True` turns on an overlay that shows the accessibility information reported by the framework.

### `theme`[​](#theme "Direct link to theme")

Customizes the theme of the application when in light theme mode. Currently, a theme can only be automatically generated from a "seed" color. For example, to generate light theme from a green color.

Value is an instance of the `Theme()` class - more information in the [theming](/docs/cookbook/theming) guide.

### `theme_mode`[​](#theme_mode "Direct link to theme_mode")

The page's theme mode.

Value is of type [`ThemeMode`](/docs/reference/types/thememode) and defaults to `ThemeMode.SYSTEM`.

### `title`[​](#title "Direct link to title")

A title of browser or native OS window, for example:

-   Python

```
page.title = "My awesome app"page.update()
```

### `url`[​](#url "Direct link to url")

The complete web app's URL.

### `vertical_alignment`[​](#vertical_alignment "Direct link to vertical_alignment")

How the child Controls should be placed vertically.

Value is of type [`MainAxisAlignment`](/docs/reference/types/mainaxisalignment) and defaults to `MainAxisAlignment.START`.

### `views`[​](#views "Direct link to views")

A list of [`View`](/docs/controls/view) controls to build navigation history.

The last view in the list is the one displayed on a page.

The first view is a "root" view which cannot be popped.

### `web`[​](#web "Direct link to web")

`True` if the application is running in the web browser.

### `width`[​](#width "Direct link to width")

A width of a web page or content area of a native OS window containing Flet app. This property is read-only. It's usually being used inside [`page.on_resized`](#on_resized) handler.

### `window`[​](#window "Direct link to window")

A class with properties/methods/events to control app's native OS window.

Value is of type [`Window`](/docs/reference/types/window).

## Methods[​](#methods "Direct link to Methods")

### `add(*controls)`[​](#addcontrols "Direct link to addcontrols")

Adds controls to page

```
page.add(ft.Text("Hello!"), ft.FilledButton("Button"))
```

### `can_launch_url(url)`[​](#can_launch_urlurl "Direct link to can_launch_urlurl")

Checks whether the specified URL can be handled by some app installed on the device.

Returns `True` if it is possible to verify that there is a handler available. A `False` return value can indicate either that there is no handler available, or that the application does not have permission to check. For example:

-   On recent versions of Android and iOS, this will always return `False` unless the application has been configuration to allow querying the system for launch support.
-   On web, this will always return `False` except for a few specific schemes that are always assumed to be supported (such as http(s)), as web pages are never allowed to query installed applications.

### `close(control)`[​](#closecontrol "Direct link to closecontrol")

Closes the provided control.

It sets the `control.open=False` and calls `update()`.

### `close_in_app_web_view()`[​](#close_in_app_web_view "Direct link to close_in_app_web_view")

Closes in-app web view opened with `launch_url()`.

📱 Mobile only.

### `error(message)`[​](#errormessage "Direct link to errormessage")

### `fetch_page_details()`[​](#fetch_page_details "Direct link to fetch_page_details")

### `get_clipboard()`[​](#get_clipboard "Direct link to get_clipboard")

Get the last text value saved to a clipboard on a client side.

### `get_control(id)`[​](#get_controlid "Direct link to get_controlid")

Get a control by its `id`.

Example:

```
import flet as ftdef main(page: ft.Page):    x = ft.IconButton(ft.Icons.ADD)    page.add(x)    print(type(page.get_control(x.uid)))ft.app(main)
```

### `get_upload_url(file_name, expires)`[​](#get_upload_urlfile_name-expires "Direct link to get_upload_urlfile_name-expires")

Generates presigned upload URL for built-in upload storage:

-   `file_name` - a relative to upload storage path.
-   `expires` - a URL time-to-live in seconds.

For example:

```
upload_url = page.get_upload_url("dir/filename.ext", 60)
```

To enable built-in upload storage provide `upload_dir` argument to `flet.app()` call:

```
ft.app(main, upload_dir="uploads")
```

### `go(route)`[​](#goroute "Direct link to goroute")

A helper method that updates [`page.route`](#route), calls [`page.on_route_change`](#on_route_change) event handler to update views and finally calls `page.update()`.

### `insert(at, *controls)`[​](#insertat-controls "Direct link to insertat-controls")

Inserts controls at specific index of `page.controls` list.

### `launch_url(url)`[​](#launch_urlurl "Direct link to launch_urlurl")

Opens `url` in a new browser window.

Optional method arguments:

-   `web_window_name` - window tab/name to open URL in: [`UrlTarget.SELF`](/docs/reference/types/urltarget#self) - the same browser tab, [`UrlTarget.BLANK`](/docs/reference/types/urltarget#blank) - a new browser tab (or in external application on mobile device) or `<your name>` - a named tab.
-   `web_popup_window` - set to `True` to display a URL in a browser popup window. Defaults to `False`.
-   `window_width` - optional, popup window width.
-   `window_height` - optional, popup window height.

### `login(provider, fetch_user, fetch_groups, scope, saved_token, on_open_authorization_url, complete_page_html, redirect_to_page, authorization)`[​](#loginprovider-fetch_user-fetch_groups-scope-saved_token-on_open_authorization_url-complete_page_html-redirect_to_page-authorization "Direct link to loginprovider-fetch_user-fetch_groups-scope-saved_token-on_open_authorization_url-complete_page_html-redirect_to_page-authorization")

Starts OAuth flow. See [Authentication](/docs/cookbook/authentication) guide for more information and examples.

### `logout()`[​](#logout "Direct link to logout")

Clears current authentication context. See [Authentication](/docs/cookbook/authentication#signing-out) guide for more information and examples.

### `open(control)`[​](#opencontrol "Direct link to opencontrol")

Opens the provided control.

Adds this control to the [`page.overlay`](#overlay), sets the `control.open=True`, then calls `update()`.

### `remove(*controls)`[​](#removecontrols "Direct link to removecontrols")

Removes specific controls from `page.controls` list.

### `remove_at(index)`[​](#remove_atindex "Direct link to remove_atindex")

Remove controls from `page.controls` list at specific index.

### `run_task(handler, *args, **kwargs)`[​](#run_taskhandler-args-kwargs "Direct link to run_taskhandler-args-kwargs")

Run `handler` coroutine as a new Task in the event loop associated with the current page.

### `run_thread(handler, *args)`[​](#run_threadhandler-args "Direct link to run_threadhandler-args")

Run `handler` function as a new Thread in the executor associated with the current page.

### `scroll_to(offset, delta, key, duration, curve)`[​](#scroll_tooffset-delta-key-duration-curve "Direct link to scroll_tooffset-delta-key-duration-curve")

Moves scroll position to either absolute `offset`, relative `delta` or jump to the control with specified `key`.

See [`Column.scroll_to()`](/docs/controls/column#scroll_tooffset-delta-key-duration-curve) for method details and examples.

### `set_clipboard(data)`[​](#set_clipboarddata "Direct link to set_clipboarddata")

Set clipboard data on a client side (user's web browser or a desktop), for example:

-   Python

```
page.set_clipboard("This value comes from Flet app")
```

## Events[​](#events "Direct link to Events")

### `on_app_lifecycle_state_change`[​](#on_app_lifecycle_state_change "Direct link to on_app_lifecycle_state_change")

Triggers when app lifecycle state changes.

You can use this event to know when the app becomes active (brought to the front) to update UI with the latest information. This event works on iOS, Android, all desktop platforms and web.

Event handler argument is of type [`AppLifecycleStateChangeEvent`](/docs/reference/types/applifecyclestatechangeevent).

### `on_close`[​](#on_close "Direct link to on_close")

Fires when a session has expired after configured amount of time (60 minutes by default).

### `on_connect`[​](#on_connect "Direct link to on_connect")

Fires when a web user (re-)connects to a page session. It is not triggered when an app page is first opened, but is triggered when the page is refreshed, or Flet web client has re-connected after computer was unlocked. This event could be used to detect when a web user becomes "online".

### `on_disconnect`[​](#on_disconnect "Direct link to on_disconnect")

Fires when a web user disconnects from a page session, i.e. closes browser tab/window.

### `on_error`[​](#on_error "Direct link to on_error")

Fires when unhandled exception occurs.

### `on_keyboard_event`[​](#on_keyboard_event "Direct link to on_keyboard_event")

Fires when a keyboard key is pressed.

Event handler argument is of type [`KeyboardEvent`](/docs/reference/types/keyboardevent).

### `on_login`[​](#on_login "Direct link to on_login")

Fires upon successful or failed OAuth authorization flow.

See [Authentication](/docs/cookbook/authentication#checking-authentication-results) guide for more information and examples.

### `on_logout`[​](#on_logout "Direct link to on_logout")

Fires after `page.logout()` call.

### `on_media_change`[​](#on_media_change "Direct link to on_media_change")

Fires when `page.media` has changed.

Event handler argument is of type [`PageMediaData`](/docs/reference/types/pagemediadata).

### `on_platform_brigthness_change`[​](#on_platform_brigthness_change "Direct link to on_platform_brigthness_change")

Fires when brightness of app host platform has changed.

### `on_resized`[​](#on_resized "Direct link to on_resized")

Fires when a user resizes a browser or native OS window containing Flet app, for example:

-   Python

```
def page_resized(e):    print("New page size:", page.window.width, page.window_height)page.on_resized = page_resized
```

Event handler argument is of type [`WindowResizeEvent`](/docs/reference/types/windowresizeevent).

### `on_route_change`[​](#on_route_change "Direct link to on_route_change")

Fires when page route changes either programmatically, by editing application URL or using browser Back/Forward buttons.

Event handler argument is of type [`RouteChangeEvent`](/docs/reference/types/routechangeevent).

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when page's scroll position is changed by a user.

Event handler argument is of type [`OnScrollEvent`](/docs/reference/types/onscrollevent).

### `on_view_pop`[​](#on_view_pop "Direct link to on_view_pop")

Fires when the user clicks automatic "Back" button in [`AppBar`](/docs/controls/appbar) control.

Event handler argument is of type [`ViewPopEvent`](/docs/reference/types/viewpopevent).

## Magic methods[​](#magic-methods "Direct link to Magic methods")

### `__contains__(control)`[​](#__contains__control "Direct link to __contains__control")

Checks if a control is present on the page, for example:

```
import flet as ftdef main(page: ft.Page):    hello = ft.Text("Hello, World!")    page.add(hello)    print(hello in page)  # True        ft.app(main)
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/page.md)

[

Previous

ListView

](/docs/controls/listview)[

Next

Pagelet

](/docs/controls/pagelet)

-   [Properties](#properties)
    -   [`auto_scroll`](#auto_scroll)
    -   [`appbar`](#appbar)
    -   [`bgcolor`](#bgcolor)
    -   [`bottom_appbar`](#bottom_appbar)
    -   [`browser_context_menu`](#browser_context_menu)
    -   [`client_ip`](#client_ip)
    -   [`client_user_agent`](#client_user_agent)
    -   [`controls`](#controls)
    -   [`dark_theme`](#dark_theme)
    -   [`debug`](#debug)
    -   [`decoration`](#decoration)
    -   [`design`](#design)
    -   [`drawer`](#drawer)
    -   [`end_drawer`](#end_drawer)
    -   [`floating_action_button`](#floating_action_button)
    -   [`floating_action_button_location`](#floating_action_button_location)
    -   [`fonts`](#fonts)
    -   [`height`](#height)
    -   [`horizontal_alignment`](#horizontal_alignment)
    -   [`locale_configuration`](#locale_configuration)
    -   [`media`](#media)
    -   [`name`](#name)
    -   [`navigation_bar`](#navigation_bar)
    -   [`on_scroll_interval`](#on_scroll_interval)
    -   [`overlay`](#overlay)
    -   [`padding`](#padding)
    -   [`platform`](#platform)
    -   [`platform_brightness`](#platform_brightness)
    -   [`pubsub`](#pubsub)
    -   [`pwa`](#pwa)
    -   [`query`](#query)
    -   [`route`](#route)
    -   [`rtl`](#rtl)
    -   [`scroll`](#scroll)
    -   [`session`](#session)
    -   [`session_id`](#session_id)
    -   [`spacing`](#spacing)
    -   [`show_semantics_debugger`](#show_semantics_debugger)
    -   [`theme`](#theme)
    -   [`theme_mode`](#theme_mode)
    -   [`title`](#title)
    -   [`url`](#url)
    -   [`vertical_alignment`](#vertical_alignment)
    -   [`views`](#views)
    -   [`web`](#web)
    -   [`width`](#width)
    -   [`window`](#window)
-   [Methods](#methods)
    -   [`add(*controls)`](#addcontrols)
    -   [`can_launch_url(url)`](#can_launch_urlurl)
    -   [`close(control)`](#closecontrol)
    -   [`close_in_app_web_view()`](#close_in_app_web_view)
    -   [`error(message)`](#errormessage)
    -   [`fetch_page_details()`](#fetch_page_details)
    -   [`get_clipboard()`](#get_clipboard)
    -   [`get_control(id)`](#get_controlid)
    -   [`get_upload_url(file_name, expires)`](#get_upload_urlfile_name-expires)
    -   [`go(route)`](#goroute)
    -   [`insert(at, *controls)`](#insertat-controls)
    -   [`launch_url(url)`](#launch_urlurl)
    -   [`login(provider, fetch_user, fetch_groups, scope, saved_token, on_open_authorization_url, complete_page_html, redirect_to_page, authorization)`](#loginprovider-fetch_user-fetch_groups-scope-saved_token-on_open_authorization_url-complete_page_html-redirect_to_page-authorization)
    -   [`logout()`](#logout)
    -   [`open(control)`](#opencontrol)
    -   [`remove(*controls)`](#removecontrols)
    -   [`remove_at(index)`](#remove_atindex)
    -   [`run_task(handler, *args, **kwargs)`](#run_taskhandler-args-kwargs)
    -   [`run_thread(handler, *args)`](#run_threadhandler-args)
    -   [`scroll_to(offset, delta, key, duration, curve)`](#scroll_tooffset-delta-key-duration-curve)
    -   [`set_clipboard(data)`](#set_clipboarddata)
-   [Events](#events)
    -   [`on_app_lifecycle_state_change`](#on_app_lifecycle_state_change)
    -   [`on_close`](#on_close)
    -   [`on_connect`](#on_connect)
    -   [`on_disconnect`](#on_disconnect)
    -   [`on_error`](#on_error)
    -   [`on_keyboard_event`](#on_keyboard_event)
    -   [`on_login`](#on_login)
    -   [`on_logout`](#on_logout)
    -   [`on_media_change`](#on_media_change)
    -   [`on_platform_brigthness_change`](#on_platform_brigthness_change)
    -   [`on_resized`](#on_resized)
    -   [`on_route_change`](#on_route_change)
    -   [`on_scroll`](#on_scroll)
    -   [`on_view_pop`](#on_view_pop)
-   [Magic methods](#magic-methods)
    -   [`__contains__(control)`](#__contains__control)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Pagelet | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/pagelet/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/pagelet/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/pagelet/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/pagelet/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Pagelet

On this page

# Pagelet

Pagelet implements the basic Material Design visual layout structure.

Use it for projects that require "page within a page" layouts with its own AppBar, BottomBar, Drawer, such as demos and galleries.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/pagelet)

### Pagelet example[​](#pagelet-example "Direct link to Pagelet example")

-   Python

```
import flet as ftdef main(page: ft.Page):    def open_pagelet_end_drawer(e):        pagelet.end_drawer.open = True        pagelet.end_drawer.update()    pagelet = ft.Pagelet(        appbar=ft.AppBar(            title=ft.Text("Pagelet AppBar title"), bgcolor=ft.Colors.AMBER_ACCENT        ),        content=ft.Text("Pagelet body"),        bgcolor=ft.Colors.AMBER_100,        bottom_app_bar=ft.BottomAppBar(            bgcolor=ft.Colors.BLUE,            shape=ft.NotchShape.CIRCULAR,            content=ft.Row(                controls=[                    ft.IconButton(icon=ft.Icons.MENU, icon_color=ft.Colors.WHITE),                    ft.Container(expand=True),                    ft.IconButton(icon=ft.Icons.SEARCH, icon_color=ft.Colors.WHITE),                    ft.IconButton(icon=ft.Icons.FAVORITE, icon_color=ft.Colors.WHITE),                ]            ),        ),        end_drawer=ft.NavigationDrawer(            controls=[                ft.NavigationDrawerDestination(                    icon=ft.Icons.ADD_TO_HOME_SCREEN_SHARP, label="Item 1"                ),                ft.NavigationDrawerDestination(                    icon=ft.Icons.ADD_COMMENT, label="Item 2"                ),            ],        ),        floating_action_button=ft.FloatingActionButton(            "Open", on_click=open_pagelet_end_drawer        ),        floating_action_button_location=ft.FloatingActionButtonLocation.CENTER_DOCKED,        width=400,        height=400,    )    page.add(pagelet)ft.app(main)
```

![](https://flet.dev/docs/controls/pagelet/img/docs/controls/pagelet/pagelet-example.png)

## Properties[​](#properties "Direct link to Properties")

### `appbar`[​](#appbar "Direct link to appbar")

An [`AppBar`](/docs/controls/appbar) control to display at the top of the Pagelet.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Background [color](/docs/reference/colors) of the Pagelet.

### `bottom_appbar`[​](#bottom_appbar "Direct link to bottom_appbar")

[`BottomAppBar`](/docs/controls/bottomappbar) control to display at the bottom of the Pagelet. If both [`bottom_appbar`](/docs/controls/pagelet#bottom_appbar) and [`navigation_bar`](/docs/controls/pagelet#navigation_bar) properties are provided, `NavigationBar` will be displayed.

### `bottom_sheet`[​](#bottom_sheet "Direct link to bottom_sheet")

The persistent bottom sheet to show information that supplements the primary content of the Pagelet. Can be any control.

### `content`[​](#content "Direct link to content")

A child Control contained by the Pagelet. The control in the content of the Pagelet is positioned at the top-left of the available space between the app bar and the bottom of the Pagelet.

### `drawer`[​](#drawer "Direct link to drawer")

A [`NavigationDrawer`](/docs/controls/navigationdrawer) control to display as a panel sliding from the start edge of the page.

### `end_drawer`[​](#end_drawer "Direct link to end_drawer")

A [`NavigationDrawer`](/docs/controls/navigationdrawer) control to display as a panel sliding from the end edge of the page.

### `floating_action_button`[​](#floating_action_button "Direct link to floating_action_button")

A [`FloatingActionButton`](/docs/controls/floatingactionbutton) control to display on top of Pagelet content.

### `floating_action_button_location`[​](#floating_action_button_location "Direct link to floating_action_button_location")

Defines a position for the `FloatingActionButton`.

Value can be of type `OffsetValue` or [`FloatingActionButtonLocation`](/docs/reference/types/floatingactionbuttonlocation). Defaults to `FloatingActionButtonLocation.END_FLOAT`.

### `navigation_bar`[​](#navigation_bar "Direct link to navigation_bar")

[`NavigationBar`](/docs/controls/navigationbar) control to display at the bottom of the page. If both [`bottom_appbar`](/docs/controls/pagelet#bottom_appbar) and [`navigation_bar`](/docs/controls/pagelet#navigation_bar) properties are provided, `NavigationBar` will be displayed.

## Methods[​](#methods "Direct link to Methods")

### `close_drawer()`[​](#close_drawer "Direct link to close_drawer")

Closes active drawer.

### `close_end_drawer()`[​](#close_end_drawer "Direct link to close_end_drawer")

Closes active end drawer.

### `show_drawer(drawer: NavigationDialog)`[​](#show_drawerdrawer-navigationdialog "Direct link to show_drawerdrawer-navigationdialog")

Displays [`drawer`](/docs/controls/pagelet#drawer).

### `show_end_drawer(drawer: NavigationDialog)`[​](#show_end_drawerdrawer-navigationdialog "Direct link to show_end_drawerdrawer-navigationdialog")

Displays [`end_drawer`](/docs/controls/pagelet#end_drawer).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/pagelet.md)

[

Previous

Page

](/docs/controls/page)[

Next

Placeholder

](/docs/controls/placeholder)

-   [Examples](#examples)
    -   [Pagelet example](#pagelet-example)
-   [Properties](#properties)
    -   [`appbar`](#appbar)
    -   [`bgcolor`](#bgcolor)
    -   [`bottom_appbar`](#bottom_appbar)
    -   [`bottom_sheet`](#bottom_sheet)
    -   [`content`](#content)
    -   [`drawer`](#drawer)
    -   [`end_drawer`](#end_drawer)
    -   [`floating_action_button`](#floating_action_button)
    -   [`floating_action_button_location`](#floating_action_button_location)
    -   [`navigation_bar`](#navigation_bar)
-   [Methods](#methods)
    -   [`close_drawer()`](#close_drawer)
    -   [`close_end_drawer()`](#close_end_drawer)
    -   [`show_drawer(drawer: NavigationDialog)`](#show_drawerdrawer-navigationdialog)
    -   [`show_end_drawer(drawer: NavigationDialog)`](#show_end_drawerdrawer-navigationdialog)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Placeholder | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/placeholder/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/placeholder/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/placeholder/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/placeholder/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Placeholder

On this page

# Placeholder

A control that draws a box that represents where other widgets will one day be added.

Useful during development to indicate that the interface is not yet complete.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/placeholder)

### Basic example[​](#basic-example "Direct link to Basic example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Placeholder(            expand=True,            color=ft.Colors.random_color()  # random material color        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/placeholder/img/docs/controls/placeholder/basic-example.png)

## Properties[​](#properties "Direct link to Properties")

### `content`[​](#content "Direct link to content")

An optional `Control` to display inside the placeholder.

### `color`[​](#color "Direct link to color")

The [color](/docs/reference/colors) of the placeholder box.

### `fallback_height`[​](#fallback_height "Direct link to fallback_height")

The height to use when the placeholder is in a situation with an unbounded height.

Value is of `float` and defaults to `400.0`.

### `fallback_width`[​](#fallback_width "Direct link to fallback_width")

The width to use when the placeholder is in a situation with an unbounded width.

Value is of `float` and defaults to `400.0`.

### `stroke_width`[​](#stroke_width "Direct link to stroke_width")

The width of the lines in the placeholder box.

Value is of `float` and defaults to `2.0`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/placeholder.md)

[

Previous

Pagelet

](/docs/controls/pagelet)[

Next

ReorderableListView

](/docs/controls/reorderablelistview)

-   [Examples](#examples)
    -   [Basic example](#basic-example)
-   [Properties](#properties)
    -   [`content`](#content)
    -   [`color`](#color)
    -   [`fallback_height`](#fallback_height)
    -   [`fallback_width`](#fallback_width)
    -   [`stroke_width`](#stroke_width)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Tabs | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/tabs/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/tabs/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/tabs/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/tabs/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   Tabs

On this page

# Tabs

The Tabs control is used for navigating frequently accessed, distinct content categories. Tabs allow for navigation between two or more content views and relies on text headers to articulate the different sections of content.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/tabs)

### Tabs[​](#tabs "Direct link to Tabs")

![](https://flet.dev/docs/controls/tabs/img/docs/controls/tabs/tabs-simple.gif)

-   Python

```
import flet as ftdef main(page: ft.Page):    t = ft.Tabs(        selected_index=1,        animation_duration=300,        tabs=[            ft.Tab(                text="Tab 1",                content=ft.Container(                    content=ft.Text("This is Tab 1"), alignment=ft.alignment.center                ),            ),            ft.Tab(                tab_content=ft.Icon(ft.Icons.SEARCH),                content=ft.Text("This is Tab 2"),            ),            ft.Tab(                text="Tab 3",                icon=ft.Icons.SETTINGS,                content=ft.Text("This is Tab 3"),            ),        ],        expand=1,    )    page.add(t)ft.app(main)
```

## `Tabs` properties[​](#tabs-properties "Direct link to tabs-properties")

### `animation_duration`[​](#animation_duration "Direct link to animation_duration")

Duration of animation in milliseconds of switching between tabs.

Defaults to `50`.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior).

### `divider_color`[​](#divider_color "Direct link to divider_color")

The [color](/docs/reference/colors) of the divider.

### `divider_height`[​](#divider_height "Direct link to divider_height")

The height of the divider.

Defaults to `1.0`.

### `enable_feedback`[​](#enable_feedback "Direct link to enable_feedback")

Whether detected gestures should provide acoustic and/or haptic feedback. On Android, for example, setting this to `True` produce a click sound and a long-press will produce a short vibration.

Defaults to `True`.

### `indicator_border_radius`[​](#indicator_border_radius "Direct link to indicator_border_radius")

The radius of the indicator's corners.

### `indicator_border_side`[​](#indicator_border_side "Direct link to indicator_border_side")

The [color](/docs/reference/colors) and weight of the horizontal line drawn below the selected tab.

### `indicator_color`[​](#indicator_color "Direct link to indicator_color")

The [color](/docs/reference/colors) of the indicator(line that appears below the selected tab).

### `indicator_padding`[​](#indicator_padding "Direct link to indicator_padding")

Locates the selected tab's underline relative to the tab's boundary. The `indicator_tab_size` property can be used to define the tab indicator's bounds in terms of its (centered) tab widget with `False`, or the entire tab with `True`.

### `indicator_tab_size`[​](#indicator_tab_size "Direct link to indicator_tab_size")

`True` for indicator to take entire tab.

### `indicator_thickness`[​](#indicator_thickness "Direct link to indicator_thickness")

The thickness of the indicator. Value must be greater than zero.

Defaults to `3.0` when `secondary=False`, else `3.0`.

### `is_secondary`[​](#is_secondary "Direct link to is_secondary")

Whether to create a secondary/nested tab bar. Secondary tabs are used within a content area to further separate related content and establish hierarchy.

Defaults to `False`.

### `label_color`[​](#label_color "Direct link to label_color")

The [color](/docs/reference/colors) of selected tab labels.

### `label_padding`[​](#label_padding "Direct link to label_padding")

The padding around the tab label.

Value is of type [`Padding`](/docs/reference/types/padding).

### `label_text_style`[​](#label_text_style "Direct link to label_text_style")

The text style of the tab labels.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

### `mouse_cursor`[​](#mouse_cursor "Direct link to mouse_cursor")

The cursor to be displayed when a mouse pointer enters or is hovering over this control. The value is [`MouseCursor`](/docs/reference/types/mousecursor) enum.

### `overlay_color`[​](#overlay_color "Direct link to overlay_color")

Defines the ink response focus, hover, and splash [colors](/docs/reference/colors) in various [`ControlState`](/docs/reference/types/controlstate) states. The following `ControlState` values are supported: `PRESSED`, `HOVERED` and `FOCUSED`.

### `padding`[​](#padding "Direct link to padding")

The padding around the Tabs control.

Value is of type [`Padding`](/docs/reference/types/padding).

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index of currently selected tab.

### `scrollable`[​](#scrollable "Direct link to scrollable")

Whether this tab bar can be scrolled horizontally.

If `scrollable` is `True`, then each tab is as wide as needed for its label and the entire Tabs controls is scrollable. Otherwise each tab gets an equal share of the available space.

### `splash_border_radius`[​](#splash_border_radius "Direct link to splash_border_radius")

Defines the clipping radius of splashes that extend outside the bounds of the tab.

Value is of type [`BorderRadius`](/docs/reference/types/borderradius).

### `tab_alignment`[​](#tab_alignment "Direct link to tab_alignment")

Specifies the horizontal alignment of the tabs within the Tabs control.

Value is of type [`TabAlignment`](/docs/reference/types/tabalignment) and defaults to `TabAlignment.START`, if `scrollable=True`, and to `TabAlignment.FILL`, if `scrollable=False`.

### `tabs`[​](#tabs-1 "Direct link to tabs-1")

A list of `Tab` controls.

### `unselected_label_color`[​](#unselected_label_color "Direct link to unselected_label_color")

The [color](/docs/reference/colors) of unselected tab labels.

### `unselected_label_text_style`[​](#unselected_label_text_style "Direct link to unselected_label_text_style")

The text style of the unselected tab labels.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

## `Tabs` events[​](#tabs-events "Direct link to tabs-events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when `selected_index` changes.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a tab is clicked.

## `Tab` properties[​](#tab-properties "Direct link to tab-properties")

### `content`[​](#content "Direct link to content")

A `Control` to display below the Tab when it is selected.

### `icon`[​](#icon "Direct link to icon")

An icon to display on the left of Tab text.

### `tab_content`[​](#tab_content "Direct link to tab_content")

A `Control` representing custom tab content replacing `text` and `icon`.

### `text`[​](#text "Direct link to text")

Tab's display name.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/tabs.md)

[

Previous

Stack

](/docs/controls/stack)[

Next

VerticalDivider

](/docs/controls/verticaldivider)

-   [Examples](#examples)
    -   [Tabs](#tabs)
-   [`Tabs` properties](#tabs-properties)
    -   [`animation_duration`](#animation_duration)
    -   [`clip_behavior`](#clip_behavior)
    -   [`divider_color`](#divider_color)
    -   [`divider_height`](#divider_height)
    -   [`enable_feedback`](#enable_feedback)
    -   [`indicator_border_radius`](#indicator_border_radius)
    -   [`indicator_border_side`](#indicator_border_side)
    -   [`indicator_color`](#indicator_color)
    -   [`indicator_padding`](#indicator_padding)
    -   [`indicator_tab_size`](#indicator_tab_size)
    -   [`indicator_thickness`](#indicator_thickness)
    -   [`is_secondary`](#is_secondary)
    -   [`label_color`](#label_color)
    -   [`label_padding`](#label_padding)
    -   [`label_text_style`](#label_text_style)
    -   [`mouse_cursor`](#mouse_cursor)
    -   [`overlay_color`](#overlay_color)
    -   [`padding`](#padding)
    -   [`selected_index`](#selected_index)
    -   [`scrollable`](#scrollable)
    -   [`splash_border_radius`](#splash_border_radius)
    -   [`tab_alignment`](#tab_alignment)
    -   [`tabs`](#tabs-1)
    -   [`unselected_label_color`](#unselected_label_color)
    -   [`unselected_label_text_style`](#unselected_label_text_style)
-   [`Tabs` events](#tabs-events)
    -   [`on_change`](#on_change)
    -   [`on_click`](#on_click)
-   [`Tab` properties](#tab-properties)
    -   [`content`](#content)
    -   [`icon`](#icon)
    -   [`tab_content`](#tab_content)
    -   [`text`](#text)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  VerticalDivider | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/verticaldivider/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/verticaldivider/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/verticaldivider/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/verticaldivider/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
        -   [Card](/docs/controls/card)
        -   [Column](/docs/controls/column)
        -   [Container](/docs/controls/container)
        -   [CupertinoListTile](/docs/controls/cupertinolisttile)
        -   [DataTable](/docs/controls/datatable)
        -   [Dismissible](/docs/controls/dismissible)
        -   [Divider](/docs/controls/divider)
        -   [ExpansionPanelList](/docs/controls/expansionpanel)
        -   [ExpansionTile](/docs/controls/expansiontile)
        -   [GridView](/docs/controls/gridview)
        -   [ListTile](/docs/controls/listtile)
        -   [ListView](/docs/controls/listview)
        -   [Page](/docs/controls/page)
        -   [Pagelet](/docs/controls/pagelet)
        -   [Placeholder](/docs/controls/placeholder)
        -   [ReorderableListView](/docs/controls/reorderablelistview)
        -   [ResponsiveRow](/docs/controls/responsiverow)
        -   [Row](/docs/controls/row)
        -   [SafeArea](/docs/controls/safearea)
        -   [Stack](/docs/controls/stack)
        -   [Tabs](/docs/controls/tabs)
        -   [VerticalDivider](/docs/controls/verticaldivider)
        -   [View](/docs/controls/view)
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Layout](/docs/controls/layout)
-   VerticalDivider

On this page

# VerticalDivider

A thin vertical line, with padding on either side.

In the material design language, this represents a divider.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/layout/verticaldivider)

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.Row(            [                ft.Container(                    bgcolor=ft.Colors.ORANGE_300,                    alignment=ft.alignment.center,                    expand=True,                ),                 ft.VerticalDivider(),                ft.Container(                    bgcolor=ft.Colors.BROWN_400,                    alignment=ft.alignment.center,                    expand=True,                ),                 ft.VerticalDivider(width=1, color="white"),                ft.Container(                    bgcolor=ft.Colors.BLUE_300,                    alignment=ft.alignment.center,                    expand=True,                ),                 ft.VerticalDivider(width=9, thickness=3),                ft.Container(                    bgcolor=ft.Colors.GREEN_300,                    alignment=ft.alignment.center,                    expand=True,                ),            ],            spacing=0,            expand=True,        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/verticaldivider/img/docs/controls/vertical-divider/vertical-divider.png)

## Properties[​](#properties "Direct link to Properties")

### `color`[​](#color "Direct link to color")

The [color](/docs/reference/colors) to use when painting the line.

### `leading_indent`[​](#leading_indent "Direct link to leading_indent")

The amount of empty space to the leading edge of the divider.

Defaults to `0.0`.

### `thickness`[​](#thickness "Direct link to thickness")

The thickness of the line drawn within the divider. A divider with a thickness of `0.0` is always drawn as a line with a width of exactly one device pixel.

Defaults to `0.0`.

### `trailing_indent`[​](#trailing_indent "Direct link to trailing_indent")

The amount of empty space to the trailing edge of the divider.

Defaults to `0.0`.

### `width`[​](#width "Direct link to width")

The divider's width. The divider itself is always drawn as a vertical line that is centered within the width specified by this value. I

Defaults to `16.0`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/verticaldivider.md)

[

Previous

Tabs

](/docs/controls/tabs)[

Next

View

](/docs/controls/view)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`color`](#color)
    -   [`leading_indent`](#leading_indent)
    -   [`thickness`](#thickness)
    -   [`trailing_indent`](#trailing_indent)
    -   [`width`](#width)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Navigation | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/app-structure-navigation/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/app-structure-navigation/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/app-structure-navigation/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/app-structure-navigation/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   Navigation

# Navigation

[

## 📄️ AppBar

A material design app bar.

](/docs/controls/appbar)

[

## 📄️ BottomAppBar

A material design bottom app bar.

](/docs/controls/bottomappbar)

[

## 📄️ CupertinoAppBar

An iOS-styled application bar.

](/docs/controls/cupertinoappbar)

[

## 📄️ CupertinoNavigationBar

An iOS-styled bottom navigation tab bar.

](/docs/controls/cupertinonavigationbar)

[

## 📄️ MenuBar

A menu bar that manages cascading child menus.

](/docs/controls/menubar)

[

## 📄️ NavigationBar

Material 3 Navigation Bar component.

](/docs/controls/navigationbar)

[

## 📄️ NavigationDrawer

Material Design Navigation Drawer component.

](/docs/controls/navigationdrawer)

[

## 📄️ NavigationRail

A material widget that is meant to be displayed at the left or right of an app to navigate between a small number of views, typically between three and five.

](/docs/controls/navigationrail)

[

Previous

View

](/docs/controls/view)[

Next

AppBar

](/docs/controls/appbar)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  AppBar | Flet   

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/appbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/appbar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/appbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/appbar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   AppBar

On this page

# AppBar

A material design app bar.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/appbar)

### AppBar[​](#appbar "Direct link to AppBar")

-   Python

```
import flet as ftdef main(page: ft.Page):    def check_item_clicked(e):        e.control.checked = not e.control.checked        page.update()    page.appbar = ft.AppBar(        leading=ft.Icon(ft.Icons.PALETTE),        leading_width=40,        title=ft.Text("AppBar Example"),        center_title=False,        bgcolor=ft.Colors.SURFACE_CONTAINER_HIGHEST,        actions=[            ft.IconButton(ft.Icons.WB_SUNNY_OUTLINED),            ft.IconButton(ft.Icons.FILTER_3),            ft.PopupMenuButton(                items=[                    ft.PopupMenuItem(text="Item 1"),                    ft.PopupMenuItem(),  # divider                    ft.PopupMenuItem(                        text="Checked item", checked=False, on_click=check_item_clicked                    ),                ]            ),        ],    )    page.add(ft.Text("Body!"))ft.app(main)
```

![](https://flet.dev/docs/controls/appbar/img/docs/controls/app-bar/app-bar.gif)

## Properties[​](#properties "Direct link to Properties")

### `actions`[​](#actions "Direct link to actions")

A list of `Control`s to display in a row after the title control.

Typically these controls are [`IconButtons`](/docs/controls/iconbutton) representing common operations. For less common operations, consider using a [`PopupMenuButton`](/docs/controls/popupmenubutton) as the last action.

**Note** that, if `AppBar.adaptive=True` and the app is opened on an iOS or macOS device, only the first element of this list will be used. This is because the `CupertinoAppBar`(which will be used on those two platforms) only accepts one - trailing - action control.

### `adaptive`[​](#adaptive "Direct link to adaptive")

If the value is `True`, an adaptive AppBar is created based on whether the target platform is iOS/macOS.

On iOS and macOS, a [`CupertinoAppBar`](/docs/controls/cupertinoappbar) is created, which has matching functionality and presentation as `AppBar`, and the graphics as expected on iOS. On other platforms, a Material AppBar is created.

Value is of type `bool` and defaults to `False`.

### `automatically_imply_leading`[​](#automatically_imply_leading "Direct link to automatically_imply_leading")

Controls whether we should try to imply the leading widget if null.

If `True` and `leading` is null, automatically try to deduce what the leading widget should be. If `False` and `leading` is null, leading space is given to title. If leading widget is not null, this parameter has no effect.

Value is of type `bool`.

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The fill [color](/docs/reference/colors) to use for an AppBar. Default color is defined by current theme.

### `center_title`[​](#center_title "Direct link to center_title")

Whether the title should be centered.

Value is of type `bool` and defaults to `False`.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior).

### `color`[​](#color "Direct link to color")

The default [color](/docs/reference/colors) for `Text` and `Icon` controls within the app bar. Default color is defined by current theme.

### `elevation`[​](#elevation "Direct link to elevation")

The app bar's elevation.

Note: This effect is only visible when using the Material 2 design (`Theme.use_material3=False`).

Value is of type [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber) and defaults to `4`.

### `elevation_on_scroll`[​](#elevation_on_scroll "Direct link to elevation_on_scroll")

The elevation to be used if this app bar has something scrolled underneath it.

Value is of type [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber).

### `exclude_header_semantics`[​](#exclude_header_semantics "Direct link to exclude_header_semantics")

Whether the `title` should be wrapped with header [`Semantics`](/docs/controls/semantics).

Value is of type `bool` and defaults to `False`.

### `force_material_transparency`[​](#force_material_transparency "Direct link to force_material_transparency")

Forces the app bar to be transparent (instead of Material's default type).

This will also remove the visual display of `bgcolor` and `elevation`, and affect other characteristics of this app bar.

Value is of type `bool`.

### `is_secondary`[​](#is_secondary "Direct link to is_secondary")

Whether this app bar is not being displayed at the top of the screen.

Value is of type `bool` and defaults to `False`.

### `leading`[​](#leading "Direct link to leading")

A `Control` to display before the toolbar's title.

Typically the leading control is an [`Icon`](/docs/controls/icon) or an [`IconButton`](/docs/controls/iconbutton).

Value is of type `Control`.

### `leading_width`[​](#leading_width "Direct link to leading_width")

Defines the width of leading control.

Value is of type [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber) and defaults to `56.0`.

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) of the shadow below the app bar.

A shadow is only visible and displayed if the `elevation` is greater than zero.

### `shape`[​](#shape "Direct link to shape")

The shape of the app bar's Material as well as its shadow.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder).

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The color of the surface tint overlay applied to the app bar's `bgcolor` to indicate elevation.

By default, no overlay will be applied.

### `title`[​](#title "Direct link to title")

The primary `Control` displayed in the app bar. Typically a [`Text`](/docs/controls/text) control that contains a description of the current contents of the app.

**Note** that, if `AppBar.adaptive=True` and the app is opened on an iOS or macOS device, this control will be automatically centered.

Value is of type `Control`.

### `title_spacing`[​](#title_spacing "Direct link to title_spacing")

The spacing around `title` on the horizontal axis. It is applied even if there are no `leading` or `actions` controls.

If you want `title` to take all the space available, set this value to `0.0`.

Value is of type [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber).

### `title_text_style`[​](#title_text_style "Direct link to title_text_style")

The style to be used for the `Text` controls in the `title`.

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

### `toolbar_height`[​](#toolbar_height "Direct link to toolbar_height")

Defines the height of the toolbar component of an AppBar.

Value is of tye [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber) and defaults to `56.0`.

### `toolbar_opacity`[​](#toolbar_opacity "Direct link to toolbar_opacity")

The opacity of the toolbar. Value ranges from `0.0` (transparent) to `1.0` (fully opaque).

Value is of type [`OptionalNumber`](/docs/reference/types/aliases#optionalnumber) and defaults to `1.0`.

### `toolbar_text_style`[​](#toolbar_text_style "Direct link to toolbar_text_style")

The style to be used for the `Text` controls in the app bar's `leading` and `actions` (but not `title`).

Value is of type [`TextStyle`](/docs/reference/types/textstyle).

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/appbar.md)

[

Previous

Navigation

](/docs/controls/app-structure-navigation)[

Next

BottomAppBar

](/docs/controls/bottomappbar)

-   [Examples](#examples)
    -   [AppBar](#appbar)
-   [Properties](#properties)
    -   [`actions`](#actions)
    -   [`adaptive`](#adaptive)
    -   [`automatically_imply_leading`](#automatically_imply_leading)
    -   [`bgcolor`](#bgcolor)
    -   [`center_title`](#center_title)
    -   [`clip_behavior`](#clip_behavior)
    -   [`color`](#color)
    -   [`elevation`](#elevation)
    -   [`elevation_on_scroll`](#elevation_on_scroll)
    -   [`exclude_header_semantics`](#exclude_header_semantics)
    -   [`force_material_transparency`](#force_material_transparency)
    -   [`is_secondary`](#is_secondary)
    -   [`leading`](#leading)
    -   [`leading_width`](#leading_width)
    -   [`shadow_color`](#shadow_color)
    -   [`shape`](#shape)
    -   [`surface_tint_color`](#surface_tint_color)
    -   [`title`](#title)
    -   [`title_spacing`](#title_spacing)
    -   [`title_text_style`](#title_text_style)
    -   [`toolbar_height`](#toolbar_height)
    -   [`toolbar_opacity`](#toolbar_opacity)
    -   [`toolbar_text_style`](#toolbar_text_style)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  BottomAppBar | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/bottomappbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/bottomappbar/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/bottomappbar/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/bottomappbar/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   BottomAppBar

On this page

# BottomAppBar

A material design bottom app bar.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/bottomappbar)

### BottomAppBar[​](#bottomappbar "Direct link to BottomAppBar")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.horizontal_alignment = page.vertical_alignment = "center"    page.floating_action_button = ft.FloatingActionButton(icon=ft.Icons.ADD)    page.floating_action_button_location = ft.FloatingActionButtonLocation.CENTER_DOCKED    page.appbar = ft.AppBar(        title=ft.Text("Bottom AppBar Demo"),        center_title=True,        bgcolor=ft.Colors.GREEN_300,        automatically_imply_leading=False,    )    page.bottom_appbar = ft.BottomAppBar(        bgcolor=ft.Colors.BLUE,        shape=ft.NotchShape.CIRCULAR,        content=ft.Row(            controls=[                ft.IconButton(icon=ft.Icons.MENU, icon_color=ft.Colors.WHITE),                ft.Container(expand=True),                ft.IconButton(icon=ft.Icons.SEARCH, icon_color=ft.Colors.WHITE),                ft.IconButton(icon=ft.Icons.FAVORITE, icon_color=ft.Colors.WHITE),            ]        ),    )    page.add(ft.Text("Body!"))ft.app(main)
```

![](https://flet.dev/docs/controls/bottomappbar/img/docs/controls/bottom-app-bar/bottom-app-bar.png)

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

The fill [color](/docs/reference/colors) to use for the BottomAppBar. Default color is defined by current theme.

### `clip_behavior`[​](#clip_behavior "Direct link to clip_behavior")

The content will be clipped (or not) according to this option.

Value is of type [`ClipBehavior`](/docs/reference/types/clipbehavior) and defaults to `ClipBehavior.NONE`.

### `content`[​](#content "Direct link to content")

A child Control contained by the BottomAppBar.

### `elevation`[​](#elevation "Direct link to elevation")

This property controls the size of the shadow below the BottomAppBar.

Defaults to `4`.

### `height`[​](#height "Direct link to height")

The height of the BottomAppBar.

Defaults to `80.0` in material 3.

### `notch_margin`[​](#notch_margin "Direct link to notch_margin")

The margin between the `FloatingActionButton` and the BottomAppBar's notch.

Can be visible only if `shape=None`.

### `padding`[​](#padding "Direct link to padding")

Empty space to inscribe inside a container decoration (background, border). Padding is an instance of [`Padding`](/docs/reference/types/padding) class.

Defaults to `padding.symmetric(vertical=12.0, horizontal=16.0)`.

### `shadow_color`[​](#shadow_color "Direct link to shadow_color")

The [color](/docs/reference/colors) of the shadow below the BottomAppBar.

### `shape`[​](#shape "Direct link to shape")

The notch that is made for the floating action button.

Value is of type [`NotchShape`](/docs/reference/types/notchshape).

### `surface_tint_color`[​](#surface_tint_color "Direct link to surface_tint_color")

The [color](/docs/reference/colors) used as an overlay on `bgcolor` to indicate elevation.

If this is `None`, no overlay will be applied. Otherwise this color will be composited on top of `bgcolor` with an opacity related to `elevation` and used to paint the BottomAppBar's background.

Defaults to `None`.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/bottomappbar.md)

[

Previous

AppBar

](/docs/controls/appbar)[

Next

CupertinoAppBar

](/docs/controls/cupertinoappbar)

-   [Examples](#examples)
    -   [BottomAppBar](#bottomappbar)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`clip_behavior`](#clip_behavior)
    -   [`content`](#content)
    -   [`elevation`](#elevation)
    -   [`height`](#height)
    -   [`notch_margin`](#notch_margin)
    -   [`padding`](#padding)
    -   [`shadow_color`](#shadow_color)
    -   [`shape`](#shape)
    -   [`surface_tint_color`](#surface_tint_color)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  NavigationRail | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/navigationrail/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/navigationrail/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/navigationrail/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/navigationrail/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
        -   [AppBar](/docs/controls/appbar)
        -   [BottomAppBar](/docs/controls/bottomappbar)
        -   [CupertinoAppBar](/docs/controls/cupertinoappbar)
        -   [CupertinoNavigationBar](/docs/controls/cupertinonavigationbar)
        -   [MenuBar](/docs/controls/menubar)
        -   [NavigationBar](/docs/controls/navigationbar)
        -   [NavigationDrawer](/docs/controls/navigationdrawer)
        -   [NavigationRail](/docs/controls/navigationrail)
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Navigation](/docs/controls/app-structure-navigation)
-   NavigationRail

On this page

# NavigationRail

A material widget that is meant to be displayed at the left or right of an app to navigate between a small number of views, typically between three and five.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/navigation/navigationrail)

-   Python

```
import flet as ftdef main(page: ft.Page):    rail = ft.NavigationRail(        selected_index=0,        label_type=ft.NavigationRailLabelType.ALL,        # extended=True,        min_width=100,        min_extended_width=400,        leading=ft.FloatingActionButton(icon=ft.Icons.CREATE, text="Add"),        group_alignment=-0.9,        destinations=[            ft.NavigationRailDestination(                icon=ft.Icons.FAVORITE_BORDER, selected_icon=ft.Icons.FAVORITE, label="First"            ),            ft.NavigationRailDestination(                icon=ft.Icon(ft.Icons.BOOKMARK_BORDER),                selected_icon=ft.Icon(ft.Icons.BOOKMARK),                label="Second",            ),            ft.NavigationRailDestination(                icon=ft.Icons.SETTINGS_OUTLINED,                selected_icon=ft.Icon(ft.Icons.SETTINGS),                label_content=ft.Text("Settings"),            ),        ],        on_change=lambda e: print("Selected destination:", e.control.selected_index),    )    page.add(        ft.Row(            [                rail,                ft.VerticalDivider(width=1),                ft.Column([ ft.Text("Body!")], alignment=ft.MainAxisAlignment.START, expand=True),            ],            expand=True,        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/navigationrail/img/docs/controls/navigation-rail/custom-navrail.png)

## `NavigationRail` properties[​](#navigationrail-properties "Direct link to navigationrail-properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Sets the [color](/docs/reference/colors) of the Container that holds all of the NavigationRail's contents.

### `destinations`[​](#destinations "Direct link to destinations")

Defines the appearance of the button items that are arrayed within the navigation rail.

The value must be a list of two or more `NavigationRailDestination` instances.

### `elevation`[​](#elevation "Direct link to elevation")

Controls the size of the shadow below the NavigationRail.

Defaults to `0.0`.

### `extended`[​](#extended "Direct link to extended")

Indicates that the NavigationRail should be in the extended state.

The extended state has a wider rail container, and the labels are positioned next to the icons. `min_extended_width` can be used to set the minimum width of the rail when it is in this state.

The rail will implicitly animate between the extended and normal state.

If the rail is going to be in the extended state, then the `label_type` must be set to `none`.

Defaults to `False`.

### `group_alignment`[​](#group_alignment "Direct link to group_alignment")

The vertical alignment for the group of destinations within the rail.

The NavigationRailDestinations are grouped together with the trailing widget, between the leading widget and the bottom of the rail.

The value must be between `-1.0` and `1.0`.

If `group_alignment` is `-1.0`, then the items are aligned to the top. If `group_alignment` is `0.0`, then the items are aligned to the center. If `group_alignment` is `1.0`, then the items are aligned to the bottom.

Defaults to `-1.0`.

### `indicator_color`[​](#indicator_color "Direct link to indicator_color")

The [color](/docs/reference/colors) of the navigation rail's indicator.

### `indicator_shape`[​](#indicator_shape "Direct link to indicator_shape")

The shape of the navigation rail's indicator.

Value is of type [`OutlinedBorder`](/docs/reference/types/outlinedborder) and defaults to `StadiumBorder()`.

### `label_type`[​](#label_type "Direct link to label_type")

Defines the layout and behavior of the labels for the default, unextended navigation rail.

When a navigation rail is extended, the labels are always shown.

Value is of type [`NavigationRailLabelType`](/docs/reference/types/navigationraillabeltype) and defaults to `None` - no labels are shown.

### `leading`[​](#leading "Direct link to leading")

An optional leading control in the rail that is placed above the destinations.

Its location is not affected by `group_alignment`.

This is commonly a [`FloatingActionButton`](/docs/controls/floatingactionbutton), but may also be a non-button, such as a logo.

### `min_extended_width`[​](#min_extended_width "Direct link to min_extended_width")

The final width when the animation is complete for setting `extended` to `True`.

Defaults to `256`.

### `min_width`[​](#min_width "Direct link to min_width")

The smallest possible width for the rail regardless of the destination's icon or label size.

Defaults to `72`.

This value also defines the min width and min height of the destinations.

To make a compact rail, set this to `56` and use `label_type='none'`.

### `selected_index`[​](#selected_index "Direct link to selected_index")

The index into `destinations` for the current selected `NavigationRailDestination` or `None` if no destination is selected.

### `selected_label_text_style`[​](#selected_label_text_style "Direct link to selected_label_text_style")

The [`TextStyle`](/docs/reference/types/textstyle) of a destination's label when it is selected.

When a destination is not selected, `unselected_label_text_style` will instead be used.

### `trailing`[​](#trailing "Direct link to trailing")

An optional trailing control in the rail that is placed below the destinations.

Its location is affected by `group_alignment`.

This is commonly a list of additional options or destinations that is usually only rendered when `extended=True`.

### `unselected_label_text_style`[​](#unselected_label_text_style "Direct link to unselected_label_text_style")

The [`TextStyle`](/docs/reference/types/textstyle) of a destination's label when it is not selected.

When a destination is selected, `selected_label_text_style` will instead be used.

## `NavigationRail` events[​](#navigationrail-events "Direct link to navigationrail-events")

### `on_change`[​](#on_change "Direct link to on_change")

Fires when selected destination changed.

## `NavigationRailDestination` properties[​](#navigationraildestination-properties "Direct link to navigationraildestination-properties")

### `icon`[​](#icon "Direct link to icon")

The [name of the icon](/docs/reference/icons) or `Control` of the destination. Example with icon name:

```
icon=ft.Icons.BOOKMARK
```

Example with Control:

```
icon=ft.Icon(ft.Icons.BOOKMARK)
```

If `selected_icon` is provided, this will only be displayed when the destination is not selected.

To make the NavigationRail more accessible, consider choosing an icon with a stroked and filled version, such as `ft.Icons.CLOUD` and `ft.Icons.CLOUD_QUEUE`. The icon should be set to the stroked version and `selected_icon` to the filled version.

### `icon_content`[​](#icon_content "Direct link to icon_content")

The icon `Control` of the destination. Typically the icon is an [`Icon`](/docs/controls/icon) control. Used instead of `icon` property.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`icon`](#icon) instead.**

### `indicator_color`[​](#indicator_color-1 "Direct link to indicator_color-1")

The [color](/docs/reference/colors) of the `indicator_shape` when this destination is selected.

### `indicator_shape`[​](#indicator_shape-1 "Direct link to indicator_shape-1")

The shape of the selection indicator. The value is an instance of [`OutlinedBorder`](/docs/reference/types/outlinedborder) class.

### `label`[​](#label "Direct link to label")

A string representing the destination's label. Will be displayed only if `label_content` is not provided.

### `label_content`[​](#label_content "Direct link to label_content")

The label `Control` for the destination. If this is provided, then `label` will be ignored.

The label must be provided when used with the `NavigationRail`. When `NavigationRail.label_type=NavigationRailLabelType.NONE`, the label is still used for semantics, and may still be used if `NavigationRail.extended=True`.

### `padding`[​](#padding "Direct link to padding")

The amount of space to inset the destination item.

Padding is an instance of [`Padding`](/docs/reference/types/padding) class.

### `selected_icon`[​](#selected_icon "Direct link to selected_icon")

The [name](/docs/reference/icons) of alternative icon or `Control` displayed when this destination is selected.

Example with icon name:

```
selected_icon=ft.Icons.BOOKMARK
```

Example with Control:

```
selected_icon=ft.Icon(ft.Icons.BOOKMARK)
```

If this icon is not provided, the NavigationRail will display `icon` in either state.

### `selected_icon_content`[​](#selected_icon_content "Direct link to selected_icon_content")

An alternative icon `Control` displayed when this destination is selected.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`selected_icon`](#selected_icon) instead.**

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/navigationrail.md)

[

Previous

NavigationDrawer

](/docs/controls/navigationdrawer)[

Next

Information Displays

](/docs/controls/information-displays)

-   [Examples](#examples)
-   [`NavigationRail` properties](#navigationrail-properties)
    -   [`bgcolor`](#bgcolor)
    -   [`destinations`](#destinations)
    -   [`elevation`](#elevation)
    -   [`extended`](#extended)
    -   [`group_alignment`](#group_alignment)
    -   [`indicator_color`](#indicator_color)
    -   [`indicator_shape`](#indicator_shape)
    -   [`label_type`](#label_type)
    -   [`leading`](#leading)
    -   [`min_extended_width`](#min_extended_width)
    -   [`min_width`](#min_width)
    -   [`selected_index`](#selected_index)
    -   [`selected_label_text_style`](#selected_label_text_style)
    -   [`trailing`](#trailing)
    -   [`unselected_label_text_style`](#unselected_label_text_style)
-   [`NavigationRail` events](#navigationrail-events)
    -   [`on_change`](#on_change)
-   [`NavigationRailDestination` properties](#navigationraildestination-properties)
    -   [`icon`](#icon)
    -   [`icon_content`](#icon_content)
    -   [`indicator_color`](#indicator_color-1)
    -   [`indicator_shape`](#indicator_shape-1)
    -   [`label`](#label)
    -   [`label_content`](#label_content)
    -   [`padding`](#padding)
    -   [`selected_icon`](#selected_icon)
    -   [`selected_icon_content`](#selected_icon_content)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Information Displays | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/information-displays/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/information-displays/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/information-displays/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/information-displays/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   Information Displays

# Information Displays

[

## 🗃️ Ads

2 items

](/docs/controls/ads)

[

## 📄️ Canvas

Canvas is a control for drawing arbitrary graphics using a set of primitives or "shapes" such as line, arc, path and text.

](/docs/controls/canvas)

[

## 📄️ CircleAvatar

A circle that represents a user.

](/docs/controls/circleavatar)

[

## 📄️ CupertinoActivityIndicator

An iOS-style activity indicator that spins clockwise.

](/docs/controls/cupertinoactivityindicator)

[

## 📄️ Icon

Displays a Material icon.

](/docs/controls/icon)

[

## 📄️ Image

An image is a graphic representation of something (e.g photo or illustration).

](/docs/controls/image)

[

## 🗃️ Map

8 items

](/docs/controls/map)

[

## 📄️ Markdown

Control for rendering text in markdown format.

](/docs/controls/markdown)

[

## 📄️ Text

Text is a control for displaying text.

](/docs/controls/text)

[

## 📄️ ProgressBar

A material design linear progress indicator, also known as a progress bar.

](/docs/controls/progressbar)

[

## 📄️ ProgressRing

A material design circular progress indicator, which spins to indicate that the application is busy.

](/docs/controls/progressring)

[

## 📄️ WebView

Easily load web pages while allowing user interaction.

](/docs/controls/webview)

[

Previous

NavigationRail

](/docs/controls/navigationrail)[

Next

Ads

](/docs/controls/ads)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Ads | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/ads/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/ads/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/ads/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/ads/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
            -   [BannerAd](/docs/controls/bannerad)
            -   [InterstitialAd](/docs/controls/interstitialad)
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   Ads

On this page

# Ads

Displays ads in your app. Only available for mobile (Android and iOS) platforms.

Packaging

To build your Flet app that uses ads control add `--include-packages flet_ads` to `flet build` command, for example:

```
flet build apk --include-packages flet_ads
```

## Examples[​](#examples "Direct link to Examples")

-   Python

```
import flet as ftimport flet.ads as adsdef main(page: ft.Page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    id_interstitial = (        "ca-app-pub-3940256099942544/1033173712"        if page.platform == ft.PagePlatform.ANDROID        else "ca-app-pub-3940256099942544/4411468910"    )    id_banner = (        "ca-app-pub-3940256099942544/6300978111"        if page.platform == ft.PagePlatform.ANDROID        else "ca-app-pub-3940256099942544/2934735716"    )    def handle_interstitial_close(e):        nonlocal iad        print("InterstitialAd closed")        page.overlay.remove(e.control)        page.overlay.append(iad := get_new_interstitial_ad())        page.update()    def get_new_interstitial_ad():        return ads.InterstitialAd(            unit_id=id_interstitial,            on_load=lambda e: print("InterstitialAd loaded"),            on_error=lambda e: print("InterstitialAd error", e.data),            on_open=lambda e: print("InterstitialAd opened"),            on_close=handle_interstitial_close,            on_impression=lambda e: print("InterstitialAd impression"),            on_click=lambda e: print("InterstitialAd clicked"),        )    def display_new_banner_ad():        page.add(            ft.Container(                content=ads.BannerAd(                    unit_id=id_banner,                    on_click=lambda e: print("BannerAd clicked"),                    on_load=lambda e: print("BannerAd loaded"),                    on_error=lambda e: print("BannerAd error", e.data),                    on_open=lambda e: print("BannerAd opened"),                    on_close=lambda e: print("BannerAd closed"),                    on_impression=lambda e: print("BannerAd impression"),                    on_will_dismiss=lambda e: print("BannerAd will dismiss"),                ),                width=320,                height=50,                bgcolor=ft.colors.TRANSPARENT,            )        )    page.overlay.append(iad := get_new_interstitial_ad())    page.appbar = ft.AppBar(        adaptive=True,        title=ft.Text("Mobile Ads Playground"),        bgcolor=ft.colors.LIGHT_BLUE_300,    )    page.add(        ft.OutlinedButton("Show InterstitialAd", on_click=lambda e: iad.show()),        ft.OutlinedButton("Show BannerAd", on_click=lambda e: display_new_banner_ad()),    )ft.app(main)
```

![](https://flet.dev/docs/controls/ads/img/docs/controls/ads/ads.gif)

## Types[​](#types "Direct link to Types")

The following types are available:

-   [`InterstitialAd`](/docs/controls/interstitialad)
-   [`BannerAd`](/docs/controls/bannerad)

## Test Values[​](#test-values "Direct link to Test Values")

AdMob [provides](https://developers.google.com/admob/flutter/banner#always_test_with_test_ads) app and ad unit IDs for testing purposes.

-   AdMob app ID: `"ca-app-pub-3940256099942544~3347511713"`
-   `BannerAd.unit_id` on Android: `"ca-app-pub-3940256099942544/9214589741"`
-   `BannerAd.unit_id` on iOS: `"ca-app-pub-3940256099942544/2435281174"`
-   `InterstitialAd.unit_id` on Android: `"ca-app-pub-3940256099942544/1033173712"`
-   `InterstitialAd.unit_id` on iOS: `"ca-app-pub-3940256099942544/4411468910"`

Remember to replace these values with your own when you're ready to package your app.

## Packaging[​](#packaging "Direct link to Packaging")

The following are to be done when packaging an app that makes use of one of the above ad controls.

### Include Ads package[​](#include-ads-package "Direct link to Include Ads package")

Add `--include-packages flet_ads` to the `flet build` command, for example:

```
flet build apk --include-packages flet_ads
```

### Specify AdMob app ID[​](#specify-admob-app-id "Direct link to Specify AdMob app ID")

Specify your [AdMob app ID](https://support.google.com/admob/answer/7356431), without which your application might crash on launch.

You can specify the app ID in two ways:

-   In your `pyproject.toml` file:

```
# for Android[tool.flet.android.meta_data]"com.google.android.gms.ads.APPLICATION_ID" = "ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy"# for iOS[tool.flet.ios.info]GADApplicationIdentifier = "ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy"
```

-   In your build command from the terminal:

```
# for Androidflet build apk ... --android-meta-data com.google.android.gms.ads.APPLICATION_ID=ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy# for iOSflet build ipa ... --info-plist GADApplicationIdentifier=ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy
```

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/ads.md)

[

Previous

Information Displays

](/docs/controls/information-displays)[

Next

BannerAd

](/docs/controls/bannerad)

-   [Examples](#examples)
-   [Types](#types)
-   [Test Values](#test-values)
-   [Packaging](#packaging)
    -   [Include Ads package](#include-ads-package)
    -   [Specify AdMob app ID](#specify-admob-app-id)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  WebView | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/webview/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/webview/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/webview/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/webview/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   WebView

On this page

# WebView

Easily load web pages while allowing user interaction.

Work in progress

This control is supported on iOS, Android, MacOS and Web platforms only; Linux and Windows versions are in the development.

Packaging

To build your Flet app that uses `WebView` control add `--include-packages flet_webview` to `flet build` command, for example:

```
flet build apk --include-packages flet_webview
```

## Examples[​](#examples "Direct link to Examples")

A simple implementation that loads the [flet.dev](https://flet.dev) website:

```
import flet as ftdef main(page: ft.Page):    wv = ft.WebView(        url="https://flet.dev",        on_page_started=lambda _: print("Page started"),        on_page_ended=lambda _: print("Page ended"),        on_web_resource_error=lambda e: print("Page error:", e.data),        expand=True,    )    page.add(wv)ft.app(main)
```

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Set the background [color](/docs/reference/colors) of the WebView.

### `enable_javascript`[​](#enable_javascript "Direct link to enable_javascript")

Enable or disable the JavaScript execution on the page. Note that disabling the JavaScript execution on the page may result to unexpected web page behaviour.

Value is of type `bool`.

### `javascript_enabled`[​](#javascript_enabled "Direct link to javascript_enabled")

Enable or disable the JavaScript execution on the page. Note that disabling the JavaScript execution on the page may result to unexpected web page behaviour.

Value is of type `bool`.

**Deprecated in v0.25.0 and will be removed in v0.28.0. Use [`enable_javascript`](#enable_javascript) instead.**

### `prevent_link`[​](#prevent_link "Direct link to prevent_link")

Specify a prefix for links to prevent navigating or downloading.

Value is of type `str`.

### `url`[​](#url "Direct link to url")

Start the WebView by loading the `url` value.

Value is of type `str`.

## Methods[​](#methods "Direct link to Methods")

### `can_go_back()`[​](#can_go_back "Direct link to can_go_back")

Whether there's a back history item. Only for Android, iOS and macOS platforms.

Returns a `bool`.

### `can_go_forward()`[​](#can_go_forward "Direct link to can_go_forward")

Whether there's a forward history item. Only for Android, iOS and macOS platforms.

### `clear_cache()`[​](#clear_cache "Direct link to clear_cache")

Clears all caches used by the WebView. Only for Android, iOS and macOS platforms.

The following caches are cleared:

-   Browser HTTP Cache
-   [Cache API](https://web.dev/articles/cache-api-quick-guide) caches. Service workers tend to use this cache.
-   Application cache

### `clear_local_storage()`[​](#clear_local_storage "Direct link to clear_local_storage")

Clears the local storage used by the WebView. Only for Android, iOS and macOS platforms.

### `disable_zoom()`[​](#disable_zoom "Direct link to disable_zoom")

Disable zooming using the on-screen zoom controls and gestures. Only for Android, iOS and macOS platforms.

### `enable_zoom()`[​](#enable_zoom "Direct link to enable_zoom")

Enable zooming using the on-screen zoom controls and gestures. Only for Android, iOS and macOS platforms.

### `get_current_url()`[​](#get_current_url "Direct link to get_current_url")

Returns the current URL that the WebView is displaying or `None` if no URL was ever loaded. Only for Android, iOS and macOS platforms.

### `get_title()`[​](#get_title "Direct link to get_title")

The title of the currently loaded page. Only for Android, iOS and macOS platforms.

### `get_user_agent()`[​](#get_user_agent "Direct link to get_user_agent")

Gets the value used for the HTTP `User-Agent:` request header. Only for Android, iOS and macOS platforms.

### `go_back()`[​](#go_back "Direct link to go_back")

Go back in the history of the webview, if `can_go_back()` is `True`. Only for Android, iOS and macOS platforms.

### `go_forward()`[​](#go_forward "Direct link to go_forward")

Go forward in the history of the webview, if `can_go_forward()` is `True`. Only for Android, iOS and macOS platforms.

### `load_file()`[​](#load_file "Direct link to load_file")

Loads the provided local file. Only for Android, iOS and macOS platforms.

It has the following parameters:

-   `absolute_path`: The path to the local file to load.

### `load_html()`[​](#load_html "Direct link to load_html")

Loads the provided HTML string. Only for Android, iOS and macOS platforms.

It has the following parameters:

-   `html`: The HTML string to load.
-   `base_url` (optional): Used when resolving relative URLs within the HTML string.

### `load_request()`[​](#load_request "Direct link to load_request")

Makes an HTTP request and loads the response in the webview. Only for Android, iOS and macOS platforms.

It has the following parameters:

-   `url`: The URL of the webview to load.
-   `method`: The method of the request. Value is of type `WebviewRequestMethod` and defaults to `WebviewRequestMethod.GET`.

### `reload()`[​](#reload "Direct link to reload")

Reload the current URL. Only for Android, iOS and macOS platforms.

### `run_javascript()`[​](#run_javascript "Direct link to run_javascript")

Runs the given JavaScript in the context of the current page. Only for Android, iOS and macOS platforms.

It has the following parameters:

-   `value`: The JavaScript code to run.

### `scroll_by()`[​](#scroll_by "Direct link to scroll_by")

Scroll by the provided amount of webview pixels. Only for Android, iOS and macOS platforms.

It has the following parameters:

-   `x`: The amount of pixels to scroll by on the x-axis.
-   `y`: The amount of pixels to scroll by on the y-axis.

### `scroll_to()`[​](#scroll_to "Direct link to scroll_to")

Scroll to the provided position of webview pixels. Only for Android, iOS and macOS platforms.

It has the following parameters:

-   `x`: The x-coordinate of the scroll position.
-   `y`: The y-coordinate of the scroll position.

## Events[​](#events "Direct link to Events")

### `on_console_message`[​](#on_console_message "Direct link to on_console_message")

Fires when a console message is logged. Only for Android, iOS and macOS platforms.

Event handler argument is of type [`WebviewConsoleMessageEvent`](/docs/reference/types/webviewconsolemessageevent).

### `on_javascript_alert_dialog`[​](#on_javascript_alert_dialog "Direct link to on_javascript_alert_dialog")

Fires when a JavaScript alert dialog is about to be shown. Only for Android, iOS and macOS platforms.

Event handler argument is of type [`WebviewJavascriptEvent`](/docs/reference/types/webviewjavascriptevent).

### `on_page_ended`[​](#on_page_ended "Direct link to on_page_ended")

Fires when all the webview page loading processes are ended. Only for Android, iOS and macOS platforms.

### `on_page_started`[​](#on_page_started "Direct link to on_page_started")

Fires soon as the first loading process of the webview page is started. Only for Android, iOS and macOS platforms.

### `on_progress`[​](#on_progress "Direct link to on_progress")

Fires when the progress of the webview page loading is changed. Only for Android, iOS and macOS platforms.

### `on_scroll`[​](#on_scroll "Direct link to on_scroll")

Fires when the scroll position changes. Only for Android, iOS and macOS platforms.

Event handler argument is of type [`WebviewScrollEvent`](/docs/reference/types/webviewscrollevent).

### `on_url_change`[​](#on_url_change "Direct link to on_url_change")

Fires when the URL of the webview page is changed. Only for Android, iOS and macOS platforms.

### `on_web_resource_error`[​](#on_web_resource_error "Direct link to on_web_resource_error")

Fires when there is error with loading a webview page resource. Only for Android, iOS and macOS platforms.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/webview.md)

[

Previous

ProgressRing

](/docs/controls/progressring)[

Next

Buttons

](/docs/controls/buttons)

-   [Examples](#examples)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`enable_javascript`](#enable_javascript)
    -   [`javascript_enabled`](#javascript_enabled)
    -   [`prevent_link`](#prevent_link)
    -   [`url`](#url)
-   [Methods](#methods)
    -   [`can_go_back()`](#can_go_back)
    -   [`can_go_forward()`](#can_go_forward)
    -   [`clear_cache()`](#clear_cache)
    -   [`clear_local_storage()`](#clear_local_storage)
    -   [`disable_zoom()`](#disable_zoom)
    -   [`enable_zoom()`](#enable_zoom)
    -   [`get_current_url()`](#get_current_url)
    -   [`get_title()`](#get_title)
    -   [`get_user_agent()`](#get_user_agent)
    -   [`go_back()`](#go_back)
    -   [`go_forward()`](#go_forward)
    -   [`load_file()`](#load_file)
    -   [`load_html()`](#load_html)
    -   [`load_request()`](#load_request)
    -   [`reload()`](#reload)
    -   [`run_javascript()`](#run_javascript)
    -   [`scroll_by()`](#scroll_by)
    -   [`scroll_to()`](#scroll_to)
-   [Events](#events)
    -   [`on_console_message`](#on_console_message)
    -   [`on_javascript_alert_dialog`](#on_javascript_alert_dialog)
    -   [`on_page_ended`](#on_page_ended)
    -   [`on_page_started`](#on_page_started)
    -   [`on_progress`](#on_progress)
    -   [`on_scroll`](#on_scroll)
    -   [`on_url_change`](#on_url_change)
    -   [`on_web_resource_error`](#on_web_resource_error)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  Buttons | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/buttons/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/buttons/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/buttons/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/buttons/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   Buttons

# Buttons

[Live example](https://flet-controls-gallery.fly.dev/buttons)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/cupertino-button.png)

## Cupertino

](/docs/controls/cupertinobutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/cupertino-filled-button.png)

## CupertinoFilled

](/docs/controls/cupertinofilledbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/elevated-button.png)

## Elevated

](/docs/controls/elevatedbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/filled-button.png)

## Filled

](/docs/controls/filledbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/filled-tonal-button.png)

## Filled Tonal

](/docs/controls/filledtonalbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/floating-action-button.png)

## Floating Action

](/docs/controls/floatingactionbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/icon-button.png)

## Icon Button

](/docs/controls/iconbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/outlined-button.png)

## Outlined

](/docs/controls/outlinedbutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/popup-menu.gif)

## Popup Menu

](/docs/controls/popupmenubutton)

[![](https://flet.dev/docs/controls/buttons/img/docs/controls/button/text-button.png)

## Text Button

](/docs/controls/textbutton)

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/buttons.md)

[

Previous

WebView

](/docs/controls/webview)[

Next

CupertinoActionSheetAction

](/docs/controls/cupertinoactionsheetaction)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoContextMenuAction | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinocontextmenuaction/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinocontextmenuaction/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinocontextmenuaction/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinocontextmenuaction/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoContextMenuAction

On this page

# CupertinoContextMenuAction

An action button typically used in [`CupertinoContextMenu`](/docs/controls/cupertinocontextmenu).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/dialogs/cupertinocontextmenu)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    page.vertical_alignment = ft.MainAxisAlignment.CENTER    page.add(        ft.CupertinoContextMenu(            enable_haptic_feedback=True,            content=ft.Image("https://picsum.photos/200/200"),            actions=[                ft.CupertinoContextMenuAction(                    text="Action 1",                    is_default_action=True,                    trailing_icon=ft.Icons.CHECK,                    on_click=lambda e: print("Action 1"),                ),                ft.CupertinoContextMenuAction(                    text="Action 2",                    trailing_icon=ft.Icons.MORE,                    on_click=lambda e: print("Action 2"),                ),                ft.CupertinoContextMenuAction(                    text="Action 3",                    is_destructive_action=True,                    trailing_icon=ft.Icons.CANCEL,                    on_click=lambda e: print("Action 3"),                ),            ],        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinocontextmenuaction/img/docs/controls/cupertino-context-menu/basic-cupertino-context-menu.gif)

## Properties[​](#properties "Direct link to Properties")

### `content`[​](#content "Direct link to content")

The child control to be shown in this action button. In case both `text` and `content` are provided, then `content` will be used.

### `is_default_action`[​](#is_default_action "Direct link to is_default_action")

Whether this action should receive the style of an emphasized, default action.

### `is_destructive_action`[​](#is_destructive_action "Direct link to is_destructive_action")

Whether this action should receive the style of a destructive action.

### `text`[​](#text "Direct link to text")

The text to be shown in the button. In case both `text` and `content` are provided, then `content` will be used.

### `trailing_icon`[​](#trailing_icon "Direct link to trailing_icon")

An optional icon to display at the right of the `text` or `content` control.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when this action button is clicked.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinocontextmenuaction.md)

[

Previous

CupertinoButton

](/docs/controls/cupertinobutton)[

Next

CupertinoDialogAction

](/docs/controls/cupertinodialogaction)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`content`](#content)
    -   [`is_default_action`](#is_default_action)
    -   [`is_destructive_action`](#is_destructive_action)
    -   [`text`](#text)
    -   [`trailing_icon`](#trailing_icon)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  PolylineLayer | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/mappolylinelayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mappolylinelayer/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/mappolylinelayer/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/mappolylinelayer/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
        -   [Ads](/docs/controls/ads)
            
        -   [Canvas](/docs/controls/canvas)
        -   [CircleAvatar](/docs/controls/circleavatar)
        -   [CupertinoActivityIndicator](/docs/controls/cupertinoactivityindicator)
        -   [Icon](/docs/controls/icon)
        -   [Image](/docs/controls/image)
        -   [Map](/docs/controls/map)
            
            -   [CircleLayer](/docs/controls/mapcirclelayer)
            -   [MarkerLayer](/docs/controls/mapmarkerlayer)
            -   [PolygonLayer](/docs/controls/mappolygonlayer)
            -   [PolylineLayer](/docs/controls/mappolylinelayer)
            -   [RichAttribution](/docs/controls/maprichattribution)
            -   [SimpleAttribution](/docs/controls/mapsimpleattribution)
            -   [TileLayer](/docs/controls/maptilelayer)
            -   [TextSourceAttribution](/docs/controls/maptextsourceattribution)
        -   [Markdown](/docs/controls/markdown)
        -   [Text](/docs/controls/text)
        -   [ProgressBar](/docs/controls/progressbar)
        -   [ProgressRing](/docs/controls/progressring)
        -   [WebView](/docs/controls/webview)
    -   [Buttons](/docs/controls/buttons)
        
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Information Displays](/docs/controls/information-displays)
-   [Map](/docs/controls/map)
-   PolylineLayer

On this page

# PolylineLayer

A layer to display [`PolylineMarker`](#polylinemarker-properties)s.

## Examples[​](#examples "Direct link to Examples")

See [`Map`](/docs/controls/map) Control.

## `PolylineLayer` Properties[​](#polylinelayer-properties "Direct link to polylinelayer-properties")

### `polylines`[​](#polylines "Direct link to polylines")

A list of [`PolylineMarker`](#polylinemarker-properties)s to be displayed.

## `PolylineMarker` Properties[​](#polylinemarker-properties "Direct link to polylinemarker-properties")

A marker for the [`PolylineLayer`](#polylinelayer-properties).

### `border_color`[​](#border_color "Direct link to border_color")

The border color of this polyline.

### `border_stroke_width`[​](#border_stroke_width "Direct link to border_stroke_width")

The border stroke width of this polyline.

Defaults to `0.0` - disabled.

### `color`[​](#color "Direct link to color")

The color of this polyline marker.

### `colors_stop`[​](#colors_stop "Direct link to colors_stop")

A list of stops for gradient colors along the polyline.

### `coordinates`[​](#coordinates "Direct link to coordinates")

The coordinates (latitude and longitude) defining the polyline.

Value is a list with items of type [`MapLatitudeLongitude`](/docs/reference/types/maplatitudelongitude).

### `gradient_colors`[​](#gradient_colors "Direct link to gradient_colors")

A list of colors in case a gradient should get used.

### `stroke_cap`[​](#stroke_cap "Direct link to stroke_cap")

The stroke cap style of the polyline.

Value is of type [`StrokeCap`](/docs/reference/types/strokecap) and defaults to `StrokeCap.ROUND`.

### `stroke_join`[​](#stroke_join "Direct link to stroke_join")

The stroke join style of the polyline.

Value is of type [`StrokeJoin`](/docs/reference/types/strokejoin) and defaults to `StrokeJoin.ROUND`.

### `stroke_width`[​](#stroke_width "Direct link to stroke_width")

The stroke width of this polyline.

### `stroke_pattern`[​](#stroke_pattern "Direct link to stroke_pattern")

The stroke pattern of this polyline.

Value is of type [`StrokePattern`](/docs/reference/types/mapstrokepattern) and defaults to `SolidStrokePattern()`.

### `use_stroke_width_in_meter`[​](#use_stroke_width_in_meter "Direct link to use_stroke_width_in_meter")

A boolean value to indicate if the stroke width is in meters or pixels.

Defaults to `False` - pixels.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/mappolylinelayer.md)

[

Previous

PolygonLayer

](/docs/controls/mappolygonlayer)[

Next

RichAttribution

](/docs/controls/maprichattribution)

-   [Examples](#examples)
-   [`PolylineLayer` Properties](#polylinelayer-properties)
    -   [`polylines`](#polylines)
-   [`PolylineMarker` Properties](#polylinemarker-properties)
    -   [`border_color`](#border_color)
    -   [`border_stroke_width`](#border_stroke_width)
    -   [`color`](#color)
    -   [`colors_stop`](#colors_stop)
    -   [`coordinates`](#coordinates)
    -   [`gradient_colors`](#gradient_colors)
    -   [`stroke_cap`](#stroke_cap)
    -   [`stroke_join`](#stroke_join)
    -   [`stroke_width`](#stroke_width)
    -   [`stroke_pattern`](#stroke_pattern)
    -   [`use_stroke_width_in_meter`](#use_stroke_width_in_meter)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoActionSheetAction | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinoactionsheetaction/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoactionsheetaction/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinoactionsheetaction/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinoactionsheetaction/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoActionSheetAction

On this page

# CupertinoActionSheetAction

An action button typically used in [`CupertinoActionSheet`](/docs/controls/cupertinoactionsheet).

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinoactionsheetaction)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page):    page.horizontal_alignment = ft.CrossAxisAlignment.CENTER    def handle_click(e):        page.add(ft.Text(f"Action clicked: {e.control.content.value}"))        page.close(bottom_sheet)    action_sheet = ft.CupertinoActionSheet(        title=ft.Row([ft.Text("Title")], alignment=ft.MainAxisAlignment.CENTER),        message=ft.Row([ft.Text("Description")], alignment=ft.MainAxisAlignment.CENTER),        cancel=ft.CupertinoActionSheetAction(            content=ft.Text("Cancel"),            on_click=handle_click,        ),        actions=[            ft.CupertinoActionSheetAction(                content=ft.Text("Default Action"),                is_default_action=True,                on_click=handle_click,            ),            ft.CupertinoActionSheetAction(                content=ft.Text("Normal Action"),                on_click=handle_click,            ),            ft.CupertinoActionSheetAction(                content=ft.Text("Destructive Action"),                is_destructive_action=True,                on_click=handle_click,            ),        ],    )    bottom_sheet = ft.CupertinoBottomSheet(action_sheet)    page.add(        ft.CupertinoFilledButton(            "Open CupertinoBottomSheet",            on_click=lambda e: page.open(bottom_sheet),        )    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinoactionsheetaction/img/docs/controls/cupertino-action-sheet/basic-cupertino-action-sheet.png)

## Properties[​](#properties "Direct link to Properties")

### `content`[​](#content "Direct link to content")

The child control to be shown in this action button. In case both `text` and `content` are provided, then `content` will be used.

### `is_default_action`[​](#is_default_action "Direct link to is_default_action")

Whether this action should receive the style of an emphasized, default action.

Defaults to `False`.

### `is_destructive_action`[​](#is_destructive_action "Direct link to is_destructive_action")

Whether this action should receive the style of a destructive action.

Defaults to `False`.

### `text`[​](#text "Direct link to text")

The text to be shown in the button. In case both `text` and `content` are provided, then `content` will be used.

## Events[​](#events "Direct link to Events")

### `on_click`[​](#on_click "Direct link to on_click")

Fires when this action button is clicked.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinoactionsheetaction.md)

[

Previous

Buttons

](/docs/controls/buttons)[

Next

CupertinoButton

](/docs/controls/cupertinobutton)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`content`](#content)
    -   [`is_default_action`](#is_default_action)
    -   [`is_destructive_action`](#is_destructive_action)
    -   [`text`](#text)
-   [Events](#events)
    -   [`on_click`](#on_click)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

  CupertinoButton | Flet  

[Skip to main content](#__docusaurus_skipToContent_fallback)

⭐️ If you like Flet, give it a star on [GitHub](https://github.com/flet-dev/flet) and join the discussion on [Discord](https://discord.gg/dzWXP8SHG8).

[

![Flet Logo](https://flet.dev/docs/controls/cupertinobutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinobutton/img/logo.svg)

**Flet**](/)[Docs](/docs/)[Gallery](/gallery)[Roadmap](/roadmap)[Blog](/blog)

[](https://github.com/flet-dev/flet)

Search

[![Flet Logo](https://flet.dev/docs/controls/cupertinobutton/img/logo.svg)![Flet Logo](https://flet.dev/docs/controls/cupertinobutton/img/logo.svg)**Flet**](/)

-   [Introduction](/docs/)
-   [Getting started](/docs/getting-started/)
    
-   [Publishing Flet app](/docs/publish)
    
-   [Extending Flet](/docs/extend/built-in-extensions)
    
-   [Controls](/docs/controls)
    
    -   [Layout](/docs/controls/layout)
        
    -   [Navigation](/docs/controls/app-structure-navigation)
        
    -   [Information Displays](/docs/controls/information-displays)
        
    -   [Buttons](/docs/controls/buttons)
        
        -   [CupertinoActionSheetAction](/docs/controls/cupertinoactionsheetaction)
        -   [CupertinoButton](/docs/controls/cupertinobutton)
        -   [CupertinoContextMenuAction](/docs/controls/cupertinocontextmenuaction)
        -   [CupertinoDialogAction](/docs/controls/cupertinodialogaction)
        -   [CupertinoFilledButton](/docs/controls/cupertinofilledbutton)
        -   [CupertinoSegmentedButton](/docs/controls/cupertinosegmentedbutton)
        -   [CupertinoSlidingSegmentedButton](/docs/controls/cupertinoslidingsegmentedbutton)
        -   [ElevatedButton](/docs/controls/elevatedbutton)
        -   [FilledButton](/docs/controls/filledbutton)
        -   [FilledTonalButton](/docs/controls/filledtonalbutton)
        -   [FloatingActionButton](/docs/controls/floatingactionbutton)
        -   [IconButton](/docs/controls/iconbutton)
        -   [MenuItemButton](/docs/controls/menuitembutton)
        -   [OutlinedButton](/docs/controls/outlinedbutton)
        -   [PopupMenuButton](/docs/controls/popupmenubutton)
        -   [SegmentedButton](/docs/controls/segmentedbutton)
        -   [SubmenuButton](/docs/controls/submenubutton)
        -   [TextButton](/docs/controls/textbutton)
    -   [Input and Selections](/docs/controls/input-and-selections)
        
    -   [Dialogs, Alerts and Panels](/docs/controls/dialogs-alerts-panels)
        
    -   [Charts](/docs/controls/charts)
        
    -   [Animations](/docs/controls/animations)
        
    -   [Utility](/docs/controls/utility)
        
-   [Cookbook](/docs/cookbook/theming)
    
-   [Tutorials](/docs/tutorials)
    
-   [Reference](/docs/reference)
    

-   [](/)
-   [Controls](/docs/controls)
-   [Buttons](/docs/controls/buttons)
-   CupertinoButton

On this page

# CupertinoButton

An iOS-style button.

## Examples[​](#examples "Direct link to Examples")

[Live example](https://flet-controls-gallery.fly.dev/buttons/cupertinobutton)

### Basic Example[​](#basic-example "Direct link to Basic Example")

-   Python

```
import flet as ftdef main(page: ft.Page):    page.add(        ft.CupertinoButton(            content=ft.Text("Normal CupertinoButton", color=ft.CupertinoColors.DESTRUCTIVE_RED),            opacity_on_click=0.3,            on_click=lambda e: print("Normal CupertinoButton clicked!"),        ),        ft.CupertinoButton(            content=ft.Text("Filled CupertinoButton", color=ft.Colors.YELLOW),            bgcolor=ft.Colors.PRIMARY,            alignment=ft.alignment.top_left,            border_radius=ft.border_radius.all(15),            opacity_on_click=0.5,            on_click=lambda e: print("Filled CupertinoButton clicked!"),        ),        ft.ElevatedButton(            adaptive=True,  # a CupertinoButton will be rendered when running on apple-platform            bgcolor=ft.CupertinoColors.SYSTEM_TEAL,            content=ft.Row(                [                    ft.Icon(name=ft.Icons.FAVORITE, color="pink"),                    ft.Text("ElevatedButton+adaptive"),                ],                tight=True,            ),        ),    )ft.app(main)
```

![](https://flet.dev/docs/controls/cupertinobutton/img/docs/controls/cupertino-button/basic-cupertino-buttons.png)

## Properties[​](#properties "Direct link to Properties")

### `bgcolor`[​](#bgcolor "Direct link to bgcolor")

Button's background [color](/docs/reference/colors).

### `color`[​](#color "Direct link to color")

Button's text [color](/docs/reference/colors).

### `disabled_bgcolor`[​](#disabled_bgcolor "Direct link to disabled_bgcolor")

The background [color](/docs/reference/colors) of the button when it is disabled.

### `content`[​](#content "Direct link to content")

A Control representing custom button content.

### `icon`[​](#icon "Direct link to icon")

Icon shown in the button.

### `icon_color`[​](#icon_color "Direct link to icon_color")

Icon [color](/docs/reference/colors).

### `min_size`[​](#min_size "Direct link to min_size")

The minimum size of the button.

Defaults to `44.0`.

### `opacity_on_click`[​](#opacity_on_click "Direct link to opacity_on_click")

Defines the opacity of the button when it is clicked. When not pressed, the button has an opacity of `1.0`.

Defaults to `0.4`.

### `padding`[​](#padding "Direct link to padding")

The amount of space to surround the `content` control inside the bounds of the button.

### `text`[​](#text "Direct link to text")

The text displayed on a button.

### `tooltip`[​](#tooltip "Direct link to tooltip")

The text displayed when hovering the mouse over the button.

### `url`[​](#url "Direct link to url")

The URL to open when the button is clicked. If registered, `on_click` event is fired after that.

### `url_target`[​](#url_target "Direct link to url_target")

Where to open URL in the web mode.

Value is of type [`UrlTarget`](/docs/reference/types/urltarget) and defaults to `UrlTarget.BLANK`.

## Events[​](#events "Direct link to Events")

### `on_blur`[​](#on_blur "Direct link to on_blur")

Fires when the button loses focus.

### `on_click`[​](#on_click "Direct link to on_click")

Fires when a user clicks the button.

### `on_focus`[​](#on_focus "Direct link to on_focus")

Fires when the button receives focus.

### `on_long_press`[​](#on_long_press "Direct link to on_long_press")

Fires when a user long-presses the button.

[Edit this page](https://github.com/flet-dev/website/edit/main/docs/controls/cupertinobutton.md)

[

Previous

CupertinoActionSheetAction

](/docs/controls/cupertinoactionsheetaction)[

Next

CupertinoContextMenuAction

](/docs/controls/cupertinocontextmenuaction)

-   [Examples](#examples)
    -   [Basic Example](#basic-example)
-   [Properties](#properties)
    -   [`bgcolor`](#bgcolor)
    -   [`color`](#color)
    -   [`disabled_bgcolor`](#disabled_bgcolor)
    -   [`content`](#content)
    -   [`icon`](#icon)
    -   [`icon_color`](#icon_color)
    -   [`min_size`](#min_size)
    -   [`opacity_on_click`](#opacity_on_click)
    -   [`padding`](#padding)
    -   [`text`](#text)
    -   [`tooltip`](#tooltip)
    -   [`url`](#url)
    -   [`url_target`](#url_target)
-   [Events](#events)
    -   [`on_blur`](#on_blur)
    -   [`on_click`](#on_click)
    -   [`on_focus`](#on_focus)
    -   [`on_long_press`](#on_long_press)

Docs

-   [Introduction](/docs)
-   [Controls reference](/docs/controls)

Community

-   [Discord](https://discord.gg/dzWXP8SHG8)
-   [Stack Overflow](https://stackoverflow.com/questions/tagged/flet)
-   [X](https://x.com/fletdev)
-   [Blusky](https://bsky.app/profile/fletdev.bsky.social)

More

-   [Blog](/blog)
-   [GitHub](https://github.com/flet-dev/flet)
-   [Support](/support)

Legal

-   [Privacy policy](/privacy-policy)

Copyright © 2025 Appveyor Systems Inc. Built with Docusaurus.
---------------------------------------------------

