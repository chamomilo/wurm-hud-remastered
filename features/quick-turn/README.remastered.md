# Quick Turn in Wurm HUD Remastered

Integrated from Quick Turn 1.0.1 with its original namespace and steering behavior.

Open Main menu > Wurm HUD Remastered > Quick Turn. On/Off applies after a complete
client restart. Disabled modules are not constructed and install no native hooks.
Disable the standalone wurm-vehicles-quick-turn.properties descriptor manually.

Cart/wagon, hitch, rider and particle presentation follow the client's calculated
heading promptly. Movement, collision and outgoing packets retain native control.
Boats, ridden creatures, dragged carts and passenger-only seats are excluded.
Legacy numeric tuning is read; the Remastered switch controls startup enablement.

The covered wagon, large cart, creature transporter and ship transporter fit
their displayed body to local terrain or bridge deck samples. A short flexible
section at the frame connects the body to the rigid drawbar. Its outer end
follows the hitched animals' displayed ground poses and occupied row positions.
Unhitched drawbars follow the body. The small cart retains its original
presentation. The edit runs in the native draw paths and uses the existing
vehicle meshes, including their materials and wheel animation.

The driver's view on these vehicles starts ahead of the chassis and above the
drawbar attachment. The eye follows the fitted chassis through turns and slopes,
while mouse look stays independent. Third-person orbit uses the same eye as its
origin. Passenger, small cart and free camera views retain their existing behavior.

The Quick Turn test task accepts `-PvehicleGeometryPacks=<WurmLauncher/packs>`
for the installed model fixtures and
`-PgraphicalCompatibilityJar=<supplied SkloGraphics.jar>` for both hook orders.

The vqt status, vqt off and vqt on console commands remain session-only controls.
They are also available in Keybinder with live English, Brazilian Portuguese,
German and Russian captions. No separate Quick Turn updater or telemetry is added.
