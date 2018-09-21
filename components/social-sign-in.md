# Social Sign In

A Social Sign In component will help users to sign in or register using social platforms like Facebook or Google.

![](../.gitbook/assets/socialfb.gif)

## Usage

```jsx
import React from "react";
import SocialSignIn from "../index";

var view = function () {
    return (
       <SocialSignIn
            clientId = {Environment.FACEBOOK.appId}
            scopes = {
                Environment.FACEBOOK.scope
            }
            type = "facebook"
            triggerElement = {
                <Button text="Connect With Facebook" style={[styles.button, styles.facebookBtn]}
                        textStyle={[styles.facebookText]}/>
            }
            onSuccess = {(result)=>{this.handleSocialSignIn("facebook",result)}}
            onError = {(error)=>{this.handleSocialSignInError("facebook",error )}}
        />
    )
}
module.exports = view

```

## Supported Properties

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| clientId | client Id for the social provider | string | - |
| scopes | scope of the access required | array | - |
| type | type of social provider \(Only `facebook` and `google` are supported as of now\) | string | - |
| triggerElement | trigger Element to trigger the authentication. It should support onPress or onClick property which will be executed as a callback. | node | - |
| onSuccess | on successful authentication | function | - |
| onError | on error in authentication | function | - |



