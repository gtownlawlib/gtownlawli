# gtownlaw.li Link Shortener

## About

gtownlaw.li is a lightweight Drupal 7.x-based application for custom link shortening built around the shURLy contrib module (https://www.drupal.org/project/shurly).

gtownlaw.li was originally developed by the Electronic Resources and Services department at the Georgetown Law Library in August 2016. The project had two primary goals:

1. Provide a branded link shortener (gtownlaw.li) for the library to assist with marketing campaigns.
2. Eliminate the need for a hosted solution—such as bit.ly—that would allow a third party company to maintain logs of users/patrons accessing library content.

Version 1.0 is a bare-bones application with no content types or nodes, only short URL translation. The site's UI uses the Bootstrap contrib theme with no code modifications. All UI customizations were accomplished through the theme settings backend.

## Dependencies

The application relies on the following contrib modules for site functionality:

- Chaos Tools - https://www.drupal.org/project/ctools
- shURLY - https://www.drupal.org/project/shurly
- Token - https://www.drupal.org/project/token
- Views - https://www.drupal.org/project/views

In addition, the following themes are utilized by default:

- Bootstrap (Front End) - https://www.drupal.org/project/bootstrap
- Ember (Admin) - https://www.drupal.org/project/ember

All dependencies listed above are included with this install profile.

Most users will likely want to include an admin toolbar of some sort, either Drupal Core's included toolbar or one of the following:

- Administration Menu - https://www.drupal.org/project/admin_menu
- Navbar - https://www.drupal.org/project/navbar

Neither of these toolbars are included with this profile.

## Usage

The install profile should set the site front page to shURLy's "Create URL" form, which presents users with two fields, one for an original long URL and another for an optional custom short URL string (the portion after your link shortener's domain). Users need not enter a short URL string; if left blank the application will generate one automatically.

The application includes two views courtesy of the shURLy module:

1. My URLs - A list of all short URLs the current user has created.
2. Short URLs - A list of all short URLs created on the site by all users. (Available only to users with Administer Short URLs permission.)

For system integrity, short URLs are not editable once they've been created, and all previously created short URL strings will continue to be considered "in-use" and unavailable for re-use, even if deleted from the application.

The shURLy module also includes a javascript bookmarket that users can place in their browser bookmarks bar for quick short URL creation.

## Maintainers

Current maintainer: Tom Boone, Associate Law Librarian for Electronic Resources and Services, Georgetown Law Library

This project has been sponsored by the Georgetown Law Library.