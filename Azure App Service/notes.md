# Azure App Service Notes

## Create an Azure Web App
1. Azure Portal -> Create a Service -> Web App
2. Follow the wizard to configure
    1. Publish: 1. Code 2. Docker Container 3. Static Web App
    2. Runtime Stack dropdown menu
    3. OS selection
    4. Region
    5. Pricing Plans
        1. App Service Plans
        2. Can deploy multiple apps to an app service plan up to the limits of the plan
        3. Azure Compute Units (ACU) a metric to estimate performance
    6. Deployment
        1. GitHub actions is Azure's CI/CD for GitHub
    7. Networking
        1. Only available for premium level tiers to control traffic
    8. Monitoring
        1. Application insights for logging
    9. Tags for metadata

## Web App Scaling and App Service
1. Once created go to View Resource
2. Multiple menus for actions or insights for your web app
    1. Deployment Center: Other deployment options beyond GitHub Actions
    2. Quickstart: Guides for deploying starter web app code
    3. App scaling: Up or Out
    4. TLS/SSL settings
    5. Backups

