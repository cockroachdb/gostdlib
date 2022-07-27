# gostdlib

gostdlib contains copies of some choice standard library packages so they can be
versioned separately from a Go installation. The list currently includes:

  * cmd/gofmt
  * go/format
  * go/printer
  * golang.org/x/sync†
  * golang.org/x/tools/cmd/goimports†
  * golang.org/x/tools/imports†

<sup>† These aren't technically standard library packages.</sup>

## Maintainer guide

To update this repository with the sources for a new Go or x/tools version,
bump the versions in bin/update, then run the script:

```
$ bin/update
```

You may need to update the patches in the `patches/` directory until tests pass
on all desired Go versions. The list of automatically tested Go versions is in
`travis.yml`.
