# lecture note about GIT-1
### Version Control and Collaboration
- It's essential to use a version control system for software development and other documentation works.
- We need a systematic management system for version control and collaboration.

### Version Control (Change vs. Snapshots)
**Change**: Overriding the initial version when there is a change, accumulating the changes that have been accumulated.
**Snapshots**: Keeping information about the entire file intact in each version.

### Collaboration (Local, Centralized, and Distributed Version Control)
- **Local**: A system where version control occurs only on the personal computer
     Version control is possible, but collaboration with others is difficult.
**Centralized**: A central server that manages the version control system exists, records multiple versions on the central server, and then requests the central server to receive and work with records when needed on the local computer.
**Distributed**: Each local computer has a copy of the data that the central server has, making it easy to recover the central server even if it goes down or files are damaged.
### Three States in Git
- **Working Directory**: Directories to contain projects that you create and work with Linux or other OS
- **Staging Area**: Intermediate step to commit step, get some or all of the content in the working directory and prepare to go to the commit stage
- **Commit (git directory (Repository))**: Recording a version at a particular point in time

### Git config: First-time setup
Git configurations are stored in three levels.
1. **System level**: —system option. Affects all uses and repositories on the system (administrative)
2. **Global (user) level**: —global option. Affects all repositories of a current user
3. **Local level**: —local option. Specific to the currnt repositorry
- Each level overrides values in the previous level: system -> global -> local
—
### Command Description
- **git init**: Initializing a repository in an existion directory, creates a subdirectory
- **git status**: Checking repository status
- **git add [file_name]**: Adding a new file to be staged (tracked)
    **Warning**: I modified the file that was ready to commit through nano, so committing as it is will commit the content before it is modified
    **git add .** : Upload all files and directories in the current directory to the staging area
- **git rm —cached [file_name]**: Unstaging a file
- **nano .gitignore**: Ignoring a file
- **git commmit -m "commit message"**: Commit
- **git branch -m [current_name] [name_yo_want_to_change]**: Change branch name