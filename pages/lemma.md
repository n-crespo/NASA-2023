# Lemma

- a `LEMMA` is a little function thingy that you can prove
- when writing a proof, you need to start it with `lemma_name: LEMMA`
  - then the prove button will appear
- a small block of code, or a theory, that you can prove in `PVS`
- the proof command `(lemma)` can also be used to call an already existing,
  proven lemma to add its logic into a proof
- `(lemma sqrt_hathat)`
  - recognizes when an real `exponentiation` (^^) is 1/2 and converts that to `sqrt()`
  - calling `lemma` that is useful in a proof
