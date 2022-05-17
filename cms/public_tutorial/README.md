An example of the public CMS tutorial can be found on https://gitlab.cern.ch/fast-hep/public/fast_cms_public_tutorial/.

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

The corresponding Github actions workflow is available on https://github.com/FAST-HEP/examples/blob/main/.github/workflows/cms-tutorial.yml