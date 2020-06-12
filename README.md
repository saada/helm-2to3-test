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


## Option 1

* Detect a v3 HelmRelease and it exists in Tiller
* Helm operator itself pauses sync loop and does the conversion automatically

## Option 2

* Shut down helm operator
* Run manual migration in all environments (non-destructive)
* Spin up helm operator with v3 support only
* Wait for each team to upgrade their HelmRelease to v3
* Turn off tiller
