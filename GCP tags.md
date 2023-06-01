# Working with tags

## Create a tag

```cmd
gcloud resource-manager tags keys create [TAG_KEY_SHORT_NAME] \
    --parent=[projects/YOUR_PROJECT_ID] or [organizations/YOUR_ORGANIZATION_ID]
```

## Add tag values
```cmd
gcloud resource-manager tags values create [TAG_VALUE_SHORTNAME] \
    --parent=[tagKeys/YOUR_TAG_KEY_ID] or 
```

## Add a description and update the tag
```cmd
gcloud resource-manager tags keys update [tagKeys/YOUR_TAG_KEY_ID] \
    --description=[DESCRIPTION]
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
- List keys:
```cmd
gcloud resource-manager tags keys list --parent=[projects/YOUR_PROJECT_ID]
```
```cmd
gcloud resource-manager tags keys list --parent=[organizations/YOUR_ORGANIZATION_ID]
```



## 
