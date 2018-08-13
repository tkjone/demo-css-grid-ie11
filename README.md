# DEMO - CSS GRID IE11

Demo app illustrating how we can go about using CSS grid with IE11. The goal is to demo the following:

- CSS Grid App Structure
- Popovers not anchored to the bottom of the screen
- Identify the limited support areas - what one has to be aware of to make this work
- Table built with flex

# Quickstart

- Run the IE 11 VM

  See [Setup instructions](https://github.com/ca-cwds/intake/wiki/Running-IE-11-or-Edge-in-VirtualBox)

- Install node deps

  ```bash
  yarn
  ```

- Build the CSS

  ```bash
  yarn build-css
  ```

- Serve the app

  ```bash
  yarn serve
  ```

  > We serve the app so you can access it on your VM.

## Grid and IE Considerations

- Auto placement does not work. Explicitly tell everything where to go.
- Use `grid-template` and not `grid`. Guides like https://css-tricks.com/snippets/css/complete-guide-grid/ will tell you to use `grid`, but this won't work with autoprefixer.
- Do not duplicate `grid-template-areas` area names. To help, we can apply BEM naming convention.
- Test often. Don't make sweeping CSS changes. Small incremental changes are best.
