# Branded types

Tipos con marca para distinguir.

**Ejemplo de la vida real**: IDs únicos.

```typescript
type UserID = string & { __brand: "UserID" };
type ProductID = string & { __brand: "ProductID" };

function createUserID(id: string): UserID {
    return id as UserID;
}

let userId = createUserID("123");
let productId: ProductID = "456" as ProductID; // Diferente tipo
```

**Notas importantes**: Previene mezclar tipos similares.