# confluent-schema-contexts

## Test Producer with different context

### Default Context

```bash
confluent kafka topic produce test-context --value-format avro --schema schema-coffee-v1.avsc --parse-key --delimiter , --sr-endpoint https://psrc-1w11j.eu-central-1.aws.confluent.cloud/contexts/:.: --sr-api-key KZNDDZSS2HA75NUS --sr-api-secret 3i9h28nVub8ZX/QsAc5uA003TlzTbzz6unCNUeum1sGpgjmtyv8Xx714DTsDVGIQ
```

Sample Message:

```bash
1, {"drink": "coffee"}
```

### Custom context (context1)

```bash
confluent kafka topic produce test-context --value-format avro --schema schema-context1-coffee-v1.avsc --parse-key --delimiter , --sr-endpoint https://psrc-1w11j.eu-central-1.aws.confluent.cloud/contexts/.context1 --sr-api-key KZNDDZSS2HA75NUS --sr-api-secret 3i9h28nVub8ZX/QsAc5uA003TlzTbzz6unCNUeum1sGpgjmtyv8Xx714DTsDVGIQ
```

Sample Message:

```bash
2, {"coffee": "coffee expresso", "number": 1}
```

### Custom context (context2)

```bash
confluent kafka topic produce test-context --value-format avro --schema schema-context2-tea-v1.avsc --parse-key --delimiter , --sr-endpoint https://psrc-1w11j.eu-central-1.aws.confluent.cloud/contexts/.context2 --sr-api-key KZNDDZSS2HA75NUS --sr-api-secret 3i9h28nVub8ZX/QsAc5uA003TlzTbzz6unCNUeum1sGpgjmtyv8Xx714DTsDVGIQ
```

Sample Message:

```bash
3, {"tea": "tea expresso", "number": 2, "description": "hot"}
```
