<p align="center">
  <a href="https://travis-ci.org/ElemeFE/element">
    <img src="https://travis-ci.org/ElemeFE/element.svg?branch=master">
  </a>
  <a href="https://coveralls.io/github/ElemeFE/element?branch=master">
    <img src="https://coveralls.io/repos/github/ElemeFE/element/badge.svg?branch=master">
  </a>
  <a href="https://cdnjs.com/libraries/shinho-sh-ui">
    <img src="https://img.shields.io/cdnjs/v/shinho-sh-ui.svg">
  </a>
  <a href="https://www.npmjs.org/package/shinho-sh-ui">
    <img src="https://img.shields.io/npm/v/shinho-sh-ui.svg">
  </a>
  <a href="https://npmcharts.com/compare/shinho-sh-ui?minimal=true">
    <img src="http://img.shields.io/npm/dm/shinho-sh-ui.svg">
  </a>
  <br>
  <a href="http://img.badgesize.io/https://unpkg.com/shinho-sh-ui/lib/index.js?compression=gzip&label=gzip%20size:%20JS">
    <img src="http://img.badgesize.io/https://unpkg.com/shinho-sh-ui/lib/index.js?compression=gzip&label=gzip%20size:%20JS">
  </a>
  <a href="http://img.badgesize.io/https://unpkg.com/shinho-sh-ui/lib/theme-chalk/index.css?compression=gzip&label=gzip%20size:%20CSS">
    <img src="http://img.badgesize.io/https://unpkg.com/shinho-sh-ui/lib/theme-chalk/index.css?compression=gzip&label=gzip%20size:%20CSS">
  </a>
  <a href="#backers">
    <img src="https://opencollective.com/element/backers/badge.svg">
  </a>
  <a href="#sponsors">
    <img src="https://opencollective.com/element/sponsors/badge.svg">
  </a>
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg">
  </a>
</p>

> A Vue.js 2.0 UI Toolkit for Web.

本项目是在element-ui 基础上，进行定制化开发。更名为shinho-sh-ui。

## Links
- Homepage and documentation
  - [International users](https://shinhotech.github.io/element/#/en-US)
  - [Chinese users](https://shinhotech.github.io/element/#/zh-CN)
  - [Spanish users](https://shinhotech.github.io/element/#/es)
  - [French users](https://shinhotech.github.io/element/#/fr-FR)
- [awesome-element](https://github.com/ElementUI/awesome-element)
- [FAQ](./FAQ.md)
- [Vue.js 3.0 migration](https://github.com/element-plus/element-plus)
- [Customize theme](http://element.eleme.io/#/en-US/component/custom-theme)
- [Preview and generate theme online](https://elementui.github.io/theme-chalk-preview)
- [Element for React](https://github.com/elemefe/element-react)
- [Element for Angular](https://github.com/ElemeFE/element-angular)
- [Atom helper](https://github.com/ElemeFE/element-helper)
- [Visual Studio Code helper](https://github.com/ElemeFE/vscode-element-helper)
- Starter kit
  - [element-starter](https://github.com/ElementUI/element-starter)
  - [element-in-laravel-starter](https://github.com/ElementUI/element-in-laravel-starter)
- [Design resources](https://github.com/ElementUI/Resources)
- Gitter
  - [International users](https://gitter.im/element-en/Lobby)
  - [Chinese users](https://gitter.im/ElemeFE/element)

## Install
```shell
npm install shinho-sh-ui -S
```

## Quick Start
``` javascript
import Vue from 'vue'
import Element from 'shinho-sh-ui'

Vue.use(Element)

// or
import {
  Select,
  Button
  // ...
} from 'shinho-sh-ui'

Vue.component(Select.name, Select)
Vue.component(Button.name, Button)
```
For more information, please refer to [Quick Start](https://shinhotech.github.io/element/#/en-US/component/quickstart) in our documentation.

## Browser Support
Modern browsers and Internet Explorer 10+.

## Changelog
Detailed changes for each release are documented in the [release notes](https://github.com/shinhotech/element/releases).

## FAQ
We have collected some [frequently asked questions](https://github.com/ElemeFE/element/blob/master/FAQ.md). Before reporting an issue, please search if the FAQ has the answer to your problem.

## Contribution
Please make sure to read the contributing guide ([中文](https://github.com/ElemeFE/element/blob/master/.github/CONTRIBUTING.zh-CN.md) | [English](https://github.com/ElemeFE/element/blob/master/.github/CONTRIBUTING.en-US.md) | [Español](https://github.com/ElemeFE/element/blob/master/.github/CONTRIBUTING.es.md) | [Français](https://github.com/ElemeFE/element/blob/master/.github/CONTRIBUTING.fr-FR.md)) before making a pull request.

[![Let's fund issues in this repository](https://issuehunt.io/static/embed/issuehunt-button-v1.svg)](https://issuehunt.io/repos/67274736)

## LICENSE
[MIT](LICENSE)
