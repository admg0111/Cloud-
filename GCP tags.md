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

- Describe keys:
```cmd
gcloud resource-manager tags keys describe [tagKeys/YOUR_TAG_KEY_ID]
```
```cmd
gcloud resource-manager tags keys describe [YOUR_PROJECT_ID/TAG_SHORT_NAME]
```
- Describe tag values:
```cmd
gcloud resource-manager tags values describe [tagValues/YOUR_TAG_VALUE_ID]
```
```cmd
gcloud resource-manager tags values describe [YOUR_PROJECT_ID/TAG_KEY_SHORT_NAME/TAG_VALUE_SHORT_NAME]
```
