---
title: "Hybrid objednávky zákazníka"
description: "Objednávka zákazníka hybrid je jediné objednávky, která obsahuje produkty, které lze přenášet z úložiště zákazníkem, jakož i výrobky, které budou dodány později nebo vyzvednutí."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid objednávky zákazníka

[!include[banner](includes/banner.md)]


Objednávka zákazníka hybrid je jediné objednávky, která obsahuje produkty, které lze přenášet z úložiště zákazníkem, jakož i výrobky, které budou dodány později nebo vyzvednutí.

V 365 Microsoft Dynamics pro operace - maloobchod, můžete vybrat buď provést všechny produkty nebo provádět vybrané produkty pro objednávky zákazníka. Produkt, který řádky, které jsou označeny jako provádět automaticky fakturovaných po vytvoření objednávky, podobně to je stejné pro objednávky, které má být vydáno až po vytvoření objednávky. Splatná částka hybrid objednávky je stanovena přidáním procento zálohy na vyskladnění a řádky dodávky výrobku se provádí řádky v plné výši. Pro objednávky hybridní systém přepínat mezi režimem objednávky zákazníka a převzetím takto:

-   Pokud mají všechny produkty v košíku **provádět dodávky**, pořadí bude zpracováván jako transakce převzetím.
-   Pokud některé nebo všechny řádky v košíku jsou nastaven na hodnotu **vybrat** nebo **expedice dodávky**, pořadí bude zpracováván jako transakce objednávky zákazníka.

Pokud je vybrán řádek nákupního košíku a **zvolené vyskladnění**, **loď vybrána**, nebo **provádět vybrané** je zaškrtnuto, pouze konkrétní vozík řádek je nastavena s tuto metodu doručení. V takovém případě po proudu toku operace bude pokračovat obvyklým způsobem. Však-li **zvolené vyskladnění**, **loď vybrána**, nebo **provádět vybrané** je vybrán bez řádku nákupního košíku je vybrána, nový otevře stránku, která obsahuje seznam všech řádků nákupního košíku. Na této obrazovce můžete vybrat více řádků najednou k nastavení způsobu dodání. Při použití této metody pro výběr řádků, bude přepsána předchozí metody doručení, který byl přiřazen k řádku.

<a name="see-also"></a>Viz také
--------

[Přehled objednávek zákazníka](customer-orders-overview.md)




