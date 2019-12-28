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
5. Add the newly created helm repo url:

        helm repo add realmc https://raw.githubusercontent.com/mhmdksh/helm-charts/master
6. Push the updated and newly packaged helm charts to the git helm repo:

        git add .
        git commit -m "New Release 8.2.0 Update"
        git push
7. Update Helm Repo Cloud for any changes

        helm repo update
8. Install specific verison of the application from the repository:
                
        helm install --version=8.1.0 realmc/wordpress --generate-name
