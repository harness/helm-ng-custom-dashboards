#Helm chart for ng-custom-dashboards

### Publishing the Chart
Bump version of the Chart in `src/ng-custom-dashboards/Chart.yaml`
```shell
OLD_VERSION=$(grep -E '^version:' src/ng-custom-dashboards/Chart.yaml | cut -d ' ' -f 2)
NEXT_VERSION=$(echo "$OLD_VERSION" | awk -F. '{print $1"."$2"."$3+1}')
sed -i -E -e "s/^version: ${OLD_VERSION}/version: ${NEXT_VERSION}/" src/ng-custom-dashboards/Chart.yaml
```

Package the Chart
```shell
helm package src/ng-custom-dashboards -d charts -u
```

Update the repo index
```shell
helm repo index charts
```

Commit the changes
```shell
git tag "$NEXT_VERSION"
git add --all
git commit -m "preparing release $NEXT_VERSION"
```

### Parameters
