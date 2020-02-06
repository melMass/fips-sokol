fips-sokol
=========

fipsified sokol (https://github.com/floooh/sokol)

fips build system: https://github.com/floooh/fips

## How to integrate:

Add the dependency to your fips.yml file:

```yaml
imports:
    fips-sokol:
        git: https://github.com/melMass/fips-sokol
```

Call `sokol_config()` and use sokol as dependency in your targets:

```cmake
sokol_config()
fips_begin_*(...)
    ...
    fips_deps(sokol)
fips_end_*(...)
```
