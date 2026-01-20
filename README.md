# Library App

## Table of Contents
- [Description](#description)
- [Project Structure](#project-structure)
- [Key Classes and Interfaces](#key-classes-and-interfaces)
- [Usage](#usage)
- [License](#license)

## Description
Library App is a console-based library management system built with .NET 8. It allows users to search for patrons, view their details, renew memberships, and manage book loans. The application uses JSON files for data persistence and follows a layered architecture with separation of concerns.

## Project Structure
- `AccelerateDevGitHubCopilot.sln`
- `src/`
  - `Library.ApplicationCore/`
    - `Library.ApplicationCore.csproj`
    - `Entities/`
    - `Enums/`
    - `Interfaces/`
    - `Services/`
  - `Library.Console/`
    - `appSettings.json`
    - `CommonActions.cs`
    - `ConsoleApp.cs`
    - `ConsoleState.cs`
    - `Library.Console.csproj`
    - `Program.cs`
    - `Json/`
      - `Authors.json`
      - `Books.json`
      - `BookItems.json`
      - `Loans.json`
      - `Patrons.json`
  - `Library.Infrastructure/`
    - `Library.Infrastructure.csproj`
    - `Data/`
- `tests/`
  - `UnitTests/`
    - `LoanFactory.cs`
    - `...`

## Key Classes and Interfaces
- [`ConsoleApp`](src/Library.Console/ConsoleApp.cs): Main class managing the console application's state machine and user interactions.
- [`JsonData`](src/Library.Infrastructure/Data/JsonData.cs): Handles loading and saving JSON data for entities like patrons, books, and loans.
- [`JsonPatronRepository`](src/Library.Infrastructure/Data/JsonPatronRepository.cs): Implements [`IPatronRepository`](src/Library.ApplicationCore/Interfaces/IPatronRepository.cs) for patron data operations.
- [`JsonLoanRepository`](src/Library.Infrastructure/Data/JsonLoanRepository.cs): Implements [`ILoanRepository`](src/Library.ApplicationCore/Interfaces/ILoanRepository.cs) for loan data operations.
- [`PatronService`](src/Library.ApplicationCore/Services/PatronService.cs): Business logic for patron-related operations.
- [`LoanService`](src/Library.ApplicationCore/Services/LoanService.cs): Business logic for loan-related operations.

## Usage
1. Navigate to the `src/Library.Console/` directory.
2. Run `dotnet run` to start the console application.
3. Follow the prompts to search patrons, view details, renew memberships, or manage loans.

```bash
cd src/Library.Console
dotnet run
```

## License
MIT License
