---
description: >-
  How to use MMW4CC to make charts for Project Sekai (extended features
  included). Last update: September 29th, 2024
icon: newspaper
---

# Usage Guide (MMW4CC)

## Quick Overview

This is the place where chart designers ("charters") spend most of their time working on a chart after adjusting timing settings. Notes, Hi-speed, and other aspects of Project Sekai chart design elements (with extended features...) can be inspected in this window.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>MMW4CC window</p></figcaption></figure>

{% hint style="warning" %}
The sub-window in the image above is organized for clarity. **This is NOT what it will look like when opening MMW4CC for the first time.**
{% endhint %}

***

## Loading and Saving Charts

* MMW4CC can open, edit, and save MikuMikuWorld for Chart Cyanvas Score files `*.ccmmws`and Universal Sekai Chart files `*.usc`.
* Load charts by selecting `File > Open` from the menu bar
* Save the current chart into MMW4CC Score file by selecting `File > Save`
* Export the current chart into `*.usc` file by selecting `File > Export USC`
  * &#x20;Export the chart into `*.sus` via [keyboard shortcuts](usage-guide-mmw4cc.md#shortcut-configuration-key-config) (by default it's `Ctrl+E`)

***

## Loading Chart Music

In the `Chart Properties` window under `Audio`, load a music file by selecting `...` next to `Music File` or typing in the path to the file. You can also adjust the music offset. The values are in milliseconds (1/1000th of a second). A higher value will start the music later and a lower value will start it sooner. The supported formats are:

* MPEG Audio Layer III (\*.mp3)
* Waveform Audio File (\*.wav)
* Free Lossless Audio Codec (\*.flac)
* Ogg Vorbis (\*.ogg)

A waveform will be displayed when the music is loaded which can help with syncing music to the notes. Selecting `View > Show Waveform` will toggle the waveform's visibility.

***

## Timeline

* Scroll through the timeline using the mouse wheel or the scrollbar
* Hold `Shift` while scrolling will change the scrolling speed. Scrolling speeds can be adjusted in `Settings > Timeline`
* Hold `Ctrl` while scrolling: Zoom in and out.
* During playback, the timeline scrolls to follow the scrollbar (<mark style="color:red;">red arrow bar</mark>).\
  To change this behavior to scroll after the cursor has passed the screen, uncheck `Cursor Auto Scroll` under `View` in the menu bar or through `Settings > Timeline`
* Hold step outlines can be turned off by unchecking `View > Show Step Outlines`
* The timeline background can be turned off or changed under `Settings > Timeline > Background`

***

## Timeline Tools

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>Timeline Tool, shown at the top</p></figcaption></figure>

Different actions can be invoked depending on the timeline tool selected. From left to right they are...

