--- 
title: "Zadávání prodejních smluv"
description: "Tato procedura popisuje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 099447252fe8fae5d44cf6cba87e8fbe0fd924e0
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="enter-sales-agreements"></a>Zadávání prodejních smluv

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za

smluvenou částku během času výměnou za zvláštní slevy. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-sales-agreement-header"></a>Nastavení záhlaví prodejní smlouvy
1. Přejděte na Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy.
2. Klikněte na položku Nová.
3. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli Klasifikace prodejní smlouvy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Rozbalte sekci Obecné.
9. V poli Výchozí závazek vyberte možnost „Závazek – hodnota produktu“.
    * Typ závazku je povinné kritérium, které je nutné přiřadit ke smlouvě k definování způsobu plnění smlouvy. Čtyři přednastavené typy umožňují nastavit cíl závazku odběratele vyjádřený jako množství nebo hodnota. Typ závazku množství lze použít pouze k určitému produktu, ale oba typy hodnot se vztahují na prodej určeného a neurčeného zboží.  
10. Do pole Datum vypršení platnosti nastavte datum na budoucí datum, kdy má vypršet platnost smlouvy.
11. Klikněte na tlačítko OK.

## <a name="set-up-product-value-commitment-lines"></a>Nastavení řádku závazku pro hodnotu produktu
1. Klikněte na položku Přidat řádek.
2. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
    * Typ závazku, který jste vybrali pro smlouvu, ovlivňuje druh informací, které lze zadat na řádky smlouvy. Například u smlouvy založené na hodnotě je třeba určit celkovou čistou částku (v dohodnuté měně) za kterou se odběratel zavazuje koupit zboží od vás. V tomto příkladu nejsou pole Množství a Jednotky na řádku k dispozici vzhledem k tomu, že vytvoříte smlouvu pro zákazníka ke koupi produktu s konkrétní hodnotou.   
5. Do pole Částka čisté zadejte peněžní částku, za kterou se zákazník zavázal nakoupit.
6. Do pole Procento slevy zadejte procentuální hodnotu, která bude použita pro řádky prodejní objednávky odběratele, které jsou propojeny s touto smlouvou.
7. Rozbalte sekci Podrobnosti řádku.
8. Vyberte možnost Ano v poli Max je vynuceno.
    * Výběr možnosti Max je vynuceno znamená, že celková částka všech řádků prodejní objednávky používající zvláštní ceny závazku, slevy nebo platební podmínky, nesmí překročit částku zadanou v závazku.  
    * Minimální a maximální částky určují rozsah hodnot, za které musí být realizován prodej u jednotlivých prodejních objednávek používajících vybranou smlouvu.   
9. Rozbalte část Záhlaví prodejní smlouvy.
    * Pokud je stav smlouvy nastaven na Platné, prodejní objednávky nesmí být přidruženy ke smlouvě a proto nemohou přispívat k plnění dohody. V této fázi lze stav změnit ručně. Stav by však normálně byl změněn při potvrzení smlouvy pro odběratele.  
10. V podokně akcí klepněte na možnost Prodejní smlouva.
11. Klikněte na možnost Potvrzení.
    * Ověřte, že možnost Označit smlouvu jako platnou je nastavena na hodnotu Ano.  
12. Vyberte možnost Ano v poli Tisk sestavy.
13. Klikněte na tlačítko OK.
14. Zavřete stránku.
    * Smlouva je nyní platná a můžete zahájit propojení smlouvy s nákupními objednávkami odběratele protiúčtem vůči potvrzenému cíli.  


