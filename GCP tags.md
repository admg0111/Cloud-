## Working with tags
#Create a tag

```cmd
gcloud resource-manager tags keys create [SHORT_NAME] \
    --parent=[projects/YOUR_PROJECT_ID] or [organizations/YOUR_ORGANIZATION_ID]
```
Example:
```cmd
gcloud resource-manager tags keys create Departamento \
    --parent=organizations/485697
```
