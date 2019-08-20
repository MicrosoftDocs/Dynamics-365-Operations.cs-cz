---
title: EUR-00011 Vygenerování sestavy Souhrnné hlášení (EU)
description: Tento postup vás provede generováním sestavy souhrnného hlášení EU.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a9a1aeeec4ea22f1153e32254f64c6b7f365a8c
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848854"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a>EUR-00011 Vygenerování sestavy Souhrnné hlášení (EU)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede generováním sestavy souhrnného hlášení EU. To zahrnuje převod interních obchodních transakcí do souhrnného hlášení EU a spuštění sestavy. Tento postup také zahrnuje vytváření interních obchodních transakcí pro účely ukázky. Další informace o výkazu se seznamem prodeje v EU včetně případných požadovaných předpokladů naleznete v nápovědě Dynamics 365 for Finance and Operations.

Postup se vztahuje na všechny evropské země/oblasti. Postup byl vytvořen použitím ukázkových dat společnosti DEMF a následně Německa jako příklad pro domácí zemi nebo oblast. Postup také využívá Portugalsko jako příklad země nebo oblasti EU. Před dokončením tohoto postupu, je nutné konfigurovat vytváření souhrnného hlášení EU.

Tento postup je určen pouze pro účetní.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Vytvoření interních prodejních transakcí pro účely ukázky
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte „PRT-001“.
4. Klikněte na tlačítko OK.
5. Do pole Číslo položky zadejte D0001.
6. Rozbalte sekci Podrobnosti řádku.
7. Klepněte na kartu Nastavení.
8. V poli Skupina DPH zboží zadejte „FULL“.
9. Klikněte na Přidat řádek.
10. Do pole Číslo položky zadejte D0003.
11. V poli Skupina DPH zboží zadejte „RED“.
12. Klikněte na položku Uložit.
13. V podokně akcí klikněte na položku Faktura.
14. Klikněte na položku Faktura.
15. Rozbalte sekci Parametry.
16. V poli Množství vyberte možnost Vše.
17. Rozbalte sekci Nastavení.
18. V poli Datum faktury nastavte datum a čas na „01/11/2016“ .
19. Klikněte na tlačítko OK.
20. Klikněte na tlačítko OK.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Převod interní obchodních transakcí do souhrnného hlášení pro EU
1. Přejděte na Daně > Deklarace > Zahraniční obchod > Souhrnné hlášení EU.
2. Klepněte na položku Převod.
3. K převodu transakcí zboží vyberte v poli Zboží možnost Ano.
4. K převodu servisních transakcí vyberte v poli Servis možnost Ano.
    * Můžete také nastavit další filtry interní obchodních transakcí k převodu.  
5. Klepněte na položku Převod.
    * Ověřte, zda byly interní transakce prodeje úspěšně přeneseny do souhrnného hlášení EU.  

## <a name="generate-the-eu-sales-list-report"></a>Generování sestavy souhrnného hlášení EU
1. Klepněte na Sestavování.
2. V poli Období vykazování vyberte „Měsíční“.
3. V poli Datum od nastavte datum a čas na „01/01/2016“ .
4. Vyberte možnost Ano v poli Generovat soubor.
5. Vyberte možnost Ano v poli Generovat sestavu.
6. V poli Název souboru zadejte „EUSalesList“.
7. V poli Název souboru sestavy zadejte „EUSalesList“.
8. Do pole ID registrace souhrnného hlášení EU zadejte „123“.
    * Toto pole je k dispozici jen pro Německo.  
    * Můžete také nastavit další filtry interní obchodních transakcí k převodu pro zahrnutí v sestavě.  
9. Klikněte na tlačítko OK.
    * Ověřte, že se zobrazí místní podokno pro potvrzení, že soubor a kontrolní sestava jsou stahovány.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>Označit řádky souhrnného hlášení EU jako Ohlášeno
1. Klepněte na položku Označit.
2. Klepněte na Označit jako ohlášené.
3. V seznamu vyberte řádek pro pole Datum fakturace.
4. Zadejte hodnotu „01/01/2016…01/31/2016“ do pole Kritéria.
5. V seznamu vyberte řádek pro pole Stav vykazování.
6. Vyberte volbu „Zahrnuto“ v poli Kritérium.
    * Můžete také nastavit další filtry interní obchodních transakcí k převodu pro označení jako Hlášeno.  
7. Klikněte na tlačítko OK.
8. Vyberte volbu „Hlášeno“ v poli Výběr.

## <a name="mark-eu-sales-list-lines-as-closed"></a>Označit řádky souhrnného hlášení EU jako Uzavřeno
1. Klepněte na položku Označit.
2. Klepněte na Označit jako uzavřené.
3. V seznamu označte řádek pro pole Datum fakturace.
4. Zadejte hodnotu „01/01/2016…01/31/2016“ do pole Kritéria.
5. V seznamu označte řádek pro pole Stav vykazování.
6. Vyberte volbu „Hlášeno“ v poli Kritérium.
    * Můžete také nastavit další filtry interní obchodních transakcí k převodu pro označení jako Uzavřeno.  
7. Klikněte na tlačítko OK.
8. Vyberte volbu „Uzavřeno“ v poli Výběr.

