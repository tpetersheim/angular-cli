# Configure HTTP Headers

Using the headers support in webpack's dev server we can configure HTTP headers for serving content.
We do this by passing a file to `--headers-config`

Say we want to add a custom header, `X-Custom-Header`, to server responses.

We create a file next to projects `package.json` called `headers.conf.json`
with the content

```json
{
  "X-Custom-Header": "yes"
}
```

and then we edit the `package.json` file's start script to be

```json
"start": "ng serve --headers-config headers.conf.json",
```

now run it with `npm start`
