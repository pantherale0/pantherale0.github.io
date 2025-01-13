## Controlling Your Arcam Solo

After configuring the Arcam Solo integration, a remote entity will be created in Home Assistant. This entity allows you to control your Arcam Solo using various commands. You can access these commands through the Home Assistant UI, automations, or scripts.

**Accessing the Remote Entity:**

The remote entity will have a name similar to `remote.your_arcam_solo_name`, where `your_arcam_solo_name` is the name you gave the integration during configuration. You can find this entity in the Developer Tools -> States menu in Home Assistant.

**Available Commands:**

The following commands are available for the Arcam Solo remote entity, corresponding directly to keys in the `IR_COMMAND_CODES`:

| Command             | Description                                   |
|----------------------|-----------------------------------------------|
| `standby_off`           | Turns the Arcam Solo on. |
| `standby_on`          | Turns the Arcam Solo off.|
| `volume_up`         | Increases the volume.                           |
| `volume_down`     | Decreases the volume.                          |
| `mute_toggle`       | Toggles the mute state.                          |
| `src_tv`            | Selects the TV input source.                    |
| `src_av`            | Selects the AV input source.                    |
| `src_dab`           | Selects the DAB input source.                   |
| `src_tape`          | Selects the Tape input source.                  |
| `src_cd`            | Selects the CD input source.                    |
| `src_aux`           | Selects the Aux input source.                   |
| `src_am`            | Selects the AM input source.                    |
| `src_fm`            | Selects the FM input source.                    |
| `bass_plus`         | Increases the bass.                             |
| `bass_minus`        | Decreases the bass.                            |
| `treble_plus`       | Increases the treble.                           |
| `treble_minus`      | Decreases the treble.                          |
| `balance_right`     | Shifts balance to the right.                   |
| `balance_left`      | Shifts balance to the left.                    |
| `display_brightness`| Adjusts display brightness.                     |
| `navigate_right`    | Navigates right in menus.                      |
| `navigate_left`     | Navigates left in menus.                       |
| `menu`              | Opens the menu.                                |
| `navigate_down`     | Navigates down in menus.                       |
| `navigate_up`       | Navigates up in menus.                         |
| `ok`                | Confirms a selection in menus.                 |
| `alarm_1_toggle`    | Toggles alarm 1.                             |
| `alarm_2_toggle`    | Toggles alarm 2.                             |
| `alarm_3_toggle`    | Toggles alarm 3.                             |
| `alarm_4_toggle`    | Toggles alarm 4.                             |
| `snooze`            | Activates snooze function.                     |
| `sleep`             | Activates sleep timer.                         |
| `mute_on`           | Turns mute on.                                |
| `mute_off`          | Turns mute off.                               |
| `standby_off`       | Turns the unit on.                             |
| `standby_on`        | Turns the unit off.                            |
| `cd_play`           | Plays the CD.                                 |
| `cd_pause`          | Pauses the CD.                                |
| `cd_stop`           | Stops the CD.                                 |
| `cd_eject`          | Ejects the CD.                                |
| `cd_track_next`     | Skips to the next track on the CD.              |
| `cd_track_previous` | Skips to the previous track on the CD.           |
| `cd_scan_back`      | Scans backward on the CD.                      |
| `cd_scan_forward`   | Scans forward on the CD.                       |
| `cd_repeat_off`     | Turns CD repeat off.                           |
| `cd_shuffle_on`     | Turns CD shuffle on.                           |
| `cd_shuffle_off`    | Turns CD shuffle off.                          |
| `cd_repeat_single`  | Repeats the current CD track.                  |
| `cd_repeat_all`     | Repeats all tracks on the CD.                   |

**Virtual Buttons:**

If the `virtual_buttons` feature is enabled (as described in the Configuration section), you'll also have separate button entities for specific commands. For example, if you have the "CD Eject" virtual button enabled, you'll have an entity like `button.arcam_solo_cd_eject` that you can use to eject the CD.

**Important Notes:**

*   Replace `remote.living_room_stereo` with the actual entity ID of your Arcam Solo remote entity.