# Notes

## Chapter 1
- Version control is a system that records changes to a file or set of files over time.
- Modern version control systems implement a database to keep track of file changes
- Simple version control gains friction when more people work on the project
- Centralized version control stores all changes on a central server and users checkout files.
- Centralized version control also represents a single point of failure
- With distributed version control systems users all store a mirror of the repository.
- [[Git]] was started to replace [[BitKeeper]], the version control system use by the [[Linux]] kernel
- [[Linus Torvalds]] developed git with the following goals:
	- Speed
	- Simple design
	- Strong support for non-linear development (thousands of parallel branches)
	- Fully distributed
	- Able to handle large projects like the Linux kernel efficiently (speed and data size)
- Git was born in 2005
- Git uses snapshots, not differences.
- Recording differences between files is called delta-based version control.
- Git stores files as a stream of snapshots.
- With every version git stores a "copy" of every file. Each "copy" can be a pointer to a previous version of the file if there are no changes.
- All git metadata is stored locally, because the repository is stored locally.
- Git has three main states for files
	- Modified
	- Staged
	- Committed