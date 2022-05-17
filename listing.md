# Adding a model to the list of electrophysiology models

_You've got a model in the repository, and now you want it to show up in the [list of electrophysiology models](https://models.physiomeproject.org/electrophysiology)._

## Step 1: Adding meta data

You'll need to make sure your model code includes meta data identifying it as an "electrophysiology" model.
In CellML 1.0/1.1, this is done by

1. Ensuring your model has a `cmeta:id` attribute with some unique id:

```
<model name="best_model" 
  xmlns="http://www.cellml.org/cellml/1.0#"
  xmlns:cmeta="http://www.cellml.org/metadata/1.0#"
  cmeta:id="MODEL_ID_GOES_HERE">
```

2. Adding some RDF elements into your CellML model:

```
<model ... >
...
  <rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#" 
           xmlns:bqs="http://www.cellml.org/bqs/1.0#" 
           xmlns:dc="http://purl.org/dc/elements/1.1/">
    <rdf:Description rdf:about="#MODEL_ID_GOES_HERE">
      <bqs:reference rdf:parseType="Resource">
        <dc:subject rdf:parseType="Resource">
          <bqs:subject_type>keyword</bqs:subject_type>
          <rdf:value>
            <rdf:Bag>
              <rdf:li>electrophysiology</rdf:li>
            </rdf:Bag>
          </rdf:value>
        </dc:subject>
      </bqs:reference>
    </rdf:Description>
  </rdf:RDF>
</model>
```

Note that the `cmeta:id` attribute does _not_ have a hash (#) before the id, while the `rdf:about` attribute does.

## Step 2: (Re-)Uploading your model

1. If you haven't done so already, you'll need to create or fork a ~github repository~ workspace (see [creating.md](./creating.md) or [updating.md](./updating.md))

2. The new model with the RDF data will need to be uploaded.

3. Finally, a new ~a git tag~ an exposure will need to be made and set to public (see [the official guide](https://aucklandphysiomerepository.readthedocs.io/en/latest/quickstart.html) or [updating.md](./updating.md))

When creating an exposure, you can select documentation for the exposure itself, and for each individual model file.
The ephys list will always link directly to your model file, so it's best to associate the docs with the model file, not with the top-level exposure.
[See here](https://github.com/PMR2/models.physiomeproject.org/issues/49#issuecomment-1128186052).
