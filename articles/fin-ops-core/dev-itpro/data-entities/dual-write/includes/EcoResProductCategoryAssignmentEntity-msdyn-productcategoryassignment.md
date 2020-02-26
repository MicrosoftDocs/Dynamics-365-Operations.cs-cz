## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Přiřazení kategorií produktů do msdyn_productcategoryassignments

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
