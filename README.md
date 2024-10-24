# Evershop

Learning Evershop

## First Time: Get Started

### 1. Make a PostgreSQL DB

For example, name it `evershop_db`

### 2. Make a GitHub repo

```bash
mkdir <project-name>
cd <project-name>
```

### 3. Start the installations

```bash
npm init
npm install @evershop/evershop
```

### 4. Add Evershop Commands

Add the following commands in the `"scripts"` section of the `package.json`.

```bash
"scripts": {
    "setup": "evershop install",
    "build": "evershop build",
    "build:skip:minify": "evershop build -- --skip-minify",
    "start": "evershop start",
    "start:debug": "evershop start --debug",
    "dev": "evershop dev",
    "user:create": "evershop user:create",
    "user:changePassword": "evershop user:changePassword"
}
```

### 5. Run Evershop Setup command

```bash
npm run setup
```

#### Answer Prompts

You'll get prompted eventually with the following questions.

Be mindful of your answers.

They're DB questions. And some are credentials so that you can login in the Admin.

**NOTE:** You should already have the PostgreSQL DB created before this so that you can answer the DB Name prompt question.

![image](/docs/images/evershop_setup_question_prompts.png)

```bash
Postgres Database Host (localhost) · localhost
✔ Postgres Database Port (5432) · 5432
✔ Postgres Database Name (evershop) · evershop_db
✔ Postgres Database User (postgres) · postgres
✔ PostgreSQL Database Password (<empty>) · cherub88
✔ Your full name · June Rockwell
✔ Your administrator user email · devapprocks@gmail.com
✔ Your administrator user password · *
```

This should generate a `.env` file for you.

### 6. Build using Evershop build command

Use the regular one if you need minification

```bash
npm run build
```

For faster build, skip minification

```bash
npm run build:skip:minify
```

### 7. Start the app

```bash
npm run start
```

### 8. Run Apps on the Browser!

Evershop comes with a Storefront and an Admin.

#### Storefront

The Storefront is in [localhost:3000](http://localhost:3000)

#### Admin

The Admin can be accessed in [localhost:3000/admin](http://localhost:3000/admin)

### 9. Add `.gitignore` file

Make sure to add a `.gitignore` file so that some files don't ever go up to GitHub.

```git
node_modules/
.env
.env.*
```
