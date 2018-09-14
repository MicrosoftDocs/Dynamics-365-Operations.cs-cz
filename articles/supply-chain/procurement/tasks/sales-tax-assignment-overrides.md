--- 
title: "Přiřazení a přepsání DPH"
description: "Tento postup ukazuje, jak přiřadit skupiny DPH k maloobchodním kanálům."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 816e00e4238cb0d90a2aea9b2bc070d31504c2ce
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a>Přiřazení a přepsání DPH

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak přiřadit skupiny DPH k maloobchodním kanálům. Provede vás také procesem vytvoření nového přepsání DPH a jeho přiřazení k existující skupině přepsání DPH. Tento postup

používá v ukázkových datech společnost USRT.

1. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.
2. V seznamu klepněte na odkaz ID maloobchodní sítě – "Houston".
3. Klikněte na položku Upravit.
    * Pole „Skupina DPH“ obsahuje seznam skupin DPH pro aktuální společnost. Aktuálně přiřazená skupina je obecnou skupinou DPH pro „Texas“. Existují také skupiny DPH pro "Washington" a "Washington, King County." Skupiny DPH mohou zahrnovat platné daně pro více obcí.  
    * Pole „Přepsání DPH“ je místo, kde lze mapovat skupiny přepisujících DPH k obchodnímu kanálu. Skupiny přepisujících DPH lze použít pro seskupení přepisujících DPH platných pro více obchodů. Namísto ručního postupného přiřazování přepisujících DPH jednoho po druhém je možné kvůli úspoře času vytvořit skupinu a přiřadit ji přímo k obchodním kanálům.  
4. Klikněte na položku Uložit.
5. Zavřete stránku.
6. Přejděte na Maloobchodní a velkoobchodní prodej > Nastavení kanálu > DPH > Přepsání DPH.
7. Klikněte na položku Nová.
8. Do pole Přepsání DPH zadejte název nového přepsání.
9. Do pole Popis zadejte popis přepsání.
10. Nastavte stav na "Povolit".
11. Rozbalte nebo sbalte oddíl Přepsání.
12. Vyberte volbu v poli Typ.
    * Skupiny DPH zboží lze použít k přepsání daně pro konkrétní zboží, které patří do dané skupiny. Například potraviny jsou obvykle daněny odlišně od pevného zboží a pravděpodobně vyžadují vlastní skupinu DPH.     Skupiny DPH jsou skupiny daní, které se vztahují k daném obchodnímu kanálu. Pokud například obchodní kanál prodává v maloobchodní i podnikatelské oblasti, je možné použít odlišné skupiny DPH zboží. Všechny platné daně by byly mapovány ke skupině prodejní daně.  
    * Nově můžete vybrat daně "Od" a "Do" nebo "Z daňové skupiny" a "Do daňové skupiny" a vytvořit tak přepisující DPH.    Pole "Od" označuje daně nebo daňovou skupinu, která bude přepsána. Přepsání podle skupiny DPH zboží nabízí jiné možnosti, než přepsání podle skupiny DPH.    Přepsání DPH můžete nastavit a přepsat daně v celé transakci nebo na konkrétních řádcích v transakci.  
13. Klikněte na položku Uložit.
14. Zavřete stránku.
15. Přejděte na Maloobchodní a velkoobchodní prodej > Nastavení kanálu > DPH > Skupiny přepsání DPH.
    * V tomto kroku přiřadíte nově vytvořené přepisující DPH ke skupině přepisujících DPH přiřazených k obchodnímu kanálu Houston.  
16. Klikněte na položku Upravit.
17. Rozbalte nebo sbalte oddíl Nastavení.
18. Klepněte na možnost Přidat.
19. V poli Přepsání DPH kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
20. Vyberte ze seznamu dříve vytvořené přepsání DPH.
21. Klikněte na odkaz na vybraném řádku v seznamu.
22. Klikněte na položku Uložit.


