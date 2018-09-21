# Header

A header bar is a navigation header that is placed at the top of the page.

## Usage {#usage}

```text
import React from 'react'
import styles from './styles'
import Header from '../index'
var view = function () {
    const {data} = this.state
    return (
        <Header
            {...data}
            titleStyle={[styles.white]}
            headerStyle={[styles.header]}
            leftContentStyle={[styles.white]}
            rightContentStyle={[styles.white]}
        />
    )
}
module.exports = view

```

## Supported properties {#supported-properties}

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| data | data to be shown in header | object | - |
| titleStyle | to add custom styles to page title | object | - |
| headerStyle | to add custom styles to header | object | - |
| leftContentStyle | styling left side content of header | object | - |
| rightContentStyle | styling right side content of header | object | - |



