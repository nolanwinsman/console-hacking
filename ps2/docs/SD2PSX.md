# SD2PSX Documentation

This documentation covers everything you should need to know with using this microSD card with this SD2PSX memory card.

Most of the information I got on this memory card is from this Youtube video [Plug and Play Raspberry Pi Makes PlayStation 2 Homebrew Way EASIER](https://www.youtube.com/watch?v=mdxDRtfEXNg)

## Why SD2PSX?

For a SLiMS PS2, the most convenient way to boot into a mod menu and boot backup games required three memory cards

1. Memory Card to boot into the hacked software
2. Memory Card to store game saves
3. Memory Card with microSD card slot to store game backups

This in my opinion is a massive pain. That is why some clever engineers solved this with the SD2PSX which handles all three functionalities in one memory card.

## Important Notes on Using This SD2PSX

1. I set this device up to work in memory card slot 1 (left). It probably mostly works in slot 2, but some paths are specifically for `mc0:` and might cause issues if in slot 2 (`mc1:`)
2. I configured this device to automatically boot into OPL (Open-PS2-Loader) instead of FreeMC Boot. OPL is the games launcher and FreeMCBoot is like the homebrew menu. If you need to access FreeMCBoot, hold **R1** on your controller when turning on the console.
3. Some people say that loading games from a microSD card through the PS2's memory card slot can yield poor performance. I have not experience this but it is a possibility.

## Copying Game Saves to SD2PSX

This Youtube video kind of explains how to do this [MemCard Pro 2 Setup Guide - Setup/WiFi/Cloud Saves/FMCB/Saves/PS3/Game Storage!](https://www.youtube.com/watch?v=UZLnDGFXMWk) starting at **16.00 minutes**.

To be honest this is kind of a pain to do. I pre-loaded all the games included in this microSD card with 100% complete save files but if you want your own saves, try to follow the guide above or just follow these high level steps. I don't love this guide since it
mostly uses one giant virtual memory card when the SD2PSX is better designed to have a single virtual memory card per game.

## [Game Art](game_art_list.md)

Simple breakdown of how to add game box art, what game box art is already there and how it works. Long Story short you should not need to add the `.png` box art files for any games listed in the markdown file above.

## How to Add More Games

Assuming you read through the **Game Art** documentation for how to make sure the games have the nice box art, adding a game is easy.

Just copy any DVD based games inside the `DVD/` folder and `CD` based games into the `CD` folder. Generally any game less than or equal to 700MB is CD based and any game greater than 700MB is generally DVD based. Or you can Google this.

If you want to make game backups using your own discs... You're on your own with that one. I don't know how to do that.

## Files

These are the relevant files/folders inside this microSD card.

| Filename     | Description                |
| ------------ | -------------------------- |
| ART/         | Game Box Art               |
| CD/          | CD based PS2 game backups  |
| docs/        | Documentation folder       |
| DVD/         | DVD based PS2 game backups |
| MemoryCards/ | Virtual Memory Cards       |
| README.md    | this file                  |
| sd2psx.uf2   | SD2PSX firmware            |


## Relevant Repos

