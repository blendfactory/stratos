# JSON Style Rules Specification

This document defines the details of JSON style rules used in the stratos_json package's JSON linter and formatter. These rules are used to ensure consistent formatting and readability of JSON files.

## JSON Style Rules Classification

Style rules are classified into the following categories:

1. **Format**: Rules related to indentation, whitespace, and line breaks
2. **Structure**: Rules related to the structure of JSON objects
3. **Naming**: Rules related to property naming conventions
4. **Value**: Rules related to value representation

## Format Rules

### F1. Indentation

#### F1.1 Indentation Style

- Key
  - `json.format.indentStyle`
- Description
  - Specifies the character type used for indentation
- Value
  - `space`
  - `tab`
- Default
  - `space`

#### F1.2 Indentation Width

- Key
  - `json.format.indentWidth`
- Description
  - Specifies the width of indentation
- Value
  - `2`
  - `4`
- Default
  - `2`

### F2. Line

#### F2.1 Line Ending Character

- Key
  - `json.format.lineEnding`
- Description
  - Specifies the line ending character
- Value
  - `lf`: LF ( `\n` )
  - `crlf`: CRLF ( `\r\n` )
  - `cr`: CR ( `\r` )
- Default
  - `lf`

#### F2.2 Line Width

- Key
  - `json.format.lineWidth`
- Description
  - Specifies the maximum number of characters per line
- Value
  - The maximum number of characters per line
- Default
  - `120`

### F3. Whitespace

#### F3.1 Trailing Whitespace

- Key
  - `json.format.trailingWhitespace`
- Description
  - Specifies how to handle unnecessary whitespace at the end of lines
- Value
  - `remove`
  - `allow`
- Default
  - `remove`

#### F3.2 Whitespace After Colon

- Key
  - `json.format.whitespaceAfterColon`
- Description
  - Specifies whether to include a space after a colon (e.g., `"name": "value"`)
- Value
  - `true`
  - `false`
- Default
  - `true`

#### F3.3 Whitespace After Comma

- Key
  - `json.format.whitespaceAfterComma`
- Description
  - Specifies whether to include a space after a comma
- Value
  - `true`
  - `false`
- Default
  - `true`

#### F3.4 Whitespace Inside Brackets

- Key
  - `json.format.whitespaceInsideBrackets`
- Description
  - Specifies how to handle whitespace immediately after or before brackets
- Value
  - `none`
  - `single`
- Default
  - `none`

### F4. Line Breaks

#### F4.1 Line Break After Object Start

- Key
  - `json.format.lineBreakAfterObjectStart`
- Description
  - Specifies whether to include a line break after the opening brace `{`
- Value
  - `true`
  - `false`
- Default
  - `true`

#### F4.2 Line Break Before Object End

- Key
  - `json.format.lineBreakBeforeObjectEnd`
- Description
  - Specifies whether to include a line break before the closing brace `}`
- Value
  - `true`
  - `false`
- Default
  - `true`

#### F4.3 Line Break After Array Start

- Key
  - `json.format.lineBreakAfterArrayStart`
- Description
  - Specifies whether to include a line break after the opening bracket `[`
- Value
  - `true`
  - `false`
- Default
  - `true`

#### F4.4 Line Break Before Array End

- Key
  - `json.format.lineBreakBeforeArrayEnd`
- Description
  - Specifies whether to include a line break before the closing bracket `]`
- Value
  - `true`
  - `false`
- Default
  - `true`

#### F4.5 Line Break Between Properties

- Key
  - `json.format.lineBreakBetweenProperties`
- Description
  - Specifies whether to include a line break between each property
- Value
  - `true`
  - `false`
- Default
  - `true`

### F5. Comma

#### F5.1 Trailing Comma

- Key
  - `json.format.trailingComma`
- Description
  - Specifies whether to allow a comma after the last element/property
    (prohibited in RFC 8259)
- Value
  - `allow`
  - `prohibit`
- Default
  - `prohibit`

#### F5.2 Comma Style

- Key
  - `json.format.commaStyle`
- Description
  - Specifies whether commas should be placed on the same line or at the
    beginning of the next line
- Value
  - `same`
  - `next`
- Default
  - `same`

## Structure Rules

### S1. Nesting

#### S1.1 Maximum Nesting Depth

- Key
  - `json.structure.maxNestingDepth`
- Description
  - Specifies the maximum depth for nested objects and arrays
- Value
  - Integer value representing maximum depth
- Default
  - `8`

#### S1.2 Simplification Recommendation

- Key
  - `json.structure.simplificationThreshold`
- Description
  - Specifies the threshold depth at which structure simplification is
    recommended
- Value
  - Integer value representing threshold depth
- Default
  - `6`

### S2. Property Order

#### S2.1 Alphabetical Order

- Key
  - `json.structure.alphabeticalOrder`
- Description
  - Specifies whether to order properties alphabetically
- Value
  - `true`
  - `false`
- Default
  - `false`

#### S2.2 Property Grouping

