

<version>2.1.10.RELEASE</version> 
swagger and spring boot works only in this version. Recent versions have issue


###Mapping and Unmapping -- doing blue green deployment
➜  ~/dev/workspace/pcf/demo git:(master) ✗ cf apps | grep prabin
prabin-cf-demo-blue            started           1/1         768M     1G     prabin-cf-demo-blue-kind-nyala.cfapps.io
prabin-cf-demo-green           started           1/1         768M     1G     prabin-cf-demo.cfapps.io, prabin-cf-demo-green-shiny-cassowary.cfapps.io


cf unmap-route prabin-cf-demo-blue cfapps.io -n prabin-cf-demo
cf map-route prabin-cf-demo-green cfapps.io -n prabin-cf-demo
