# Deploying the 1Password SCIM Bridge on Fly

```
# Setup app
fly launch --copy-config

# Launch Redis
fly redis create --enable-eviction --no-replicas --plan Free

# Add secrets
fly secrets set OP_SESSION=(cat ~/Downloads/scimsession | base64 -) OP_REDIS_URL="redis://..."

fly deploy \
		--image 1password/scim \
		--image-label v2.6.2  \
		--strategy immediate
```
