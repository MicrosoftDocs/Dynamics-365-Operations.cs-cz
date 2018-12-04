---
title: "Ganttův diagram pro plánování úloh"
description: "Plánovači výroby mohou kontrolovat a optimalizovat plány výroby pomocí Ganttova diagramu."
author: johanhoffmann
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3726038d9782891988e16cb98cf04cf47b7e66c
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="gantt-chart-for-job-scheduling"></a>Ganttův diagram pro plánování úloh

[!include [banner](../includes/banner.md)]

Ganttův diagram je navržen tak, aby plánovačům výroby umožňoval řídit a optimalizovat plán výroby. Ganttův diagram nastavuje transparentní tok operací a usnadňuje nastavení plánu výroby. Bere přitom v úvahu úbytky materiálu nebo zdrojů. To plánovačům umožní nejlépe využít dostupné zdroje, minimalizovat nedokončenou výrobu a optimalizovat propustnost u výrobních zakázek.

Ganttův diagram je vizuální znázornění naplánovaných aktivit v rámci definovaného časového intervalu. Aktivity jsou plánovány u zdrojů, které mají kapacitu definovanou v kalendáři kapacity. V Ganttově diagramu lze zobrazit následující typy aktivit.

-   Úlohy z výrobních zakázek, u nichž jsou naplánované úlohy.
-   Úlohy z plánovaných výrobních zakázek.
-   Naplánované aktivity projektu podle úlohy typu Hodinová prognóza.

Ganttův graf lze otevřít dvěma různými způsoby, **Zobrazení objednávky** a **Zobrazení zdrojů**[](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true). V **Zobrazení objednávky** jsou aktivity seskupeny pod výrobními zakázkami. To může být užitečné, například pokud chcete mít přehled o všech úlohách náležejících do stejné objednávky. V **Zobrazení zdrojů** jsou všechny úlohy seskupeny podle jednotlivých zdrojů. Toto zobrazení je vhodné při optimalizaci plánu na úrovni zdroje, například stroje nebo skupiny strojů. Ganttův diagram na následujícím obrázku ukazuje **zobrazení objednávky** a **zobrazení zdrojů** s těmito klíčovými prvky:

1.  Aktivita Ganttova diagramu
2.  Ikona nedostatku materiálu
3.  Ikona dostupnosti materiálu
4.  Ikona data dodání na objednávce
5.  Panel kapacity

## <a name="order-view"></a>Zobrazení objednávek

