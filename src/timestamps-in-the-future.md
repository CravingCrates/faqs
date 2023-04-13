# Importing/exporting fails due to timestamps in the future

Some shared decks include cards/notes with invalidate creation dates, eg
they say cards were created in the year 40000 instead of the year 2023.
This causes a variety of problems, and causes any cards created after
importing such a deck to end up with similarly-invalid timestamps.

To prevent this problem spreading, recent Anki versions will refuse to
export decks that have invalid dates.

## When exporting

If you receive this message when exporting, you can fix it using one
of the following methods:

- On a 2.1.61+ computer version, use the Tools>Check Database menu item.
- On AnkiMobile 2.0.90+, use Check Database in the preferences screen.

## When importing

The Anki versions mentioned in the previous section can now automatically fix problem decks when importing.
