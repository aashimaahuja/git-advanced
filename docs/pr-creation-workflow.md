Validate that you are on feature branch
If not then pull main and create a feature branch from main using branch naming conventions
Once on the correct branch, add relevant feature changes to staging.
If changes are already staged, create commit using conventional commits format
use ghb cli for creating a PR.
Generate nice description with the changes
Assign it to myself
Add reviewers

Commit types

feat - for new features
fix: - for bug fixes
Other types ( build:, chore:, refactor:, test:, style: , docs:)
BREAKING CHANGE (use ! to draw attention)

Examples
feat(lang): add Polish language [Ticket_id]
feat(user login): add login form [Ticket_id]
refactor: Extract validation helper function [Ticket_id]

Make sure to append ticket_ids along with commit

Ask for JIRA id if not provided

## Branch naming examples

feature/T-456-user-authentication
bugfix/T-789-fix-header-styling
docs/T-654-update-readme

Make sure it starts with ticket id, ask if not provided

PR format

## Summary

## Description

## Screenshots

## Additional Info
