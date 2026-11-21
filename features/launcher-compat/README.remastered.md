# Launcher compatibility in Wurm HUD Remastered

Launcher compatibility is a separately selectable module. After confirmed login
it sends one quiet /alts request in the existing connection and exports the
observed roster, Character Screen paperdoll image, current position, nearest
known settlement, skills, owned inventory/equipment/container metadata and the
observed map with a player arrow. No separate Steam login or character creation
is performed. Servers without /alts return an explicit unavailable/no-response
state. Unknown container contents and unknown settlements are not invented.

Sklo Launcher 0.4.0 sets the export directory for its child client. For an ordinary
client start the fallback is user-home/.sklolauncher/hud-inbox. JSON/PNG snapshots
are local and include character identity and inventory data; they are not uploaded.
Exports continue while the launcher is closed and are imported on its next start.
Normal disconnect captures before session cleanup. Crashed sessions retain entry
avatar/location/map and show no data for dumps. The next successfully loaded
session of the same alt fills those dumps with explicit source attribution.
Keep a manual backup of launcher data. Automatic snapshot pruning is not included.

Manual verification:
1. Install this ZIP manually and launch a known character from Sklo Launcher.
2. Check that /alts does not echo; only its correlated reply is hidden. Other
   chat, combat, skill and manual examine messages must remain visible.
3. After login inspect the alt data browser: skills, items, equipment, containers,
   avatar and observed map/heading. Unknown contents must not appear as empty.
4. Move/turn, log out normally, reopen the launcher and compare the final snapshot.
5. Check a different server and a server without /alts. Saved cards must survive.
6. Disable Launcher synchronization, restart, and confirm no new exports/requests.
