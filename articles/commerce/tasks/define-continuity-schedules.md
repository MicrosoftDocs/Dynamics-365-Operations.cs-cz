---
title: " Definování plánů trvání"
description: Toto téma vás provede nastavením programu trvání (označovaném také jako opakované objednávky).
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8414377ddec0e001f003f842866725eb58bd75a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791600"
---
# <a name="define-continuity-schedules"></a> Definování plánů trvání

[!include [banner](../includes/banner.md)]

Toto téma vás provede nastavením programu trvání (označovaném také jako opakované objednávky). Toto téma používá v ukázkových datech společnost USRT.


## <a name="create-continuity-program"></a>Vytvoření programu trvání
1. Přejděte na Retail and Commerce > Trvání > Programy trvání.
2. Klikněte na možnost Nový.
3. V poli ID plánu zadejte ID plánu trvání
4. V poli zahájení objednávky vyberte "První událost".
    * Jestliže odběratel zadá novou objednávku pro program kontinuity, existují dvě možnosti, pro které bude výrobek expedován: 1. První událost: první produkt v programu kontinuity bude expedován.  2. Aktuální událost: bude expedován aktuální produkt. Například tři měsíce do programu, zákazník obdrží třetí produkt v programu.  
5. Vyberte možnost "Ano" u výzvy k zadání počátečního data objednávky.
6. Klikněte na položku Přidat řádek.
7. V poli Číslo zboží zadejte číslo zboží pro první produkt (0013).
8. Napište "CP".
9. Zadejte datum, kdy bude možné první produkt objednat.
10. Klikněte na Přidat řádek.
11. Do pole Číslo zboží zadejte „0014“.
12. V poli kód intervalu data vymažte hodnotu, aby bylo prázdné.
    * Vymažte pro tuto proceduru datový interval. Datum bude postupně narůstat od počátečního data první položky.  
13. Sem zadáte interval, ve kterém budou dodávány produkty. Napište 30.
    * Pro měsíční program zadejte interval 30 dnů.  
14. Klikněte na položku Přidat řádek.
15. Do pole Číslo zboží zadejte „0015“.
16. Napište 'Konec'.
17. Klikněte na položku Uložit.

## <a name="assign-to-continuity-item"></a>Přiřazení k trvalému zboží
1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. Vyberte zboží '0016'.
    * Pro tuto proceduru vyberte číslo položky 0016. Za normálních okolností budete mít vytvořený uvolněný produkt, který má aplikovanou další trvalou obchodní logiku při umístění do prodejní objednávky v kontaktním středisku.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na položku Upravit.
5. Rozbalte nebo sbalte oddíl Prodej.
6. Sem zadejte program trvání, který tato položka představuje. Zadejte kód plánu, který jste vytvořili dříve.
    * Když je prostřednictvím kontaktního střediska prodáno zboží, z vybraného programu trvání se aplikuje další obchodní logika.  
7. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]