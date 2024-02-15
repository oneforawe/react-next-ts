# React-Next-TS

This repository is a template for
[React](https://react.dev) app projects using
[Next](https://nextjs.org/) and written in
[TypeScript](https://www.typescriptlang.org).

The purpose of this repo is:

* to act as a template to easily start new projects without re-writing common
  "boilerplate" code and configurations,
* to act as a reference to recall how to write certain patterns of code and
  accomplish certain tasks (such as achieving robust file-line-ending control
  with the repo code and steps below, to avoid issues later in development), and
* to demonstrate this particular approach and organization of code for any such
  React TypeScript project, using a generic folder structure, typescript and
  css/scss [code linting](./doc/Development.md) (geared for usage with
  [VSCode](https://code.visualstudio.com/)), and optional features such as redux
  state management, helper hooks for cyclic state refreshing, services with
  external API calls, and so on.

See the [development notes](./doc/Development.md) for tips on setting up the
repo properly with VSCode and usage of `eslint` and `stylelint`.  See the
[web development](./doc/WebDev.md) notes for more general notes and elaboration
on setup with node.  And see the [creation notes](./doc/Creation.md) for details
on how this repo was created and how to re-create it.

## Initial Readme Intro

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

* [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
* [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
