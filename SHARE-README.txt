IT Project Management UI Preview

Open index.html to navigate the five proposal screens. The .dc.html screens use support.js and vendor/; keep all files and folders together.

For local viewing, start a web server in this folder (for example: python -m http.server 8000) and open http://localhost:8000. This also works when uploaded to a static website host.

OneDrive is suitable for storing and sharing the folder, but its file preview is not a reliable web host for interactive HTML. For a client-facing live demo, upload this complete folder to a static hosting service and share the hosted index.html URL. In OneDrive, share the whole folder if you want the client to download the source package.

Deploy to Azure Static Web Apps

The GitHub Actions workflow deploys this static site from the repository root whenever changes are pushed to main.

1. In GitHub, open Settings > Secrets and variables > Actions for this repository and add a repository secret named AZURE_STATIC_WEB_APPS_API_TOKEN.
2. Set its value to the deployment token for the Azure Static Web App named project-management-preview. Do not commit the token or put it in the workflow file.
3. Push the workflow and site files to main, or rerun the workflow from the Actions tab. The deployment URL is shown on the Static Web App's Overview page in Azure.
