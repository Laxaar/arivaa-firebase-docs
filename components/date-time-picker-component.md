# Date Time

The Date Time component allow users to choose a date from the calendar and time from picker. It supports following types

1. `date`: It provides a calender to select date.
2. `time`: It provides a time picker to select time.
3. `datetime`: It provides a both calender and time pick to select date and time.

Date Time component has following display modes

1. `inline`: In this Component is rendered as a part of page \(default\).
2. `modal`: In this Component is rendered inside a modal window.

## Usage

```javascript
import React from "react";
import ArivaaDateTime from '../index'

var view = function () {
    return (
        <ArivaaDateTime
            visible={visible}
            type={'date'}
            value={value}
            onChange={onChange}
            displayMode="modal"
            onHide={this.onHide.bind(this)}
            onShow={this.onShow.bind(this)}
        />
    )
}

module.exports = view

```

## Supported Properties

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| visible | it is a boolean indicating whether Date Time Picker should visible or not \(for display as a modal purpose\) | boolean | false |
| type | `date`, `time` and `datetime` to show respective date and time views | string | `datetime` |
| value | it is a object of date which is selected by default \(points to current date\) if not passed or invalid value is passed. | object | - |
| onChange | it is a function called when user make changes to picker. It receives a parameter which is a object of date. | function | - |
| displayMode | it represents display mode of picker. Supported modes are `modal` and `inline`. | string | `modal` |
| onShow | it is a function called when date time picker becomes visible. | function | - |
| onHide | it is a function called when date time picker vanishes. | function | - |



