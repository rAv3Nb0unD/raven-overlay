# raven-overlay

I use the repo by pulling it as a folder named `local`. You might want to see metadata and profiles folders to change repo name to `raven-overlay` or whatever you want.

This repository is for some programs that are not in any of the additional overlays in eselect repository.

## Important
KEYWORDS here is `amd64`, not `~amd64`, because i trust this repo and believe it is consistent and not breaking my system.

## Packages info
- `x11-terms/termius` - it will definitely break when a new upstream version comes out. This is because termius download does not provide package version choices, it gives only latest. The thing the overlay user will have to do is to create a new termius-<version>.ebuild and run ebuild manifest:
```bash
cp termius-<oldver>.ebuild termius-<newver>.ebuild
ebuild termius-<newver>.ebuild manifest

emerge -av x11-terms/termius
```
