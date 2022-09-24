### Instalar desde PowerShell

```
Install-WindowsFeatures -Name Hyper-V IncludeManagementTools -Restart
```

### Habilitar virtualización anidada

```
Set-VMProcessor -VMName nombre-de-maquina ExposeVirtualizationExtensions $True
```