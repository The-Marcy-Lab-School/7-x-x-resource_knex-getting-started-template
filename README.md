# Knex Getting Started

- [Knex Getting Started](#knex-getting-started)
- [How to use this repo](#how-to-use-this-repo)
- [Using Knex](#using-knex)

This repo is designed to get you up and running quickly with Knex. It has the setup files and skeleton code for you to put into your own project. It's not really designed to *teach* you per se, just give you a quick start.

# How to use this repo
This repo assumes you *already have* a main express project that you're working on. That means you have a `package.json` file and a `src` directory. If you don't have that, you should start there first! For clarity when we say "this repo" we mean this knex getting started repo, and when we say "main project" we mean your express project.

1. In your main project, run `npm install knex pg dotenv`
2. Copy this repo's `scripts` from the `package.json` into your main repo's `package.json` (remember, when copying json, you can't have trailing commas)
3. Copy this repo's `knexfile.js` and `.env.template` files into the root of your main project.
4. In your main project make a copy of `.env.template` as `.env` and fill in the details for your database
5. Copy over the `db` directory (and all its children directories) from this repo into your main project's `src` directory

That's it! You're done with this repo, now everything should be done through your main project!

# Using Knex
Technically, you don't *need* any of the scripts we added. You can just use `npx knex <whatever command>` to get things done. However, I'm willing to bet, you'll forget the literal commands to run migrations and seeds and whatnot. The reason that they're in the `package.json` is for documentation. It's called "readable code" and it's a good practice to get into. No need to google syntax, it's right there in your package.json!

Adding another model is easy, you just have to import the `knex.js` file in the `models` directory. You can see the example model in `db/models/example.js`.