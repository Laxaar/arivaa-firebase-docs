# Image

An image component with progress indicator for images in React Native.

![](../.gitbook/assets/screen-shot-2018-09-12-at-4.13.16-pm.png)

## Usage {#usage}

```text
import React from 'react'
import styles from './styles'
import Image from '../index'

var view = function () {
    return (
        <Image
            style={[styles.image]}
            source={'https://placeimg.com/300/300/any'}
        />
    )
}
module.exports = view

```

## Supported properties {#supported-properties}

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| source | image source  | string | - |
| style | passing custom style to image | object | - |



