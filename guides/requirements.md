# Requirements

## Functional Requirements

- **Module Structure**: Each module must follow the established directory structure.
- **Function Implementations**:
  - **Action Functions**: Perform transactions and utilize the `sendTransactions` function from `FunctionOptions`.
  - **Getter Functions**: Retrieve data without performing transactions.
- **Tools Implementation**: Provide a `tools.ts` file defining functions and their parameters for LLM integration, following the OpenAI function calling specification.
- **HTTP requests**: Use the [Axios](https://axios-http.com/docs/intro)
- **Error Handling**: Functions must handle errors gracefully, using the `toResult` transformer for standardized responses.
- **Input Validation**: All functions must perform thorough input validation and provide informative error messages.
- **Documentation**: Each module must include a `README.md` with a brief description and sample user questions.

## Non-Functional Requirements

- **Programming Language**: TypeScript with the NestJS framework.
- **Code Standards**: Follow the provided coding guidelines and design patterns.
- **Performance**:
  - Functions should be optimized for performance.
  - Getter functions should not return more than **500 tokens** of data to prevent overloading the AI context.
  - Large data retrievals should be split into multiple smaller functions.
- **Naming Conventions**:
  - Function names should match the file names (one function per file).
  - Use clear and descriptive names for variables and functions.
- **Comments and Documentation**:
  - Use JSDoc comments for public classes and methods.
  - Include comments to explain complex logic or important sections.

## Code Requirements

- **Formatting**
  - Use settings from `.prettierrc`
  - Single quotes
  - 4 spaces indentation
  - Maximum line length 180 characters
