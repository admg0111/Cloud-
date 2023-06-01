# Working with tags

## Create a tag

```cmd
gcloud resource-manager tags keys create [SHORT_NAME] \
    --parent=[projects/YOUR_PROJECT_ID] or [organizations/YOUR_ORGANIZATION_ID]
```
Example:
```cmd
gcloud resource-manager tags keys create Departamento \
    --parent=organizations/485697030
```

## Get tag info

- Describe:
```cmd
gcloud resource-manager tags keys describe [tagKeys/YOUR_TAG_ID]
```
```cmd
gcloud resource-manager tags keys describe [YOUR_PROJECT_ID/TAG_SHORT_NAME]
```
- List:
