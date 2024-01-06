# Websoft Algolia Search For PWA Studio (React js)

This package provides a `Algolia Search` with  `PWA Studio `of Magento.


## Installation

-To install this extension

First Move the `websoft-algolia-search` folder to `extension` Folder under root of `pwa` folder

add it as a `devDependency` to your app by below comand
`yarn add --dev link:extensions/websoft-algolia-search` 



-To Activate Auto Complete to the search

got to SearchBar component and override it by your favorite way and 

add this import 

```react
import {AutoComplete} from '@websoft/websoft-algolia-search/src/components/AutoComplete';
```

and remove all `Form` code from return and add instead `<AutoComplete />`


## Configuration

Go to this file

`pwa-root/extensions/websoft-algolia-search/src/config.js`

Open and edit you data

```react
export const algoliaConfig = {
    ALGOLIA_INDEX_NAME: 'magento_',
    ALGOLIA_APP_ID: 'xxxxxxxxxx',
    ALGOLIA_API_KEY: 'xxxxxxxxxxxxxxxxxxxxxxxxx',
};
```

## Extra Configuration

you need to define new filters as the current added, so, you have tow files 

- searchPage.js: like below
```react
    <Panel header={formatMessage({
                id: 'Color',
                defaultMessage: 'Color'
            })}>
        <RefinementList
        attribute="color"
        searchable={true}
        searchablePlaceholder=".."
        />
    </Panel>
```

- route.js: in these places

`createURL, routeToState, getStateMapping`


---------------------------------------------------------------------------------

## Screeshots


![AutoComplete](https://i.ibb.co/B2p5twz/Screenshot-2024-01-07-at-01-58-24.png)

![InstanceSearch](https://i.ibb.co/h8mhK22/Screenshot-2024-01-07-at-01-49-10.png)
