# slides

A collection of slide decks.

## Create a new slide deck from an existing slide deck

1. Recursively copy the directory of the original slide deck to the new location, commit.
    - Directory name semantics: what-venue-where
2. Do the same in the `docs` subdirectory.
3. Tweak the `docs` symlink in the new location.
4. Check that rendering the copied slide deck works.
5. Add a post in `content/posts`
    - File format matches directory format
    - Date: Presentation date
    - Title: Slide deck title, venue, location
6. Render with `blogdown::serve_site()`
