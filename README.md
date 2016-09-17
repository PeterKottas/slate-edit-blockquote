# slate-edit-blockquote

[![NPM version](https://badge.fury.io/js/slate-edit-blockquote.svg)](http://badge.fury.io/js/slate-edit-blockquote)
[![Linux Build Status](https://travis-ci.org/GitbookIO/slate-edit-blockquote.png?branch=master)](https://travis-ci.org/GitbookIO/slate-edit-blockquote)

A Slate plugin to handle keyboard events in blockquotes. Blockquotes can contain blocks.

### Install

```
npm install slate-edit-blockquote
```

### Features

Natural keybindings:

- Pressing <kbd>Enter</kbd> twice exit the blockquote

### Simple Usage

```js
import EditBlockquote from 'slate-edit-blockquote'

const plugins = [
  EditBlockquote()
]
```

#### Arguments

This plugin accepts options to redefine the following block types:

- ``[type: String]`` — type for blockquotes
- ``[typeDefault: String]`` — type for default block in blockquote.

### Utilities

`slate-edit-blockquote` exports utilities and transforms:

#### `utils.isSelectionInBlockquote`

`plugin.utils.isSelectionInBlockquote(state: State) => Boolean`

Return true if selection is inside a blockquote (and it can be unwrap).

#### `transforms.wrapInBlockquote`

`plugin.transforms.wrapInBlockquote(transform: Transform) => Transform`

Wrap current block in a new blockquote.
