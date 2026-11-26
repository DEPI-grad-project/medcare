# Contributing to MediCare

## Branch strategy

- `main`: stable branch; do not push feature work directly.
- `develop`: shared integration branch.
- `feature/<short-name>`: new functionality branched from `develop`.
- `bugfix/<short-name>`: non-urgent bug fixes branched from `develop`.
- `hotfix/<short-name>`: urgent production fixes branched from `main`.

Examples:
- `feature/authentication`
- `feature/doctors`
- `feature/appointments`
- `feature/medical-records`
- `feature/admin-dashboard`

## Pull requests

1. Create a focused branch from the appropriate base branch.
2. Keep commits small and use descriptive messages.
3. Open a pull request into `develop` for normal feature work.
4. Explain the change and include testing notes.
5. Resolve review comments before merging.
6. Merge to `main` only through an approved release pull request.

Prefer Squash and merge to keep the target branch history readable.

## Development conventions

- Use the same .NET SDK and target framework across the team.
- Follow consistent C# naming conventions.
- Keep controllers thin; put business rules in application services.
- Do not make Business depend on Data.
- Coordinate EF Core migrations through one designated migration owner.
- Never commit passwords, API keys, connection strings containing credentials, or local secrets.
- Use .NET User Secrets for local development secrets.

## Before opening a pull request

- Build the solution successfully.
- Run relevant tests.
- Review the diff for accidental changes and generated files.
- Update documentation when behavior, setup, or architecture changes.
