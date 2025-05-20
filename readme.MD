# Ingress Controller

REGION_CODE=us-east-1
CLUSTER_NAME=expense
ACC_ID=090808669085

### Setting Permissions

* Create an IAM OIDC provider
```
eksctl utils associate-iam-oidc-provider \
    --region $REGION_CODE \
    --cluster $CLUSTER_NAME \
    --approve
```

## update kubeconfig file for your cluster
```
aws eks update-kubeconfig --region $REGION_CODE --name $CLUSTER_NAME
```