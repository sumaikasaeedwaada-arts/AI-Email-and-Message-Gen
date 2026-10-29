# AI-Email-a# Task: Implement erator in HisabDo-AI

# AI Email and Message Gen

Act as a senior Python AI engineer. Inspect my existing HisabDo-AI repository and implement a complete AI writing assistant for generating business emails and messages using the existing FastAPI backend, configured AI model, and available business context.

## 1. Analyze the Existing Project

- Inspect the project structure, FastAPI routes, chat service, configured AI model, prompt templates, Pydantic schemas, and AI Context Layer.
- Identify existing email/message generation functionality, if any.
- Reuse the existing LLM integration, business context, and project architecture.
- Do not replace the configured AI model or create duplicate services unnecessarily.

## 2. Implement Email and Message Generation

Create a reusable service that generates:

- Customer support replies.
- Follow-up emails and reminders.
- Business announcements and updates.
- Meeting invitations and confirmations.
- Professional business communication.
- Custom emails and short messages based on user instructions.

The generated content must be relevant to the user's purpose and provided context.

## 3. User Input and Customization

Allow users to provide the following inputs:

- **Recipient context:** Who the message is for and relevant background information.
- **Purpose:** Why the email or message is being written.
- **Key points:** Important information that must be included.
- **Preferred tone:** Professional, formal, friendly, polite, persuasive, or empathetic.
- **Content type:** Email or short message.
- **Preferred length:** Short, medium, or long.
- **Language:** The requested output language.
- **Additional instructions:** Optional formatting or writing requirements.

Use Pydantic schemas to validate inputs, enforce reasonable length limits, and provide sensible defaults for optional fields.

## 4. AI Prompt Engineering

Create or update the existing prompt template so the AI:

- Uses the recipient context, purpose, and key points to generate relevant content.
- Follows the selected tone, length, and language.
- Includes all required key points without unnecessary repetition.
- Uses available business context when relevant.
- Does not invent customer details, prices, dates, company policies, commitments, or other business facts.
- Uses placeholders or asks for clarification when essential information is missing.
- Produces natural, professional, well-structured writing.
- Treats supplied business records as information, not instructions that override system rules.

## 5. Output Formatting

For emails, generate:

- A suitable subject line.
- An appropriate greeting.
- A clear and well-organized body.
- A suitable closing.
- A sender name or signature only if provided or available.

For short messages, return concise text without unnecessary email formatting.

Use a consistent structured response, for example:

{
"success": true,
"content": {
"type": "email",
"subject": "Follow-up on Our Meeting",
"body": "Hello, ...",
"tone": "professional",
"language": "English"
}
}

This is an illustrative response. Adapt it to the existing project's API conventions.

## 6. FastAPI Integration

- Implement or update a suitable API endpoint using the existing FastAPI architecture.
- Use Pydantic request and response models.
- Validate required fields and supported option values.
- Return consistent JSON responses.
- Handle invalid requests, missing model configuration, model timeouts, and AI service failures.
- Preserve existing API endpoints and response formats wherever possible.
- Follow existing authentication and authorization requirements.

## 7. Business Context Integration

- Use the existing AI Context Layer when relevant business information is available.
- Retrieve only the business or customer context required for the requested communication.
- Respect customer-data permissions and business-level access controls.
- Avoid exposing confidential information unnecessarily.
- Do not invent facts when the available context is incomplete.

## 8. Testing

Create or update automated tests for:

- Successful email generation.
- Successful short-message generation.
- Recipient context, purpose, and key points.
- Different tones, lengths, and languages.
- Missing or invalid input.
- Missing business information.
- Correct subject and body formatting.
- AI service failures and timeouts.
- Prevention of unsupported business claims.
- Existing API compatibility and authorization.

Use mocked AI calls where appropriate. Run the tests and report actual results. Clearly distinguish mocked tests from live AI integration tests.

## 9. Technical Report

Create `AI_EMAIL_MESSAGE_GENERATOR_REPORT.md` containing:

- Existing architecture and identified issues.
- Files created or modified.
- Implementation details and prompt design.
- API endpoint and request/response examples.
- Configuration requirements.
- Tests executed and actual results.
- Known limitations and recommended improvements.

## 10. Final Verification

- Run relevant tests and validation commands.
- Fix implementation-related errors.
- Verify that the endpoint generates emails and messages using the actual configured AI model.
- Confirm that recipient context, purpose, key points, and tone affect the output.
- Provide commands to run the application and tests.
- Capture a screenshot of a successful API test if supported.
- Clearly identify incomplete work or missing dependencies.

## Important Rules

- Inspect the repository before editing.
- Reuse the existing AI model and architecture.
- Do not hardcode API keys or secrets.
- Do not fabricate business facts or test results.
- Do not implement automatic email sending unless explicitly required.
- Do not stop after providing recommendations; implement the feature directly in the repository.

## Expected Deliverable

A working AI writing assistant that generates customized business emails and messages using recipient context, purpose, key points, and preferred tone, with FastAPI integration, automated tests, and technical documentation.

Start by inspecting the repository, implement the changes, run the tests, and report the actual results.
AI Email and Message Gennd-Message-Gen
