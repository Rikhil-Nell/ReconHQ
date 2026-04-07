 backend/app/
     │
     ├── shared/                         # NEW — moving from api/deps.py, controllers/rbac_controller.py
     │   ├── __init__.py
     │   ├── deps.py
     │   ├── rbac.py
     │   ├── exceptions.py
     │   └── models/
     │       ├── __init__.py
     │       └── base.py
     │
     ├── domains/
     │   ├── __init__.py
     │   │
     │   ├── auth/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   ├── user.py
     │   │   │   ├── role.py
     │   │   │   ├── oauth_account.py
     │   │   │   └── refresh_token.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_auth.py
     │   │
     │   ├── participants/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   ├── participant.py
     │   │   │   └── nfc_token.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_participants.py
     │   │
     │   ├── zones/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas/
     │   │   │   ├── __init__.py
     │   │   │   ├── zone.py
     │   │   │   └── queue.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   ├── zone.py
     │   │   │   ├── queue.py
     │   │   │   └── checkin.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_zones.py
     │   │
     │   ├── points/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas/
     │   │   │   ├── __init__.py
     │   │   │   ├── earn.py
     │   │   │   └── leaderboard.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   ├── ledger.py
     │   │   │   ├── config.py           # point values per activity/reason code
     │   │   │   ├── passport.py
     │   │   │   └── leaderboard.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_points.py
     │   │
     │   ├── shop/                       # NEW
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas/
     │   │   │   ├── __init__.py
     │   │   │   ├── item.py
     │   │   │   └── redemption.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   ├── item.py
     │   │   │   └── redemption.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_shop.py
     │   │
     │   ├── schedule/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   └── session.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_schedule.py
     │   │
     │   ├── announcements/              # NEW — replaces announcement.py in schedule
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   └── announcement.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_announcements.py
     │   │
     │   ├── teams/                      # NEW — read-only CTFd/KOTH mirror
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   └── team.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_teams.py
     │   │
     │   ├── incidents/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   ├── crud.py
     │   │   ├── schemas/
     │   │   │   ├── __init__.py
     │   │   │   ├── inbound.py
     │   │   │   └── internal.py
     │   │   ├── models/
     │   │   │   ├── __init__.py
     │   │   │   └── incident.py
     │   │   └── tests/
     │   │       ├── __init__.py
     │   │       └── test_incidents.py
     │   │
     │   ├── webhooks/
     │   │   ├── __init__.py
     │   │   ├── router.py
     │   │   ├── controller.py
     │   │   ├── service.py
     │   │   └── schemas.py
     │   │                               # no models/ — no owned tables
     │   │
     │   └── admin/
     │       ├── __init__.py
     │       ├── router.py
     │       ├── controller.py
     │       ├── service.py
     │       ├── schemas.py
     │       └── tests/
     │           ├── __init__.py
     │           └── test_admin.py
     │                                   # no models/ — no owned tables
     │
     └── api/
         └── v1/
             ├── __init__.py
             └── api.py