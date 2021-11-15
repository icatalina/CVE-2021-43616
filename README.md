Repo demonstrating CVE-2021-43616 / https://github.com/npm/cli/issues/2701

Remove the `node_modules` folder and run `npx npm@8 ci`, you can see how
npm will install version 2.2.x (2.2.16 at the time of this commit) even though
package-lock.json requires 2.0.0

```
cat node_modules/shortid/package.json
```

I've commited the `node_modules` from the original install so the issue is obvious
after running `npm ci`
