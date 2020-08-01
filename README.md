# nx workspace lint issue with .nxignore

this is related to https://github.com/nrwl/nx/issues/3376

nx-version `10.0.7`

* in `libs\api-interfaces` there is a file `README.md`
* when we run `nx workspace-lint` we should not get an error, because this file is listed in `.nxignore`
* but we do get an error: 
```
>  NX   ERROR  The following file(s) do not belong to any projects:

  - libs/README.md

```
