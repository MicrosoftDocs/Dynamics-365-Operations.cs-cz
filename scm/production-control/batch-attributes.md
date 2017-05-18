---
title: "Atributy dávky"
description: "V tomto článku jsou informace o atributech dávky. Atributy dávky umožňují charakterizovat suroviny a hotové výrobky, které vytvářejí skladové dávky. Tento článek rovněž vysvětluje postup přiřazení atributů dávky a způsob, jakým je můžete vyhledat při rezervaci dávek."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8225460ccb311c79db45d618e8b02233e7bab51c
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="batch-attributes"></a>Atributy dávky

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace o atributech dávky. Atributy dávky umožňují charakterizovat suroviny a hotové výrobky, které vytvářejí skladové dávky. Tento článek rovněž vysvětluje postup přiřazení atributů dávky a způsob, jakým je můžete vyhledat při rezervaci dávek.

Atributy dávky umožňují charakterizovat suroviny a hotové výrobky, které vytvářejí skladové dávky. Atributy dávky se mohou lišit v závislosti na celé řadě faktorů (například na podmínkách prostředí, na kvalitě surovin použitých při výrobě dávky nebo na výsledku dokončených produktů). Počet a typy použitých atributů dávky se mohou výrazně lišit také mezi různými odvětvími. Zde jsou dva příklady použití atributů dávky:

-   V mlékárenském průmyslu může mít mléko jako surovina pro výrobu sýra například atributy udávající obsah tuku a hmotnostní procento. Sýr vyrobený z mléka může mít další atributy, například podíl sušiny a stáří.
-   V ocelářském průmyslu může mít vyráběná ocel například atributy udávající procentuální obsah hořčíku, stříbra a zinku.

Pro zjednodušení správy počtu a typů atributů můžete použít skupiny atributů dávky. Tímto způsobem nemusíte přidávat jednotlivé atributy zvlášť.

## <a name="assign-batch-attributes"></a>Přiřazení atributů dávky
Atributy dávky se přiřazují k jednotlivým produktům, které jsou zahrnuty do skladových dávek nebo jsou přiřazeny k produktům, které jsou asociovány s konkrétními odběrateli. Před přiřazením atributu dávky na úrovni odběratelů je nutné přiřadit je na úrovni produktu. Výrobek musí mít dimenze dávky nastavené na **Aktivní** ve skupině sledování dimenze. Pokud chcete přiřadit atribut dávky k jednotlivým produktům, použijte stránku specifickou pro produkt. Je-li atribut specifický pro produkt odběratele, použijte stránku specifickou pro odběratele. Po přidání atributu k produktu se také definují další parametry. Několik příkladů:

-   Minimální a maximální rozsah pro atribut typu **Celé číslo** nebo **Zlomek**.
-   Akce tolerance pro atribut typu **Celé číslo** nebo **Zlomek**. Pokud hodnota atributu spadá mimo rozsah minima a maxima, akce může být upozornění nebo chybová zpráva.
-   Cílová hodnota základního atributu. Tato hodnota je optimální hodnota atributu a platí pro všechny typy atributů.

Lze otevřít stránky pro produkty, které vyberete na stránce **Uvolněné produkty** v modulu Řízení informací o produktu. Po přiřazení atributů dávky k produktu můžete přiřadit specifické hodnoty k atributům na stránce **Atributy skladové dávky**.

## <a name="reserve-batches"></a>Rezervace dávek
Atribut dávky můžete vyhledat, pokud rezervujete dávku pro prodejní objednávku s cílem naplnit objednávku odběratele, nebo vydáváte dávky pro výrobní zakázku. Hledání pomáhá vyhledat skladovou dávku, která obsahuje produkt, který má požadovaný atribut dávky. Po nalezení jedné nebo více dávek je možné rezervovat produkt pro původní řádek skladové transakce.