[![Zobrazení objednávek](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Zobrazení prostředků
[![Zobrazení prostředků](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Aktivity
Aktivity se zobrazují jako panely a jsou uspořádány v mřížce na časovém měřítku s plánovaným počátečním a koncovým časem, což nastavuje délku pruhů úměrnou době potřebné pro dokončení aktivity. Aktivity budou zobrazeny podle časového rozmezí. Časové rozmezí můžete upravit v nabídce, kde vyberete jednotku pro počáteční a koncové datum a čas, například hodiny nebo dny. Úpravou časového měřítka můžete nastavit fokus na časový interval, ve kterém chcete spravovat aktivity. 

Abyste měli lepší přehled, jsou k dispozici různé možnosti kontroly barvy aktivit. Můžete konfigurovat jednotlivé barvy pro aktivity, použít motiv barvy, který slouží jako všeobecný motiv barvy používané pro aplikaci nebo nastavit barvu, která bude kontrolována barevným kódem pro výrobní zakázky. 

Časový interval pro aktivity má odstín pozadí. Období označená bílým odstínem označují časový interval s určenou kapacitou prostředku aktivity, zatímco období označená šedým odstínem označují časové intervaly bez definované kapacity. 

Na levé straně grafu jsou další informace o aktivitě, například zdroje u, kterého je aktivita naplánována, a číslo výrobní objednávky. Propojení mezi úlohami náležejícími do stejné objednávky je označeno šipkou. 

V dialogovém okně aktivity získáte další informace o dané aktivitě. Otevřete dialogové okno poklikáním na aktivitu nebo výběrem nabídky **Informace**. V dialogovém okně aktivita se zobrazí naplánované počáteční a koncové datum a čas a informace o tom, jaké materiály se mají při aktivitě používat. 

Aktivity mohou být seskupeny na úrovních seskupení. Úrovně seskupení jsou hierarchické a lze je použít k logickému seskupení aktivit. Pokud například máte rozložení kde jsou výrobní aktivity seskupeny podle pracoviště, výrobních jednotek, skupin zdrojů a zdrojů, můžete pomocí úrovní seskupení seskupit aktivity podle tohoto rozložení. Úrovně seskupení lze rozbalit a sbalit na úrovni jednotlivých seskupení nebo pro všechny úrovně v grafu s použitím tlačítek **Rozbalit vše** a **Sbalit vše** v nabídce. Také můžete nakonfigurovat úrovně seskupení tak, aby bylo možné je rozbalit nebo sbalit při otevření grafu.

### <a name="material-availability"></a>Dostupnost materiálu

Ganttův graf je možné nastavit tak, aby plánovači poskytoval podrobné informace o stavu materiálu pro jednotlivé aktivity. To může být užitečné například, když je materiál zpožděný a ovlivňuje plán výroby. V takovém případě budou zvýrazněny problémy s materiálem v Ganttově diagramu, což usnadňující plánovači pochopit důsledky a provést nezbytné úpravy. 

U úlohy se zobrazí ikona nedostatku materiálu, pokud je počáteční datum naplánované úlohy pozdější než datum dostupnosti materiálu spotřebovávaného úlohou. Datum dostupnosti materiálu se vypočítává na základě informací o odkazech v dynamickém hlavním plánu. U úlohy, která spotřebovává materiál, který je doložený proti nákupní objednávce s příjmem pozdějším, než je plánované datum zahájení úlohy, se například zobrazí ikona úbytku materiálu.

### <a name="indicator-of-material-availability-date"></a>Indikátor data dostupnosti materiálu

Při nastavení grafu pro zobrazení úloh s nedostatkem materiálu se může zobrazit také ikona, která ukazuje datum dostupnosti materiálu pro úlohu. Ikona se bude zobrazovat, pouze pokud je datum dostupnost materiálu v rámci definovaného časového intervalu grafu. Pokud se datum dostupnosti materiálu nachází mimo stanovený časový interval, můžete ze seznamu materiálu v dialogovém okně úlohy načíst podrobnější informace o dostupnosti materiálu. V seznamu je také ikona zobrazující materiály zpožděné pro úlohu. Úlohu můžete přeplánovat pomocí data dostupnosti materiálu jako počátečního data.

### <a name="indicator-of-order-delivery-date"></a>Indikátor dat dodání objednávky

Tato ikona označuje datum dodání výrobní zakázky. Tato ikona se zobrazí pouze v zobrazení objednávky.

### <a name="capacity-bar"></a>Panel kapacity

Graf lze konfigurovat tak, aby zobrazoval panel kapacity prostředku. Tento panel podává přehled o kapacitě prostředku pro aktivitu v definovaném časovém intervalu v diagramu. Panel kapacity se nezobrazí pro časová období, kdy zdroj není rezervován. V obdobích, ve kterých je zdroj rezervován pro kapacitu, se panel kapacity zobrazuje jako plný pruh. Období, kdy je zdroj obsazen, se na panelu zobrazují silnější čarou s červenou barvou. Například pokud se dvě úlohy překrývají, na panelu kapacity bude uvedena rezervace v časovém intervalu, kde existuje překrytí. Panel kapacita se aktualizuje dynamicky při plánování práce. Panel kapacita aktivujete v nabídce **Zobrazit panel kapacity**. Lze ho zobrazit pouze v **zobrazení zdrojů**. Jestliže chcete získat podrobnější zobrazení vytížení kapacity prostředku, použijte graf **vytížení kapacity**, který lze otevřít z nabídky nebo kontextové nabídky pro vybranou aktivitu.

## <a name="job-scheduling-in-the-gantt-chart"></a>Plánování úloh v Ganttově diagramu
Ganttův graf nabízí různé možnosti provedení úprav výrobního plánu. V Ganttově grafu můžete přeplánovat aktivity v rámci interakce přetažení nebo z nabídky plánu. V procesu plánování můžete zohlednit kapacitu prostředku, schopnosti prostředku a materiálové omezení.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Naplánujte úlohu jako vstup funkce přetažení

Úlohu můžete znovu naplánovat v rámci definovaného časového intervalu interakci přetažení. Můžete znovu naplánovat pouze úlohu na stejném prostředku a můžete naplánovat pouze jednu úlohu v daném okamžiku.

### <a name="schedule-a-job-from-the-menu"></a>Naplánování úlohy z nabídky

V nabídce **plánování úloh** můžete naplánovat jednu nebo více vybraných úloh v grafu na základě způsobu plánování a data plánování. K dispozici jsou tři různé směry plánu.

-   Dopředu od data plánování
-   Zpět od data plánování
-   Dopředu od data dostupnosti materiálu

Není možné plánovat úlohy mimo stanovený časový interval Ganttova diagramu. Pokud tak učiníte, úloha zůstane neplánovaná a zobrazí se chybová zpráva, "Nelze naplánovat úlohu v rámci načteného časového období."

### <a name="schedule-previous-jobs"></a>Naplánovat předchozí úlohy

V síti, aktivit, jako jsou úlohy náležející do stejné výrobní zakázky, můžete vybrat funkci **naplánovat předchozí úlohy** k naplánování předchozích úloh vzhledem k vybrané úloze v síti. V následujícím příkladu je zvýrazněná aktivita vybraná úloha. Diagram znázorňuje stav před naplánováním předchozí úlohy a po naplánování předchozí úlohy. 

[![Naplánovat předchozí úlohu](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Naplánovat následující úlohy

Můžete použít funkci **Naplánovat následující úlohy** k naplánování dalších úloh vzhledem k vybrané úloze v síti aktivit. V následujícím příkladu je zvýrazněná aktivita vybraná úloha. Diagram znázorňuje stav před naplánováním následující úlohy a po naplánování následující úlohy. 

[![Naplánovat následující úlohu](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Plánování kolem úlohy

Můžete použít funkci **Plánování kolem úlohy** k naplánování další úlohy a předchozí úlohy vzhledem k vybrané úloze v síti aktivit. V následujícím příkladu je zvýrazněná aktivita vybraná úloha. Diagram znázorňuje stav před naplánováním úlohy a po naplánování úlohy. 

[![Plánování kolem úlohy](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Uspořádat úlohy

Pomocí funkce **Uspořádat** můžete uspořádat vybrané aktivity ve stejném prostředku. Tyto aktivity mohou být ve stejné síti aktivit, ale náležet také do různých sítí. Při použití funkce uspořádání budou mezery mezi vybranými aktivitami odstraněny. Tato funkce slouží k optimalizaci kapacity využití zdrojů. Diagram znázorňuje stav před naplánováním úlohy a po naplánování úlohy. 

[![Uspořádat úlohu](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Opětovné přiřazení aktivit z jednoho zdroje do druhého

Úlohu můžete znovu přiřadit z jednoho zdroje do druhého. To může být užitečné v situacích, kdy je stroj porouchaný nebo přetížený a je nutné najít jiný dostupný zdroj, který může provést úlohu.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Nové přidělení aktivity jako interakce přetažení

V zobrazení **zdroj** můžete opětně přiřadit aktivitu jinému zdroji v Ganttově diagramu pomocí přetažení. To provedete tak, že vyberete řádek, ve kterém je aktivita naplánována. Po výběru můžete přetáhnout řádek do zdroje v grafu seskupeném podle jiné úrovně seskupení zdrojů.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Nové přiřazení aktivity z nabídky plánu úloh

Můžete opětně přiřadit úlohy z dialogového okna **Naplánovat úlohu** otevřeného z nabídky **Naplánovat úlohu**. V této nabídce můžete pouze přiřadit úlohu k prostředku, který již je načten v Ganttově diagramu. Pokud vyberete pouze jednu úlohu, bude rozevírací nabídka zdroje seřazena podle použitelných zdrojů. Pokud vyberete více úloh, nebudou k dispozici žádné informace o příslušných prostředcích ze seznamu zdrojů.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Načtení dalších zdrojů pro Ganttův diagram
V **zobrazení zdrojů** můžete načítat další zdroje do Ganttova diagramu. To může být užitečné, pokud chcete vyhledat alternativní zdroj pro úlohu, která je naplánována pro stroj, který je přetížený nebo rozbitý. Na stránce **Načíst další zdroje** se zobrazí seznam zdrojů, které jsou platné k datu otevření seznamu. Použitelné zdroje vzhledem k vybrané úloze v Ganttově grafu budou uvedeny jako první. Pokud máte více úloh, které jsou vybrány před otevřením seznamu, nezobrazí se žádná indikace použitelných zdrojů. Na stránce **Načíst další zdroje** můžete vybrat jeden nebo více zdrojů, které budou načteny do Ganttova diagramu při potvrzení výběru. Pokud neexistují žádné úlohy naplánované pro vybraný zdroj v časovém intervalu Ganttova diagramu, bude zdroj umístěn na úrovni seskupení zdrojů v dolní části seznamu aktivit v Ganttově diagramu.

### <a name="access-the-gantt-chart"></a>Přístup do Ganttova diagramu

Ganttův diagram lze otevřít z následujících stránek.


|                                                 <strong>Stránka</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Popis</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Přehled výrobních zakázek a podrobnosti</strong>                                    | Na stránce <strong>přehled výrobních zakázek a podrobnosti</strong> můžete otevřít Ganttův diagram z jedné nebo více vybraných objednávek. Otevření grafu z položky <strong>Ganttův diagram</strong> načte všechny úlohy související s vybranou výrobní zakázkou, ale také úlohy z jiných výrobních zakázek, které jsou naplánovány pro stejné zdroje. Otevírání grafu z <strong>Ganttův diagram – rychlé zobrazení</strong> položku pouze načte úloh souvisejících s vybranou výrobní zakázky. V tomto zobrazení není možné plánovat úlohy. |
|                                               <strong>Zdroj</strong>                                                |                                                                                                                                                        Na stránce <strong>Zdroj</strong> můžete otevřít Ganttův diagram z položky nabídky <strong>Ganttův diagram</strong>. Když je tato možnost vybraná, budou načteny všechny úlohy naplánované ve zdroji ve vybraném časovém intervalu do grafu.                                                                                                                                                         |
|                                            <strong>Skupina zdrojů</strong>                                             |                                                                                                                                                 Na stránce <strong>Skupina zdrojů</strong> můžete otevřít Ganttův diagram z položky nabídky <strong>Ganttův diagram</strong>. Když je tato možnost vybraná, budou načteny všechny úlohy naplánované ve skupině zdrojů ve vybraném časovém intervalu do grafu.                                                                                                                                                 |
|                                             <strong>Ganttovy diagramy</strong>                                              |                                                                                 Na stránce <strong>Ganttovy diagramy</strong> můžete nakonfigurovat Ganttovy diagramy podle zdrojů a skupin zdrojů. Například pokud chcete řídit aktivity výroby pro konkrétní sady zdrojů nebo skupiny zdrojů, můžete nastavit jednotlivé konfigurace na stránce <strong>Ganttovy diagramy</strong>. Pak můžete otevřít Ganttův graf z jednotlivých konfigurací.                                                                                 |
|                                       <strong>Hodinové prognózy</strong> (projekt)                                        |                                                                                                                              Pro zdroje lze naplánovat úlohy aktivit projektu typu <strong>Hodinová prognóza</strong>. Na stránce <strong>Hodinová prognóza</strong> v nabídce <strong>plánování</strong> můžete otevřít Ganttův diagram na objednávce, chcete-li zobrazit naplánované aktivity projektu typu hodinová prognóza.                                                                                                                               |
|           <strong>Úloha k dokončení</strong> (seznam v pracovním prostoru <strong>Dílenské řízení výroby</strong>)            |                                                                                               Pracovní prostor <strong>Úlohy k dokončení seznamu pro Správu dílenské výroby</strong> ukazuje úlohy z výrobních a dávkových objednávek, které budou probíhat z vybraných zdrojů pracovního prostoru. V položce nabídky <strong>Ganttův diagram</strong> můžete otevřít Ganttův diagram, kde budou do grafu načteny všechny úlohy, které jsou v seznamu vybrané.                                                                                               |
| <strong>Výrobní zakázky pro uvolnění</strong> (otevřena z pracovního prostoru <strong>Dílenské řízení výroby</strong>) |                                                                                                                                         Stránka Výrobní zakázky pro uvolnění se otevírá z pracovního prostoru <strong>Dílenské řízení výroby</strong>. Na této stránce se zobrazí plánované výrobní a dávkové objednávky čekající na uvolnění. Na této stránce můžete otevřít Ganttův diagram pro vybrané výrobní zakázky.                                                                                                                                          |

## <a name="additional-resources"></a>Další zdroje  
[Vizuální plánování s Ganntovým diagramem pro výrobu a dávkové objednávky (video)](https://youtu.be/BtbuShkGj4I)

[Vizuální plánování výroby (ukázkový skript)](https://mbs.microsoft.com/customersource/northamerica/365Enterprise/learning/documentation/how-to-articles/365finoptvisschep)


