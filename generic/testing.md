# Testing Best Practices

## Core Testing Principles

### Test Distribution

- Write 80% unit tests, 15% integration tests, 5% end-to-end tests
- Prioritize small, fast, deterministic tests
- Every code change requires accompanying tests

### Test Quality

- Tests should be hermetic (self-contained)
- Make tests clear, simple, and focused on specific behaviors
- Test both success paths and failure scenarios
- Tests are documentation - they show how code should be used

## Writing Good Unit Tests

### Focus on Behavior, Not Implementation

- Test public APIs, not internal methods
- Verify system state and outcomes, not internal interactions
- Tests should remain valid when implementation changes
- Avoid testing specific implementation details

### Test Structure

- Use given-when-then structure for clarity
- Write descriptive test names that explain expected behavior
- Create one test per behavior/scenario
- Keep tests complete and concise

### Avoid Logic in Tests

- State inputs and outputs directly - don't compute them
- Avoid string concatenation, loops, and conditionals in tests
- Move necessary logic to helper functions
- Tests should be concrete input/output examples

## Test Maintainability

### Write "Unchanging Tests"

- Tests should only change when requirements change
- Minimize brittleness by avoiding implementation details
- Prefer clarity over code reuse (DAMP over DRY)
- Make tests self-explanatory

### Helper Methods

- Create test utilities with sensible defaults
- Keep helper functions simple
- Consider testing complex test utilities

### Clear Failure Messages

- Provide context about expected vs actual outcomes
- Make it easy to understand what went wrong
- Include relevant test data in error messages

## Key Quotes

- "If you liked it, then you shoulda put a test on it" (Beyoncé Rule)
- "Automated testing is foundational to enabling software to change"
- "After preventing bugs, the most important purpose of a test is to improve engineers' productivity"
- "Tests should focus on testing your code's public API"
