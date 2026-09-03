# Archi Workspace

Private shared Archi model for the Concillium Partners architecture team.

Repository: <https://github.com/bauyusefatteyih-tech/archi-workspace>

## First-time setup

1. Ask the repository owner to add your GitHub username as a collaborator.
2. Install Archi 5.9 and the coArchi 0.9.7 collaboration plug-in.
3. In Archi, choose the coArchi command to import a remote model.
4. Use `https://github.com/bauyusefatteyih-tech/archi-workspace.git` as the repository URL.
5. Authenticate with your own GitHub username and personal access token. Never share or commit tokens.

## Team workflow

1. Refresh the collaboration model before starting work.
2. Work in your assigned diagram folder and prefix new views with your team identifier.
3. Save the model, review your changes, and use coArchi to commit them with a clear message.
4. Refresh again before publishing, resolve any reported conflicts, then publish your commit.
5. Keep reusable elements shared, but avoid having two people rename or delete the same element at the same time.

coArchi provides Git-based asynchronous collaboration. It does not provide simultaneous cursor-level co-editing. Frequent small commits and dedicated views minimize conflicts.

## Publish an HTML report

From PowerShell in the main `Archi Workspace` folder:

```powershell
.\Publish-ArchiReport.ps1 -ModelRepositoryPath '.\collaboration\archi-workspace'
```

The report and ZIP package are created under `published`. Keep architecture reports private unless publication is explicitly approved.

The publishing script also accepts `-SharePointFolder` when a licensed SharePoint document library is synced to the computer. The current Microsoft tenant has no SharePoint Online license, so that destination is not available yet.
