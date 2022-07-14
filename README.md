# git_workflows

1. Setup a basic workflow to test changeset. When i raise a PR, a job should run to test (echo test)
2. Setup a workflow to test and deploy a change set (conditional workflow, deploy only on merge to main branch)
3. Setup a workflow to test, lint, and deploy a change set (one or more jobs based on event)
4. Setup a workflow dispatch to boot Linode instances with metadata specified input
5. Setup a workflow based on publish event
6. Setup a workflow call to link workflows 
7. Understand reusable workflows and setup workflow call which can reuse workflows from another repo


1.

Created workflow PR_test.yml

name: PR_Test

# Controls when the workflow will run
on:
  # Triggers the workflow on push or pull request events but only for the "main" branch

  pull_request:
    branches: [ "main" ]


# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v3
      - run: echo "Insert tests here"
      
 On pushing from test_branch to main, pull req is created 
 
 Workflow triggered, checks passed
 
 <img width="820" alt="image" src="https://user-images.githubusercontent.com/53597532/178982850-31505290-c0d0-44cf-b274-c5b8d7656a89.png">
