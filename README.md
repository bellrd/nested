# Nested

A go package to get deeply nested value from map[string]any

## Example
```json
{
  "key": {
      "nestedKey": [
        {
          "deeplyNestedKey": "value"
        }
      ]
  }
}

```
### Get(data map[string]any, keys ...string)
```go
value, err := nested.Get(data, "key", "nestedKey", "0", "deeplyNestedKey")
```
### Gets(data map[string]any, key string)
```go
value, err := nested.Gets(data, "key.nestedKey.0.deeplyNestedKey")
```
