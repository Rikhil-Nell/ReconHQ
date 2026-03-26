## Venue

- **Primary anchor:** SAC (Student Activity Center) + campus distributed zones
- **Load-in / load-out:** Day 1 08:00 setup start / Day 3 20:00 command room close
- **Parking:** designated speaker/sponsor lot + general participant guidance
- **Zone map:** to be finalized by T-30

---

## Infrastructure Blueprint

### Network Architecture

- Cloud-first architecture (not campus Wi-Fi dependent).
- Segmentation via OpenVPN overlay network:
    - **VPN overlay:** participant access to CTF/KOTH challenge targets
    - **Campus Wi-Fi (best-effort):** for accessing cloud services (CTFd, app backend, scoreboard)
    - **Sponsor/demo internet:** separate guest network (rate-limited)
    - **Ops network:** 4G/5G backup for command & control
- Firewall deny-by-default on all AWS security groups.
- VPN subnet (10.8.0.0/16) with per-participant .ovpn configs for anti-cheat tracking.

### Hosting

- **CTF:** CTFd on AWS EC2 (t3.xlarge) with daily snapshot backups.
- **KOTH:** 10× AWS EC2 instances (t3.medium) with automated reset every 30–60 min.
- **OpenVPN Server:** AWS EC2 (t3.large) for participant VPN access to challenge targets.
- **App backend:** AWS EC2/ECS with CDN + uptime monitor + fallback page.
- **Database:** Neon Postgres (managed, serverless).

### Fallbacks

- Backup 4G/5G enterprise routers for critical systems.
- Read-only backup scoreboard webpage.
- Manual score capture sheet for absolute fallback.

---

## AV / Tech

- **Microphones:** TBD based on venue acoustics
- **Projector / screen:** main stage + side zone displays
- **Wi-Fi:** event-managed network (see infra blueprint above)
- **Campus screens:** content pipeline for live updates, sponsor loops, crowd indicators

---

## Crowd Flow and Capacity Controls

### Capacity Model

- Main hall: fixed seated capacity with hard cap.
- Side zones: each has occupancy cap and queue threshold.
- App displays red/amber/green crowd indicators.

### Controls

- Wristband or QR color coding by participant type.
- Staggered starts for side events.
- Overflow waiting lounges with live stream.

### Queue Policy

- 15 min grace per slot.
- No-shows auto-release seats.

---

## Outstation Logistics (Lodging, Travel, Food)

### Audience Segments

- In-campus students.
- Outstation participants (city/state).
- Speakers/sponsors.

### Lodging Plan

- **Tier A:** speaker/sponsor hotel block near campus.
- **Tier B:** participant hostel/partner budget hotels.
- **Emergency overbooking buffer:** 10% rooms.

### Travel Desk

- Pre-arrival guide with nearest station/airport routes.
- Shuttle windows at fixed intervals.
- Night safety transport for post-midnight movement.

### Food Plan

- 3 meal windows + midnight snack for overnight tracks.
- Veg/non-veg clearly labeled; allergy markers mandatory.
- Water points every major zone.

---

## Merch and Identity System

### Merch Lineup

- Lanyard + RFID enabled badge (where feasible).
- Sticker packs, tees, limited challenge coins, sponsor swag.

### Distribution

- Core kit at check-in.
- Unlockable merch via points milestones.

### Anti-Loss

- Controlled inventory sheet with hourly reconciliation.

---

## Staffing

### Volunteer Model

- 50-person workforce across functional pods.
- Full handbook: [Recon — Volunteer Handbook](https://www.notion.so/Recon-Volunteer-Handbook-19b2e40001e8445aa18259768fbab9fb?pvs=21)
- Zone-level SOPs: [Recon — Zone SOPs](https://www.notion.so/Recon-Zone-SOPs-a49ef27cd1774166977dd8d7fe9a056b?pvs=21)

### Shift Structure

- Standard shifts: 6 hours; overnight shifts: 4–5 hours.
- No one works more than 10 active duty hours/day.
- Overnight shifts must rotate; next-day rest is mandatory.

---

## Risk / Contingencies

Full risk register with 18 tracked risks: [Recon — Risk Register](https://www.notion.so/Recon-Risk-Register-1206301103964681b90df3512e5cc8a8?pvs=21)

### Top 6 Priority Risks

1. **R1** — Network reliability
2. **R2** — Power continuity
3. **R3** — CTF uptime
4. **R6** — Crowd control
5. **R8** — Out-of-scope security actions
6. **R12** — Food/logistics integrity

### Quick Reference

- **Weather plan:** travel advisories + flexible check-in + extended arrival windows
- **Backup power:** UPS for core infra + generator contract
- **First aid:** onsite medical desk + ambulance contact on standby

---

## Vendor Tracker

|Vendor Category|Status|Lock Deadline|Notes|
|---|---|---|---|
|Internet provider|TBD|T-20||
|Router/network hardware|TBD|T-20||
|Power backup (UPS/generator)|TBD|T-20||
|Print (badges, signage, merch)|TBD|T-20||
|Food / catering|TBD|T-14|Veg/non-veg + allergy markers|
|Lodging partner(s)|TBD|T-14|10% overbooking buffer|
|Transport / shuttles|TBD|T-14|Night safety routes required|
|AV / stage equipment|TBD|T-14||