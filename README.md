# lint_tracker
A repo to hold information on our most up to date linting warnings and errors to check against when running scripts on PRs


### How does this work? 
- Everytime an iOS PR runs, we generate a summary of the linting errors and compare it the one stored in the top level of this repo. 

- If there are any new warnings, the lint step of CI will not pass. 

- If there are no new warnings, or warnings have reduced, it will pass.

- Once the PR is merged, we upload the new version of the summary to this repo. 

- When a new version is uploaded, we move the old version to the old_ios folder, with the timestamp at which it was replaced.

- In the future, this means we could generate historical graphs of linting errors over time. 
