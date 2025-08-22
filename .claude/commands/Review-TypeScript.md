# Claude Command: Review

This command helps you review code and bring it into compliance with the project's TypeScript coding guidelines.

## Usage

```
/review
```

Or to specify a particular file:
```
/review [file-path]
```

## What This Command Does

It performs the code review by following these steps:

### Step 1: Read the Coding Guidelines
First, it uses the Read tool to read the project's TypeScript coding guidelines:

```
Read ./.claude/code-guidelines/typescript.md
```

### Step 2: Identify Files for Review
- If the user specifies a file path, it reviews that file.
- If no path is specified, it checks for staged TypeScript files using `git status`.
- If there are no staged files, it scans for all TypeScript files in the project (`packages/**/*.ts`).

### Step 3: Analyze Each File
For each file to be reviewed:
1. It reads the file's content using the Read tool.
2. It analyzes the code against the rules in the coding guidelines.
3. It identifies code patterns that do not comply with the guidelines.
4. It generates specific suggestions for modification for each issue.

### Step 4: Generate the Review Report
It creates a detailed report that includes:
- 📁 File path
- ⚠️ Issues found (including line numbers and specific descriptions)
- ✅ Issues that can be automatically fixed
- ⚠️ Complex cases that require manual review
- 🔧 Specific modification suggestions (showing a before-and-after code comparison)

### Step 5: Apply Modifications
- It asks the user if they want to apply the automatic fixes.
- It uses the Edit or MultiEdit tool to apply safe modifications.
- It provides detailed explanations for issues that require manual judgment.

### Step 6: Verify Changes
After the modifications are applied:
1. It runs `bun lint` to check the code quality.
2. If there are errors, it reports the issues and suggests solutions.
3. It confirms that all changes comply with the coding guidelines.

## Important Reminders

- Always read the latest version of the coding guidelines file first.
- Ensure you understand the purpose of each rule before making changes.
- Provide detailed explanations and reasoning for complex refactoring.
- Verify that the code still works correctly after modification.
