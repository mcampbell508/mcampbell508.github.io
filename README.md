# mcampbell508.github.io

My Personal GitHub based site accessible at [mcampbell508.github.io](https://mcampbell508.github.io/).

This site is a personal blog written in markdown and [Jekyll](https://jekyllrb.com/).

Currently I am using the [lanyon](https://github.com/poole/lanyon) theme which was created by [Mark Otto](https://github.com/mdo).

## Serving the site locally

```
cd /path/to/repo
bundle exec jekyll server
```

Then visit http://127.0.0.1:4000/. Push to Github `master` branch to make changes public.

## Compiling Resume

- Make sure all dependencies are installed:

```
sudo apt install pandoc context
```

- Build the files:
```
cd /path/to/repo/resume
make
```

- Commit any newly created files and `git push origin master`

Credits should go to [this repo](https://github.com/mszep/pandoc_resume) for the inspiration to compile a resume from markdown to HTML, PDF and Word Doc formats.
