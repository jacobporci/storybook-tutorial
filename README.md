# Storybook tutorial

Presentation link:
https://bit.ly/3hQTlaI

## Prerequisites:

- install dependencies
  - `yarn` or `npm i`
- Run storybook
  - `yarn storybook` or `npm run storybook`

## Exercise 1 - Default Export

1. Create a [default export](https://storybook.js.org/docs/react/writing-stories/introduction#defining-stories) (`metadata`) for your Button component

   Include:

   - `title`
     > The title will control how the component is structured in the Storybook's left navigation bar
     >
     > ```
     > title: 'Components/Button'
     > ```
     >
     > will be displayed as:
     >
     > ```
     > - Components
     >   - Button
     > ```
   - `component`
     > `component` lets Storybook know the types, comments, etc. of the imported component

2. Create a [named export](https://storybook.js.org/docs/react/writing-stories/introduction#defining-stories) story for your component

> It is recommended you use UpperCamelCase for your story exports, for example:
>
> ```
> export const ButtonWithALabel
> ```
>
> will show up in Storybook as:
>
> ```
> Button with a label
> ```

## Exercise 2 - Creating a story variant

1. Create a [named story](https://storybook.js.org/docs/react/writing-stories/introduction#defining-stories) for small Button variant

> It is recommended to create story variants to immediately display what the component looks like in that state

## Exercise 3 - Utilizing [Controls](https://storybook.js.org/docs/react/essentials/controls) addon

1. Create a **Template** component that passes in the [args](https://storybook.js.org/docs/react/writing-stories/args) to the the Button component(no additional props needed).
2. Bind the `Template` component to your story
3. Observe how the component in the canvas is controlled
4. Go to **Docs** tab, click **Show code** to show the implementation of this component
5. Observe how the **code implementation** changes as you change the controls

> This is a very useful tool for developers to enable them to have a glance or even let them just copy-paste the actual implementation of their desired variant of the component

## Exercise 4 - Setting default [Args](https://storybook.js.org/docs/react/writing-stories/args)

1. Add `args` to your story metadata (default export)
   - include: - `label`

> Storybook is not yet smart enough to get the default value of props from your component declaration when using `Typescript`. But I think this is possible when you use `defaultProps`

## Exercise 5 - Overriding [args](https://storybook.js.org/docs/react/writing-stories/args) for your story variants

1. Update your `small` Button story variant to utilize the **Template** component
2. Override the metadata [args](https://storybook.js.org/docs/react/writing-stories/args) (or the default value) to show the `small` Button variant

## Exercise 6 - Modifying [Controls](https://storybook.js.org/docs/react/essentials/controls)

1. In the metadata (default export), add [argTypes](<[Controls](https://storybook.js.org/docs/react/essentials/controls)>) to modify the control for `backgroundColor` to show a color picker instead of a textfield
   - refer to this for controls matrix: https://storybook.js.org/docs/react/essentials/controls#annotation
2. Observe how the `backgroundColor` control is now a color picker

> Storybook sometimes isn't smart enough to generate the right control from the type, so we need to override the controls in order for the UI documentation to be user(developer, designer, QA) friendly.
