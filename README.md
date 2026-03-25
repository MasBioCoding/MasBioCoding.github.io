# MasBioCoding.github.io

Personal site and blog built with Jekyll.

## Working setup

This repository was last confirmed working with:

- Ruby `3.4.1`
- Bundler `2.4.22`
- Jekyll `4.3.2`
- Minima `2.5.1`

The site config lives in [`_config.yml`](/Users/masjansma/Desktop/MasBioCoding.github.io/_config.yml). The current production URL there is `https://masjansma.nl`.

## Local preview

From the repository root:

```bash
bundle install
bundle exec jekyll serve
```

Then open:

```text
http://127.0.0.1:4000
```

If you prefer, `http://localhost:4000` should also work.

## Environment setup

Use Ruby `3.4.1` before running Bundler or Jekyll.

If you are still using `chruby`, the command is:

```bash
chruby ruby-3.4.1
```

Then verify the environment:

```bash
ruby -v
bundle -v
bundle exec jekyll -v
```

Expected versions:

```text
ruby 3.4.1
Bundler version 2.4.22
jekyll 4.3.2
```

## Notes for Future Me

- Always run Jekyll through Bundler: `bundle exec jekyll serve`
- If `Gemfile` changes, run `bundle install` again
- If `_config.yml` changes, restart the Jekyll server

## Ruby 3.4 note

This repo explicitly includes a few gems that older Jekyll dependencies expect on Ruby `3.4`:

- `webrick`
- `csv`
- `base64`
- `bigdecimal`

If local preview suddenly fails with errors like `cannot load such file -- bigdecimal`, check that those gems are still present in [`Gemfile`](/Users/masjansma/Desktop/MasBioCoding.github.io/Gemfile) and rerun:

```bash
bundle install
```