<table data-full-width="false"><thead><tr><th width="72" data-type="files">Icon</th><th width="151">Tool</th><th width="361">Description</th><th>Default Shortcut</th></tr></thead><tbody><tr><td><a href="../.gitbook/assets/timeline_select.png">timeline_select.png</a></td><td>Select</td><td><mark style="color:blue;"><code>Left Click</code></mark> or <mark style="color:blue;"><code>Drag</code></mark>: Select notes.<br><mark style="color:blue;"><code>Ctrl + Left Click</code></mark>: Append selection.<br><mark style="color:blue;"><code>Alt + Left Click</code></mark>: Subtract selection.<br>- Click anywhere else in the timeline to deselect.</td><td><mark style="color:blue;"><code>1</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_tap.png">timeline_tap.png</a></td><td>Tap</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a tap note.</td><td><mark style="color:blue;"><code>2</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_hold (2).png">timeline_hold (2).png</a></td><td><a href="../making-a-chart/creating-slide-shapes.md">Hold</a></td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a hold note.<br><mark style="color:blue;"><code>Left Drag</code></mark>: Place a holdStart point, release to place the holdEnd point.<br>- Clicking on a hold or hold step note will cycle the note's ease type.</td><td><mark style="color:blue;"><code>3</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_hold_step_normal (2).png">timeline_hold_step_normal (2).png</a><a href="../.gitbook/assets/timeline_hold_step_hidden.png">timeline_hold_step_hidden.png</a><a href="../.gitbook/assets/timeline_hold_step_skip (1).png">timeline_hold_step_skip (1).png</a></td><td><a href="../making-a-chart/creating-slide-shapes.md">Hold Step</a></td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a hold step note.<br>- Cycles the hold step's type when clicked on the hold step note.<br>- Cycles the hold step's type when clicking the icon or using the keyboard shortcut.</td><td><mark style="color:blue;"><code>4</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_flick_default.png">timeline_flick_default.png</a><a href="../.gitbook/assets/timeline_flick_left.png">timeline_flick_left.png</a><a href="../.gitbook/assets/timeline_flick_right.png">timeline_flick_right.png</a></td><td>Flick</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a flick note.<br>- Cycles the flick's direction when clicked on the flick note.<br>- Cycles the current flick's direction when clicking the icon or using the keyboard shortcut.</td><td><mark style="color:blue;"><code>5</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_critical.png">timeline_critical.png</a></td><td>Critical</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a critical note.<br>- Toggles between normal and critical if clicked on a note.</td><td><mark style="color:blue;"><code>6</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_trace.png">timeline_trace.png</a></td><td>Trace</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a trace note.<br>- Toggles between normal and trace if clicked on a note.</td><td><mark style="color:blue;"><code>7</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_guide_green_out.png">timeline_guide_green_out.png</a></td><td>Guide Notes</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a guide note.<br><mark style="color:blue;"><code>Left Drag</code></mark>: Place a guideStart point, release to place the guideEnd point.<br>- Cycles the guide's color when clicked on the guide note.<br>- Cycles the current guide's color when clicking the icon or using the keyboard shortcut.</td><td>None</td></tr><tr><td><a href="../.gitbook/assets/timeline_damage.png">timeline_damage.png</a></td><td>Damage</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a damage note.<br>- Toggles between normal and damage if clicked on a note.</td><td>None</td></tr><tr><td><a href="../.gitbook/assets/timeline_bpm.png">timeline_bpm.png</a></td><td>BPM</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a BPM change event.<br>- Click the BPM to change the value.</td><td><mark style="color:blue;"><code>8</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_time_signature.png">timeline_time_signature.png</a></td><td>Time Signature</td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a time signature change event.<br>- Click the time signature to change the value.</td><td><mark style="color:blue;"><code>9</code></mark></td></tr><tr><td><a href="../.gitbook/assets/timeline_hi_speed.png">timeline_hi_speed.png</a></td><td><a href="../making-a-chart/hi-speed.md">Hi-Speed</a></td><td><mark style="color:blue;"><code>Left Click</code></mark>: Place a hi-speed change event.<br>- Click the hi-speed to change the value.</td><td><mark style="color:blue;"><code>0</code></mark></td></tr></tbody></table>

{% hint style="info" %}
You can change keyboard shortcuts by going to `Settings > Key Config.`
{% endhint %}

***

## Placing and Modifying Notes

* Place notes by selecting the appropriate timeline tool and left clicking on the timeline
* Select a note and drag it to move it around
* Select and drag either the left or right edges of the note to resize it

### Timeline Menu

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption><p>TImeline Menu</p></figcaption></figure>

* **Playback buttons:** Previous Measure, Stop, Play/Pause, Next Measure
  * **Stop:** Teleport to measure 0.
* **Divisions:** Select the desired note division from the division select menu at the bottom. To use a custom division, input a number between 4 and 1920
* **Snap Mode:** Changes how the notes should be 'snapped' at when moving one or multiple notes at a different specified division.&#x20;
  * Relative Snap: Do not snap the notes. Move it like how it is.
  * Absolute Snap: Snap a note to a desired division. If selecting multiple notes, it will move until one of the multiple notes is snapped.
  * Individual Absolute Snap: Snap all selected notes to a desired division.
* **Go to Measure:** Input a positive number to teleport to that measure in the timeline
* **Timeline Speed:** Change the speed in the timeline to 25%, 50%, 75%, 100%.
* **Zoom:** Change how far the note appears in the timeline. Use `Ctrl+Click` to edit the value.

### Guide Notes

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption><p>Guide Notes</p></figcaption></figure>

Guide notes are similar to regular slides with a few differences:

* They do not count towards combo
* The steps always use the step type `Hidden`
* They fade out as they approach the end point

`(*.sus only)` Place a step near the end point to control the amount of fade. The closer the step is to the end point, the less fade there will be.

### Hidden Hold Point

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption><p>Hidden Hold Point</p></figcaption></figure>

The start and end points of a hold can be hidden. A hidden point does not require tapping at the start or releasing at the end. It will also not count towards combo. To create a hidden point:

* Select the hold points to hide/unhide
* From the context menu under `Hold Type` select either `Normal` or `Hidden`

***

## Context Menu

Right-click anywhere on the timeline to open the context menu. Most of the functions are self-explanatory and can be used as keyboard shortcuts.

