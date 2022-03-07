---
title: " Definování bodů věrnostních odměn"
description: Tato procedura vás provede definováním bodů věrnostních odměn.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 509db13f1bae9f41537a5d91aeba862ed2e4291d72739e83e22fb860791d6355
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738665"
---
# <a name="define-loyalty-reward-points"></a> Definování bodů věrnostních odměn

[!include [banner](../includes/banner.md)]

Tato procedura vás provede definováním bodů věrnostních odměn. Body věrnostní odměny byste měli nastavit ještě před nastavením věrnostního programu. Tato procedura používá data ukázkové společnosti USRT.

1. Přejděte do nabídky Retail and Commerce > Odběratelé > Věrnost > Body věrnostní odměny.
2. Klikněte na možnost Nový.
3. Zadejte hodnotu do pole ID bodu odměny.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte možnost v poli Typ bodu odměny.
    * Vyberte Množství, pokud chcete věrnostní body zaokrouhlit na nejbližší celé číslo. Pokud chcete, aby body odměny byly zaokrouhlování podle pravidel zaokrouhlení měny, vyberte Množství. Vyberete-li možnost Množství, přeskočte další krok této procedury.  
6. Zadejte hodnotu do pole Měna.
    * Pro typ částky bodů odměny budou mít všechny udělené body vybranou měnu. Pro body odměny pro typ množství toto pole nelze použít – vynechejte tento krok.  
7. Zaškrtněte nebo zrušte zaškrtnutí políčka Lze uplatnit.
8. Zadejte číslo do pole Uplatnit hodnocení.
    * Uplatnit hodnocení se používá, když dvě nebo více uplatnitelných bodových odměn je možné použít pro zaplacení produktů. Pokud dva body odměny mají stejné hodnocení pro uplatnění, pak se použije ten, který vyžaduje snížení počtu bodů.  
9. Zadejte číslo do pole Hodnota času konce platnosti.
    * Body odměny vyprší za zadaný počet dní, měsíců nebo roků po jejich vydání. Hodnota „0“ znamená, že body věrnostní odměny nikdy nevyprší.  
10. Vyberte možnost v poli Jednotka času konce platnosti.
11. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]