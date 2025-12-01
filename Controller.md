# 📘 Controller Feature (Trian.js)

The **Controller Feature** in Trian.js helps developers quickly generate, update, and maintain controllers inside each module.  
This feature ensures consistent code structure, reduces repetition, and keeps large projects organized.

---

## 🚀 Controller CLI Commands

```bash
trian make:controller <module_name>/<controller_name>
trian controller update <module_name>
trian controller update-all
```

### **Create a New Controller**
Example: `trian make:controller order/getOne`
```bash
trian make:controller <module_name>/<controller_name>
```

### **Update controllers syntax in the module**
Example: `trian make:controller order`
```bash
trian controller update <module_name>
```

### **Update controllers syntax in all module**
```bash
trian controller update-all
```