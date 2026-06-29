---
id: Precategory
aliases: []
tags:
  - Note
  - Incomplete
---
202606181415

Tags : [[Category Theory]], [[Homotopy Type Theory]]

# Precategory

---

A *Precategory* is the more direct/ naive implementation of a category in HoTT. Here we assume that the collection of objects is a type, and the collection of morphisms is a set (we are assuming this as we want to implement 1-categories and not $\infty$ categories in general), here is the agda implementation:
```agda
record Precategory (o h : Level) : Type (lsuc (o ⊔ h)) where
  field
    Ob : Type o
    Hom : Ob → Ob → Type h
    Hom-set : (x y : Ob) → is-set (Hom x y)
    id : ∀ {x} → Hom x x
    _∘_ : ∀ {x y z} → Hom y z → Hom x y → Hom x z
    idr : ∀ {x y} (f : Hom x y) → f ∘ id ≡ f
    idl : ∀ {x y} (f : Hom x y) → id ∘ f ≡ f
    assoc : ∀ {w x y z} (h : Hom w x) (g : Hom x y) (f : Hom y z)
          → f ∘ (g ∘ h) ≡ (f ∘ g) ∘ h
```

here, we have the standard notion of an isomorphism, there exists an inverse.

---

# References

