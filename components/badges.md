# Badges

Badges are used to add show a numeric or boolean information \(mostly\) related to specific context like user, notifications, calls etc. We provide Avatar and Icon Badges by default and to create a custom badge according to use cases.

![](../.gitbook/assets/screen-shot-2018-09-12-at-1.30.40-pm.png)

## Usage {#supported-properties}

{% code-tabs %}
{% code-tabs-item title="Arivaa Badge Demo > view.js" %}
```text
import React from "react";
import styles from "./styles";
import ArivaaBadge from "../../badge";

var view = function () {
    return (
        <ArivaaBadge
            text={30}
            overflowCount={20}
            size={'large'}
            style={styles.badge}
            contentStyle={styles.badgeStyle}
            content={
                <View style={[styles.badgeContent]}>
                </View>
            }
        />
    )
}
module.exports = view

```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Supported properties {#supported-properties}

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| size | size of badge, optional: `large` `small` | string | small |
| ​text | text or number inside badge | ​string \| number | - |
| dot | show badge as a red dot | boolean | false |
| overflowCount | max count to show | number | `99` |
| style | styling of the badge | object | - |



