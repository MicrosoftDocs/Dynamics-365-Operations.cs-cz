---
title: Nastavení čárových kódů
description: Tento článek popisuje, jak lze používat čárové kódy v aplikaci Dynamics 365 Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b7a668f8b44c5f573957a91ab19a8b7fac7a95ba
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024883"
---
# <a name="set-up-bar-codes"></a>Nastavení čárových kódů

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak lze používat čárové kódy v aplikaci Dynamics 365 Retail.

Čárové kódy slouží pro nákup a prodej produktů, sledování variant produktů a nastavení zákazníků a zaměstnanců. Čárové kódy slouží také pro vydávání a schvalování kupónů, dárkových poukazů a dobropisů. k maloobchodním produktům lze nastavit standardní čárové kódy nebo vlastní, podnikové čárové kódy. Produkty mohou mít více čárových kódů. Například produkt může mít více čárových kódů, pokud pochází od různých výrobců, nebo pokud má varianty, které jsou založeny na velikosti, stylu či barvě. Čárové kódy mohou obsahovat hmotnost nebo cenu produktu. Masky čárových kódů jsou šablony, které slouží k vytvoření čárových kódů.

> [!NOTE]
> Přiřadíte-li každé kombinaci variant jedinečný čárový kód, program po skenování čárového kódu na registrační pokladně vyhledá variantu produktu, která je prodávána. Díky tomu lze také shromažďovat a zobrazovat statistické údaje o prodeji podle variant. Každé skupině velikostí, barev a stylů lze přiřadit jedinečné číslo, které v čárovém kódu identifikuje skupinu. Retail pomocí masky čárového kódu automaticky generuje čárové kódy pro každou kombinaci variant. To může být užitečné v případě, že je k dispozici mnoho velikostí, barev a stylů, protože počet kombinací s každým přidaným kódem varianty značně vzrůstá. Pokud tato funkce není použita, musí být čárové kódy ručně přiděleny ke každé kombinaci představující variantu produktu.

Čárové kódy lze vytvářet ručně nebo automaticky. Pokud chcete vytvořit čárové kódy, proveďte následující úlohy v pořadí, ve kterém jsou uvedeny.

1. [Nastavení znaků masky čárového kódu](set-up-bar-code-masks.md).
2. [Nastavení masek čárových kódů](set-up-bar-code-masks.md).
3. Konfigurace nastavení čárových kódů.
4. Vytváření čárových kódů pro produkty.

## <a name="additional-resources"></a>Další zdroje

[Nastavení masek čárových kódů](set-up-bar-code-masks.md)
