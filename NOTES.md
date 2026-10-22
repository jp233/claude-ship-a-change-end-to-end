# Notes

## Plan
Add `PUT /users/:id`. The store gets an `updateUser` helper (data access stays in `db/store.js`), and the route in `routes/users.js` follows the existing GET/POST handlers. An unknown id returns 404 "User not found". A missing or empty `name` or `email` returns 400 "name and email are required".

## Model
Claude Sonnet 5.5 (`claude-sonnet-5-5`) in Claude Code. The change was small and the patterns were already in the codebase.

## Commit split
1. Store helper and route for the update endpoint.
2. This `NOTES.md`.

## Review
No separate review has been run yet; I'll fill this in after one. Self-check while writing: the validation requires strings, so a non-string `name` returns 400 instead of crashing on `.trim()`.
