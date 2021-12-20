# mediaWiki Chart

MediaWiki helps you collect and organize knowledge and make it available to people.

## Chart Details

This helm chart is using SQLite DB as a backend database.

TODO: Add support for other DB.

## Installing the Chart

To install the chart:

```
[swapnil@bharshankar mediaWiki]$ helm install wiki-app . -f values.yaml -n <namespace>
NAME: wiki-app
LAST DEPLOYED: Mon Dec 20 20:10:00 2021
NAMESPACE: ns1
STATUS: deployed
REVISION: 1
NOTES:
Thank you for installing mediawiki.
1. Get the application URL by running these commands:
     NOTE: It may take a few minutes for the LoadBalancer IP to be available.
           You can watch the status of by running 'kubectl get --namespace <namespace> svc -w wiki-app-mediawiki'
  export SERVICE_IP=$(kubectl get svc --namespace <namespace> wiki-app-mediawiki --template "{{ range (index .status.loadBalancer.ingress 0) }}{{.}}{{ end }}")
  echo http://$SERVICE_IP:
[swapnil@bharshankar mediaWiki]$
```

To get mediaWiki UI. Fetch the IP using above command shown in NOTES section and access it from browser.

References:
[MediaWiki Documentation](https://www.mediawiki.org/wiki/MediaWiki "MediaWiki Webpage")

