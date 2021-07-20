# Storybook tutorial

Presentation link:
https://bit.ly/3hQTlaI

## Prerequisites:

- install dependencies
- Run storybook

## Exercise 1 - Default Export

1. Create a [default export](https://storybook.js.org/docs/react/writing-stories/introduction#defining-stories)(`metadata`) for your Button component

   Include:

   - title
   - component

2. Create a [named export](https://storybook.js.org/docs/react/writing-stories/introduction#defining-stories) story for your component

## Exercise 2 - Creating a story variant

1. Create a [named story](https://storybook.js.org/docs/react/writing-stories/introduction#defining-stories) for small Button variant

## Exercise 3 - Utilizing [Controls](https://storybook.js.org/docs/react/essentials/controls) addon

1. Create a **Template** component that passes in the [args](https://storybook.js.org/docs/react/writing-stories/args) to the the Button component(no additional props needed).
2. Bind the `Template` component to your story
3. Observe how the component in the canvas is controlled
4. Go to **Docs** tab, click **Show code**
5. Observe how the code changes as you change the controls

## Exercise 4 - Setting default [args](https://storybook.js.org/docs/react/writing-stories/args)

1. Add `args` to your story metadata
   - include:
     - label
     - backgroundColor

## Exercise 5 - Overriding [args](https://storybook.js.org/docs/react/writing-stories/args) for your story variants

1. Update your `small` Button story variant utilizing the **Template** component
2. Override the [args](https://storybook.js.org/docs/react/writing-stories/args) in the metadata to show the `small` Button variant
3.

## Exercise 6 - Modifying [Controls](https://storybook.js.org/docs/react/essentials/controls)

1. In the metadata, add [argTypes](<[Controls](https://storybook.js.org/docs/react/essentials/controls)>) to modify the control for `backgroundColor` to show a color picker
   - refer to this for controls matrix: https://storybook.js.org/docs/react/essentials/controls#annotation
2. Observe how the `backgroundColor` control is now a color picker

> Storybook sometimes isn't smart enough to generate the right control from the type, so we need to override the controls in order for the UI documentation to be user(developer, designer, QA) friendly.
