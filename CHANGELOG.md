# Changelog

## v1.2 — Complete Tycoon (2026-07-09)

**Live**: https://sj88wonderpark.sj88ai.com/ (109KB, 2642 lines)

### 3 NEW SYSTEMS (Direction C: Save + Weather + Staff)

### 1. 💾 Save/Load System
- Auto-save every 30s to localStorage slot 0
- 3 save slots with Day/Money/Ride count display
- Per-slot actions: ▶ Load · 🗑️ Delete
- Quick Save button: instant save to slot 1
- Export JSON: downloads `sj88-park-day{N}-{timestamp}.json`
- Import: file picker → JSON.parse → restore
- `saveGame/loadGame/exportSave/importSave` functions

### 2. 🌦️ Weather System (5 states)
- WEATHERS const: sunny (1.0×) / cloudy (0.9×) / rain (0.6×) / storm (0.3×) / snow (0.4×)
- Modifiers: spawnMult, tipMult, moodDelta, skyTint
- CSS particles: 100 rain drops / 60 snowflakes / fog overlay / cloud overlay
- Storm lightning flash every 3s
- Auto-rotate every 90s (30% chance to keep same)
- Sky tint: scene.fogColor shifts based on weather

### 3. 👨‍💼 Staff System (3 types)
- STAFF_TYPES: janitor ($30/d), mechanic ($60/d), mascot ($80/d)
- Mesh: cylinder body + sphere head + type-specific accessory
- Patrol AI: random target → walk → idle 1-3s → new target
- Hire cost: 3 days upfront ($90-240)
- Daily payroll: deducted on day change
- Effects: janitor +happiness, mechanic +reliability, mascot +spawn

**Verified live**:
- ✅ All 5 weather states rendering with particles
- ✅ Staff modal: 3 hire cards + active staff list
- ✅ Save modal: 3 slots with auto-save data
- ✅ Live URL: https://sj88wonderpark.sj88ai.com/ HTTP 200, 109KB

---

## v1.1 — Living Park Rating Flywheel (2026-07-09)

### 1. ⭐ 5-Star Park Rating System (CORE FLYWHEEL)
- Rating computed live: diversity + happiness + income + crowd
- Spawn multiplier = 0.3 + 0.7 × (rating/5)²
- Income multiplier = 1 + 0.1 × rating
- HUD star widget + entrance 3D billboard

### 2. ✨ Visual Juices
- 🏮 12 lanterns around park (warm flicker at night)
- 🌅 60s day/night cycle
- 🎈 Balloons on 20% of visitors
- 📸 Photo-taking state
- 🪙 Gold coin particles on earn
- 🎆 Confetti burst on rating milestones

### 3. 👨‍👩‍👧 Visitor Groups (NEW)
- 30% of spawns are families of 2-3

### 4. 🔊 Web Audio Synthesis
- Coin, ding, star-up arpeggio
- 🔊/🔇 toggle

### 5. 📊 Stats Modal
- Click rating/day card

### 6. 🌙 Time-of-Day Indicator