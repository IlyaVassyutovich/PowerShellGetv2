```powershell
Import-Module ./tools/build.psm1
Install-Dependencies
Update-ModuleManifestFunctions
Publish-ModuleArtifacts

# Won't work from elevated prompt (as in vscode during development)
Publish-Module -Name .\dist\PowerShellGet -Repository agamemnon
dotnet nuget push .\PowerShellGet.2.3.0-beta.nupkg --source GitHub
```
