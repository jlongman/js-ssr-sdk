# How to deploy

## Via shell script

1. Run `./deploy.sh`

1. Make sure new package is available via NPM: https://www.npmjs.com/package/configcat-nuxt

1. Add release notes: https://github.com/configcat/nuxt-sdk/releases

2. Update `configcat-nuxt` dependency in all sample applications:
   And test them by following their `README.md`.

or

## Manually

2. Run tests
   ```bash
    npm test
    ```

3. Create a new version (patch, minor, major)
Increase version number by using `npm version patch | minor | major`

    *Example: increasing patch version* 
    ```bash
    npm version patch
    ```
1. Push tag to remote
    
    If you tag the commit, TravisCI automatically publishes the package to NPM. 
    ```bash
    git push origin <new version>
    ```
    *Example: git push origin v1.1.17*

    You can follow the build status here -> https://travis-ci.com/configcat/nuxt-sdk

1. Make sure new package is available via NPM: https://www.npmjs.com/package/configcat-nuxt

1. Add release notes: https://github.com/configcat/nuxt-sdk/releases

2. Update `configcat-nuxt` dependency in all sample applications:
   And test them by following their `README.md`.