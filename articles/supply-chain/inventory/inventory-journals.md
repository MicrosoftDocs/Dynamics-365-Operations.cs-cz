---
title: "Skladové deníky"
description: "Tento článek popisuje, jak můžete použít deníky zásob k zaúčtování různých typů transakcí fyzických zásob."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 968bf9a243d0c0cc9f0dfec474cb207ca32f9eeb
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-journals"></a>Skladové deníky

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tento článek popisuje, jak můžete použít deníky zásob k zaúčtování různých typů transakcí fyzických zásob.

Deníky zásob v aplikaci Microsoft Dynamics 365 for Finance and Operations se používají ke zpracovávání různých typů transakcí fyzických zásob, například k zaúčtování výdejů a příjmů, pohybu zásob, vytváření kusovníků a odsouhlasení fyzických zásob. Všechny tyto deníky zásob se používají podobným způsobem, avšak rozděleny jsou do různých typů.

## <a name="types-of-inventory-journals"></a>Typy deníků zásob
K dispozici jsou následující typy deníků zásob:

-   Pohyb
-   Úprava zásob
-   Převést
-   Kusovník
-   Doručení položky
-   Výrobní vstup
-   Inventura
-   Inventura podle štítků

### <a name="movement"></a>Pohyb

Při použití deníku pohybů zásob můžete při přidání zásob přidat náklady k položce, ale další náklady je nutné na konkrétní účet hlavní knihy přidělit ručně určením protiúčtu hlavní knihy při vytvoření deníku. Tento typ deníku zásob je užitečný, když chcete položku vydat podle různých oddělení nebo pokud chcete odebrat položky ze skladu pro účely výdajů.

### <a name="inventory-adjustment"></a>Úprava zásob

Když použijete deník úpravy zásob, můžete náklady přidat k položce při přidání zásob. Další náklady jsou automaticky zaúčtovány na specifický účet hlavní knihy na základě nastavení účetního profilu skupiny položek. Tento typ deníku zásob použijte k aktualizaci zisků a ztrát na množství zásob, když si položka má uchovat svůj výchozí protiúčet hlavní knihy. Když zaúčtujete deník úpravy zásob, je zaúčtován příjem nebo výdej zásob, změní se hodnota zásob a vytvoří se transakce hlavní knihy.

### <a name="transfer"></a>Převést

Deníky převodů slouží k převodu položek mezi skladovými umístěními, dávkami nebo variantami produktu, aniž by byly přidruženy dopady na náklady. Například lze převést položky z jednoho skladu do jiného skladu v rámci téže společnosti. Při použití deníku převodů je nutné zadat obě dimenze zásob „z“ a „do“(například pracoviště a sklad). Množství na skladě pro definované dimenze zásob se příslušným způsobem změní. Převody zásob odpovídají okamžitému pohybu materiálu. Během tranzitu nejsou zásoby sledovány. Pokud potřebujete zásoby sledovat i během tranzitu, použijte namísto toho převodní příkaz. Pokud zaúčtujete deník převodů, vytvoří se transakce zásob pro každý řádek deníku:

-   Výdej ze skladu ve skladovém místě „z“
-   Příjem na sklad ve skladovém místě „do“

### <a name="bom"></a>Kusovník

Pokud vykážete kusovník jako dokončený, můžete vytvořit deník kusovníku. Prostřednictvím deníku kusovníku můžete kusovník přímo zaúčtovat. Toto zaúčtování vygeneruje příjem produktu na sklad společně s přidruženým kusovníkem a výdejem produktů zahrnutých v kusovníku ze skladu. Tento typ deníku zásob je užitečný u jednoduchých nebo velkoobjemových výrobních scénářů, u kterých nejsou potřeba postupy.

### <a name="item-arrival"></a>Doručení položky

Deník doručení položek slouží k evidenci příjmu položek (například z nákupní objednávky). Deník doručení položky může být vytvořen v rámci řízení doručení na stránce **Přehled doručení** nebo můžete položku deníku vytvořit ručně na stránce **Doručení položky**. Pokud umožníte, aby deník doručení položek kontroloval výdejní skladová místa, aplikace Finance and Operations vyhledá místo pro přijaté položky a (pokud je v něm prostor) vygeneruje cílová skladová místa pro příchozí položky.

### <a name="production-input"></a>Výrobní vstup

Deníky výrobních vstupů fungují jako deníky doručení položek, ale používají se pro výrobní zakázky.

### <a name="counting"></a>Inventura

Deníky inventur umožňují opravu aktuálních zásob na skladě, které jsou evidovány pro položky nebo skupiny položek, a následné zaúčtování skutečného fyzického počtu tak, aby bylo možné provést úpravy potřebné kvůli odsouhlasení rozdílů. Zásady inventury lze přidružit k inventurním skupinám pro usnadnění seskupení položek s různou charakteristikou tak, aby tyto položky mohly být zahrnuty do deníku inventur. Například můžete nastavením inventurních skupin provádět inventuru položek, které mají určité frekvence, nebo provádět inventuru položek, když zásoba klesne na danou úroveň. Více informací o definici inventurních skupin naleznete v tématu [Definování procesů inventur zásob (Průvodce záznamem úloh)](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Inventura podle štítků

Deníky inventur podle štítků slouží k přiřazení očíslovaného štítku k šarži. Štítek by měl obsahovat číslo štítku, číslo položky a množství položky. Aby bylo zajištěno, že se každý štítek použije jenom jednou a že se použijí všechny štítky, mělo by mít každé číslo položky jedinečnou sadu štítků s vlastní číselnou řadu. Pro každý štítek lze nastavit tři hodnoty stavu:

-   **Použito** – číslo položky bylo pro tento štítek použito.
-   **Anulováno** – číslo položky bylo pro tento štítek anulováno.
-   **Chybí** – číslo položky pro tento štítek chybí.

Po zaúčtování deníku inventur podle štítků je vytvořen nový deník inventur na základě řádků deníku inventur podle štítků. Další informace o inventuře podle štítků naleznete v tématu [Inventura zásob podle štítků](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Práce s deníky
Deník může používat vždy jen jeden uživatel. Pokud s deníky chce pracovat více uživatelů najednou a vytvářet v nich řádky, musí uživatel vybrat deníky, které nejsou právě používány, aby se předešlo jejich přepsání. V situacích, kdy více oddělení používá stejný typ deníku, je vhodné vytvořit několik deníků (například jeden pro každé oddělení). Je rovněž vhodné deníky rozdělit tak, aby byla každá rutina zaúčtování zadána do svého jedinečného deníku zásob. Chcete-li účtovat rutiny, které jsou přiřazeny ke skladovým transakcím, vytvořte jeden deník pro periodické úpravy zásob a druhý deník pro inventury zásob.

## <a name="posting-journal-lines"></a>Řádky účetních deníků
Vámi vytvořené řádky deníku můžete zaúčtovat kdykoli, dokud položku neuzamknete před dalšími transakcemi. Data, která zadáte do deníku, zůstanou v deníku, i když deník zavřete bez zaúčtování řádků.

