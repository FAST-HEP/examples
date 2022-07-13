# CMS Level 1 Trigger analysis

To run:

```bash
fasthep download --json cms/l1t/remote_data.json --destination data/cms/l1t

fast_carpenter \
  --outdir=output/cms/l1t \
  cms/l1t/cms_l1t_data.yml \
  cms/l1t/cms_l1t_processing.yml
```

or (via `fast-cli`):
```
fasthep carpenter cms/l1t/cms_l1t_data.yml cms/l1t/cms_l1t_processing.yml -o output/cms/l1t
```
