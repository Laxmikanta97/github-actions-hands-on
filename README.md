<!-- GitHub Actions Hands-On Banner -->
<p align="center">
  <img src="https://github.com/user-attachments/assets/37308b74-c1a1-4076-9c84-8d381f62836b" alt="GitHub Actions Hands-On Banner" width="800">
</p>

# GitHub Actions Hands-On
-------------------------
A practical guide and workflow examples for automating CI/CD with GitHub Actions.

1. **GitHub Actions: Introduction to GitHub actions for Beginners**
    * Core Components of GitHub Actions
    * Understanding Workflow,Jobs,Events,Actions,Runners
    * Creating your first GitHub Action Workflow

2. **GitHub Actions: Working with GitHub Actions variables**
    * Utilizing variables and secrets for secure storage of sensitive information
    * Understanding environment variables, Configuration Varianles , Using Context variables 
    * User inputs in Manual Workflow
# ==========================================================
# Variable concepts used in this workflow
# ==========================================================
#
# 1. Workflow-level environment variable
#    env:
#      cloud: google-cloud
#
#    Can be used throughout the workflow:
#      $cloud
#
# 2. Job-level environment variable
#    jobs:
#      greeting_job:
#        env:
#          Greeting: Hello
#
#    Can be used by every step in greeting_job:
#      $Greeting
#
# 3. Step-level environment variable
#    steps:
#      - env:
#          First_Name: Laxmikanta
#
#    Can be used only inside that step:
#      $First_Name
#
# 4. GitHub Actions configuration variable
#    ${{ vars.PROJECT_ID }}
#
#    PROJECT_ID should be created in:
#    Repository -> Settings -> Secrets and variables -> Actions -> Variables
#
# 5. Environment variables vs GitHub variables
#
#    Environment variable:
#      $Greeting
#      $First_Name
#      $cloud
#
#    GitHub Actions expression:
#      ${{ vars.PROJECT_ID }}
#
# 6. Variable precedence
#
#    If the same variable name is defined at multiple levels,
#    the more specific level takes precedence:
#
#      Workflow -> Job -> Step
#
#    Step-level value overrides Job-level value,
#    and Job-level value overrides Workflow-level value.
#
