# GSP1006
Quick Solution for Managing Vault Tokens Lab (GSP1006)

Link: https://www.cloudskillsboost.google/focuses/32201?parent=catalog

## Solution
Copy and paste this block of codes into the Cloud Shell:

```bash
cat > token_policies.txt <<EOF_END
[
  "default",
  "jenkins"
]
EOF_END


export PROJECT_ID=$(gcloud config get-value project)
gsutil cp token_policies.txt gs://$PROJECT_ID
```
