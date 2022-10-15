# 🧩 React Lifecycle Hooks

<p>
  <a href="https://bettertyped.com/">
    <img src="https://custom-icon-badges.demolab.com/static/v1?label=&message=BetterTyped&color=333&logo=BT" />
  </a>
  <a href="https://github.com/BetterTyped/react-lifecycle-hooks">
    <img src="https://custom-icon-badges.demolab.com/github/stars/BetterTyped/react-lifecycle-hooks?logo=star&color=118ab2" />
  </a>
  <a href="https://github.com/BetterTyped/react-lifecycle-hooks/blob/main/License.md">
    <img src="https://custom-icon-badges.demolab.com/github/license/BetterTyped/react-lifecycle-hooks?logo=law&color=yellow" />
  </a>
  <a href="https://github.com/semantic-release/semantic-release">
    <img src="https://custom-icon-badges.demolab.com/badge/semver-commitzen-e10079?logo=semantic-release&color=e76f51" />
  </a>
  <a href="https://github.com/BetterTyped/react-lifecycle-hooks">
    <img src="https://custom-icon-badges.demolab.com/badge/typescript-%23007ACC.svg?logo=typescript&logoColor=white" />
  </a>
  <a href="https://www.npmjs.com/package/@better-hooks/lifecycle">
    <img src="https://custom-icon-badges.demolab.com/bundlephobia/min/@better-hooks/lifecycle?color=64BC4B&logo=package" />
  </a>
  <a href="https://www.npmjs.com/package/@better-hooks/lifecycle">
    <img src="https://custom-icon-badges.demolab.com/npm/v/@better-hooks/lifecycle.svg?logo=npm&color=E10098" />
  </a>
</p>

## About

React lifecycle turned into dev friendly and readable hooks

## Key Features

🔮 **Simple usage**

🚀 **Fast and light**

💎 **No external dependencies**

## Installation

```bash
npm install --save @better-hooks/lifecycle
```

or

```bash
yarn add @better-hooks/lifecycle
```

---

## Examples

```tsx
import React from "react";
import { useDidMount, useDidRender, useDidUpdate, useWillUnmount,useIsMounted, useWillMount } from "@better-hooks/lifecycle";

const MyComponent: React.FC = () => {
  const [isOpen, setIsOpen] = React.useState(false)

  // returns ref with the mounted boolean state
  const mounted = useIsMounted()

  // Method for the component rerendering
  const forceUpdate = useForceUpdate()

  // Called before mount
  useWillMount(() => {
    // ...
  })

  // Called on component mount
  useDidMount(() => {
    // ...
  })

  // Called second, when initial DOM changes are triggered
  useDidRender(() => {
    // ...
  })

  // Called when isOpen change
  useDidUpdate(() => {
    // ...
  }, [isOpen])

  // Called when isOpen change but also on mount
  useDidUpdate(() => {
    // ...
  }, [isOpen], true)

  // Called last
  useWillUnmount(() => {
    // ...
  })


  return (
    // ...
  )
}

```
