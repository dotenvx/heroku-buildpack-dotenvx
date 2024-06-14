![dotenvx](https://dotenvx.com/better-banner.png)

> install `dotenvx` to heroku
> ```
> heroku buildpacks:add https://github.com/dotenvx/heroku-buildpack-dotenvx
> ```

## Usage

Add `dotenvx` to your Procfile.

```yaml
# Procfile
web: dotenvx run -- node index.js
```

> See [full usage guide](https://dotenvx.com/docs/platforms/heroku)

---

To publish buildpack: `heroku buildpacks:publish dotenvx/heroku-buildpack-dotenvx main`
