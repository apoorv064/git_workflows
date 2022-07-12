# git_workflows

1. Setup a basic workflow to test changeset. When i raise a PR, a job should run to test (echo test)
2. Setup a workflow to test and deploy a change set (conditional workflow, deploy only on merge to main branch)
3. Setup a workflow to test, lint, and deploy a change set (one or more jobs based on event)
4. Setup a workflow dispatch to boot Linode instances with metadata specified input
5. Setup a workflow based on publish event
6. Setup a workflow call to link workflows 
7. Understand reusable workflows and setup workflow call which can reuse workflows from another repo
