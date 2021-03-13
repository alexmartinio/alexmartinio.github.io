```powershell
$Algorithm = 'SHA1'
$Hash = '315dbdeaf8cf59ab47fee4dc499e3579cb54341f'
$Path = '.\manjaro-architect-20.0.3-200607-linux56.iso'

if ((Get-FileHash -Path $Path -Algorithm $Algorithm).Hash -eq $Hash) {
    Write-Prompt -ForegroundColor Green -Object 'File hash matches'
}
else {
    Write-Warning -Message 'File hash does not match!'
}
```
