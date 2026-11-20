# Changelog

All notable changes to VVulfmann's Playlist Randomizer. Each release's notes on GitHub (and on the Foundry
package listing) come from its section here.

## 0.2.4

### Fixed

- **No more hitch when a randomized sound plays.** Foundry used to stutter for a moment every time a randomized
  sound started or finished, because each one redrew the entire Playlists sidebar for every connected player. Now
  only the row for that sound changes, so play stays smooth even in worlds with a large playlist library.
- With several players connected, a randomized sound finishing now sends far fewer repeated updates: once one
  player's update arrives, the others stop sending theirs.

### Changed

- Verified on Foundry VTT v14 build 370.

## 0.2.3

### Fixed

- Deleting or editing a playlist in a compendium no longer stops randomized sounds in a world playlist that shares
  its IDs (for example, one imported from that compendium).

## 0.2.2

### Changed

- Simpler README focused on how the module behaves.

## 0.2.1

### Changed

- New module description.

## 0.2.0

### Added

- World settings under **Configure Settings**: the **Default Frequency** for new randomized sounds, and the shortest
  and longest wait for **Often**, **Sometimes** and **Seldom**.
- Changing a wait range re-rolls the waits already in progress at that frequency.

### Changed

- Default waits are now Often 15–30 s, Sometimes 30–60 s, Seldom 1–2 min.

## 0.1.1

- First release: **Randomize** playback for playlist sounds. A randomized sound plays, waits a random time, then
  plays again, in every playlist mode.
