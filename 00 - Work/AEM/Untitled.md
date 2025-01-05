
Load Package

```
curl -u admin:admin -F file=@/path/to/package.zip -F name=large-package.zip http://localhost:4502/crx/packmgr/service.jsp?cmd=install
```

```
curl -u admin:admin -F file=@/Users/manuelestrella/Desktop/PalladiumHotel/PalladiumProMig.zip -F name=PalladiumProMig.zip http://localhost:4502/crx/packmgr/service.jsp
```


```
curl -u admin:admin -F cmd=install file=@/Users/manuelestrella/Desktop/PalladiumHotel/PalladiumProMig.zip http://localhost:4502/crx/packmgr/service.jsp
```

```
curl -u admin:admin -F cmd=install http://localhost:4502/crx/packmgr/service/.json/etc/packages/palladium-pro/test.zip
```


```
curl -u admin:admin -X POST "http://localhost:4502/crx/packmgr/service/console.html/etc/packages/PalladiumProMig.zip?cmd=contents"
```


List All Packages
```
curl -u admin:admin http://localhost:4502/crx/packmgr/list.jsp
```

Load and Install
```js
curl -u admin:admin -F file=@/Users/manuelestrella/Desktop/PalladiumHotel/PalladiumProMig.zip -F name="PalladiumProMig" -F force=true -F install=true http://localhost:4502/crx/packmgr/service.jsp
```

http://localhost:4502/libs/granite/core/content/login.html?resource=%2F&$$login$$=%24%24login%24%24&j_reason=unknown&j_reason_code=unknown

http://localhost:4502/libs/granite/core/content/login.html?resource=%2F&$$login$$=%24%24login%24%24&j_reason=unknown&j_reason_code=unknown