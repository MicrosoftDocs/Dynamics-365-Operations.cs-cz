---
title: Entity dat projektu
description: Toto téma obsahuje informace o různých entitách, které lze použít k importu a exportu dat produktu.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 340cb33537c7ba07555e1f0b6437fa4a3458a11a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208609"
---
# <a name="product-data-entities"></a>Entity dat projektu

[!include [banner](../includes/banner.md)]

K importu a exportu dat produktu musíte použít datové entity. Následující tabulka obsahuje podrobné informace o datových entitách týkajících se produktů a popisuje jejich účel.

| Celek | Název (typ) stromu aplikačních objektů (AOT) | Poznámky |
|--------|-------------------------------------------|-------|
| Produkty V2 | EcoResProductV2Entity | Tato entita slouží k importu a exportu sdílených produktů – jedinečných produktů a základních produktů. Umožňuje aktualizace. Nepodporuje operace SQL založené na sadě. Je povolen pro protokol OData (Open Data Protocol). |
| Uvolněné produkty V2 | EcoResReleasedProductV2Entity | Tato entita slouží k importu a exportu vydaných produktů – jedinečných produktů a základních produktů. Umožňuje aktualizace. Vyžaduje, aby byl sdílený produkt již vytvořen. Při importu nového produktu dojde k vydání tohoto sdíleného produktu. Existují také samostatné entity, které lze použít k importu a exportu vydaných základních produktů a vydaných jedinečných variant. Tato entita nepodporuje operace SQL založené na sadě nebo operacích odstranění. Je povolena pro OData. |
| Tvorba uvolněného produktu V2 | EcoResReleasedProductCreationV2Entity | Tato entita slouží k importu sdílených produktů a vydaných produktů v jediném kroku. Přestože podporuje export, toto použití se nedoporučuje, protože účelem této entity je vytvoření produktu. Nepodporuje aktualizace. Podporuje omezenou sadu polí (pole, která jsou k dispozici v dialogovém okně pro vytvoření produktu). Nepodporuje operace SQL založené na sadě. Není vystavena přes OData. |
| Varianty produktu | EcoResProductVariantEntity | Tato entita slouží k importu a exportu variant sdílených produktů. Umožňuje aktualizace. Vyžaduje, aby byly hodnoty dimenzí již vytvořeny. Integrační klíč je základní produkt plus dimenze produktu. Tato entita nepodporuje operace SQL založené na sadě. Je povolena pro OData. Podporuje operace odstranění. Nelze ji rozšířit přidáním nových dimenzí produktu. |
| Varianty produktu podle identifikace čísla produktu | EcoResProductNumberIdentifiedProductVariantEntity | Tato entita slouží k importu a exportu variant sdílených produktů. Umožňuje aktualizace. Vyžaduje, aby byly hodnoty dimenzí již vytvořeny. Integrační klíč je číslo produktu (zatímco integrační klíč pro entitu **vVarianty produktu** je základní produkt a dimenze produktu. |
| Uvolněné varianty produktu | EcoResReleasedProductVariantEntity | Tato entita slouží k importu a exportu variant vydaných produktů. Umožňuje aktualizace. Vyžaduje, aby byly varianty sdíleného produktu již vytvořeny. Při importu nové varianty produktu dojde k vydání varianty sdíleného produktu. Tato entita nepodporuje operace SQL založené na sadě. Je povolena pro OData. Přestože podporuje operace odstranění, toto použití v současné době způsobuje poškození dat z důvodu chyby na aktuální platformě. Tuto entitu nelze rozšířit přidáním nových dimenzí produktu. |
| Uvolněné varianty produktu podle identifikace čísla produktu | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Tato entita připomíná entitu **Varianty vydaného produktu**, ale integračním klíčem je číslo produktu místo základního produktu plus dimenze produktu. Lze ji rozšířit přidáním nových dimenzí produktu. |
| Prodejné uvolněné produkty | EcoResSellableReleasedProductEntity | Tato entita slouží k exportu pouze prodejných produktů. Prodejné produkty jsou produkty, které mají informace potřebné k tomu, aby mohly být použity v prodejní objednávce. Stejná pravidla platí, když je produkt ověřen pomocí funkce **Ověřit** na stránce **Vydané produkty**. |
| Vydané jedinečné produkty V2 | EcoResDistinctProductV2Entity | Tato entita slouží k exportu pouze jedinečných produktů. Tyto jedinečné produkty mohou být produkty, produkty podtypu a varianty produktu. |
| Vydané základní produkty V2 | EcoResProductMasterV2Entity | Tato entita slouží k importu a exportu základních produktů. Není povolena pro správu dat. |
| Položka – čárový kód | EcoResProductBarcodeEntity | Tato entita slouží k exportu produktů a čárových kódů. |
| Stavy životního cyklu produktu | EcoResProductLifecycleSateEntity | Tato entita slouží k importu a exportu různých stavů časově omezené podpory produktů, které lze přiřadit k produktu. |

> [!NOTE]
> Datovou entitu **Vydané produkty V2** můžete použít k importu produktů do systému pouze v případě, že byl sdílený produkt již vytvořen. V opačném případě musíte pro import produktů do systému použít datovou entitu **Vytvoření produktu**.
