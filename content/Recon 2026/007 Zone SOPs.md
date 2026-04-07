Use this as the operating one-pager for each zone. Fill names and phone numbers before T-7.

---

## Common SOP for All Zones


- **Owner:** `<TBD name>` | **Backup:** `<TBD name>` | **Escalation:** Ops Chief → Event Director
- **Open checklist:** power, internet, signage, queue markers, QR scan test, safety check
- **Slot cadence:** default 45 minutes session + 10 minutes reset unless noted
- **Capacity control:** hard cap enforced, no overfill; overflow goes to wait queue
- **Incident logging:** every disruption > 5 min logged with timestamp and action taken
- **Close checklist:** equipment count, damage log, pending rewards, handover note 

---

## 1) RFID Lock Hunt + Puzzle Box (Viki and Swarnim)

- **Objective:** participants solve clue trail and unlock RFID lockbox
- **Capacity:** 30 active hunters/hour, 6 at lock station at once
- **Assets:** 3 RFID locks, 8 active keycards, 2 spare readers, clue kit v1–v4
- **Staff:** 1 owner, 2 referees, 2 runners, 1 anti-tamper spotter
- **Rules:** no force/opening attempts with tools; only event-issued cards
- **Reset:** key logic rotates every 2 hours, clue cards rotated every 4 hours
- **Win condition:** valid unlock under timed attempt window (max 3 attempts/session)
- **Failure fallback:** if reader fails, switch to spare reader; if lock fails, move to backup lockbox

---

## 2) Hardware Badge + IoT Village (Izhaan)

- **Objective:** hands-on build + secure firmware learning
- **Capacity:** 40 benches per batch
- **Assets:** MCU kits, solder stations, ESD mats, goggles, first-aid, spare components
- **Staff:** 1 owner, 4 mentors, 2 safety marshals, 1 inventory controller
- **Tracks:** beginner blink; sensor integration; basic firmware hardening
- **Safety:** PPE mandatory in solder area; no food/liquids near benches
- **Reset:** tool cleanup and kit replenishment every batch
- **Win condition:** badge powers on, challenge test passes, QR completion issued
- **Failure fallback:** if solder section saturates, route overflow to no-solder firmware station

---

## 3) Gaming Arena (Ryan)

- **Objective:** keep engagement high and distribute crowd load
- **Capacity:** depends on rigs/consoles; publish current capacity in app
- **Assets:** rigs/consoles, LAN switch, controller/peripheral spares, anti-cheat setup
- **Staff:** 1 owner, 2 bracket admins, 1 technical support, 1 queue controller
- **Format:** 20-minute slots, fixed mini-brackets, no custom match length
- **Reset:** account logout + peripheral wipe + station health check after each slot
- **Win condition:** bracket points and passport points
- **Failure fallback:** if a station fails, auto-remap match and credit wait-time bonus

---

## 4) Application Security Zone

- **Objective:** teach real-world application vulnerabilities, exploitation flow, and mitigation in a controlled lab
- **Capacity:** fixed scheduled batch; target 40-60/session depending on room and demo visibility
- **Assets:** projector, presenter laptop, internet, vulnerable training app, browser tools, session deck/guide
- **Staff:** 1 owner/speaker, 1 assistant, 1 queue or room controller
- **Rules:** only event-provided lab targets; no testing outside the approved environment
- **Reset:** lab state checked before each batch; demo accounts and credentials rotated as needed
- **Win condition:** participants complete the guided tasks and submit takeaways or challenge answers
- **Failure fallback:** convert to speaker-led walkthrough mode if live exploitation infra is unstable

---

## 5) Media Forensics & Deepfake Lab

- **Objective:** run a hands-on forensic lab on manipulated image, video, and audio evidence
- **Capacity:** 10-15 participants per batch
- **Assets:** primary laptop, backup laptop, projector, local HTTP server, FFmpeg, Audacity, GIMP, StegSolve, ExifTool, printed score sheets
- **Staff:** 1 owner, 1 technical assistant, 1 scoring/proctor volunteer
- **Rules:** use only supplied files and tools; no tampering with scoring sheets or batch files
- **Reset:** 15-minute buffer between batches to clear scores, restart local services, and restock prize tokens
- **Win condition:** most validated challenge solves across ELA, de-blur, and spectrogram tracks
- **Failure fallback:** distribute challenge bundle from backup laptop and collect answers offline

