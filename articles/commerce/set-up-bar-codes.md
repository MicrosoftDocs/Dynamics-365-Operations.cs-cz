---
title: Nastavení čárových kódů
description: Tento článek popisuje, jak lze používat čárové kódy v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.industry: Retail
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
ms.openlocfilehash: 5771ada4a9bba92fb32155ae425f08d6429b46e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271789"
---
# <a name="set-up-bar-codes"></a>Nastavení čárových kódů

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak lze používat čárové kódy v aplikaci Dynamics 365 Commerce.

Čárové kódy slouží pro nákup a prodej produktů, sledování variant produktů a nastavení zákazníků a zaměstnanců. Čárové kódy slouží také pro vydávání a schvalování kupónů, dárkových poukazů a dobropisů. K produktům lze nastavit standardní čárové kódy nebo vlastní, podnikové čárové kódy. Produkty mohou mít více čárových kódů. Například produkt může mít více čárových kódů, pokud pochází od různých výrobců, nebo pokud má varianty, které jsou založeny na velikosti, stylu či barvě. Čárové kódy mohou obsahovat hmotnost nebo cenu produktu. Masky čárových kódů jsou šablony, které slouží k vytvoření čárových kódů.

> [!NOTE]
> Přiřadíte-li každé kombinaci variant jedinečný čárový kód, program po skenování čárového kódu na registrační pokladně vyhledá variantu produktu, která je prodávána. Díky tomu lze také shromažďovat a zobrazovat statistické údaje o prodeji podle variant. Každé skupině velikostí, barev a stylů lze přiřadit jedinečné číslo, které v čárovém kódu identifikuje skupinu. Commerce pomocí masky čárového kódu automaticky generuje čárové kódy pro každou kombinaci variant. To může být užitečné v případě, že je k dispozici mnoho velikostí, barev a stylů, protože počet kombinací s každým přidaným kódem varianty značně vzrůstá. Pokud tato funkce není použita, musí být čárové kódy ručně přiděleny ke každé kombinaci představující variantu produktu.

Čárové kódy lze vytvářet ručně nebo automaticky. Pokud chcete vytvořit čárové kódy, proveďte následující úlohy v pořadí, ve kterém jsou uvedeny.

1. [Nastavení znaků masky čárového kódu](set-up-bar-code-masks.md).
2. [Nastavení masek čárových kódů](set-up-bar-code-masks.md).
3. Konfigurace nastavení čárových kódů.
4. [Vytváření čárových kódů pro produkty](../supply-chain/pim/tasks/create-bar-code-product.md)

## <a name="additional-resources"></a>Další zdroje

[Nastavení masek čárových kódů](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
