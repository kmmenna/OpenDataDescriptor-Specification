# OpenDataDescriptor Specification
The OpenDataDescriptor has as the main point describes data formats allowing the extraction of information with a semantic way, without making sense of the application or content of the data described.


## Characteristics

- ODD is not a parser, it describes how to parse something
- Low verbosity
- Only supports binary formats
- Support for static formats (size not depends of the data itself)
- Support for dynamic formats (the data changes size, for example, dynamic arrays)
- Declarative: besides segmenting the data, documenting the purpose


## Implemetation requirements:

- its not necessary the implementation knows how to interpret all the standard data formats
- Is prohibited extract data for a fomat small than original, for example, extract a int64 for a int32, but the oposite is permited
- The fallback for any format is a bit array, but must be always opt for the closest supported