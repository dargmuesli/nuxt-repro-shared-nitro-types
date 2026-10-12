Since Nuxt 4.6.0, `nuxt typecheck` fails on server handlers as soon as a file in `shared/` imports from `nuxt/app`, even type-only.

`pnpm install && pnpm typecheck` reports `server/api/hello.ts(1,16): error TS2304: Cannot find name 'defineEventHandler'.`

It passes on Nuxt 4.5.2, and with the `prepare:types` workaround in `nuxt.config.ts` uncommented.
