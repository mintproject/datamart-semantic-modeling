### Annotate a dataset

`POST: /v1/annotate`

Inputs:

```json
{
    "ontologies": ["http://wikiba.se/ontology#"],
    "source": [
        {"name": "<column name>", "values": ["<value of the column in first row>", "<value of the column in second row>", "..."]}
    ]
}
```

Outputs:

```JSON
{
    "sm": {
        "<ont_class_id>": {
            "iri": "<uri of the ontology class>",
            "properties": [
                ["<ontology predicate 1>", "<column_index>"], 
                ["<ontology predicate 2>", "<column_index>"]
            ],
            "links": [
                ["<ontology predicate 1>", "<ont_class_id>"]
            ]
        }
    },
    "prefixes": {
        "<prefix>": "<url>"
    }
}
```

### Draw the semantic model

`POST: /v1/draw`

Inputs:

```JSON
{
    "sm": {
        "<ont_class_id>": {
            "iri": "<uri of the ontology class>",
            "properties": [
                ["<ontology predicate 1>", "<column_index>"], 
                ["<ontology predicate 2>", "<column_index>"]
            ],
            "links": [
                ["<ontology predicate 1>", "<ont_class_id>"]
            ]
        }
    },
    "prefixes": {
        "<prefix>": "<url>"
    },
    "columns": ["<name of column 1>", "<name of column 2>"]
}
```

Outputs: return an image (`image/png`)
