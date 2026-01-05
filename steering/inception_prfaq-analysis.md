# PRFAQ Analysis

**Assume the role** of a product owner and business analyst

**Purpose**: Analyze PRFAQ (Press Release/FAQ) document to extract and refine requirements and user stories for AI-DLC workflow.

**Trigger**: User mentions "PRFAQ" in their request (e.g., "Using AI-DLC with PRFAQ", "Start from PRFAQ", "PRFAQ 기반으로 시작")

## Prerequisites

- Workspace Detection must be complete
- User has indicated they want to start from PRFAQ

## PRFAQ Document Structure

A typical PRFAQ contains:

1. **Press Release Section**
   - Headline
   - Subheadline
   - Problem Statement
   - Solution Description
   - Customer Quote
   - How It Works
   - Call to Action

2. **FAQ Section**
   - Customer FAQs (external perspective)
   - Internal FAQs (stakeholder perspective)

## Execution Steps

### Step 1: Detect PRFAQ Source

**Check in order:**

1. **File Detection**: Look for PRFAQ document in workspace
   - `./PRFAQ.md`
   - `./prfaq.md`
   - `./docs/PRFAQ.md`
   - `./docs/prfaq.md`

2. **Chat Input**: If no file found, ask user:
  PRFAQ 문서를 찾을 수 없습니다. 다음 중 하나를 선택해주세요:

  A) PRFAQ 파일 경로를 직접 지정 (예: ./documents/my-prfaq.md)
  B) PRFAQ 내용을 채팅에 직접 붙여넣기
  C) PRFAQ 없이 일반 Requirements Analysis로 진행

  [Answer]:

1. **Fallback**: If user chooses C or no PRFAQ available, proceed to standard Requirements Analysis (load `inception_requirements-analysis.md`
)

### Step 2: Parse PRFAQ Structure

**Extract and categorize content:**

## PRFAQ Parsing Results

### Press Release Elements

- **Headline**: [extracted]
- **Problem Statement**: [extracted]
- **Solution**: [extracted]
- **Target Customer**: [extracted]
- **Key Benefits**: [extracted]
- **How It Works**: [extracted]

### FAQ Elements

- **Customer FAQs**: [list]
- **Internal FAQs**: [list]

**Save to**: `aidlc-docs/inception/requirements/prfaq-parsing.md`

### Step 3: Auto-Refine and Identify Gaps

**Analyze PRFAQ for:**

1. **Clarity Issues**
   - Vague or ambiguous statements
   - Missing specifics (numbers, metrics, constraints)
   - Undefined terms or acronyms

2. **Completeness Gaps**
   - Missing functional requirements
   - Missing non-functional requirements (performance, security, scalability)
   - Missing user scenarios or edge cases
   - Missing technical constraints

3. **Consistency Issues**
   - Contradictions between sections
   - Misaligned problem-solution statements
   - Inconsistent terminology

**Generate initial refined output:**

## Auto-Refined Analysis

### Identified Strengths

- [Clear aspects of the PRFAQ]

### Identified Gaps

- [List of missing or unclear items]

### Preliminary Requirements (Draft)

#### Functional Requirements

- FR-1: [derived from PRFAQ]
- FR-2: [derived from PRFAQ]

#### Non-Functional Requirements

- NFR-1: [derived or inferred]
- NFR-2: [derived or inferred]

### Areas Needing Clarification

- [List of questions to ask user]

### Step 4: Generate Clarifying Questions

**Create**: `aidlc-docs/inception/requirements/prfaq-clarification-questions.md`

**Question Categories:**

1. **Problem Clarification**
   - Is the problem statement accurate and complete?
   - Are there additional pain points not mentioned?

2. **Solution Scope**
   - What features are MVP vs future?
   - What is explicitly out of scope?

3. **User/Customer Details**
   - Who are the primary user personas?
   - What are the key user journeys?

4. **Technical Constraints**
   - Are there specific technology requirements?
   - What are the integration points?

5. **Success Metrics**
   - How will success be measured?
   - What are the acceptance criteria?

**Question Format:**

# PRFAQ Clarification Questions

Based on your PRFAQ analysis, please answer the following questions to refine the requirements.

## Problem & Solution

### Q1: Problem Validation

The PRFAQ states the problem as: "[extracted problem]"

Is this accurate and complete?
A) Yes, this captures the problem well
B) Partially - needs additions (please specify)
C) No - the problem should be restated

[Answer]:

### Q2: Solution Scope

The proposed solution includes: "[extracted solution summary]"

