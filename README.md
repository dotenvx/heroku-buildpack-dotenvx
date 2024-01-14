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

Set `DOTENV_KEY` on heroku.

```shell
heroku config:set DOTENV_KEY='dotenv://:key_1234...@dotenvx.com/vault/.env.vault?environment=production'
```

On deploy, dotenvx will decrypt your `.env.vault` file using the `DOTENV_KEY` and inject your env just in time.

```
$ heroku logs --tail
heroku[web.1]: Starting process with command `dotenvx run -- node index.js`
app[web.1]: [dotenvx@0.9.0] injecting env (1) from encrypted .env.vault
```

---

> See [full guide to usage](https://dotenvx.com/docs/platforms/heroku)

---

To publish buildpack: `heroku buildpacks:publish dotenvx/heroku-buildpack-dotenvx main`
