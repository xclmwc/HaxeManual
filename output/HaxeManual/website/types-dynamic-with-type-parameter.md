## 2.7.1 Dynamic with Type Parameter

`Dynamic` is a special type because it allows explicit declaration with and without a [type parameter](type-system-type-parameters.md). If such a type parameter is provided, the semantics described in [Dynamic](types-dynamic.md) are constrained to all fields being compatible with the parameter type:

```haxe
var att : Dynamic<String> = xml.attributes;
// valid, value is a String
att.name = "Nicolas";
// dito (this documentation is quite old)
att.age = "26";
// error, value is not a String
att.income = 0;
```

---

Previous section: [Dynamic](types-dynamic.md)

Next section: [Implementing Dynamic](types-dynamic-implemented.md)