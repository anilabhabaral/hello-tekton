- Create Tasks and pipeline:
```
$ oc apply -f .infra/
```
- Run Pupeline:
```
$ tkn pipeline start anil-maven-test-pipeline \
    -w name=test01,volumeClaimTemplateFile=https://raw.githubusercontent.com/anilabhabaral/hello-tekton/main/.infra/pvc/pvc-anil.yaml \
    --use-param-defaults
```
