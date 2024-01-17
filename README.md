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

- To create a trigger for github PUSH events use the follwing commands one by one:
```
$ oc apply -f .infra/trigger/template.yaml

$ oc apply -f .infra/trigger/binding.yaml

$ oc apply -f .infra/trigger/trigger.yaml

$ oc apply -f .infra/trigger/event-listener.yaml

```