# How to get start with Trian.js

## 🚀 CLI Commands
```bash
npx trianjs@latest create:project <project_name>
```

```bash
trian init
```

## **Create Your New Project**
Case 1: If you do not have your project folder, use this command.
```bash
npx trianjs@latest create:project <project_name>
```

## **Init Your Project**
Case 2: If you already have a project folder, use this command.
```bash
npm install trianjs@latest
npm install -g trianjs@latest
trian init
```

## **Result**
```bash
node_modules/
src/
-app/
--controllers/
---posts/
----createPost.ts
----index.ts
---README.md
--databases/
---migrations/
----YY-mm-dd-create_posts_table.ts
---config.ts
---README.md
--modules/
---index.ts
---post.module.ts
---README.md
--repositories/
---post.repo.ts
---README.md
--index.ts <-(app)
.env
package-lock.json
package.json
tsconfig.json
```