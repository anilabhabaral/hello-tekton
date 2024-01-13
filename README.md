- Create Tasks and pipeline:
```
$ oc apply -f .infra/
```
- Run Pupeline:
```
$ tkn pipeline start anil-maven-test-pipeline \
    -w name=test01,volumeClaimTemplateFile=https://raw.githubusercontent.com/openshift/pipelines-tutorial/master/01_pipeline/03_persistent_volume_claim.yaml \
    --use-param-defaults
```
