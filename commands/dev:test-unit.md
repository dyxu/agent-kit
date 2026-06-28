---
description: Write comprehensive unit tests for target code
---

# Write Unit Tests

Create comprehensive unit tests for the target code and generate the test file with proper imports and setup according to the project's testing conventions.

## Inputs

- Target file, symbol, module, or feature to test: `$ARGUMENTS`

## Steps

1. **Identify the target and conventions**
   - Use `$ARGUMENTS` to locate the file, symbol, module, or feature under test.
   - Inspect nearby tests and project configuration to identify the test framework, file naming, imports, fixtures, and setup style.
   - If no target is provided, ask for the target before creating tests.
2. **Test coverage**
   - Test public methods, functions, and externally observable behavior.
   - Cover edge cases and error conditions.
   - Test both positive and negative scenarios.
   - Aim for meaningful coverage of behavior, not implementation details.
3. **Test structure**
   - Use the project's testing framework conventions.
   - Write clear, descriptive test names.
   - Follow the Arrange-Act-Assert pattern when it fits the local style.
   - Group related tests logically.
4. **Test cases to include**
   - Happy path scenarios.
   - Edge cases and boundary conditions.
   - Error handling and exception cases.
   - Realistic external-boundary behavior using existing project test utilities; do not introduce new mocks.
5. **Test quality**
   - Make tests independent and isolated.
   - Ensure tests are deterministic and repeatable.
   - Keep each test focused on one behavior.
   - Add helpful assertion messages only when they clarify failures.
6. **Verify**
   - Run the targeted test file or nearest relevant test command.
   - If targeted tests pass, run the smallest broader suite that covers the changed area when practical.
   - Report the command run and result.

## Write Unit Tests Checklist

- [ ] Target file, symbol, module, or feature identified
- [ ] Existing testing framework conventions followed
- [ ] Public behavior covered
- [ ] Edge cases and boundary conditions covered
- [ ] Error handling and exception cases covered
- [ ] Positive and negative scenarios included
- [ ] Clear, descriptive test names written
- [ ] Arrange-Act-Assert pattern followed where appropriate
- [ ] Tests independent, deterministic, and repeatable
- [ ] No new mocks introduced
- [ ] Targeted tests run and passing
