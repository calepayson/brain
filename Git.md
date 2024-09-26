# Cheat Sheet
- Commands related to a remote repository:
	- `git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`
	- `git push` or `git push origin main
- Commands related to the workflow:
	- `git add .`
	- `git commit -m "A message describing what you have done to make this snapshot different"`
- Commands related to checking status or log history
	- `git status`
	- `git log`

The basic Git syntax is `program | action | destination`.

## Best Practices
- **Atomic Commits** - Each commit only relates to one feature or task.
- **Useful Commits** - Each atomic commit should have a descriptive commit message
### Good Commit Messages
- Commits have two parts, a subject and a body
	- The **Subject** should be a brief summary of the change you made to the project
	- The **Body** should be a concise but clear description of  what you did
		- (Describe the problem you commit solves and how)
- This only works if commits are atomic so commit every time you **get a piece of code to work, fix a bug, or fix a typo**