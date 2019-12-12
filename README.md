# Network

```powershell
Get-NetAdapterAdvancedProperty > NetworkDriverPropertiesBefore.txt
Get-NetAdapterAdvancedProperty | Where DisplayName -match Offload | Set-NetAdapterAdvancedProperty -DisplayValue 'Disabled'
Get-NetAdapterAdvancedProperty | Where DisplayName -match 'Receive Side Scaling' | Set-NetAdapterAdvancedProperty -DisplayValue 'Disabled'
Get-NetAdapterAdvancedProperty | Where DisplayName -match 'Virtual Machine Queues' | Set-NetAdapterAdvancedProperty -DisplayValue 'Disabled'
Get-NetAdapterAdvancedProperty > NetworkDriverPropertiesAfter.txt
```
