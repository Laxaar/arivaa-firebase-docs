# Carousel

The carousel is a slide show for cycling through a series of content. It works with a series of images, text, or custom markup.

![](../.gitbook/assets/carousel%20%281%29.gif)

## Usage

```markup
import React from 'react'
import styles from './styles'
import {View, Text} from 'react-native'
import Carousel from '../index'
import {ImageCard} from '../../card'
import Icon from '../../icon'

var view = function () {
    let data = []
    for (let i = 0; i < 5; i++) {
        data.push({
            slide: (<ImageCard image={'https://placeimg.com/640/480/any'}/>),
            title: 'Slide Number ' + i
        })

    }

    return (
        <Carousel
            autoplay={false}
            selectedIndex={this.state.selectedIndex}
            data={data}
            previousArrow={<Icon type="ionicons" style={[styles.arrow]} name='ios-arrow-back-outline'/>}
            nextArrow={<Icon type="ionicons" style={[styles.arrow]} name='ios-arrow-forward-outline'/>}
            onChange={(index) => {
                alert('Slide changed to ' + index)
            }}
        />
    )
}
module.exports = view

```



## Supported properties {#supported-properties}

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| ​autoplay | ​autoplay mode active | ​boolean | ​false​ |
| ​data | data to be shown in slides | array | - |
| selectedIndex | current selected index | number | `0` |
| previousArrow | custom previous arrow | string \| node | - |
| nextArrow | custom next arrow | string \| node | - |
| onChange | on change slide event handler | function | - |



