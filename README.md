# Tailwind CSS: `@scope` variants canonicalize to unrelated `@scope` variants

```sh
npm install
npm run repro
```

- **Expected** (v4.3.3): `[@scope_(.card)]:flex`
- **Actual** (v4.3.4 and v4.3.5): `in-blue:flex`

`in-blue` is the `@custom-variant` in `input.css`. It scopes to `[data-theme='blue']`, not `.card`, so the two classes generate different CSS.
