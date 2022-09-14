# chaskiq-helm
a helm/charts for chaskiq

## Quick start

### Installing the Chart

To install the chart with the release name `chaskiq` using a dedicated namespace(recommended):

```shell
helm install --create-namespace --namespace chaskiq chaskiq ./chaskiq-helm
```

Go to the chaskiq pod and execute
```shell
bundle exec rails db:setup
bundle exec rails db:migrate
bundle exec rails db:seed
bundle exec rails admin_generator
```

### Uninstalling

To uninstall/delete the `chaskiq`:

```shell
helm delete chaskiq --namespace chaskiq
```