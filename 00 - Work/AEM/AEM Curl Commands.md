
### Uninstall a bundle

```
curl -u admin:admin -daction=uninstall http://localhost:4505/system/console/bundles/"name of bundle"
```

### Install a bundle

```
curl -u admin:admin -F action=install -F bundlestartlevel=20 -F 
bundlefile=@"name of jar.jar" http://localhost:4505/system/console/bundles
```

### Build a bundle

```
curl -u admin:admin -F bundleHome=/apps/centrica/bundles/name of bundle -F descriptor=/apps/centrica/bundles/com.centrica.cq.wcm.core-bundle/name_of_bundle.bnd http://localhost:4505/libs/crxde/build
```

Stop a bundle
        curl -u admin:admin http://localhost:4505/system/console/bundles/org.apache.sling.scripting.jsp 
        -F action=stop

Start a bundle
        curl -u admin:admin http://localhost:4505/system/console/bundles/org.apache.sling.scripting.jsp 
        -F action=start

Delete a node (hierarchy) - (this will delete any directory / node / site)
        curl -X DELETE http://localhost:4505/path/to/node/jcr:content/nodeName -u admin:admin

### Upload & Install package

```
curl -u admin:admin -F file=@"name of zip file" -F name="name of package" -F force=true -F install=true http://localhost:4505/crx/packmgr/service.jsp
```

### Upload DO NOT install package

```
curl -u admin:admin -F file=@"name of zip file" -F name="name of package" -F force=true -F install=false http://localhost:4505/crx/packmgr/service.jsp
```

Rebuild an existing package in CQ
        curl -u admin:admin -X POST http://localhost:4505:/crx/packmgr/service/.json/etc/packages/name_of_package.zip?cmd=build

Download (the package)
        curl -u admin:admin http://localhost:4505/etc/packages/export/name_of_package.zip > name of local package file

Upload a new package
        curl -u admin:admin -F package=@"name_of_package.zip" http://localhost:4505/crx/packmgr/service/.json/?cmd=upload

### Install an existing package

```
curl -u admin:admin -X POST http://localhost:4502/crx/packmgr/service/.json/etc/packages/export/name of package?cmd=install
```

Activate
        curl -u admin:admin -X POST -F path="/content/path/to/page" -F cmd="activate" http://localhost:4502/bin/replicate.json

Deactivate
        curl -u admin:admin -X POST -F path="/content/path/to/page" -F cmd="deactivate" http://localhost:4502/bin/replicate.json

Tree Activation
        curl -u admin:admin -F cmd=activate -F ignoredeactivated=true -F onlymodified=true 
        -F path=/content/geometrixx http://localhost:4502/etc/replication/treeactivation.html

Lock page
        curl -u admin:admin -X POST -F cmd="lockPage" -F path="/content/path/to/page" -F "_charset_"="utf-8" http://localhost:4502/bin/wcmcommand

Unlock page
        curl -u admin:admin -X POST -F cmd="unlockPage" -F path="/content/path/to/page" -F "_charset_"="utf-8" http://localhost:4502/bin/wcmcommand

Copy page
        curl -u admin:admin -F cmd=copyPage -F destParentPath=/path/to/destination/parent -F srcPath=/path/to/source/locaiton http://localhost:4502/bin/wcmcommand
        
Create Replication Agents
        curl -u admin:admin 'http://localhost:4502/bin/wcmcommand' -H 'Content-Type: application/x-www-form-urlencoded; charset=UTF-8' --data 'cmd=createPage&_charset_=utf-8&parentPath=/etc/replication/agents.author&title=ReplicationAgentTest&label=&template=/libs/cq/replication/templates/agent'
        
Modify Replication Agent
        curl -u admin:admin 'http://localhost:4502/etc/replication/agents.author/publish/jcr:content' 
        -H 'Content-Type: application/x-www-form-urlencoded; charset=UTF-8' 
        --data './sling:resourceType:cq/replication/components/agent
        ./jcr:lastModified:
        ./jcr:lastModifiedBy:
        _charset_:utf-8
        :status:browser
        ./jcr:title:Default Agent
        ./jcr:description:Agent that replicates to the default publish instance.
        ./enabled:true
        ./enabled@Delete:
        ./serializationType:durbo
        ./retryDelay:60001
        ./userId:
        ./logLevel:info
        ./reverseReplication@Delete:
        ./transportUri:http://localhost:4502/bin/receive?sling:authRequestLogin=1
        ./transportUser:admin
        ./transportPassword:{a2e783c38fce5db63df574b413a0820d557bb756e3bf5a6870f63fbfc3961e62}
        ./transportNTLMDomain:
        ./transportNTLMHost:
        ./ssl:
        ./protocolHTTPExpired@Delete:
        ./proxyHost:
        ./proxyPort:
        ./proxyUser:
        ./proxyPassword:
        ./proxyNTLMDomain:
        ./proxyNTLMHost:
        ./protocolInterface:
        ./protocolHTTPMethod:
        ./protocolHTTPHeaders@Delete:
        ./protocolHTTPConnectionClose@Delete:true
        ./protocolConnectTimeout:
        ./protocolSocketTimeout:
        ./protocolVersion:
        ./triggerSpecific@Delete:
        ./triggerModified@Delete:
        ./triggerDistribute@Delete:
        ./triggerOnOffTime@Delete:
        ./triggerReceive@Delete:
        ./noStatusUpdate@Delete:
        ./noVersioning@Delete:
        ./queueBatchMode@Delete:
        ./queueBatchWaitTime:
        ./queueBatchMaxSize:'