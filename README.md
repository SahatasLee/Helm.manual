# Helm

Helm is the package management solution for Kubernetes. A package manager automates the process of installing, upgrading, configuring, and removing software packages. Like Yum/RPM/APT in the Linux ecosystem and Chocolatey/Homebrew in Windows/Mac machines, Helm simplifies the software installation lifecycle in Kubernetes. [Getting Started.](https://helm.sh/docs/chart_template_guide/getting_started/)

## Helm Structure

```sh
mychart/
  Chart.yaml          # A YAML file containing information about the chart
  LICENSE             # OPTIONAL: A plain text file containing the license for the chart
  README.md           # OPTIONAL: A human-readable README file
  values.yaml         # The default configuration values for this chart
  values.schema.json  # OPTIONAL: A JSON Schema for imposing a structure on the values.yaml file
  charts/             # A directory containing any charts upon which this chart depends.
  crds/               # Custom Resource Definitions
  templates/          # A directory of templates that, when combined with values,
                      # will generate valid Kubernetes manifest files.
  templates/NOTES.txt # OPTIONAL: A plain text file containing short usage notes
  ...
```

## Start

```sh
$ helm create mychart
mychart/
  Chart.yaml
  values.yaml
  charts/
  templates/
  ...
```

##

```sh
helm get manifest release-name

helm install --debug --dry-run release-name ./mychart
```