---

## 6) Hacking Arena

- **Objective:** demonstrate common cyber attack chains and teach the defense story behind them
- **Capacity:** 80-100 participants per batch
- **Assets:** 3-4 laptops, projector, hotspot/router, QR printouts, mic/audio support, station materials
- **Staff:** 1 zone lead, 1 technical operator, 4 station leads, 2 crowd managers, 1 technical backup
- **Rules:** demos stay simulated and in-scope; no use of live personal accounts or real unauthorized targets
- **Reset:** station state, demo accounts, and presentation flow checked between batches
- **Win condition:** participants complete station rotation and defense summary checkpoints
- **Failure fallback:** collapse to central demo plus moderated discussion if one or more stations fail

---

## 7) Cyber Expo Zone

- **Objective:** showcase participant-built cyber projects through live demos and structured booth interaction
- **Capacity:** 10-20 stalls, 30-50 visitors in-zone at a time
- **Assets:** tables, chairs, extension boards, Wi-Fi, stall labels, poster space, QR feedback forms
- **Staff:** 1 zone lead, 1 logistics helper, judges optional if formal evaluation is enabled
- **Rules:** every stall must demonstrate a real use case or working prototype; idle poster-only booths are not accepted
- **Reset:** booth health check every 2 hours; reassign empty or failed stalls quickly
- **Win condition:** judged winner set if evaluation is active, otherwise zone tracks visitor engagement and completions
- **Failure fallback:** allow explanation-only demos if hardware fails and merge underused stalls during low traffic

---

## 8) Art Zone: Hack the Canvas

- **Objective:** provide a non-technical creative zone that keeps traffic distributed while matching the event theme
- **Capacity:** 20-25 comfortable, 30 max at a time
- **Assets:** black chart paper, A4 sheets, pencils, markers, neon pens, white gel pens, graffiti wall material, collaborative canvas, optional laptops/tablets
- **Staff:** 1 zone coordinator, 2 activity assistants, 1 material manager, 1 crowd manager, 1 optional digital-station helper
- **Rules:** shared walls/canvas stay respectful and event-safe; no damage to venue surfaces
- **Reset:** replenish stationery continuously and rotate crowded stations as needed
- **Win condition:** open-participation zone; success measured by throughput and quality of shared installations
- **Failure fallback:** close the optional digital station first and continue with manual stations only

---

## 9) Escape Room: System Breach

- **Objective:** run a timed team puzzle experience around cyber-themed clues, locks, and ciphers
- **Capacity:** teams of 3-4; target 4-5 teams per round if space supports parallel setups
- **Assets:** printed clues, cipher sheets, lockboxes, number/key locks, keys, themed props, enclosed room, timers
- **Staff:** 1 game master, 1-2 inside observers, 1 reset manager, 1 registration manager
- **Rules:** no forcing locks, opening props, or bypassing clue order; hints only through staff
- **Reset:** 2-5 minutes between runs to replace clues, relock boxes, and verify puzzle order
- **Win condition:** final password or last lock solved before timeout
- **Failure fallback:** convert to guided puzzle run if a lock or prop fails mid-session

---

## 10) Sponsor Demo Street

- **Objective:** structured sponsor engagement with technical activity
- **Capacity:** dynamic; one queue per stall
- **Assets:** stalls, power drops, internet profiles, signage, QR lead forms
- **Staff:** 1 zone owner, 1 sponsor relations rep, 2 floor stewards
- **Rules:** each demo block must include interactive component
- **Reset:** booth turnover checklist every 2 hours
- **Win condition:** participant completions and sponsor challenge leaderboard points
- **Failure fallback:** reroute sessions to adjacent booths and publish delays in app

---

## Zone Handover Template (End of Shift)


- **Shift start/end:** `<TBD time>`
- **Sessions completed:** `<TBD count>`
- **Incidents:** `<yes/no + details>`
- **Consumables used:** `<TBD list>`
- **Pending actions for next shift:** `<TBD list>` 
