# 📘 Global Repositorty Feature (Trian.js)

`Global Repositorty Feature` helps 
The Global Repository Feature helps you organize your database access, makes it easier to write unit tests with mock data, and also gives you type-safety to prevent unexpected runtime errors.

---

## 🚀 CLI Commands

```bash
trian make:repo <module_name>
trian repo update
```

### **Create a new repository**
Example: `trian make:repo order`
```bash
trian make:repo <module_name>
```

### **Update/Generate global repository type cached for type-safety**
```bash
trian repo update
```

### **How to use?**
Step 1: You need to provide dependency(DI) in the module, like following this line.
```bash
import { $Repository } from 'trianjs/core';

// The key name must be like in the controller parameter dependency.
dependencies: {
    'globalRepo': $Repository
}
```

Step 2: If you want to use type-safety. You need to import type caching in the controller.
```bash
import 'trianjs/repository';
```