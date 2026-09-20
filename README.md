# a2ui-spikes binaries

Images and videos for [a2ui-spikes](https://github.com/polina-c/a2ui-spikes),
served as a site at **https://polina-c.github.io/a2ui-spikes-binaries/**.

They live here rather than in the main repo so that clones of it stay small.
The CUJ recordings alone are several megabytes each, and a repository that grows
by that much every week gets slow to clone and stays slow, because git keeps
every version of a file forever.

## Why GitHub Pages

A `.webm` committed to a repo cannot be played on github.com. The blob page
offers a download and nothing else, and `raw.githubusercontent.com` serves
`.webm` as `audio/webm`, so a raw link plays the sound of a screen recording
and shows no picture. Pages serves the same file as `video/webm`, so it plays.

Pages is enabled on `main` at the repository root, so every file is reachable at
the path it has here.

## Layout

Each file sits at the path it would have had in the main repo, so a link there
and a file here can be matched up by eye:

```
ci/experiments/<date>-<time>/index.html          gallery for one experiment
ci/experiments/<date>-<time>/videos/<framework>.webm
ci/experiments/<date>-<time>/videos/<framework>-<step>.png
```

`index.html` at the root lists the experiments, and `style.css` beside it is
shared by every gallery, so adding an experiment is markup and no CSS.

## Linking from a2ui-spikes

Use the Pages origin, not a github.com or raw URL:

```
https://polina-c.github.io/a2ui-spikes-binaries/<path>
```

A video link goes to the experiment gallery, where it plays with the other arms
next to it. A screenshot link goes straight at the `.png`, which also lets it be
embedded with `![...](...)`.

Push the file here before writing the link, and check that the link resolves.
A link to a file that was never pushed looks exactly like a working one until
someone clicks it. Pages takes a moment to redeploy after a push.
