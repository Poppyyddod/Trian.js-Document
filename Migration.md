# 📘 Migration Feature (Trian.js)

`Migratiob Feature` helps you to manage your database with code and track changes in the database.

---

## 🚀 CLI Commands
Example: `trian make:migration create_order_table`
For make a new migration file.
```bash
trian make:migration <migration_name>
```

Example: `trian run migrate:up mysql`
For run up method.
```bash
trian run migration:up <driver>
```

Example: `trian run migrate:down mysql`
For run down method.
```bash
trian run migration:down <driver>
```