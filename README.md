# SeQuenC Helm charts repository

This repository is intended to store helm charts for components that constitute the SeQuenC platform.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

`helm repo add sequenc https://sequenc-consortium.github.io/helm-charts`

If you had already added this repo earlier, run `helm repo update` to retrieve the latest versions of the packages.  
You can then run `helm search repo <alias>` to see the charts.

To install the <chart-name> chart:

`cd qunicorn-chart`

`helm install my-<chart-name> .`

To uninstall the chart:

`helm delete my-<chart-name>`


------------------------------------------------------------------------------------------------------------------------------------


Converting YAML Files Into Helm Charts
We do it in 2 ways:
1) Using helmify
2) Manually
   
First, we will understand using Helmify
Step 1. Installation of helmify
Step2. Convert YAML files to Helm chart
For single yaml file: 
`cat <your-yamlfile-name>.yaml | helmify <chart-name>`
From directory with yamls:
`awk 'FNR==1 && NR!=1  {print "---"}{print}' /<my_directory>/*.yaml | helmify <helmchart-folder-name>`




