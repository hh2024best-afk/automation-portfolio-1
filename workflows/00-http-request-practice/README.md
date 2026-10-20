# Week 1 Day 2 — HTTP GET GitHub API

## What it does
Sends an HTTP GET request to the GitHub API to retrieve information about the n8n repository.

## Tools
- n8n
- Make.com
- GitHub REST API

## API endpoint
https://api.github.com/repos/n8n-io/n8n

## Expected data
- full_name
- stars
- open_issues

## Tests
1. Normal input: Use the correct URL. Expect status 200 and three fields extracted.
2. Bad input: Misspell the repository name. Expect status 404. Record how each platform displays the error.
3. Empty input: Point the Set node at a field that does not exist. Record whether the result is blank, null, or an error.

## Where to check
- n8n: Executions
- Make.com: Run history and output bubbles

## How to verify the fix
Restore the correct URL and field name, then confirm a successful run on both platforms.

## Security audit
The exported n8n workflow and Make.com blueprint were checked for possible secrets and credentials.