# 📘 Controller Feature (Trian.js)

`Controller Feature` helps developers quickly generate, update, and maintain controllers inside each module.  
This feature ensures consistent code structure, reduces repetition, and keeps large projects organized.

---

## 🚀 CLI Commands

```bash
trian make:controller <module_name>/<controller_name>
trian controller update <module_name>
trian controller update-all
```

### **Create a new controller**
Example: `trian make:controller order/getOne`
```bash
trian make:controller <module_name>/<controller_name>
```
Result: You will see this
```bash
// Uncomment the following line for globalRepo type-safety.
import 'trianjs/repository';

import type { TrianBaseController, TrianContext, TrianRoute, TrianMiddleware } from 'trianjs/core/types';
import { TrianHandleErrorCls, RepoCache } from 'trianjs/core';

export default class ControllerName implements TrianBaseController {
    // Context data (request, response, etc...)
    private context = {} as TrianContext;

    // Global repository (use for call use database access)
    private globalRepo = {} as RepoCache;

    get route(): TrianRoute {
        return {
            module: '<module_name>',
            method: 'get',
            path: '/<module_name>'
        };
    }

    get middleware(): Array<TrianMiddleware> {
        return [];
    }

    async handle() {
        try {
            /////////////////////////////
            /// Business handle logic ///
            /////////////////////////////

            return this.context.response.status(200).json({});
        } catch (error) {
            // Trian auto runtime, validation errors handle(Required!, if you are using our Trian.js library)
            return TrianHandleErrorCls.responseToClient(this.context, error);
        }
    }
}
```

### **Update controllers in the module**
Example: `trian make:controller order`
```bash
trian controller update <module_name>
```

### **Update controllers in all module**
```bash
trian controller update-all
```