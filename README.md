# Where's DigitalCrafts?

This program displays the states which have cities named "Atlanta", "Houston", "Tampa".

# Bugs to fix

- [x] After lots of debugging, code stopped running. `node index.js` does nothing

The main function main() was not being called as it was commented out:

`// main();`

- [x] Started crashing after adding "tampa" search

The original function was not being called by the correct file (db):

` const statesWithATampa = statesWithCity('tampa');`

One the syntax was corrected as below, the function ran successfully 😁

`const statesWithATampa = db.statesWithCity('tampa');`

- [x] Prints "Atlanta" locations twice (instead of Houston)

The second function statesWithAHouston() was using a different function in its for-loop:

` const statesWithAHouston = db.statesWithCity('houston'); console.log('\n\nThere is a Houston in these states:') for (let st of statesWithAnAtlanta) { console.log(st); }`

I corrected swapped out the function in the for-loop with the correct one:

` const statesWithAHouston = db.statesWithCity('houston'); console.log('\n\nThere is a Houston in these states:'); for (let st of statesWithAHouston) { console.log(st); }`

For each bug you fix, add documentation to this README about how you fixed it (include before/after code samples).

# For the more curious:

`db.js` includes more functions that you can try out. In `index.js`, try to `console.log()` the results of the following function calls:

- `getByAbbreviation('ak')`
- `searchByName('dakota')`
  - Why does this only return results for North Dakota (and not South Dakota)?
