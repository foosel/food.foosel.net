# 🌎 Source of food.foosel.net

## Requirements

- [Hugo](https://gohugo.io)
- Optional: [Task](https://taskfile.dev) (to run the tasks below)

## Tasks

### `task serve`

Starts the Hugo server, draft, future and expired content included. The server will be available at http://localhost:1313.

On Termux, the server will also be run with `--noBuildLock` as that is needed in that environment.

### `task build`

Creates a production build of the site. The result will be placed in the `public` folder.

On Termux, the build will also be run with `--noBuildLock` as that is needed in that environment.

### `task to-single -- <path>`

Converts the given page bundle to a single page. The page bundle's `content/<slug>/index.md` will be moved to `content/<slug>.md`
and the folder will be deleted. Note that this will not work if the page bundle contains any other files than `index.md`.

### `task to-bundle -- <path>`

Converts the given single page to a page bundle. The single page's `content/<slug>.md` will be moved to `content/<slug>/index.md`.
