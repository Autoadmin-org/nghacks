# Create an Angular Library

1. Change directory to `main`

2. Create library

```bash
ng g lib <lib-name>
```

> - This command will create the library on `main/projects/<lib-name>`.
> - Will update angular.json, tsconfig.json & tsconfig.base.json on `main` workspace.

3. Add npm scripts to serve & build the new lib on `main/package.json`

4. Update lib `package.json` with basic information.

> - Add `@nghacks` scope to the package name.
> - Add `description`, `keywords`, `author`, `repository`, `homepage`, `bugs`, `license`, `private`

```bash
"serve:<lib-name>": "ng build --project=<lib-name> --watch",
"build:prod:<lib-name>": "ng build --project=<lib-name> --prod"
```

5. Update existing script `build:packages:prod` on `main/package.json`

```bash
"build:packages:prod": "<existing npm commands> && build:prod:<lib-name>",
```

6. Develop the library.

7. Add proper version number.

8. Write proper readme.

9. Build & publish the package to NPM

10. Create Github Action to update NPM package on push