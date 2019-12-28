# Private Helm-Charts Repository
## Notes:
### Setup Git
1. Fetch the helm chart:

        helm fetch --untar stable/wordpress
2. Modify the helm chart
3. Package back the helm chart

        helm package wordpress
4. Create helm repository index file, and update it with new packages added:

        helm repo index .
5. Update Helm Repo Cloud for any changes

        helm repo update
    
