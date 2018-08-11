# DEMO - CSS GRID IE11

I am interested in seeing how much of CSS we can use of CSS Grid and still have it work on IE11. This will build out a basic app shell with a table as the main content.

Illustrating:

- App Structure
- Main content scrollable - to access the main content
- Popovers not anchored to the bottom of the screen
- Remove overflow: hidden
- Making CSS Grid IE safe
- Identify the limited support areas - what one has to be aware of to make this work

# TODO

- [ ] content area organized via columns + grid gap
- [ ] demo popover

# Quickstart

To test this, you can run the `index.html` file in the browser, but you will also need to run IE11 on your local environment. To do this, I run a VM. To setup IE11 see [the instructions](https://github.com/ca-cwds/intake/wiki/Running-IE-11-or-Edge-in-VirtualBox)

- install deps

  ```bash
  yarn
  ```

- build the css

  ```bash
  yarn build-css
  ```

- serve the app

  ```bash
  yarn server
  ```

  > We serve the app so you can access it on your VM.

## Grid and IE Considerations

We can build CSS Grid safely and all we have to do is be aware and consider some of the following rules:

- Auto placement does not work. You must explicitly tell everything where it needs to go.
- Do not duplicate `grid-template-areas` area names. To help, we can apply BEM naming convention. We can duplicate in media queries when the rules are applied to the same element.
- You can use things like `grid-column: 1 / span 2;` but you can't count backwards.
- Test often. Don't make sweeping css changes. make small incremental changes and test that they are working across the board.

## Thank You

This is a breakdown and test of what was presented in [CSS Grid in IE](https://css-tricks.com/css-grid-in-ie-css-grid-and-the-new-autoprefixer/) series of articles.
