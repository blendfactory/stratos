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

#### F1.1 Indentation Type

Use spaces or tabs (Default: spaces)

#### F1.2 Indentation Width

2 spaces or 4 spaces (Default: 2 spaces)

#### F1.3 Consistent Indentation

Nodes at the same depth should have the same indentation level

### F2. Line Ending

#### F2.1 Line Ending Character

LF (`\n`) or CRLF (`\r\n`) (Default: LF)

#### F2.2 Newline at End of File

Include/exclude a newline at the end of file (Default: include)

### F3. Whitespace

#### F3.1 Trailing Whitespace

Remove unnecessary whitespace at the end of lines

#### F3.2 Whitespace After Colon

Include one space after a colon (e.g., `"name": "value"`)

#### F3.3 Whitespace After Comma

Include one space after a comma

#### F3.4 Whitespace Inside Brackets

No whitespace immediately after or before brackets

### F4. Line Breaks

#### F4.1 Line Break After Object Start

Include/exclude a line break after the opening brace `{`

#### F4.2 Line Break Before Object End

Include/exclude a line break before the closing brace `}`

#### F4.3 Line Break After Array Start

Include/exclude a line break after the opening bracket `[`

#### F4.4 Line Break Before Array End

Include/exclude a line break before the closing bracket `]`

#### F4.5 Line Break Between Properties

Include a line break between each property

### F5. Comma

#### F5.1 Trailing Comma

Allow/prohibit comma after the last element/property (prohibited in RFC 8259)

#### F5.2 Comma Style

Place on the same line or at the beginning of the next line

## Structure Rules

### S1. Nesting

#### S1.1 Maximum Nesting Depth

Maximum depth for nested objects and arrays (Default: 8)

#### S1.2 Simplification Recommendation

Recommend simplifying structure when exceeding certain depth

### S2. Property Order

#### S2.1 Alphabetical Order

Order/don't order properties alphabetically

#### S2.2 Property Grouping

Group semantically related properties

#### S2.3 Standard Properties First

Place standard properties like `id`, `type` at the beginning

### S3. Array Formatting

#### S3.1 Single Line Arrays

Place short arrays on a single line (configurable threshold)

#### S3.2 Multi-line Arrays

Split long arrays across multiple lines

## Naming Rules

### N1. Property Name Format

#### N1.1 Naming Convention

camelCase, snake_case, kebab-case, PascalCase, etc. (Default: camelCase)

#### N1.2 Consistency

Use consistent naming conventions within the same object

#### N1.3 Avoid Reserved Words

Don't use JavaScript reserved words as property names

### N2. Property Name Constraints

#### N2.1 Length Limit

Maximum length for property names (Default: 50 characters)

#### N2.2 Allowed Characters

Set of allowed characters (alphanumeric, underscore, hyphen, etc.)

#### N2.3 Naming Pattern

Property names that follow specific patterns (specified by regular expressions)

## Value Rules

### V1. String

#### V1.1 Quotation Marks

Use double quotation marks (`"`) (JSON standard)

#### V1.2 Escape Sequences

Differentiate between necessary and unnecessary escape sequences

#### V1.3 Length Limit

Limit the maximum length of string values (Default: none)

### V2. Number

#### V2.1 Precision

Precision of floating-point numbers (limit on decimal places)

#### V2.2 Exponential Notation

Allow/prohibit exponential notation (`1e10`)

#### V2.3 Leading Zero

Prohibit leading zeros in integers (JSON standard)

### V3. Boolean and null

#### V3.1 Notation

Write `true`, `false`, `null` in lowercase (JSON standard)

#### V3.2 Explicit Values

Prefer explicit values over implicit `null`

### V4. Arrays and Empty Values

#### V4.1 Empty Arrays

Policy for using empty arrays `[]`

#### V4.2 Empty Objects

Policy for using empty objects `{}`

#### V4.3 Consistent Types

Recommend that elements in an array are of the same type
