# helm-2to3-test

## Trigger

* if helm 2to3 conversion is destructive
    * user has to have an explicit flag or spec.convert: true to apply the migration
* else
    * ...


## Use case

* We want to slowly migrate HelmReleases to v3 over 30 days
* HelmRelease

## Things to migrate

* Helm chart
* HelmRelease crd object
* Tiller state

## Questions

* Is helm 2to3 conversion destructive?
* When should we trigger the conversion?
