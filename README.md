# Archi Workspace

Public shared Archi model and ready-to-run toolkit for the Concillium Partners architecture team.

Repository: <https://github.com/bauyusefatteyih-tech/archi-workspace>

## One-download Windows setup

Download the complete Windows x64 package:

**[Archi-Workspace-Windows-x64-v1.0.0.zip](https://github.com/bauyusefatteyih-tech/archi-workspace/releases/download/workspace-v1.0.0/Archi-Workspace-Windows-x64-v1.0.0.zip)**

1. Extract the ZIP to a normal folder.
2. Double-click `Setup-and-Start-Archi.cmd`.
3. Wait for Archi's first launch; plug-in initialization can take several minutes.
4. The included collaboration-flow sample opens automatically.

The package includes Archi 5.9, coArchi 0.9.7, the EAKG knowledge-graph plug-in, the Archimesh client plug-in, a real sample model, a published HTML example, and the illustrated PDF tutorial. It contains no passwords, tokens, or user-specific settings.

## First-time setup

1. Use the complete package above; no separate Archi or plug-in installation is required.
2. In Archi, choose the coArchi command to import a remote model.
3. Use `https://github.com/bauyusefatteyih-tech/archi-workspace.git` as the repository URL.
4. Public read access does not require repository membership.
5. To publish changes, ask the repository owner for contributor access and authenticate with your own GitHub personal access token. Never share or commit tokens.

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
