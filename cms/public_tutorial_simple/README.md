# CMS Public HEP Tutorial

An example of the public CMS tutorial can be found on [CERN Gitlab](https://gitlab.cern.ch/fast-hep/public/fast_cms_public_tutorial/).

It implements the following workflow:

```mermaid
graph LR;
    input_files([download input files])
    curator([run fast-curator])
    carpenter([run fast-carpenter])
    plotter([run fast-plotter])
    input_files --> curator
    curator --> carpenter
    carpenter --> plotter
```

The corresponding Github actions workflow is available in [.github/workflows/cms-tutorial.yml](https://github.com/FAST-HEP/examples/blob/main/.github/workflows/cms-tutorial.yml)

## To run

```bash
EXAMPLE=cms/public_tutorial_simple
# download input data
fasthep download --json ${EXAMPLE}/remote_data.json --destination data/${EXAMPLE}
# make sure extra python modules can be found
export PYTHONPATH=$PWD/${EXAMPLE}:$PYTHONPATH

fasthep carpenter ${EXAMPLE}/data.yml ${EXAMPLE}/processing.yml -o output/${EXAMPLE} --backend=local
```
