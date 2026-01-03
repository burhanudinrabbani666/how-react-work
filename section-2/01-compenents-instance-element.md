# Components VS Instance VS Element

## Components

- Description oa a piece of UI
- A component is a function that return react elemnets (element tree), usually written as JSX
- Blueprint or templates

## Instence

- Instence are created when we use components
- React internally calls tab()
- Actally "physically" manifestation of a components
- Has its own state and props
- Has a lifcycle (can be "born", "lives" and "die")

## Element

**RETURNS**

JSX is converted to react.creatElements() **function calls**.
a React element is the **result of these function calls**.
information neccessary to create **DOM elements**.

[Next: instances and elements](./02-instances-and-elements.md)
