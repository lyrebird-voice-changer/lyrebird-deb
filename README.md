# lyrebird-deb

Debian package environment for [Lyrebird voice changer](https://github.com/lyrebird/lyrebird-voice-changer).

The code in this repo is only updated on every release, to find development builds of Lyrebird see the [original repo](https://github.com/lyrebird/lyrebird-voice-changer).

## Archived

As of December 2023, Lyrebird has ceased development and is now archived. Thank you to our users and contributors.

As an alternative, we recommend looking at [Easy Effects](https://github.com/wwmm/easyeffects).

## Files

  * `lyrebird/usr/bin/lyrebird` - Bootstrap script that launches `share/lyrebird/app.py`, does not need to be modified across versions.
  * `lyrebird/usr/share/applications/lyrebird.desktop` - Desktop file that needs the version number incremented across versions.
  * `lyrebird/usr/share/lyrebird` - The main directory containing Lyrebird app code from the repo. `app.py` should reside in the root of this file. Be careful not to include `__pycache__` directories when building a `.deb`.

## Build

  1. Copy the essential files from the main Lyrebird repo to `lyrebird/usr/share/lyrebird`
  2. Read the Files section and ensure all version numbers have been updated.
  3. Place the main repo code (cleanup needed) in `lyrebird/usr/share/lyrebird`.
  4. Run `build.sh`, `lyrebird.deb` will be built.

## Naming Scheme

`lyrebird_x.x.x-x.deb`

