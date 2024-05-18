[https://learn.microsoft.com/en-us/azure/devops/cli/?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/cli/?view=azure-devops)

**What can you manage ?** 
**1. Pipelines - Automate builds, tests, and deployments.** 

   - `az pipelines create --name "MyPipeline" --repository "https://github.com/example/repo" --branch master`

**2. Repos - Manage source code repositories.**
   - `az repos create --name "MyRepo"`

**3. Boards - Handle work items, boards, backlogs, sprints, and queries.**
   - `az boards work-item create --title "New Work Item" --type "User Story"`

**4. Artifacts - Manage package feeds and packages.**
   - `az artifacts universal publish --feed "MyFeed" --name "MyPackage" --version "1.0.0" --path "."

**5. Service connections - Manage connections to external services.**
   - `az devops service-endpoint create --service-endpoint-configuration "serviceEndpoint.json"`

These commands provide a foundation for automating and managing your Azure DevOps projects directly from the command line, streamlining workflows and increasing efficiency.