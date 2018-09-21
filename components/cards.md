# Cards

A card is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content.We provide a ready made image and list cards since they are most commonly used. Even if you want to create your own custom card, You can use our primary card component.

![](../.gitbook/assets/card.gif)

## Usage {#usage}

```text
import React from "react";
import styles from "./styles";
import {View} from "react-native";
import SimpleCard from "../../card";
import ImageCard from "../imageCard";
import ListCard from "../listCard";
import Config from "./config";
import {getImage, getRandom} from "../../util";
var view = function () {
    return (
        <View style={[styles.container]}>
            <SimpleCard
                cardStyle={[styles.cardStyle]}
                headerContent={getRandom("text")}
                bodyContent={getRandom("paragraph")}
                footerContent={getRandom("text")}
            />
            <ListCard
                headerContent={'Contact List'}
                data={getRandom("contacts").map((contact, index) => {
                    return {
                        key: index,
                        title: contact.name,
                        subTitle: contact.phone,
                        image: getImage(contact.avatar)
                    }
                })}
            />
            <ImageCard
                cardStyle={[styles.cardStyle]}
                image={getRandom("image")}
                imageStyles={styles.imageStyles}
                overlay={true}
                overlayTitle={getRandom("text")}
                overlaySubTitle={getRandom("text")}
                footerItems={Config.footerItems}
            />
        </View>
    )
}
module.exports = view;
```

## Supported properties {#supported-properties}

#### Simple Card Properties

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| headerContent | content to be shown in card header | string \| node | null |
| bodyContent | content to be shown inside card | string \| node | null |
| footerContent | content to be shown in card footer | string \| node | null |
| cardStyle | styling of the card  | object | - |

#### List Card Properties

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| headerContent | content to be shown in card header | string \| node | null |
| cardStyle | styling of the card  | object | - |
| data | list of data to be shown in rows | JSON | - |

#### Image Card Properties

| Properties | Descrition | Type | Default |
| :--- | :--- | :--- | :--- |
| headerContent | content to be shown in card header | string \| node | null |
| cardStyle | styling of the card  | object | - |
| image | image source  | string | - |
| imageStyles | adding custom styles to image | object | - |
| overlay | to show overlay over the image | boolean | false |
| overlayTitle | title of the overlay content | string \| node | - |
| overlaySubTitle | sub title of the overlay content  | string \| node | - |
| footerItems | list of links to be shown in footer   | array | - |



