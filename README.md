# \<lazy-page-manager\>

---

基於yaml&json文檔的頁面管理模組



## Example

```
	<lazy-page-manager id="manager" default-path="/home/list"></lazy-page-manager>
```

## Doc Example (yaml)

```
info:
  title: 123
build: dev
config: 
  global:
    #共用參數
    status: 123123123
  dev:
    #測試主機用的config
  publish:
    #正式機使用的config
elementsDir: apps
defaultPath: /home
roles:
sitemap:
  - pattern: /home
    ele: x-home
    fragments:
      - x-home-header
      - x-home-footer
    pages: 
      - pattern: /list
        ele: x-home-list
        pages:
          - pattern: /detail
            ele: x-home-detail
            dialog: true
      - pattern: /list1
        ele: x-home-list
      - pattern: /list2
        ele: x-home-list
      - pattern: /detail
        ele: x-home-detail
        dialog: true

```

## API

`TODO`


## Lifecycle
```
import
|
active
|----> animaion-finish
|    |-----> lazy-pages-start


unactive
|<FALSE>|-----> end
|<TRUE> |-----> animaion-finish
```



## TODO

* 瀏覽器上&下一頁的狀態判斷(苦手中…)
