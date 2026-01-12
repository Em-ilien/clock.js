# Clock.js

This project is a clock webapp.

See demo at https://www.em-ilien.fr/clock/

![alt text](image.png)

## Tech stack

Svelte, SvelteKit, vite

## Installation

To install the library, use npm:

```bash
npm install clock.svelte
```

## Usage

Here is an example of using Clock.js:

```svelte
<script>
	import { Clock } from 'clock.svelte';
</script>

<div>
	<Clock />
</div>
```

/!\ The [clock background image](./src/lib/clock.png) has to be placed into your main svelte application's $lib folder (path /src/lib/clock.png).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

Emilien Cosson

## Contribution

Any contributions are welcome! Please follow these steps to contribute:

1. Open an issue on GitHub to discuss your changes.
2. Make your changes and submit a Pull Request (PR).
3. Commits should follow the syntax below:

```
<type>(<scope>): <subject>

<description>

<footer>
```

- **Type** defines the type of commit (build, ci, docs, feat, fix, perf, refactor, style, test).
- **Scope** defines which part of the library/application is affected (optional).
- **Subject** is a brief description of the changes, using the imperative mood and without a capital letter or period.
- **Description** provides a more detailed explanation of the motivations behind the change (following the same rules as the Subject).
- **Footer** contains important changes (Breaking Changes) and references to GitHub/GitLab issues or others.

## Developing

Start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

Everything inside `src/lib` is part of the library, everything inside `src/routes` can be used to test or preview the component.

## Building

To build the library:

```bash
npm run package
```

To create a production version of the showcase app:

```bash
npm run build
```

To preview the production build with `npm run preview`.

> To deploy the app, install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## Publishing

```bash
npm version patch   # 2.0.4 → 2.0.5
npm version minor   # 2.0.4 → 2.1.0
npm version major   # 2.0.4 → 3.0.0

npm publish
npm login
```

