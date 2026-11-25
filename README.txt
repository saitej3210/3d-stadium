ARENA 3D STADIUM - NIGHT / TICKET / SKYBOX UPDATE

What's new
- Night mode (default) with floodlight banks, roof LED rim, stars + moon, glowing red facade,
  glowing blue LED bands, aisle step lights, plaza lamps. Top-right button toggles Night/Day.
- Realistic seats: vivid red with blue accents, curved backrest, tip-up seat pan, steel legs,
  divider armrests. 3 detail levels (near / mid / far) + frustum culling for speed.
- Ticket card (tap a seat): "Your view" thumbnail, stand, block, row, seat, gate, barcode, price.
- "Upgrade +Rs" button flies you to a sky-box seat (glass-front lounge, leather armchairs);
  "Confirm upgrade" / "Back to my seat". "Skyboxes" button also appears in block view.
- Sky-box level added at the top of the upper tier (roof raised 3 m to make room).

- Block select -> camera zooms right into the block so seats are big and easy to pick.
  Drag = move around the block, scroll = zoom, hovered seat glows cyan + tooltip (row/seat/price),
  tap a free seat = seat view + ticket. 'Block view' button toggles the wide block overview.

Run: open index.html in a modern browser with WebGL2.
Note: client-side demo. Availability and prices are demo-generated.
- v3: fans in taken seats, scrolling LED ads, live scoreboards (clock+score), moving players+ball, flags, dugouts, light shafts, railing/pillar restricted-view warning, skybox bar+TV, crowd audio (Sound button), minimap+filters, cart, checkout, ticket PNG download.
Test links: ?n=0 (day)  ?go=s:0:5:12:50 (seat)  ?go=x:63:5 (skybox)  &snap=1 (no camera easing)

- v6 seats + crowd pass
  * Seats: desaturated plastic red with a navy / white block mosaic and per-seat tone variation, plus aisle handrails (posts + top rail) in both tiers.
  * Crowd: real people instead of boxes: torso, arms, head with hair, trousers and shoes; mixed shirts (club colours + casual), varied skin tones, adults and kids. Detail LOD by distance.
  * Stadium wave rolls around the bowl, and everyone's arms go up when a goal is scored (live scoreboard goals).
  * Stadium is busier (more seats taken), so the crowd looks full.

- v7
  * Opening: camera starts above a realistic volumetric cloud sea and flies down THROUGH the clouds (day and night lighting), then into the stadium. Add ?nocloud to disable on slow devices.
  * Fireworks: far fewer shells and stars, rarer finale. They launch only from outside the stadium - nothing on the pitch, no pitch fountains, no sparks falling into the bowl.
  * Crowd, players, ball and crowd camera-flashes removed.
- v7b: night cleanup - removed the 24 spotlight cones landing on the pitch, the 24 sky shafts, aisle step-light flares, plaza lamp flares and the big haze flares; fewer roof flares; softer floodlight cones; weaker red wash on the ground.
- v7c: all light-shaft beams removed (16 rainbow sky shafts + floodlight cones) - they were what lit up the camera and the green ground at night.

- v8: view realism
  * Sky panel (top-right "Sky"): time-of-day slider + time-lapse (moving sun, shadows, golden hour, dusk), weather (Clear / Fog / Rain / Storm with lightning + rain sound), event modes (Football / Cricket / Concert).
  * Cricket: oval mowing, rope, 30-yard circle, pitch strip, stumps, cricket scoreboard. Concert: stage, LED walls, truss lights, runway, glowing floor, phone lights.
  * Big-screen replays: goal replay (football), FOUR / SIX / WICKET replays (cricket).
  * Ticket "Sun check": 09:00-18:00 shade / sun / glare bar for the selected seat (stand-structure shadow, same model as the shader).
  Test links: ?tod=17.8  ?wx=fog|rain|storm  ?ev=cricket|concert  ?sky=1

- v9: realistic seats pass (seats only, everything else unchanged)
  * New moulded stadium-seat shell: waisted backrest with rounded shoulders, concave scoop, lumbar bulge, side bolsters, back-lean, rolled top lip, moulded ribs on the rear, thick contoured seat pan with hip dish, raised side lips and waterfall front edge.
  * TIP-UP SEATS: free seats are folded up (pan swings 80 degrees on a hinge in the vertex shader); taken seats are down. Your hovered / selected seat folds down.
  * Hinge barrel, hinge brackets, steel standards with base plates + bolts, rear brace, divider panel + rounded arm rail.
  * Printed SEAT NUMBER plate on the front of every backrest (matches the number on the ticket), vent slots, drainage holes on the pan, rib grooves on the rear, orange-peel micro-texture, wear/dirt, sun-faded rolled edges.
  * Plastic shading: Fresnel + sun/sky reflection by day, light reflections at night.
  * Baked contact shadows on the concrete under every row.
  * Block close-up: camera now starts closer (10 m), scroll zooms down to 3 m; block no longer painted orange when zoomed, seats keep their real colours (free = folded up, taken = down). Hovered seat still glows cyan.
  * 4 seat LODs by distance keep it fast. Test links: ?zoom=4 (closer block cam), ?nocloud

- v10: seat click -> zoom + ticket -> "Seat view" button; VIP skybox clickable (zoom + sofa select); sofas in VIP boxes; Skyboxes button removed.
- v11: VIP lounge upgrade (3-part sofas, rug, side lamps, bar stools+props, wood slats, TV, downlights, VIP sign, warm interior glow), VIP button + box browse.

- v12: realism + colour grading pass (rendering only, no feature changes)
  * Colour grading (done in linear light): day / night / golden-hour / overcast / fog / rain aware white balance, teal shadows + amber highlights, filmic shoulder + toe, vibrance, tinted lifted blacks, vignette with cool edges, film grain, halation round hot lights, subtle lens chromatic aberration + sharpening.
  * SSAO (contact ambient occlusion) from the resolved depth buffer: seats, steps, roof underside and stands get real contact darkening.
  * Seats: tidy club colour design (red with navy bands + scattered navy/white seats), per-seat tone/hue variation, slight installation irregularity (tiny yaw/position/width jitter), crease + underside occlusion, scuffs and scratches, sun-faded tops, broader clear-coat reflection at night.
  * Materials: concrete weathering streaks/stains + wet sheen in rain, floodlight sheen and blade detail on the pitch, more natural daylight sky gradient.
  * Test links: ?grade=0 (grading off), ?ao=0 (no SSAO), ?fx=0 (no post at all), ?aodbg=1 (show AO buffer).

- v13: fireworks + skylights pass. Nothing plays automatically on open (clean cloud approach). 🎆 Finale = shells rise from the whole roof ring, lean outward with a gentle swing and burst high above; sparks are killed before they reach the bowl and firework flashes no longer light the pitch/seats. 🔦 Skylights = 24 thin beams from the roof rim into the sky only (pitch, seats, sky and clouds are not tinted). Click Skylights again to change colour theme, then off.
- v13b: block-to-block aisle LEDs (stair-nosing strips on every aisle, dark until Skylights is on, then they take the show colours). Finale shells now also lean INWARD over the open bowl and burst higher, and half the skylight beams converge above the pitch, so both show up from seat view. Firework flashes still never light pitch/seats.