* **Shrink Up:** Places the selected notes 1 tick apart starting from the latest note
* **Shrink Down:** Places the selected notes 1 tick apart starting from the earliest note
* **Connect Holds:** Merges two holds together
* **Split Hold:** Split a hold note to two separate hold notes
* **Repeat Hold Mids:** Insert selected Hold Mids at the next division repeatedly (you can make zigzag hold note easily with this tool)
* **Convert Hold to Traces:**
  * _Add Traces for Hold:_ Add trace notes in-between the hold points. The number of traces can be changed depending on the number of measure divisions specified.
  * _Convert Hold to Traces:_ Turn the holds into trace notes. The number of traces can be changed depending on the number of measure divisions specified. <mark style="color:red;">(Note: at this time, the hold flick at the end is only converted to normal trace note.)</mark>
* **Interpolate Hi-Speeds:** Insert Hi-Speeds in-between the selected Hi-Speed and changes value in a linear interpolation. The more divisions selected, the 'smoother' the speed change.

***

## Adjusting Settings

### Language

Currently, English and other 5 languages can be selected. Selecting `Auto` will detect the current system's language and choose the appropriate language. If the system's language is not supported by the program, it will default to English.

### Auto Save

Just like the original MikuMikuWorld, MMW4CC supports auto save. It is enabled by default. The interval (in minutes) and maximum number of auto save entries can be configured. Auto saved charts are located in the `auto_save` folder.

### Timeline Settings

* The timeline width can be changed from the `Lane Width` setting under Timeline
* A separate size for notes can be applied by unchecking `Match notes size to timeline width` and selecting the desired note size
* Checking `Return to last tick on Pause` will return the cursor to the last selected division upon pausing

### Shortcut Configuration (Key Config)

* Several actions be assigned a keyboard shortcut
* If multiple shortcuts are assigned to an action, the topmost one will be displayed in menus
* Add more shortcuts if needed by selecting `Add`. Up to 4 shortcuts can be created per action

***

## Lane Extension

An extended feature for [Chart Cyanvas](https://cc.sevenc7c.com). Extended lanes enable the notes to be able to be placed outside the initial boundary of the Project Sekai playfield.\
\
It can be adjusted in the `Chart Properties > Metadata` section. Up to 100 extended lanes can be adjusted, though the notes can be placed infinitely further away with the use of [Note Properties](usage-guide-mmw4cc.md#note-properties).

<figure><img src="../.gitbook/assets/image (4) (1).png" alt="" width="563"><figcaption><p>Lane Extension</p></figcaption></figure>

***

## Note Properties

When selecting **ONLY&#x20;**_**ONE**_ note (tap, holdStart, holdEnd, flick, etc.), the metadata or configuration information about the note is shown at the note properties sub-window. The metadata can include details such as where the note is, type of notes, lane and width, and more.\
\
Here, you can adjust the value in each metadata in a very customizable way, with an additional feature of adjustable lane/width note value in decimals (e.g. 5.50 width).

<figure><img src="../.gitbook/assets/image (18).png" alt="" width="375"><figcaption><p>Note properties for a tap note</p></figcaption></figure>

***

## Layers

You can use layers to make notes and hi-speed in a "different playing field".

<figure><img src="../.gitbook/assets/image (22).png" alt="" width="154"><figcaption><p>Layers</p></figcaption></figure>

### Create a Layer

* Click on `Create Layer` in the Layers sub-window. Input a name.

### Move a Layer

* Use :arrow\_up: and :arrow\_down: to move a layer.

### Hide/Show notes in a Layer

* Use the eye icon to hide/show notes.

### Place notes in another Layer

* When you have 2+ layers, click on the layer you want to work with.

### Move notes to another Layer

<figure><img src="../.gitbook/assets/image (21).png" alt="" width="291"><figcaption><p>Move notes to another layer</p></figcaption></figure>

* <mark style="color:blue;">`Right Click`</mark> on the notes you want to select, then select `Layer` and click the layer you want to move notes to.

### Merging a Layer

* Click on the :arrow\_heading\_down: to merge the layer into a layer under it.

{% hint style="warning" %}
You cannot remove a layer the normal way. To "delete" it, move the notes from a layer you want to "delete", then merge it.
{% endhint %}

***

## Note Presets

<figure><img src="../.gitbook/assets/image (15).png" alt="" width="266"><figcaption><p>Note Preset</p></figcaption></figure>

### Create a Preset

* Select the notes and/or hi-speed events desired then click on `Create Preset` in the Presets sub-window. Input a name and optionally a description.

### Insert a Preset

* Click on any of the presets available in the presets window, move the cursor to the desired position and click to place down the notes. You can search for a specific preset by typing its name in the search box

### Deleting Presets

* Click on the trash icon next to the preset button to remove it

***