For the initial release (MVP), which capabilities are essential?
A) All mentioned capabilities
B) Only core capabilities (please list)
C) Need to discuss priorities

[Answer]:

## [Continue with other categories...]

**Wait for user answers before proceeding.**

### Step 5: Analyze Answers and Follow-up

**MANDATORY**: After receiving answers:

1. Check for remaining ambiguities
2. If ambiguities exist, generate follow-up questions
3. Repeat until all critical items are clarified
4. User can explicitly request to proceed despite remaining questions

### Step 6: Generate Requirements Document

**Create**: `aidlc-docs/inception/requirements/requirements.md`

**Structure:**

# Requirements Document

## Source

- **Based on**: PRFAQ Document
- **PRFAQ Location**: [path or "provided via chat"]
- **Analysis Date**: [timestamp]

## Executive Summary

[Brief summary derived from PRFAQ headline and solution]

## Problem Statement

[Refined from PRFAQ, incorporating clarification answers]

## Target Users

[Derived from PRFAQ customer description and FAQ answers]

## Functional Requirements

### Core Features (MVP)

| ID | Requirement | Source | Priority |
|----|-------------|--------|----------|
| FR-1 | [requirement] | PRFAQ Section X | Must Have |
| FR-2 | [requirement] | Clarification Q2 | Must Have |

### Future Features

| ID | Requirement | Source | Priority |
|----|-------------|--------|----------|
| FR-F1 | [requirement] | PRFAQ FAQ | Nice to Have |

## Non-Functional Requirements

| ID | Category | Requirement | Source |
|----|----------|-------------|--------|
| NFR-1 | Performance | [requirement] | Inferred/Clarified |
| NFR-2 | Security | [requirement] | PRFAQ FAQ |

## Constraints and Assumptions

[Derived from PRFAQ and clarifications]

## Success Criteria

[Derived from PRFAQ and clarifications]

## Traceability

| Requirement | PRFAQ Section | Clarification |
|-------------|---------------|---------------|
| FR-1 | Press Release - Solution | Q2 |

### Step 7: Generate User Stories

**Create**: `aidlc-docs/inception/user-stories/user-stories.md`

**Derive from PRFAQ:**

- Press Release "How It Works" → User journeys
- Customer FAQs → User scenarios and edge cases
- Problem Statement → Pain points to address

**Structure:**

# User Stories

## Source

- **Derived from**: PRFAQ Document + Clarification Answers

## Personas

[Derived from PRFAQ target customer description]

### Persona 1: [Name]

- **Role**: [role]
- **Goals**: [goals from PRFAQ]
- **Pain Points**: [from problem statement]

## Epic: [Main Product/Feature Name]

### User Story 1

As a [persona],
I want to [action derived from PRFAQ],
So that [benefit from PRFAQ].

Acceptance Criteria:

- [ ] [criterion derived from FAQ or clarification]
- [ ] [criterion]

Source: PRFAQ Section [X], Clarification Q[Y]

### User Story 2

[Continue...]

## Story Map

[Optional: Visual representation of user journey]

### Step 8: Update State Tracking

Update `aidlc-docs/aidlc-state.md`:

## Stage Progress

### 🔵 INCEPTION PHASE

- [x] Workspace Detection
- [x] Reverse Engineering (if applicable)
- [x] PRFAQ Analysis ← NEW
- [x] Requirements Analysis (via PRFAQ)
- [x] User Stories (via PRFAQ)

### Step 9: Present Completion and Get Approval

**Log approval prompt in audit.md, then present:**

# 📄 PRFAQ Analysis Complete

## Summary

- **PRFAQ Source**: [file path or "chat input"]
- **Requirements Generated**: [count] functional, [count] non-functional
- **User Stories Generated**: [count] stories across [count] epics
- **Clarifications Resolved**: [count] questions answered

## Generated Artifacts

- aidlc-docs/inception/requirements/prfaq-parsing.md
- aidlc-docs/inception/requirements/requirements.md
- aidlc-docs/inception/user-stories/user-stories.md

│ **📋 <u>REVIEW REQUIRED:</u>**
│ Please examine the generated documents above.

│ **🚀 <u>WHAT'S NEXT?</u>**
│
│ **You may:**
│
│ 🔧 Request Changes - Ask for modifications to requirements or user stories
│ ✅ Approve & Continue - Proceed to Workflow Planning

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

**Wait for explicit user approval before proceeding.**

## Fallback Behavior

**If PRFAQ is not available or user declines:**

- Log the decision in audit.md
- Proceed to standard `inception_requirements-analysis.md`
- Do not generate PRFAQ-specific artifacts
