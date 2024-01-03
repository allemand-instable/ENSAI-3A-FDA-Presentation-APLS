## modifications

📁 jsconfig.json

```json
{
  "compilerOptions": {
    ...
    // ⚠️ NEEDED FOR VSCODE PATH INTELLISENSE
    "paths": {
        "$lib/*": ["./src/lib/*"],
        "$slides/*": ["./src/slides/*"],
        "$APLS/*" : ["./src/slides/APLS/*"],
    }
  }
}
```

📁 vite.config.js

```js
export default defineConfig({
  plugins: [svelte()],
  resolve: {
    alias: {
      $lib: "/src/lib",
      $slides: '/src/slides',
      $APLS: '/src/slides/APLS'
    },
  },
});

```