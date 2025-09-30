# Changelog Style Guide

This document is based on [Keep a Changelog](https://keepachangelog.com/) standards, providing unified changelog writing specifications applicable to all projects.

## Core Principles

- **Changelogs are for humans, not machines** - Content should be clear and readable
- **Every version should have a corresponding entry** - No release version should be omitted
- **Similar types of changes should be categorized** - For quick information location
- **Versions and sections should be linkable** - Support direct references
- **Latest versions displayed first** - Reverse chronological order
- **Display release dates** - Provide time reference
- **Follow semantic versioning** - Version numbers should be meaningful

## File Specifications

- **File Format**: Markdown (`.md`)
- **Recommended Filename**: `CHANGELOG.md`
- **Encoding**: UTF-8
- **Location**: Project root directory

## Change Type Categories

### Added
For new features and functionality additions

**Examples:**
- Added user registration functionality
- Added database connection pool support
- Added new API endpoint `/users/{id}`

### Changed
For modifications to existing functionality

**Examples:**
- Changed login validation logic optimization
- Changed dependency library updated to version 1.2.0
- Changed configuration file format modification

### Deprecated
For features that will be removed in upcoming versions

**Examples:**
- Deprecated legacy API v1 will be removed in next version
- Deprecated config.ini configuration method, please use config.json

### Removed
For features that have been deleted

**Examples:**
- Removed support for Python 2.7
- Removed deprecated legacy API

### Fixed
For bug fixes

**Examples:**
- Fixed issue where users couldn't log out
- Fixed memory leak problem
- Fixed data import encoding error

### Security
For security-related fixes and improvements

**Examples:**
- Security fixed SQL injection vulnerability
- Security strengthened password validation rules
- Security updated dependencies to fix security vulnerabilities

## Standard Format Template

```markdown
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- New features to be released

### Changed
- Feature changes to be released

### Fixed
- Bug fixes to be released

## [1.1.0] - 2023-12-15

### Added
- Added user permission management functionality
- Support for batch data import

### Changed
- Optimized database query performance
- Updated user interface design

### Fixed
- Fixed login timeout issue
- Resolved data synchronization exceptions

## [1.0.0] - 2023-11-01

### Added
- Initial version release
- Basic user management functionality
- Database integration

### Security
- Implemented user authentication
```

## Version Control Recommendations

### Version Number Format
Follow [Semantic Versioning](https://semver.org/) specification:
- `MAJOR.MINOR.PATCH` (e.g., 1.0.0)
- Major version: Incompatible API changes
- Minor version: Backward-compatible functionality additions
- Patch version: Backward-compatible bug fixes

### Date Format
Use ISO 8601 format: `YYYY-MM-DD`

### Unreleased Section
- Always maintain an `[Unreleased]` section
- Used to record upcoming changes
- Rename to specific version number when releasing

## Writing Best Practices

### Content Requirements
- **Be specific and clear**: Avoid vague descriptions like "fixed some issues"
- **User-focused**: Focus on user-perceivable changes
- **Concise and clear**: One change per line, highlight key points
- **Consistent tense**: Use past tense or present tense consistently

### Good Examples
```markdown
### Added
- Added email notification feature with task completion reminders
- Added data export to CSV format option

### Fixed
- Fixed table display issues in Firefox browser
- Resolved potential data loss in bulk delete operations
```

### What to Avoid
```markdown
### Changed
- Some optimizations ❌
- Fixed bugs ❌
- Updated stuff ❌
```

## Tool Integration Suggestions

### Automated Generation
- Can use Git commit messages to generate drafts
- Should be manually reviewed and improved
- Ensure end-user readability

### Version Links
```markdown
[Unreleased]: https://github.com/user/project/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/user/project/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/user/project/releases/tag/v1.0.0
```

## Reference Resources

- [Keep a Changelog](https://keepachangelog.com/)
- [Semantic Versioning](https://semver.org/)
- [Conventional Commits](https://www.conventionalcommits.org/)

---

*This guide applies to all projects and requires no project-specific modifications.*
