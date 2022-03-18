<a href="https://logsight.ai/"><img src="https://logsight.ai/assets/img/logol.png" width="150"/></a>

**Your Ally for Intelligent DevOps Pipelines**

logsight.ai infuses deep learning and AI-powered analytics to enable continuous software delivery and proactive troubleshooting



# Hello logsight.ai from Github Actions
This repository illustrates the [logsight.ai Stage Verifier](https://docs.logsight.ai/#/monitor_deployments/stage_verifier) via GitHub Actions.

The repository contains [main.yml](https://github.com/aiops/hello-logsight/blob/main/.github/workflows/main.yml) workflow that:
1. Set ups connection to logsight.ai
2. Executes the [hello-logsight.py](https://github.com/aiops/hello-logsight/blob/main/hello_logsight.py) application, which generates logs
3. Verifies the logs from the new deployment in comparison to the previous one

## Hands-on
### Requirements
1. Register an account at [logsight.ai](https://demo.logsight.ai/)

### Steps
1. **Fork** the repository 
2. Go to **Actions** and click on **I understand my workflows, go ahead and enable them**
3. **Setup repository secrets** by going into Settings => Secrets => Actions => New repository secret
   1. `Name`: **LOGSIGHT_USERNAME** should have `Value` of your logsight.ai username
   2. `Value`: **LOGSIGHT_PASSWORD** should have `Value` of your logsight.ai password
   3. Make sure you use the exact same `Names`
4. The repository contains two **pull requests** named **Baseline** and **Candidate** you can check them out at https://github.com/aiops/hello-logsight/pulls
5. Merge the **Baseline** pull request into `main` by clicking on the **Baseline** request and clicking on **Merge pull request** => **Confirm Merge**
6. Merge the **Candidate** pull request into `main` by clicking on the **Candidate** request and clicking on **Merge pull request** => **Confirm Merge**
7. The Stage Verifier GitHub Actions 
8. In the end, the workflow creates a report that specifies the **deployment risk**

Continue reading at the [Docs.](https://docs.logsight.ai/#/monitor_deployments/github_action)