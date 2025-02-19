---
title: Unpointed maps between pointed types
---

```agda
module structured-types.unpointed-maps where

open import foundation.dependent-pair-types
open import foundation.universe-levels

open import structured-types.pointed-types
```

## Idea

The type of unpointed maps between pointed types is a pointed type, pointed at the constant function.

## Definition

```agda
unpointed-map-Pointed-Type :
  {l1 l2 : Level} → Pointed-Type l1 → Pointed-Type l2 → Pointed-Type (l1 ⊔ l2)
pr1 (unpointed-map-Pointed-Type A B) = type-Pointed-Type A → type-Pointed-Type B
pr2 (unpointed-map-Pointed-Type A B) x = pt-Pointed-Type B
```
