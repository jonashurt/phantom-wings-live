# Phantom Wings — live content

Public files the game **Phantom Wings: Squadron Ace** downloads at startup.

- `contracts.json` — the pilot contracts catalog, signed (RSA-2048 / SHA-256).
- `dailies.json` — the daily challenges catalog, signed the same way.
  The game verifies the signature with the public key it ships with and ignores
  anything that doesn't match, so only files signed with the developer's
  private key are ever used.

Served through GitHub Pages: `https://jonashurt.github.io/phantom-wings-live/<file>`

Do not edit these files by hand: any change breaks the signature and the
game will ignore it. Edit the source catalog, raise its `version`, re-sign with
`scripts/_tools/SignContracts.gd` and replace the file here.
