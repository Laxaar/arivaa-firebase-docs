# Select

Select Component is a component which features a drop down list that enables users to select one or more items. It has following types

1. `dropdown`: In this, Drop Down list is opened as modal \(default\).
2. `picker`: In this, Drop Down list is opened at bottom of picker.

We can also customise it to whether user can select multiple items or not.

## Usage

```markup
import React from 'react'
import styles from './styles'
import {View} from 'react-native'
import Select from '../index.js'

var view = function () {
    const data = [{
        label: 'Item 1',
        value: 'Item 123'
    }, {
        label: 'Item 2',
        value: 'Item 2244'
    }, {
        label: 'Item 3',
        value: 'Item 324421'
    }]
    const value = 'Item 123'
    const onChange = (value) => {
        //alert(value);
    }
    return (
        <View style={[styles.container]}>            
            <Select
                data={data}
                multiple={true}
                value={[value]}
                onChange={onChange.bind(this)}
                type="dropdown"
            />
            <Select
                data={data}
                value={value}
                onChange={onChange.bind(this)}
                type="picker"
            />
        </View>
    )
}
module.exports = view

```

## Supported Properties

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| data | it is a array of objects having properties label and value of options which are to be shown to users. | array | - |
| multiple | it is a Boolean indicating whether user can choose multiple options or not. | boolean | false |
| value | it is a array of strings of values which are to be selected by default. | array | - |
| onChange | it is a function called when user make changes to selected items. | function | - |
| type | It is a string representing type of select component, Supported types of select components are `dropdown` and `picker`. | string | `dropdown` |



