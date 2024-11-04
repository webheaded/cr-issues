# Comic Releases - Kitchen Sink

## Overview

**Comic Releases - Kitchen Sink** is a WordPress plugin built to manage, display, and track comic book release data. Designed for both public use and administrative ease, this plugin connects with a separate database to serve real-time information about upcoming releases and user watchlists. It also features robust tools for querying external APIs to keep release information up-to-date.

This repository tracks **issues, enhancements, and bugs** related to Comic Releases - Kitchen Sink. We welcome reports of issues and contributions from the community!

## How to Report Issues

If you encounter bugs, have feature requests, or want to contribute, please open an issue here with as much detail as possible:
- Steps to reproduce the bug
- Expected vs. actual behavior
- Screenshots, if applicable
- Any error messages or logs

## Features

### Public Features

- **Database Integration**  
  Connects to a separate (non-WordPress) database with tables:
  - `upcoming_collected` for upcoming releases
  - `watchlist2` for users’ watchlisted items

- **DataTables Integration**  
  Renders both main and watchlist tables on the site with extensive DataTables options via shortcodes:
  - `[crTable]` for the main table
  - `[watchlist2]` for the user-specific watchlist

- **User Watchlist**  
  Allows users to add items to a personalized watchlist and track various attributes, such as status, notes, and more.

### Admin Features

- **Database Management**  
  Admin pages to manage book records, including AJAX-powered in-line editing, plus the ability to add new books using the ISBN.

- **API Integration**  
  Tools for querying Penguin Random House, Diamond, and Lunar Distribution APIs to automatically populate release data.

- **Solicit Formatting**  
  Pulls book data from the PRH API, offering a formatted text box for solicitations.

- **Release Updater Scripts**  
  Scripts to manually update release data:
  - **PRH Updater** - Pulls JSON data for Penguin Random House releases.
  - **Diamond Updater** - Pulls JSON data for Diamond publisher releases.
  - **Lunar Updater** - Scrapes Lunar Distribution's site for Image publisher releases.

### Code Overview

This plugin’s functionality is primarily divided between two main classes:

#### `BookDatabase` Class
Handles all database interactions and provides methods to:
- Retrieve books with filters, watchlist status, and linked previews or affiliate links.
- Manage user watchlists.
- Generate dynamic SQL conditions, convert ISBN formats, and handle publisher links.

#### `APIHandler` Class
Manages API interactions with:
- Methods to pull and parse data from PRH, Diamond, and Lunar APIs.
- Discord webhook integration to notify users of updates.
  

Thank you for your interest and contributions!
