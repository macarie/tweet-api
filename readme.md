# @macarie/tweet-api

A fork of [`vercel/react-tweet`](https://github.com/vercel/react-tweet) that exports only the contents of the API and utils files.

## Install

`@macarie/tweet-api` is published on [JSR](https://jsr.io); install it by picking the command for your package manager and/or runtime:

```bash
npx jsr add @macarie/tweet-api       # npm
pnpm dlx jsr add @macarie/tweet-api  # pnpm
deno add @macarie/tweet-api          # Deno
bunx jsr add @macarie/tweet-api      # Bun
```

## Usage

```ts
import { enrichTweet, getTweet } from "@macarie/tweet-api";

const apiResponse = await getTweet(id);

if (apiResponse === undefined) {
	throw new Error(`Tweet doesn't exist: ${id}`);
}

const tweet = enrichTweet(api);
```

Reading the [`Tweet` component's](https://github.com/vercel/react-tweet/blob/main/packages/react-tweet/src/tweet.tsx) source code can help you infer the usage (and utility) of other helpers and utils.

## Notes

> [!CAUTION]
> **Expect breaking changes between minor versions.** This package does not follow SemVer conventions.
>
> The package is intentionally kept as `0.X.Y` so that package managers won't update it automatically.
