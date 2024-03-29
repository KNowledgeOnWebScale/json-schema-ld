# Supported JSON Schema keywords


| JSON Schema Keyword | RDF vocabulary                        | RDF data shape                  | Comment                                                                    |
|---------------------|---------------------------------------|---------------------------------|----------------------------------------------------------------------------|
| "id/$id"            | `jsonsc-ld:Schema`                    |                                 | a unique identifier for a JSON schema                                      |
| "$schema"           |                                       |                                 | defines which dialect of JSON Schema a JSON Schema was written for         |
| "type": "string"    | `ex:property rdfs:range xsd:string.`  | `[sh:datatype xsd:string]`      | string-type schema                                                         |
| "type": "number"    | `ex:property rdfs:range xsd:decimal.` | `[sh:datatype xsd:decimal]`     | accepts any numeric type, either integers or floating point numbers        |
| "type": "integer"   | `ex:property rdfs:range xsd:integer.` | `[sh:datatype xsd:integer]`     | accepts any numeric type, either integers or floating point numbers        |
| "type": "object"    | `ex:property rdf:type rdf:Property.`  | `[sh:path ex:property]`         | a base schema in which other type schemas wrapped                          |
| "type": "array"     |                                       |                                 | similar to object type schema                                              |
| "type": "boolean"   | `ex:property rdfs:range boolean.`     | `[sh:datatype xsd:boolean]`     | boolean-type schema                                                        |
| "type": "null"      |                                       |                                 | accepts only "null" value.                                                 |
| "title"             | `dcterms:title`                       | `sh:name`                       |                                                                            |
| "description"       | `dcterms:description`                 | `sh:description`                |                                                                            |
| "comment"           | `rdfs:comment`                        | `rdfs:comment`                  |                                                                            |
| "example"           | `skos:example`                        | `skos:example`                  |                                                                            |
| "deprecated"        | `owl:deprecated`                      | `owl:deprecated`                |                                                                            |
| "readonly"          | `jsonsc:readOnly`                     | `jsonsc:readOnly`               |                                                                            |
| "writeonly"         | `jsonsc:writeOnly`                    | `jsonsc:writeOnly`              |                                                                            |
| "const"             |                                       | `sh:hasValue`                   | has a constant value                                                       |
| "minLength"         |                                       | `sh:minLength`                  |                                                                            |
| "maxLength"         |                                       | `sh:maxLength`                  |                                                                            |
| "pattern"           |                                       | `sh:pattern`                    | sh:pattern can be only applied to a shape that are literals with datatype  |
|                     |                                       |                                 | xsd:string                                                                 |
| "format"            |                                       | `sh:datatype`                   | "date-time": "xsd:dateTime", "time": "xsd:time", "date": "xsd:date",       |
|                     |                                       |                                 | "idn-email": "schema:email", "hostname": "xsd:string",                     |
|                     |                                       |                                 | "idn-hostname": "xsd:string", "ipv4": "xsd:string", "ipv6": "xsd:string",  | 
|                     |                                       |                                 | "uuid": "uuidType", "uri": "xsd:anyURI", "uri-reference": "xsd:string",    |
|                     |                                       |                                 | "iri": "xsd:string", "iri-reference":"xsd:string",                         |
|                     |                                       |                                 | "uri-template": "xsd:string", "json-pointer": "xsd:string",                |
|                     |                                       |                                 | "relative-json-pointer": "xsd:string", "regex": "jsonsc:pattern"           |
| "minItems"          |                                       | `sh:minCount`                   |                                                                            |
| "maxItems"          |                                       | `sh:maxCount`                   |                                                                            |
| "enum"              |                                       | `skos:Concept`                  | each element in the enum array is of type skos:Concept.                    |
| "minimum"           |                                       | `sh:minInclusive`               |                                                                            |
| "exclusiveMinimum"  |                                       | `sh:minExclusive`               |                                                                            |
| "maximum"           |                                       | `sh:maxInclusive`               |                                                                            |
| "exclusiveMaximum"  |                                       | `sh:maxExclusive`               |                                                                            |
| "required"          |                                       | `sh:minCount 1` `sh:maxCount 1` |                                                                            |
| "not"               |                                       | `sh:not`                        |                                                                            |
| "allOf"             |                                       | `sh:and`                        |                                                                            |
| "oneOf"             |                                       | `sh:xone`                       |                                                                            |
| "anyOf"             |                                       | `sh:or`                         |                                                                            |
