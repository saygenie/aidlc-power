# AI-DLC Power for Kiro IDE

AI-DLC (AI-Driven Development Life Cycle) is an intelligent software development workflow that adapts to your needs, maintains quality standards, and keeps you in control of the process.

This is a **Kiro Power** package that provides AI-DLC workflow capabilities in Kiro IDE.

## Installation

### From Local Directory (Development)

1. Open Kiro IDE
2. Click the Powers icon in the sidebar
3. Click "Add power from Local Path"
4. Select this directory: `~/Desktop/aidlc-power-v2`
5. Click "Add" to install

### From GitHub (Production)

1. Open Kiro IDE
2. Click the Powers icon in the sidebar
3. Click "Add Custom Power" → "GitHub"
4. Enter the repository URL
5. Click "Add" to install

## Usage

Start any software development project by stating your intent starting with the phrase **"Using AI-DLC, ..."** in the chat.

**Example prompts:**
- "Using AI-DLC, build a REST API for user management"
- "Using AI-DLC, create a React dashboard application"
- "Using AI-DLC, refactor the authentication module"

AI-DLC workflow automatically activates and guides you through:
1. **Inception Phase** - Requirements, user stories, application design
2. **Construction Phase** - Functional design, NFR design, code generation
3. **Operations Phase** - Deployment and monitoring (future)

## Three-Phase Adaptive Workflow

- **🔵 INCEPTION PHASE**: Determines **WHAT** to build and **WHY**
  - Requirements analysis and validation
  - User story creation (when applicable)
  - Application Design and creating units of work
  - Risk assessment and complexity evaluation

- **🟢 CONSTRUCTION PHASE**: Determines **HOW** to build it
  - Detailed component design
  - Code generation and implementation
  - Build configuration and testing strategies
  - Quality assurance and validation

- **🟡 OPERATIONS PHASE**: Deployment and monitoring (future)
  - Deployment automation and infrastructure
  - Monitoring and observability setup
  - Production readiness validation

## Key Features

- **Adaptive Intelligence**: Only executes stages that add value to your specific request
- **Context-Aware**: Analyzes existing codebase and complexity requirements
- **Risk-Based**: Complex changes get comprehensive treatment, simple changes stay efficient
- **Question-Driven**: Structured multiple-choice questions for clarity
- **Always in Control**: Review execution plans and approve each phase

## Directory Structure

```
aidlc-power-v2/
├── POWER.md                    # Power entry point with workflow
├── README.md                   # This file
├── LICENSE                     # MIT-0 License
├── mcp.json                    # MCP configuration
└── steering/                   # Flat structure steering files
    ├── common_*.md             # Common rules and guidelines
    ├── inception_*.md          # Inception phase steering
    ├── construction_*.md       # Construction phase steering
    └── operations_*.md         # Operations phase steering
```

## Learn More

- [AI-DLC Methodology Blog](https://aws.amazon.com/blogs/devops/ai-driven-development-life-cycle/)
- [Kiro Powers Documentation](https://kiro.dev/docs/powers/)

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
