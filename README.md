# GitHub Copilot Development Labs

Hands-on exercises for using GitHub Copilot in Visual Studio Code. The workspace includes guided labs, sample applications, and test projects covering code analysis, feature development, refactoring, unit testing, performance profiling, and spec-driven development.

## Repository layout

- `Instructions/` - Markdown lab instructions
- `LabFiles/` - Source code and exercises used by the labs
- `Allfiles/` - Supporting files and course content
- `index.md` - Jekyll index for the published exercise catalog

## Featured projects

### C# unit testing lab

The project in `LabFiles/04-develop-unit-tests-xunit/AccelerateDevGHCopilot` demonstrates:

- xUnit tests for application services
- NSubstitute repository mocks
- Reusable loan and patron test factories
- Infrastructure tests for `JsonLoanRepository`
- JSON test data copied to the test output directory

Run the C# tests from the repository root:

```bash
dotnet build LabFiles/04-develop-unit-tests-xunit/AccelerateDevGHCopilot/tests/UnitTests/UnitTests.csproj
dotnet test LabFiles/04-develop-unit-tests-xunit/AccelerateDevGHCopilot/tests/UnitTests/UnitTests.csproj
```

Run only the `JsonLoanRepository.GetLoan` tests:

```bash
dotnet test LabFiles/04-develop-unit-tests-xunit/AccelerateDevGHCopilot/tests/UnitTests/UnitTests.csproj --filter 'FullyQualifiedName~GetLoanTest'
```

### Python unit testing lab

The Python project in `LabFiles/04-python-develop-unit-tests-pytest/AccelerateDevGHCopilot` demonstrates both `unittest` and pytest styles:

```bash
cd LabFiles/04-python-develop-unit-tests-pytest/AccelerateDevGHCopilot/library
python -m unittest discover -v tests
pytest tests -v
```

## Prerequisites

- Git
- Visual Studio Code
- GitHub Copilot
- .NET SDK 9.0 or later for the C# labs
- Python 3.10 or later for the Python labs
- The C# Dev Kit and Python extensions for Visual Studio Code

## Working with the labs

1. Open the repository root in Visual Studio Code.
2. Choose a lab under `Instructions/Labs/`.
3. Open the matching project under `LabFiles/`.
4. Follow the lab prompts and run the validation commands for that project.

The lab instructions are designed to be followed sequentially, but each project can also be opened and tested independently.

## License

See [LICENSE](LICENSE) for licensing information.
