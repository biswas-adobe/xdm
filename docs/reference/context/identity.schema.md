
# Identity Schema

```
https://ns.adobe.com/xdm/context/identity
```

Identity is used to clearly distinguish people that are interacting with digital experiences. Identity is established by an identity provider, which itself is referenced in the `namespace` attribute. Within each `namespace`, the identity is unique.

| [Abstract](../../abstract.md) | [Extensible](../../extensions.md) | [Status](../../status.md) | [Identifiable](../../id.md) | [Custom Properties](../../extensions.md) | [Additional Properties](../../extensions.md) | Defined In |
|-------------------------------|-----------------------------------|---------------------------|-----------------------------|------------------------------------------|----------------------------------------------|------------|
| Can be instantiated | Yes | Stabilizing | Yes | Forbidden | Permitted | [context/identity.schema.json](context/identity.schema.json) |
## Schema Hierarchy

* Identity `https://ns.adobe.com/xdm/context/identity`
  * [Extensibility base schema](../common/extensible.schema.md) `https://ns.adobe.com/xdm/common/extensible`
  * [Namespace](namespace.schema.md) `https://ns.adobe.com/xdm/context/namespace`


## Identity Example
```json
{
  "@id": "https://data.adobe.io/entities/identity/id123",
  "xdm:namespace": {
    "xdm:code": "AA12345"
  }
}
```

# Identity Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [@id](#@id) | `string` | Required if identity is specified as a combination of namespace and id. Either namespace and id or xid attribute is required  | Identity (this schema) |
| [xdm:namespace](#xdmnamespace) | Namespace | Required if identity is specified as a combination of namespace and id. Either namespace and id or xid attribute is required | Identity (this schema) |
| [xdm:primary](#xdmprimary) | `boolean` | Optional | Identity (this schema) |
| [xdm:xid](#xdmxid) | `string` | Required if identity is specified in the native xid form. Either namespace and id or xid attribute is required | Identity (this schema) |
| `*` | any | Additional | this schema *allows* additional properties |

## @id
### Identifier

Identity of the consumer in the related namespace.

`@id`
* is required if identity is specified as a combination of namespace and id. Either namespace and id or xid attribute is required
* type: `string`
* defined in this schema

### @id Type


`string`
* format: `uri` – Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## xdm:namespace
### Namespace

The namespace associated with the `xid` attribute and matched up with the AAM data source integration code.

`xdm:namespace`
* is required if identity is specified as a combination of namespace and id. Either namespace and id or xid attribute is required
* type: Namespace
* defined in this schema

### xdm:namespace Type


* [Namespace](namespace.schema.md) – `https://ns.adobe.com/xdm/context/namespace`





## xdm:primary
### Primary

Indicates this identity is the preferred identity. Is used as a hint to help systems better organize how identities are queried.

`xdm:primary`
* is optional
* type: `boolean`
* defined in this schema

### xdm:primary Type


`boolean`





## xdm:xid
### Experience Identifier

When present, this value represents a cross-namespace identifier that is unique across all namespace-scoped identifiers in all namespaces.

`xdm:xid`
* is required if identity is specified as a combination of namespace and id. Either namespace and id or xid attribute is required
* type: `string`
* defined in this schema

### xdm:xid Type


`string`





