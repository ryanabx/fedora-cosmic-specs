# Fedora COSMIC RPM spec files

This repository is just a submodule checkout of all the spec files we maintain for Fedora COSMIC

## Initialize submodules (no update)

```sh
git submodule update --init --recursive
```

## Update Submodules

```sh
git submodule update --init --recursive --remote
```

## Clean Submodules (Can be used after working on patches to spec files)

```sh
git submodule foreach git clean -ffdx
git submodule foreach git reset --hard
```

## Create a patch for a specfile (for use in cosmic-packaging)

```sh
cd cosmic-<PACKAGE>
# Make specfile changes
git add .
git commit -sm "My Patch"
git format-patch -1
# Patch will be located in the directory
```
