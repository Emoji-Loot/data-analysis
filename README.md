<p align="center">
  <h1 align="center">Emoji-Loot</h1>
</p>

# Emoji Loot

## Distribution

- tokenIds `1` to `7778` claimable by user.
- tokenIds `7778` to `7999` claimable by contract owner.
- Each token has attributes: `weapons`, `faces`, `body`, `location`, `sport`, `pets`, `flowers`, `traffic`.

## Output

- [loot.json](./loot.json) contains all tokenIds and their attributes.
- [occurences.json](./occurences.json) contains the number of occurences by attribute.
- [rare.json](./rare.json) contains a mapping of `lootId` to `score` (which is the sum of number of occcrences of each child attribute for a `lootId`), sorted ascending by `score`. It also includes `rarest` which is how rare the loot bags attributes are (`1` == `rarest`, `8000` == `least rare`), based on this specific ranking mechanism.
- [probability.json](./probability.json) contains a mapping of `lootId` to `rank` by probabilistic occurence rather than rank (`P(A in bag at slot 1)` and `P(B in bag at slot 2)`, then `P(A in slot 1 and B in slot 2)` is the product of the 2 probabilities).
- [images.json](./images.json) contains the base64 encoded SVG of each tokenId
