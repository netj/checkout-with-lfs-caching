# checkout-with-lfs-caching
GitHub Action for checkout with LFS caching

This will [cache](https://docs.github.com/en/actions/guides/caching-dependencies-to-speed-up-workflows) your entire list of LFS files and avoid using download quota. If any LFS file changes, the full list of files will be downloaded again. See also [the original issue](https://github.com/actions/checkout/issues/165) on `actions/checkout`.
  
## Usage
In your Action `.yml` file, simply replace your checkout step from

```
    steps:
      - name: Checkout
        uses: actions/checkout@v2
        with:
          lfs: true
```

to

```
    steps:
      - name: Checkout
        uses: netj/checkout-with-lfs-caching@v1
```
