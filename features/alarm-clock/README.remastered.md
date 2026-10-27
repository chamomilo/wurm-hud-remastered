# Alarm Clock in Wurm HUD Remastered

Compared with the latest public standalone release: [Alarm Clock v0.3.10](https://github.com/chamomilo/wurm-alarm-clock/releases/tag/v0.3.10).

Keep food, water, prayer, meditation, Favor and custom reminders, including
All on / All off, saved preferences, chimes and reminders while the list is closed.

- The alarm window displays actual game time and adds Lock time with separate
  HH:MM fields. ASCII digits, hours 0-23 and minutes 0-59 are validated. The
  initial lock value is 12:00, with locking off. Valid edits apply immediately.
- TimeLock changes the local sky and lighting while the real calendar and alarm
  deadlines continue. Turning it off immediately restores the normal sky.
- The draggable brass HUD clock has 42 px and 84 px size choices, scaled for the
  viewport. Independent hands follow real game time, including fractional hour
  movement, while a time lock is active. Ringing reminders use the same artwork.
- Hover shows actual time, optional locked time, then enabled alarms and their
  countdowns. Food, water and Favor show their condition when no exact countdown
  is available. Time digits and editors use aligned, centred 20 px body text.

New controls and hints support English, Brazilian Portuguese, German and
Russian. Clock and lock preferences are saved beside the existing alarms.

Install and configure this component using the [Remastered guide](../../README.md).
