# Apache HTTP Serve (httpd) S2I Sample Application



The application serves a single static html page via httpd.

To build and run the application:

```
$ s2i build https://github.com/xgoss/httpd-ex centos/httpd-24-centos7 myhttpdimage
$ docker run -p 8080:8080 myhttpdimage
$ # browse to http://localhost:8080
```

`$ oc new-app centos/httpd-24-centos7~https://github.com/xgoss/httpd-ex`


You can also build and deploy the application on OpenShift, assuming you have a
working `oc` command line environment connected to your cluster already:
You can also deploy the sample template for the application:

`$ oc new-app -f https://raw.githubusercontent.com/xgoss/httpd-ex/master/openshift/templates/httpd.json`r
