---
title: "Okamžité doplnění"
description: "Toto téma popisuje, jak můžete použít okamžité doplnění k doplňování zásob při selhání směrnice skladového místa pro přidělení zásob."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a11a26df85647aa36cd30c42f81be4ec2af4409b
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="immediate-replenishment"></a>Okamžité doplnění

[!include [banner](../includes/banner.md)]

Okamžité doplnění umožňuje doplňování zásob ihned při selhání směrnice skladového místa pro přidělení zásob. Doplnění je založeno na jednom řádku v nastavení směrnice skladového místa. Pokud nejsou zásoby na skladě v jednotce měření, která je určena tímto řádkem, dojde okamžitě doplnění této měrné jednotky.

Okamžité doplnění představuje alternativu metody rozdělení zásob, kdy je rozdělení zásob založeno na více řádcích ve směrnici skladového místa a kde je poptávka sečtena na konci přidělení a doplněna v jednotce měření, která je určena poslední řádkou směrnice skladového místa.

Výhody používání okamžitého doplnění spočívají v tom, že doplnění mohou být omezena specifickou jednotkou množství lze směrovat do konkrétních míst.

## <a name="business-scenario"></a>Scénáře obchodu

Například máte sklad, který má zvláštní výdejové oblasti pro měrné jednotky pole a každá. Chcete optimalizovat proces výběru výběrem co největšího počtu polí a následným výdejem zbývajícího množství, které je menší než pole v oblasti "každé".

V takovém případě můžete použít okamžité doplnění. Ve směrnici skladového místa nastavíte okamžité doplnění pro pole, aby poptávka po doplnění byla použita co nejdříve, když dojde k úbytku polí, která lze vyskladnit pro požadované množství. Tímto způsobem můžete optimalizovat proces vyskladnění tak, aby obsahoval co největší počet polí. Okamžité doplnění vygeneruje doplnění polí a poptávka nebude předána, takže množství budou vyskladněna v měrné jednotce "každý". Jinak řečeno pouze množství, které má být vydáno v "každé" měrné jednotce (to znamená množství menší než pole) bude převzata z oblasti "každý". Jestliže nastane nedostatek v oblasti "pole", můžete vybrat libovolný počet polí z celkové poptávky. Zbývající množství poté bude převzato z oblasti "každý".

## <a name="where-it-applies"></a>Kdy se to používá

Okamžité doplnění se používá během provedení vlny, pokud se nezdaří přidělení pro řádek skladového místa, který má nastavenou šablonu doplnění.

## <a name="set-up-immediate-replenishment"></a>Nastavení okamžitého doplnění

- Přejděte na **řízení skladu** \> **nastavení** \> **směrnice skladového místa**a poté na kartu **řádky** v seznamu **šablona pro okamžité doplnění**, vyberte šablonu doplnění pro poptávku vlny.

Šablona doplnění je použita v případě, že se nepodařilo přidělit vyhrazenou měrnou jednotku řádku směrnice skladového místa.

## <a name="troubleshooting"></a>Řešení potíží

Je-li okamžité doplnění vybráno pro řádek směrnice skladového místa, ale žádné doplnění není generováno při použití šablony doplnění poptávky tohoto řádku směrnice skladového místa, musí být prozkoumány dvě hlavní příčiny:

- Ujistěte se, že je šablona doplnění poptávky, která je použita, je nastavena na použití správných šablon místa a pracovních šablon typu **doplnění**.
- Ujistěte se, že je dostatečné množství zásob na skladě ve skladových místech, kde šablona doplnění poptávky vyhledá zásoby na skladě pro doplnění.

