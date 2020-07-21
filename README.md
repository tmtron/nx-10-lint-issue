# nx workspace lint issue with .gitignore

* in `libs\ui` 
  * create a file `.gitignore`
    * file contents: `ignore.this`
  * create a file `ignore.this` - content does not matter
* now run `./node_modules/.bin/nx workspace-lint`, this will fail with:
```
>  NX   ERROR  The following file(s) do not belong to any projects:

  - libs/api-interfaces/ignore.this
```
* this is a bug, because files listed in the `.gitignore` file should be ignored

see https://github.com/nrwl/nx/issues/3376
