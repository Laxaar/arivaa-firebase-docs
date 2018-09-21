# Footer

Place the footer at the bottom of the page to add an additional navigation for the application.

## Usage {#usage}

```text
import React from 'react'
import Footer from '../index'

var view = function () {
    const {data} = this.state
    return (
        <Footer data={data}/>
    )
}
module.exports = view

```

## Supported properties {#supported-properties}

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| data | list of links to be shown in footer | array | - |



