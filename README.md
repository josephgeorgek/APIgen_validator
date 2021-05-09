# APIgen_validator

#  tutorials\

standards
https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.0.2.md#operationObject


To launch

https://github.com/OpenAPITools/openapi-style-validator

java -jar openapi-style-validator.jar -s ./path/to/spec.yaml -o ./path/to/options.json
java -jar openapi-style-validator-cli-1.6-all.jar -s swagger.json 

Example using the default output path for the jar (replace <version> with the current version):

java -jar modules/cli/build/libs/openapi-style-validator-cli-<version>-all.jar -s specs/petstore.yaml -o specs/options.json
Command Line
Parameter 	Required? 	Description
-s, -source 	yes 	The path to your json/yaml spec file
-o, -options 	no 	The path to your json options file
Options File

The options file is described in json (example in specs/options.json), and has the following possible values:
Option 	Type 	Possible Values 	Description
validateInfoLicense 	boolean 	true, false 	Ensures that there is a license section in the info section
validateInfoDescription 	boolean 	true, false 	Ensures that there is a description attribute in the info section
validateInfoContact 	boolean 	true, false 	Ensures that there is a contact section in the info section
validateOperationOperationId 	boolean 	true, false 	Ensures that there is an operation id for each operation
validateOperationDescription 	boolean 	true, false 	Ensures that there is a description for each operation
validateOperationTag 	boolean 	true, false 	Ensures that there is a tag for each operation
validateOperationSummary 	boolean 	true, false 	Ensures that there is a summary for each operation
validateModelPropertiesExample 	boolean 	true, false 	Ensures that the properties of the Schemas have an example value defined
validateModelRequiredProperties 	boolean 	true, false 	Ensures that all required properties of the Schemas are listed among their properties
validateModelNoLocalDef 	boolean 	true, false 	Not implemented yet
validateNaming 	boolean 	true, false 	Ensures the names follow a given naming convention
ignoreHeaderXNaming 	boolean 	true, false 	Exclude from validation header parameters starting with x-
pathNamingConvention 	string 	CamelCase, HyphenCase, UnderscoreCase, UnderscoreUpperCase, AnyCase 	Naming convention for paths
parameterNamingConvention 	string 	CamelCase, HyphenCase, UnderscoreCase, UnderscoreUpperCase, AnyCase 	Naming convention for parameters
headerNamingConvention 	string 	CamelCase, HyphenCase, UnderscoreCase, UnderscoreUpperCase, AnyCase 	Naming convention for headers
propertyNamingConvention 	string 	CamelCase, HyphenCase, UnderscoreCase, UnderscoreUpperCase, AnyCase 	Naming convention for properties
Supported Extensions
