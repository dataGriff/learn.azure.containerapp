# Azure Container App Deployment Learning

- [Idea Sourced from Medium](https://medium.com/@abhimanyubajaj98/seamless-azure-container-apps-deployment-with-terraform-c2e56d719465)

Updated my own template terraform in this clone. Updated to latest azurerm provider and allowed terraform.sh to apply if I pass in param.

```bash
sh ./cde/terraform.sh True
```

## Notes

- Container reg, container environment and log analytics should be in separate platform hosted. In here just for quick try.
- First run of terraform seemed to create container app all fine portal but terraform failed and the activity log failed. Terraform state file did not bring in the new resource even though was there, so I had to remove and start again...
- Issue with deployment of container app due to ingress, see [issue here](https://github.com/hashicorp/terraform-provider-azurerm/issues/20435). HAve tried the config trichling suggested in my terraform. And yes this works.