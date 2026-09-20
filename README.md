# a2ui-spikes binaries

Images and videos for [a2ui-spikes](https://github.com/polina-c/a2ui-spikes).

They live here rather than in the main repo so that clones of it stay small.
The experiment CUJ recordings alone are several megabytes each, and a repository
that grows by that much every week gets slow to clone and stays slow, because
git keeps every version forever.

## Layout

Each file sits at the path it would have had in the main repo, so that a link
in `a2ui-spikes` and the file here can be matched up by eye:

```
ci/experiments/<date>-<time>/videos/<framework>.webm
ci/experiments/<date>-<time>/videos/<framework>-<step>.png
```

## Linking from a2ui-spikes

Use the raw URL, which serves the file itself and lets a screenshot be embedded
with `![...](...)`:

```
https://raw.githubusercontent.com/polina-c/a2ui-spikes-binaries/main/<path>
```

Push the file here before writing the link, since a link to a file that has not
been pushed looks the same as a working one until someone clicks it.
