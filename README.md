<p align="center">
  <img src="https://github.com/DieTime/react-native-date-picker/raw/master/assets/logo.png" style="margin-bottom: -30px" width="320"/>
</p>

<p align="center">
    <img src="https://img.shields.io/npm/types/@dietime/react-native-date-picker" alt="npm type definitions"/>
</p>

React Native customizable date picker component for iOS, Android and Web. Designed using ScrollView. Looks identical on all
devices.

## 💻 Example
<img style="margin-top: 10px" src="https://github.com/DieTime/react-native-date-picker/raw/master/assets/example.gif" height="400" alt="component-gif-preview"/>

## 💬 Installation

1. *Add dependencies to the project*

    ```bash
    yarn add git+https://github.com/51m0n397/react-native-date-picker.git
    
    npm install git+https://github.com/51m0n397/react-native-date-picker.git --save
    ```

2. *Install additional dependencies*

    ```bash
    yarn add react-native-linear-gradient
    
    npm install react-native-linear-gradient --save
    ```
    2.b. (Optional) *For web support, install additional dependencies*

    ```bash
    yarn add react-native-web-linear-gradient
    
    npm install react-native-web-linear-gradient --save
    ```
    *and alias the package in your webpack config*
    
    ```javascript
    resolve: {
        alias: {
            'react-native': 'react-native-web',
            ...
            'react-native-linear-gradient': 'react-native-web-linear-gradient',
        }
    }
    ```

3. *Then, import with ...*

    ```js
    import DatePicker from 'react-native-date-picker';
    ```


## 👩‍💻 Usage

- *Simple code example*
    ```javascript
    import React, {useState} from "react";
    import {Text, View} from "react-native";
    
    import DatePicker from "react-native-date-picker";
    
    export default function App() {
        const [date, setDate] = useState();
    
        return (
            <View>
                <Text>{date ? date.toDateString() : "Select date..."}</Text>
                <DatePicker
                    value={date}
                    onChange={(value) => setDate(value)}
                    format="yyyy-mm-dd"
                />
            </View>
        );
    }
    ```

## 📚 Documentation

| Prop       | Required | Type                      | Description                                                   |
|:---------- |:--------:|:------------------------- | ------------------------------------------------------------- |
| value      | ✅        | Date or null or undefined | Initial date for component                                    |
| onChange   | ✅        | (value: Date) : void      | Callback on date change event                                 |
| height     | ⛔        | number                    | Custom component height                                       |
| width      | ⛔        | number or string          | Custom component width such as `100` or `'50%'`                   |
| fontSize   | ⛔        | number                    | Custom digits font size                                       |
| textColor  | ⛔        | string                    | Custom digits text color such as hex, rgb or rgba             |
| endYear    | ⛔        | number                    | Max year in component, default is current year                |
| startYear  | ⛔        | number                    | Min year in component, default is `endYear - 100`             |
| markColor  | ⛔        | string                    | Custom middle mark color such as `hex`, `rgb` or `rgba`             |
| markHeight | ⛔        | number                    | Custom height of middle mark                                  |
| markWidth  | ⛔        | number or string          | Custom width of middle mark such as `100` or `'50%'`              |
| fadeColor  | ⛔        | string                    | Custom color for top and bottom fade effect `only hex colors!` |
| format     | ⛔        | string                    | Custom picker format like reshuffle of `yyyy`, `mm`, `dd`. Example: `'yyyy-mm-dd'` or `'dd-mm-yyyy'` and other |

## 📂 Project Layout

- [`example`](/example) *Simple project with date picker. It is presented on gif.*
- [`src`](/src) *Source code of date picker.*
- [`lib`](/lib) *Shared packages.*
    - [`commonjs`](/lib/commonjs) *Package built as common js library.*
    - [`module`](/lib/module) *Package built as module.*
    - [`typescript`](/lib/typescript) *Built files for static typing.*

## 📃 License

Source code is made available under the [MIT license](LICENSE.md). Some dependencies may be licensed differently.

## ☕ Support

You can support me so that there will be more good open source projects in the future
<p align="center" style="padding: 10px 0 20px 0">
  <a href="https://www.buymeacoffee.com/glazzkoff" target="_blank">
    <img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="50" width="220">
  </a>
</p>
