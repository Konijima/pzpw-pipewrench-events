# PipeWrench-Events (For PZPW)

[![Build](https://github.com/Konijima/pzpw-pipewrench-events/actions/workflows/Build.yml/badge.svg)](https://github.com/Konijima/pzpw-pipewrench-events/actions/workflows/Build.yml)

## Description
PipeWrench-Events is an extension for the PipeWrench library, packaging Project Zomboid's events in an API that takes advantage of the TypeScript environment. [EventEmitters](https://github.com/asledgehammer/PipeWrench-Events/blob/398ab440505416eb250f430c8776969a4ec8bd45/PipeWrench-Events.d.ts#L74-L89) and [EventConsumers](https://github.com/asledgehammer/PipeWrench-Events/blob/398ab440505416eb250f430c8776969a4ec8bd45/PipeWrench-Events.d.ts#L292-L298) , are provided as events and their associated consumer types for listeners.

## Custom EventEmitters
```ts
import * as Events from 'PipeWrench-Events';

// Example consumer type
export type MusicTrackUpdateListener = (
    track: string,
    volume: number
) => void;

// Example EventEmitter.
const MusicTrackUpdate = new Events.EventEmitter<MusicTrackUpdateListener>('MusicTrackUpdate');

// Example implementation.
MusicTrackUpdate.addListener((track: string, volume: number) => {
  print(`Playing Track: ${track} (Volume: ${volume})`);
});
```

## Setup
- (This library is installed in [PipeWrench-Template](https://github.com/asledgehammer/PipeWrench-Template))

## Notes
- The documentation is transcribed from [pzwiki.net](https://pzwiki.net/wiki/Modding:Lua_Events)

# Support

![](https://i.imgur.com/ZLnfTK4.png)

## Discord Server
https://discord.gg/u3vWvcPX8f

If you like what I do and helped your community a lot, feel free to buy me a coffee!
https://ko-fi.com/jabdoesthings
https://www.paypal.com/paypalme/JabJabJab
