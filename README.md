# Heading Tool

![Version of EditorJS that the plugin is compatible with](https://badgen.net/badge/Editor.js/v2.0/blue)

Provides SubPoints Blocks for the [Editor.js](https://ifmo.su/editor).

## Installation

Get the package

```shell
yarn add @kalebu2468/editorjs-subpoints
```

Include module at your application

```javascript
import SubPoint from "@kalebu2468/editorjs-subpoints";
```

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    subpoints: SubPoints,
  },

  ...
});
```

## Shortcut

You can insert this Block by a useful shortcut. Set it up with the `tools[].shortcut` property of the Editor's initial config.

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    subpoints: {
      class: SubPoints,
    },
  },

  ...
});
```

## Config Params

All properties are optional.

| Field        | Type       | Description                   |
| ------------ | ---------- | ----------------------------- |
| placeholder  | `string`   | subpoint's placeholder string |
| levels       | `number[]` | enabled subpoint levels       |
| defaultLevel | `number`   | default subpoint level        |

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    subpoints: {
      class: SubPoints,
      config: {
        placeholder: 'Enter a subpoint',
        levels: [4],
        defaultLevel: 4
      }
    }
  }

  ...
});
```

## Tool's settings

![An image showing the subpoint block tool](https://capella.pics/634ad545-08d7-4cb7-8409-f01289e0e5e1.jpg)

You can select one of six levels for heading.

## Output data

| Field | Type     | Description       |
| ----- | -------- | ----------------- |
| text  | `string` | subpoint's text   |
| level | `number` | level of subpoint |

```json
{
  "type": "subpoints",
  "data": {
    "text": "Why Telegram is the best messenger",
    "level": 4
  }
}
```