- Key
  - `json.structure.propertyGrouping`
- Description
  - Specifies whether to group semantically related properties
- Value
  - `true`
  - `false`
- Default
  - `false`

#### S2.3 Standard Properties First

- Key
  - `json.structure.standardPropertiesFirst`
- Description
  - Specifies whether to place standard properties (like `id`, `type`) at the
    beginning
- Value
  - `true`
  - `false`
- Default
  - `true`

### S3. Array Formatting

#### S3.1 Single Line Arrays

- Key
  - `json.structure.singleLineArrays`
- Description
  - Specifies the threshold for the number of items to place arrays on a single
    line
- Value
  - `threshold`: Maximum number of items for single line
- Default
  - `3`

#### S3.2 Multi-line Arrays

- Key
  - `json.structure.multiLineArrays`
- Description
  - Specifies whether to split long arrays across multiple lines
- Value
  - `true`
  - `false`
- Default
  - `true`

## Naming Rules

### N1. Property Name Format

#### N1.1 Naming Convention

- Key
  - `json.naming.convention`
- Description
  - Specifies the naming convention for property names
- Value
  - `camelCase`
  - `snake_case`
  - `kebab-case`
  - `PascalCase`
  - `none`
- Default
  - `camelCase`

#### N1.2 Consistency

- Key
  - `json.naming.consistency`
- Description
  - Specifies the required level of consistency in naming conventions within the
    same object
- Value
  - `strict`
  - `recommended`
  - `none`
- Default
  - `strict`

#### N1.3 Avoid Reserved Words

- Key
  - `json.naming.avoidReservedWords`
- Description
  - Specifies whether to avoid using JavaScript reserved words as property names
- Value
  - `true`
  - `false`
- Default
  - `true`

### N2. Property Name Constraints

#### N2.1 Length Limit

- Key
  - `json.naming.maxLength`
- Description
  - Specifies the maximum length for property names
- Value
  - Integer value representing maximum length
- Default
  - `50`

#### N2.2 Allowed Characters

- Key
  - `json.naming.allowedCharacters`
- Description
  - Specifies the set of characters allowed in property names
- Value
  - String pattern for allowed characters
- Default
  - `[a-zA-Z0-9_-]`

#### N2.3 Naming Pattern

- Key
  - `json.naming.pattern`
- Description
  - Specifies a regular expression pattern for property names
- Value
  - Regular expression string
- Default
  - `null`

## Value Rules

### V1. String

#### V1.1 Quotation Marks

- Key
  - `json.value.quotationMarks`
- Description
  - Specifies the type of quotation marks for string values
- Value
  - `double`
- Default
  - `double`

#### V1.2 Escape Sequences

- Key
  - `json.value.escapeSequences`
- Description
  - Specifies how to handle escape sequences in string values
- Value
  - `necessary`
  - `all`
- Default
  - `necessary`

#### V1.3 Length Limit

- Key
  - `json.value.stringMaxLength`
- Description
  - Specifies the maximum length for string values
- Value
  - Integer value or `null` for no limit
- Default
  - `null`

### V2. Number

#### V2.1 Precision

- Key
  - `json.value.numberPrecision`
- Description
  - Specifies the precision (decimal places) for floating-point numbers
- Value
  - Integer value representing max decimal places
- Default
  - `null`

#### V2.2 Exponential Notation

- Key
  - `json.value.exponentialNotation`
- Description
  - Specifies whether to allow exponential notation (e.g., `1e10`)
- Value
  - `allow`
  - `prohibit`
- Default
  - `allow`

#### V2.3 Leading Zero

- Key
  - `json.value.leadingZero`
- Description
  - Specifies whether to allow leading zeros in integers
- Value
  - `prohibit`
- Default
  - `prohibit`

### V3. Boolean and null

#### V3.1 Notation

- Key
  - `json.value.booleanNullNotation`
- Description
  - Specifies the notation for boolean and null values
- Value
  - `lowercase`
- Default
  - `lowercase`

#### V3.2 Explicit Values

- Key
  - `json.value.explicitValues`
- Description
  - Specifies the preference level for explicit values over implicit `null`
- Value
  - `preferred`
  - `required`
  - `optional`
- Default
  - `preferred`

### V4. Arrays and Empty Values

#### V4.1 Empty Arrays

- Key
  - `json.value.emptyArrays`
- Description
  - Specifies the policy for using empty arrays `[]`
- Value
  - `allow`
  - `discourage`
  - `prohibit`
- Default
  - `allow`

#### V4.2 Empty Objects

- Key
  - `json.value.emptyObjects`
- Description
  - Specifies the policy for using empty objects `{}`
- Value
  - `allow`
  - `discourage`
  - `prohibit`
- Default
  - `allow`

#### V4.3 Consistent Types

- Key
  - `json.value.consistentArrayTypes`
- Description
  - Specifies the required level of type consistency for elements in an array
- Value
  - `recommended`
  - `required`
  - `optional`
- Default
  - `recommended`
