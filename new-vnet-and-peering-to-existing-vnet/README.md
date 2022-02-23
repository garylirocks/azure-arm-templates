
This template creates a new vnet and peer it to an existing vnet in another resource group (same subscription), because the peering needs to be created at the both ends, so there's a nested template to create the peering at the other end.

You could customize paramaters in `params.json`

```sh
az deployment group create \
  --resource-group temp-rg \
  --template-file ./template.json \
  --parameters @params.json
```