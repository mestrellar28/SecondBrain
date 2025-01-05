  
#### Guide
[Get your aem together with aem compose](https://wttech.blog/blog/2023/get-your-aem-together-with-aem-compose/)

#### Check health of AEM instances and dispatcher

```
sh taskw check
```
#### Destroy AEM instances and dispatcher

```
sh task destroy
```

#### Initialize project  

```
sh task init
```
#### Destroy then setup again AEM instances and dispatcher

```
sh taskw resetup
```

#### Restart AEM instances and dispatcher  

```
sh taskw restart
```

#### Setup AEM instances and dispatcher  

```
sh taskw setup
```

#### Start AEM instances and dispatcher (aliases: up)

```
sh taskw start
```

#### Check status of AEM instances and dispatcher

```
sh taskw status
```

#### Stop AEM instances and dispatcher (aliases: down)

```
sh taskw stop
```

#### Check health of AEM author instance

```
sh taskw aem:author:check
```

#### Build AEM application using Maven

```
sh taskw aem:build
```

#### Deploy AEM application

```
sh taskw aem:deploy
```

#### Destroy AEM instances

```
sh taskw aem:destroy
```

#### Provision AEM instances by installing packages and applying configurations (aliases: aem:configure)

```
sh taskw aem:provision
```

#### Check health of AEM publish instance

```
sh taskw aem:publish:check
```

#### Start and provision AEM instances then build and deploy AEM application

```
sh taskw aem:setup
```

#### Start AEM instances (aliases: aem:up)

```
sh taskw aem:start
```

#### Check status of AEM instances

```
sh taskw aem:status
```

#### Stop AEM instances (aliases: aem:down)

```
sh taskw aem:stop
```

#### Tail logs of AEM instances

```
sh taskw aem:tail
```

#### Tail logs of AEM author instance

```
sh taskw aem:tail:author
```

#### Tail logs of AEM publish instance

```
sh taskw aem:tail:publish
```

#### Build AEM dispatcher image

```
sh taskw dispatcher:build
```

#### Check health of AEM dispatcher

```
sh taskw dispatcher:check
```

#### Destroy AEM dispatcher

```
sh taskw dispatcher:destroy
```

#### Add AEM dispatcher domains to hosts file

```
sh taskw dispatcher:hosts
```

#### Login to AEM dispatcher shell

```
sh taskw dispatcher:login
```

#### Destroy then setup again AEM dispatcher

```
sh taskw dispatcher:resetup
```

#### Restart AEM dispatcher

```
sh taskw dispatcher:restart
```

#### Setup AEM dispatcher

```
sh taskw dispatcher:setup
```

#### Start AEM dispatcher using custom image (aliases: dispatcher:up)

```
sh taskw dispatcher:start
```

#### Check status of AEM dispatcher

```
sh taskw dispatcher:status
```

#### Stop AEM dispatcher (aliases: dispatcher:down)

```
sh taskw dispatcher:stop
```

#### Test AEM dispatcher image

```
sh taskw dispatcher:test
```