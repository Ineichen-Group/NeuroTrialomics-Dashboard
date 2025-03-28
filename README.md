# NeuroTrialomics-Dashboard

Reference code: https://github.com/wch/retirement-simulation-dashboard/tree/main

## Setup 

This dashboard was created using [Quarto Dashboards with Shiny for Python](https://quarto.org/docs/dashboards/interactivity/shiny-python/index.html).

You can install the required libraries in a local environment via:
```
conda env create -f environment.yml
```

## Code and local testing

The main file is [./neurotrial_dashboard.qmd](./neurotrial_dashboard.qmd).

You can run the following to preview the dashboard in localhost:
```
quarto preview neurotrial_dashboard.qmd
```

The command should also result in the following outputs:

```
neurotrial_dashboard.html
neurotrial_dashboard_files/
app.py
```

You can run this as a normal Shiny application with shiny run to make sure it works as expected.
```
shiny run
```

## Deployment to shinyapps.io

As described in [Cloud hosting](https://shiny.posit.co/py/docs/deploy-cloud.html):

```
rsconnect deploy shiny /path/to/app --name <NAME> --title my-app
```

where:
- < NAME >: This specifies the account or server name that you have set up in your rsconnect configuration. It determines where the app will be deployed.
- my-app: This sets the title of the application as it will appear in the deployment environment.

The /path/to/app should contain the above mentioned files and all the required data used for the app to run, i.e., the upper most folder of the whole project.


