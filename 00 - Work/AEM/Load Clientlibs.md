
#### Load CSS and JS

![[css-and-js.png]]

#### Load only CSS

![[css.png]]

#### Cargar JS de forma asíncrona

![[js-async.png]]


#### Cargar JS de forma diferida

![[js-defer.png]]


```
<!--/* Load CSS and Defer JS */-->
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
categories=['naturgy.site'], defer=true}">
${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```