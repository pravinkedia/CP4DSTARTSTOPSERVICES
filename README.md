# CP4DSTARTSTOPSERVICES

## How to Stop the CP4D Services

### Stop the Deployments

oc scale --replicas=0 deployment  zen-audit zen-core zen-core-api zen-data-sorcerer  zen-watchdog zen-watcher  ibm-nginx ibm-dmc-addon-api ibm-dmc-addon-ui  iis-services iis-xmetarepo igc-ui-react  metadata-discovery jobs-api  jobs-ui  ia-analysis dv-addon dsx-influxdb cpd-install-operator catalog-api  dc-main  dmc-0-1614155349588655-ibm-dmc-admin dmc-0-1614155349588655-ibm-dmc-dbapi  dmc-0-1614155349588655-ibm-dmc-explain  dmc-0-1614155349588655-ibm-dmc-job-scheduler  dmc-0-1614155349588655-ibm-dmc-job-scheduler  dmc-0-1614155349588655-ibm-dmc-nginx  dmc-0-1614155349588655-ibm-dmc-registry-manager  dmc-0-1614155349588655-ibm-dmc-runsql ds-nginx-proxy  dsx-influxdb wkc-glossary-service wkc-gov-ui  wkc-metadata-imports-ui  wkc-search  wkc-workflow-service icpd-till   dv-api dv-caching dv-service-provider  dv-unified-console  event-logger-api dataview-api-service dap-dashboards-api redis-ha-haproxy usermgmt spaces  ds-entitlement asset-files-api audit-trail-service  ax-environments-api-deploy ax-environments-ui-deploy bigsql-addon  bigsql-service-provider dataconn-engine-opdiscovery dataconn-engine-service  dataconn-engine-service  dataconn-engine-spark-cluster  gov-admin-ui  gov-app-config-service  gov-catalog-search-index gov-catalog-search-service  gov-enterprise-search-ui gov-insights-service  gov-quality-ui  gov-ui-commons gov-user-prefs-service  gremlin-console ngp-projects-api  odf-fast-analyzer omag  portal-catalog  portal-common-api   portal-dashboards portal-job-manager  portal-main  portal-notifications spawner-api finley-ml wdp-activities  wdp-connect-connection wdp-connect-connector wdp-dataprep  wdp-dataview wdp-lineage  wdp-policy-service wdp-profiling wdp-profiling-messaging  wdp-profiling-ui wdp-search  wdp-shaper wml-main

### Stop the StatefullSets

oc scale --replicas=0 sts cassandra dmc-0-1614155349588655-ibm-dmc-monitor dmc-0-1614155349588655-ibm-redis-server ds-engine-compute  dv-engine  dv-metastore dv-utils elasticsearch-master is-en-conductor is-engine-compute kafka  rabbitmq-ha  redis-ha-server shop4info-event-consumer shop4info-mappers-service  shop4info-mappers-wkc shop4info-rest shop4info-scheduler shop4info-type-registry-service  wdp-couchdb wdp-db2 zookeeper dv-worker zen-metastoredb rabbitmq-ha redis-ha-server wdp-couchdb elasticsearch-master

## How to Start the CP4D Services

### Start the Deployments

oc scale --replicas=1 deployment  zen-audit zen-core zen-core-api zen-data-sorcerer  zen-watchdog zen-watcher  ibm-nginx ibm-dmc-addon-api ibm-dmc-addon-ui  iis-services iis-xmetarepo igc-ui-react  metadata-discovery jobs-api  jobs-ui  ia-analysis dv-addon dsx-influxdb cpd-install-operator catalog-api  dc-main  dmc-0-1614155349588655-ibm-dmc-admin dmc-0-1614155349588655-ibm-dmc-dbapi  dmc-0-1614155349588655-ibm-dmc-explain  dmc-0-1614155349588655-ibm-dmc-job-scheduler  dmc-0-1614155349588655-ibm-dmc-job-scheduler  dmc-0-1614155349588655-ibm-dmc-nginx  dmc-0-1614155349588655-ibm-dmc-registry-manager  dmc-0-1614155349588655-ibm-dmc-runsql ds-nginx-proxy  dsx-influxdb wkc-glossary-service wkc-gov-ui  wkc-metadata-imports-ui  wkc-search  wkc-workflow-service icpd-till   dv-api dv-caching dv-service-provider  dv-unified-console  event-logger-api dataview-api-service dap-dashboards-api redis-ha-haproxy usermgmt spaces  ds-entitlement asset-files-api audit-trail-service  ax-environments-api-deploy ax-environments-ui-deploy bigsql-addon  bigsql-service-provider dataconn-engine-opdiscovery dataconn-engine-service  dataconn-engine-service  dataconn-engine-spark-cluster  gov-admin-ui  gov-app-config-service  gov-catalog-search-index gov-catalog-search-service  gov-enterprise-search-ui gov-insights-service  gov-quality-ui  gov-ui-commons gov-user-prefs-service  gremlin-console ngp-projects-api  odf-fast-analyzer omag  portal-catalog  portal-common-api   portal-dashboards portal-job-manager  portal-main  portal-notifications spawner-api finley-ml wdp-activities  wdp-connect-connection wdp-connect-connector wdp-dataprep  wdp-dataview wdp-lineage  wdp-policy-service wdp-profiling wdp-profiling-messaging  wdp-profiling-ui wdp-search  wdp-shaper wml-main

### Start the StatefullSets

oc scale --replicas=1 sts cassandra dmc-0-1614155349588655-ibm-dmc-monitor dmc-0-1614155349588655-ibm-redis-server ds-engine-compute  dv-engine  dv-metastore dv-utils elasticsearch-master is-en-conductor is-engine-compute kafka  rabbitmq-ha  redis-ha-server shop4info-event-consumer shop4info-mappers-service  shop4info-mappers-wkc shop4info-rest shop4info-scheduler shop4info-type-registry-service  wdp-couchdb wdp-db2 zookeeper

oc scale --replicas=2 sts dv-worker

oc scale --replicas=3 sts zen-metastoredb rabbitmq-ha redis-ha-server wdp-couchdb elasticsearch-master
