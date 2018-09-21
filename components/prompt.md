# Prompt

A Prompt component is useful when you need to ask for some quick information from a user.

## Usage {#usage}

```text
import React from 'react'
import styles from './styles'
import {View, Text, Alert} from 'react-native'
import Button from '../../button'
import prompt from '../index'

var view = function () {
    return (
        <View style={[styles.container]}>
            <View style={[styles.section]}>
                <Button
                    onClick={async () => {
                        let value = await prompt('Your information', 'Please enter your info')
                        alert(value)
                    }} 
                    type={'bordered'} 
                    text={'Show Prompt'}
                />
            </View>
        </View>
    )
}
module.exports = view

```

## Supported properties {#supported-properties}

#### prompt\(title, message, callbackOrActions, type?, defaultValue?\) {#Modal.prompt(title,-message,-callbackOrActions,-type?,-defaultValue?)}

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| title | title of the prompt modal | string or React.Element | - |
| message | message | string or React.Elemen | - |
| callbackOrActions | button group {text, onPress} or callback | Array or Function | - |
| type | prompt style | String \(`default`, `secure-text`, `login-password`\) | `default` |



