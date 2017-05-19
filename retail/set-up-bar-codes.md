---
title: "Nastavení kódů dat"
description: "Tento článek popisuje způsob použití čárových kódů v aplikaci Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 5c4c15b5b225f64868675c02e065259b5310d188
ms.contentlocale: cs-cz
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-bar-codes"></a>Nastavení kódů dat

[!include[banner](includes/banner.md)]


Tento článek popisuje způsob použití čárových kódů v aplikaci Microsoft Dynamics 365 for Operations - Retail.

Čárové kódy slouží pro nákup a prodej produktů, sledování variant produktů a nastavení zákazníků a zaměstnanců. Čárové kódy slouží také pro vydávání a schvalování kupónů, dárkových poukazů a dobropisů. k maloobchodním produktům lze nastavit standardní čárové kódy nebo vlastní, podnikové čárové kódy. Produkty mohou mít více čárových kódů. Například produkt může mít více čárových kódů, pokud pochází od různých výrobců, nebo pokud má varianty, které jsou založeny na velikosti, stylu či barvě. Čárové kódy mohou obsahovat hmotnost nebo cenu produktu. Masky čárových kódů jsou šablony, které slouží k vytvoření čárových kódů. **Poznámka:** Přiřadíte-li každé kombinaci variant jedinečný čárový kód, program po skenování čárového kódu na registrační pokladně vyhledá variantu produktu, která je prodávána. Díky tomu lze také shromažďovat a zobrazovat statistické údaje o prodeji podle variant. Každé skupině velikostí, barev a stylů lze přiřadit jedinečné číslo, které v čárovém kódu identifikuje skupinu. Dynamics 365 for Operations používá masku čárového kódu k automatickému generování čárových kódů pro každou kombinaci variant. To může být užitečné v případě, že je k dispozici mnoho velikostí, barev a stylů, protože počet kombinací s každým přidaným kódem varianty značně vzrůstá. Pokud tato funkce není použita, musí být čárové kódy ručně přiděleny ke každé kombinaci představující variantu produktu. Čárové kódy lze vytvářet ručně nebo automaticky. Pokud chcete vytvořit čárové kódy, proveďte následující úlohy v pořadí, ve kterém jsou uvedeny.

1.  [Nastavení znaků masky čárového kódu](set-up-bar-code-masks.md).
2.  [Nastavení masek čárových kódů](set-up-bar-code-masks.md).
3.  Konfigurace nastavení čárových kódů.
4.  Vytváření čárových kódů pro produkty.


<a name="see-also"></a>Viz také
--------

[Nastavení masek čárových kódů](set-up-bar-code-masks.md)




