## Order Return Tax

Represents a tax being returned that applies to one or more return line items in an order.

Fixed-amount, order-scoped taxes are distributed across all non-zero return line item totals.
The amount distributed to each return line item is relative to that item’s contribution to the
order subtotal.

### Structure

`OrderReturnTax`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uid` | `String` | Optional | Unique ID that identifies the return tax only within this order. |
| `source_tax_uid` | `String` | Optional | `uid` of the Tax from the Order which contains the original charge of this tax. |
| `catalog_object_id` | `String` | Optional | The catalog object id referencing [CatalogTax](#type-catalogtax). |
| `name` | `String` | Optional | The tax's name. |
| `type` | [`String (Order Line Item Tax Type)`](/doc/models/order-line-item-tax-type.md) | Optional | Indicates how the tax is applied to the associated line item or order. |
| `percentage` | `String` | Optional | The percentage of the tax, as a string representation of a decimal number.<br>For example, a value of `"7.25"` corresponds to a percentage of 7.25%. |
| `applied_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `scope` | [`String (Order Line Item Tax Scope)`](/doc/models/order-line-item-tax-scope.md) | Optional | Indicates whether this is a line item or order level tax. |

### Example (as JSON)

```json
{
  "uid": null,
  "source_tax_uid": null,
  "catalog_object_id": null,
  "name": null,
  "type": null,
  "percentage": null,
  "applied_money": null,
  "scope": null
}
```

