# @zxcvbn-ts/language-en

The Gaeilge (Irish) dictionary and language package for zxcvbn-ts

## Install

#### npm:

`npm install @zxcvbn-ts/language-ga-ie --save`

#### yarn:

`yarn add @zxcvbn-ts/language-ga-ie`

## Setup

```js
import { ZxcvbnFactory } from '@zxcvbn-ts/core'
import * as zxcvbnCommonPackage from '@zxcvbn-ts/language-common'
import * as zxcvbnGaPackage from '@zxcvbn-ts/language-ga-ie'

const password = 'somePassword'
const options = {
  translations: zxcvbnGaPackage.translations,
  graphs: zxcvbnCommonPackage.adjacencyGraphs,
  dictionary: {
    ...zxcvbnCommonPackage.dictionary,
    ...zxcvbnGaPackage.dictionary,
  },
}
const zxcvbn = new ZxcvbnFactory(options)
zxcvbn.check(password)
```

## Sources

- commonWords.json is generated from the OpenSubtitles 2024 dataset provided via OPUS (https://opus.nlpl.eu/datasets/OpenSubtitles). The dataset is licensed under ODC-BY (Open Data Commons Attribution License) and requires attribution when redistributed.
