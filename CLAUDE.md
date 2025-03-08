# Claude Code Project Rules

## Project Overview

Stratos is a set of Dart packages for linting and formatting JSON, JSONC, YAML, and Markdown files. It's structured as a monorepo using Dart Pub Workspace and Melos.

## Technical Stack

### Environment

- sdk: ^3.7.1

### Dependencies

- args: ^2.6.0
- path: ^1.9.1

### Dev Dependencies

- melos: ^7.0.0-dev.3
- test: ^1.25.15

## Directory Structure

```
.
└── packages/
    ├── stratos/           # Main CLI tool that brings together the functionality of all packages
    ├── stratos_json/      # JSON linting and formatting
    ├── stratos_jsonc/     # JSONC linting and formatting
    ├── stratos_yaml/      # YAML linting and formatting
    └── stratos_markdown/  # Markdown linting and formatting
```

## Development Commands

```shell
# Bootstrap all packages with Melos
melos bootstrap

# Run analyzer for all package
dvm dart analyze

# Run format for all packages
melos format

# Check for circular dependencies between packages
melos list --cycles

# Run tests for all packages
melos run test --no-select
```

## Style Guidelines

- Follow Dart's official style guide
  - https://dart.dev/effective-dart/style
- Use semantic versioning for package versions
  - https://dart.dev/tools/pub/versioning#semantic-versions
- Follow conventional commits for commit messages
  - https://www.conventionalcommits.org/en/v1.0.0

## Publishing

- Tag format for publishing: `{package_name}-v{semver}`
  - Example: `stratos-v0.1.0` for the main package
  - Example: `stratos_json-v0.1.0` for the JSON package

## Claude Code Work Process

You are an AI assistant with advanced problem-solving capabilities. Please follow these instructions to efficiently and accurately complete tasks for the Stratos project.

1. **Analyze Instructions and Plan**
   - Summarize the main tasks concisely
   - Consider implementation methods within the constraints of the technical stack
   - Identify key requirements and constraints
   - List potential challenges
   - Enumerate specific steps for task execution in detail
   
   **Preventing Duplicate Implementations**
   Before implementation, check for:
   - Existing similar functionality
   - Functions or classes with identical or similar names
   - Processes that can be generalized

2. **Execute Tasks**
   - Execute the identified steps one by one
   - During implementation, pay attention to:
     - Adherence to the appropriate directory structure
     - Consistency in naming conventions
     - Proper placement of common processes

3. **Quality Control and Problem Resolution**
   - Quickly verify the results of each task
   - In case of errors or inconsistencies, isolate the problem, identify the cause, and implement countermeasures

4. **Final Verification**
   - After completing all tasks, evaluate the entire deliverable
   - Confirm consistency with the original instructions
   - Verify that there is no duplication in the implemented features

## Important Notes

- If there are any unclear points, be sure to confirm before starting work
- If important decisions are required, report them and obtain approval
- Do not make changes that are not explicitly instructed
- Do not change the versions listed in the technical stack
- Consider package dependencies carefully and avoid circular dependencies
