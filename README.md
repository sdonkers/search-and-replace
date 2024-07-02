# search-and-replace
Search and Replace text within the Block Editor.

https://github.com/badasswp/search-and-replace/assets/149586343/d4acfab3-338b-434f-b09c-769df9331095

## Why Search and Replace for Block Editor?

This plugin brings the familiar __Search and Replace__ functionality that PC users have grown accustomed to in __Microsoft Word__ and __Google Docs__ to the block editor. It enhances user efficiency by allowing quick text searches and bulk changes throughout content, saving time and ensuring consistency.

It also reduces the risk of manual errors, streamlining workflows for content creators and site administrators, ultimately improving the overall management of WordPress sites.

### Hooks

#### `search-replace-for-block-editor.restrictedBlocks`

This custom hook (filter) provides the ability to exclude the search and replace functionality away from specific blocks:

```js
import { addFilter } from '@wordpress/hooks';

addFilter(
  'search-replace-for-block-editor.restrictedBlocks',
  'restrictedBlocks',
  (restrictedBlocks) => {
    if (restrictedBlocks.indexOf('core/paragraph')) {
      restrictedBlocks.push('core/paragraph')
    }

    return restrictedBlocks;
  }
);
```

**Parameters**

- restrictedBlocks _`{string[]}`_ List of Restricted Blocks.
