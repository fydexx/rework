# Disclaimer

See [LICENSE.md](LICENSE.md).

This work is not affiliated nor endorsed by Google Inc.

# Compile the book by yourself

## Dependencies

See `requirements.txt` for Python's dependencies. On addition to that, you will
need:
- Pandoc
- Sane latex environment
- Some latex fonts (in Fedora: `yum install texlive-collection-fontsextra texlive-collection-fontsrecommended`)

## Compilation

The compilation of the book has 3 phases:

1. Scrapping [rework.withgoogle.com](rework.withgoogle.com), save as JSON.
2. Convert JSON to Markdown
3. Convert Markdown to a human readable format (e.g. PDF, EPUB)

In the shell, that translates to:

```shell
./bin/scrap | ./bin/json2markdown  | ./bin/markdown2humanreadable
```

or the same:

```shell
./bin/main
```

The first command line is more convenient if you are debugging or changing
things because you have the opportunity to skip any of the steps if you save
the intermediate output to a file.
