# Project with TS Node and Paths Configuration

This project uses the `paths` compiler option to shared code between two typescript
projects in the same workspace.

This project also uses `ts-node` to run the application. 

In order for `ts-node` to find the modules in the `paths`, the `tsconfig-paths`
package needs to be installed.

## Running

Run the application with `ts-node` using the `-r tsconfig-paths/register` option.

```
npx ts-node -r tsconfig-paths/register --project app1/tsconfig.json app1/src/index.ts
```

## TS Config

Alternateively, add the `ts-node` section to the `tsconfig.json`

"ts-node": {
    "require": ["tsconfig-paths/register"]
}

## Author

Maverik Minett  maverik.minett@gmail.com

## Copyright

© 2023 Maverik Minett

## License

MIT
