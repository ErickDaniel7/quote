<div align="center"><h3>Random Quote of the day</h3></div><br>

<!--STARTS_HERE_QUOTE_README-->
<i>❝“It is easier to change the specification to fit the program than vice versa.”— Alan Perlis   ❞</i>
<!--ENDS_HERE_QUOTE_README-->
```

5. Go to Workflows menu (mentioned in step 1), click `Update Quote Readme`, click `Run workflow`.
6. Go to your profile page, you will be able to see a random quote/fact wherever you placed [this](#update-your-readme) comment on README.

---

### Examples

1. If you want to use this action for a README that is not present in current workflow repository.

```yml
- uses: siddharth2016/update-readme-image@main
  with:
    GH_TOKEN: ${{ secrets.GH_TOKEN }}     # Needed if README repository is not profile repo
    REPOSITORY: <username>/<differentrepo>
```

Using `REPOSITORY` will change README present in that repository head.

For example, if your workflow is present in `<username>/repo1` and you want to update README present in `<username>/repo2`, then assign `REPOSITORY` to `<username>/repo2` in workflow at `<username>/repo1`.

2. You can specify a commit message to override the default _"Update with quote-readme"_.

```yml
- uses: siddharth2016/update-readme-image@main
  with:
    GH_TOKEN: ${{ secrets.GH_TOKEN }}     # Needed if README repository is not profile repo
    REPOSITORY: <username>/<differentrepo>  # Needed if README repository is not current repo
    COMMIT_MESSAGE: <your-commit-message>       # default - Update with quote-readme
```

3. You can also choose if you only want either a random `quote` or a random `funfact` to appear on your readme, by default it is `both`.

```yml
- uses: siddharth2016/update-readme-image@main
  with:
    GH_TOKEN: ${{ secrets.GH_TOKEN }}     # Needed if README repository is not profile repo
    REPOSITORY: <username>/<differentrepo>  # Needed if README repository is not current repo
    COMMIT_MESSAGE: <your-commit-message>       # default - Update with quote-readme
    OPTION: both            # default - both, can be one of (quote, funfact, both), if 'both' then will display either a quote or a fact
```

---

### Tests

To run tests simply execute the following in the directory containing `main.py`:

```bash
python -m unittest discover
```

---

#### Another intriguing action you would want to use - [wallpaper-day](https://github.com/ErickDaniel7/wallpaper-day/tree/main)
