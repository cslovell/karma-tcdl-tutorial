## titles list.csv

### PyTransforms
#### _aggregation_uri_
From column: _BL Record ID_
>``` python
return blAggregationUri(getValue("BL Record ID"))
```

#### _source_reseource_uri_
From column: _BL Record ID_
>``` python
return blSourceResourceUri(getValue("BL Record ID"))
```

#### _collection_title_
From column: _Number in Series_
>``` python
return blCollectionTitle(getValue("Part of Series"),getValue("Number in Series"))
```

#### _collection_uri_
From column: _collection_title_
>``` python
return blCollectioncUri(getValue("collection_title"))
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _BL Record ID_ | `dct:identifier` | `dpla:SourceResource1`|
| _Date of Publication_ | `skos:prefLabel` | `edm:TimeSpan1`|
| _Physical Description_ | `dc:format` | `dpla:SourceResource1`|
| _Place of Publication_ | `skos:prefLabel` | `edm:Place1`|
| _Publisher_ | `dct:publisher` | `dpla:SourceResource1`|
| _Title Name_ | `dct:title` | `dpla:SourceResource1`|
| _aggregation_uri_ | `uri` | `ore:Aggregation1`|
| _collection_title_ | `dct:title` | `dctype:Collection1`|
| _collection_uri_ | `uri` | `dctype:Collection1`|
| _source_reseource_uri_ | `uri` | `dpla:SourceResource1`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `dpla:SourceResource1` | `dc:date` | `edm:TimeSpan1`|
| `dpla:SourceResource1` | `dct:isPartOf` | `dctype:Collection1`|
| `dpla:SourceResource1` | `dct:spatial` | `edm:Place1`|
| `ore:Aggregation1` | `edm:aggregatedCHO` | `dpla:SourceResource1`|
| `ore:Aggregation1` | `edm:dataProvider` | `xsd:British Library`|
