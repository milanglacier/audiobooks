# audiobooks

A monorepo for the audiobooks I make. Each audiobook lives in its own
submodule with its own GitHub repository.

## Audiobooks

### [rust-audiobook](https://github.com/milanglacier/rust-audiobook)

A Chinese-language audiobook that teaches Rust by ear, one chapter at a time,
made for the commute. It covers ownership, borrowing and lifetimes, structs and
enums, error handling, traits, iterators and closures, concurrency, smart
pointers, async and Tokio, and the wider ecosystem. Every chapter has a
transcript that highlights the paragraph being read aloud. Listen at
<https://rust-audiobook.vercel.app>.

### [hart-crane-appreciation](https://github.com/milanglacier/hart-crane-appreciation)

A Chinese-language audiobook project for appreciating Hart Crane's poetry. Its
book setup and Vercel build are ready; the outline and chapters will be written
later. Source notes are kept locally outside Git.

## Development

Each top-level directory is a git submodule pointing at its own repository.
Work inside the submodule, run its own commands there (see its README), then
update the gitlink in this monorepo.

To clone everything:

```bash
git clone --recurse-submodules <this repo's URL>
```
