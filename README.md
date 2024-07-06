# Azure DevOps Release Pipeline Agent Pool Updater

This PowerShell script updates the agent pool ID of all release pipelines in a specified Azure DevOps project.

## Prerequisites

- PowerShell 5.1 or later
- Azure DevOps Personal Access Token (PAT) with sufficient permissions to read and update release pipelines

## Usage

1. Clone this repository or download the script to your local machine.

2. Open the script in your preferred text editor and update the following variables with your specific values:

   ```powershell
   $organization = "your_organization"    # Azure DevOps organization name
   $project = "your_project"              # Azure DevOps project name
   $agentPoolId = "your_agent_pool_id"    # New agent pool ID
   $pat = "your_personal_access_token"    # Personal Access Token
   ```

3. Run the script in PowerShell.

## Script Details

The script performs the following steps:

1. Retrieves the list of all release pipelines in the specified Azure DevOps project.
2. Iterates over each pipeline, retrieves its current configuration, updates the agent pool ID, and sends the updated configuration back to Azure DevOps.
3. Outputs the progress and confirms when all pipelines have been updated.

## Example

Below is an example of how to set the variables in the script:

```powershell
$organization = "myOrganization"
$project = "myProject"
$agentPoolId = "new_agent_pool_id"
$pat = "myPersonalAccessToken"
```

## Notes

- Ensure your PAT has the necessary permissions to read and update release pipelines.
- The script uses the Azure DevOps REST API version 6.0.

Feel free to adjust the content as needed to better fit your specific project and requirements.