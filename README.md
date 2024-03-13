# Self hosted Agent

https://vstsagentpackage.azureedge.net/agent/3.234.0/vsts-agent-linux-x64-3.234.0.tar.gz

```
~/$ mkdir myagent && cd myagent
```

```
tar zxvf ~/Downloads/vsts-agent-linux-x64-3.234.0.tar.gz
```

```
 ./config.sh
```
```
 ./run.sh
```

```
https://dev.azure.com/adityaelegant
```

```
ladktgkcxuwq5at2wtnubi2lzb2m5nyuymqqhagpqx4nezckowka
```


```
siruwbl3icm55eb4xqzhz4pve73umi2wa5s3lg37a4d64v2j4upa
```


```
steps:
- script: |
    echo "registry=$(npmRegistry)" > .npmrc
    echo "//$(npmRegistry):_authToken=$(npmToken)" >> .npmrc
  displayName: 'Set up .npmrc'
```


















```
# Read the .npmrc file
$content = Get-Content -Path .\.npmrc

# Print the content
Write-Output "Current .npmrc content:"
Write-Output $content

# Replace the token
$newToken = "<Your-New-Token>"
$content = $content -replace "//registry.npmjs.org/:_authToken=.*", "//registry.npmjs.org/:_authToken=$newToken"

# Write the new content back to the .npmrc file
$content | Out-File -FilePath .\.npmrc

# Print the updated content
Write-Output "Updated .npmrc content:"
Get-Content -Path .\.npmrc
```
