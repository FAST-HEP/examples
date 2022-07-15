# CMS Level 1 Trigger analysis

## To run

```bash
EXAMPLE=cms/l1t
fasthep download --json ${EXAMPLE}/remote_data.json --destination data/${EXAMPLE}

fast_carpenter \
  --outdir=output/${EXAMPLE} \
  ${EXAMPLE}/data.yml \
  ${EXAMPLE}/processing.yml
```

or (via `fast-cli`):

```bash
fasthep carpenter ${EXAMPLE}/data.yml ${EXAMPLE}/processing.yml -o output/${EXAMPLE}
```
