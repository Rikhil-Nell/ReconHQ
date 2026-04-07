# auth
google login: /auth/google/login
google callback: /auth/google/callback
refresh: /auth/refresh
logout: /logout

# users
create: /users/create_user
get: /users/{user_id}
patch: /users/{user_id}
delete: /users/{user_id} (soft deletion)

# admin
 list all users: /admin/list_users
   /zones
     GET    /zones                          # list all with live status + queue depth
     PATCH  /zones/{id}/status              # override to open/amber/closed (admin override)
     PATCH  /zones/{id}/point-multiplier   # adjust point value for this zone live
     GET    /zones/{id}/queue               # current queue snapshot

   ──────────────────────────────────────────

   /points
     GET    /points/config                  # current point values per activity/reason code
     PATCH  /points/config/{activity_id}   # update a point value live
     POST   /points/award                   # manual award: participant_id, amount, reason
     DELETE /points/transactions/{id}       # revoke a specific award with reason
     GET    /points/leaderboard             # current standings
     POST   /points/leaderboard/freeze      # lock rankings (pre-awards)
     DELETE /points/leaderboard/freeze      # unfreeze

   ──────────────────────────────────────────

   /shop
     GET    /shop/items                     # list items with price + remaining inventory
     POST   /shop/items                     # create item
     PATCH  /shop/items/{id}               # reprice or adjust inventory count
     DELETE /shop/items/{id}               # pull item from shop
     POST   /shop/redemptions               # participant redeems (participant-facing)
     GET    /shop/redemptions               # list all redemptions, filterable by status
     PATCH  /shop/redemptions/{id}/fulfill  # merch desk marks physically handed over

   The fulfillment endpoint is what the person at the merch desk uses — they scan/look up the redemption ID and tap
   fulfill. Without this you have no handover record.

   ──────────────────────────────────────────

   /incidents
     POST   /incidents                      # n8n webhook posts here (inbound from Google Form)
     GET    /incidents                      # live feed, filterable by severity/zone/status
     GET    /incidents/{id}
     PATCH  /incidents/{id}                 # update status to resolved, add resolution note

   ──────────────────────────────────────────

   /announcements
     POST   /announcements                  # create + dispatch (push + in-app)
     GET    /announcements                  # history
     DELETE /announcements/{id}             # retract

   The POST triggers whatever push mechanism you wire up (FCM or similar). Keep the dispatch async — don't block the
   HTTP response on delivery.

   ──────────────────────────────────────────

   /teams (read-only log, no ownership of competition logic)
     GET    /teams                          # list teams with platform (ctf/koth), member count
     GET    /teams/{id}                     # detail with member list
     POST   /teams/sync                     # admin-triggered pull from CTFd API to refresh local log

   This domain owns no competition state — it's a local mirror of what CTFd reports, useful for the dashboard without
    depending on CTFd being up when you need to look something up.

   ──────────────────────────────────────────

   /admin (aggregates only, no owned tables)
     GET    /admin/dashboard                # single endpoint returning: active incidents count by severity, zone
     statuses, leaderboard top 5, shop redemption queue depth, announcement history count

   One fat read endpoint the dashboard polls every 30-60 seconds. Keeps the frontend simple and reduces round trips
   during high-load periods.

   ──────────────────────────────────────────

   The zones, points, shop, and incidents domains each own their own tables. teams owns a read-only mirror table.
   announcements owns a log table. admin owns nothing and aggregates across all of them.