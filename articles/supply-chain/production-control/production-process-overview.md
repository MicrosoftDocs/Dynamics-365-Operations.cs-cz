---
title: Přehled výrobního procesu
description: Toto téma poskytuje přehled procesů výroby. Popisuje různé fáze výrobní zakázky, dávkové objednávky a kanbany od vytvoření objednávky po uzavření finančního období.
author: johanhoffmann
ms.date: 09/13/2019
ms.topic: article
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace, ProdParmCostEstimation, ProdParmRelease, ProdSchedule, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19832"
- intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a07733f7e1e830fa1c1c4c8e0cfdc5b41d10750
ms.sourcegitcommit: efccf0838c74cf65382bb6cd852f9bc30ca69230
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727328"
---
# <a name="production-process-overview"></a>Přehled výrobního procesu

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled procesů výroby. Popisuje různé fáze výrobní zakázky, dávkové objednávky a kanbany od vytvoření objednávky po uzavření finančního období.

Výroba produktů – proces nazýván také jako výrobní cyklus, řídí konkrétní kroky, které jsou nutné k dokončení výroby položky. Životní cyklus začíná vytvořením výrobní zakázky, dávkové objednávky nebo kanbanu. Na konci je dokončená vyrobená položka připravená pro zákazníka nebo do jiné fáze výroby. Dokončení jednotlivých kroků životního cyklu vyžaduje různé druhy informací. Dokončení jednotlivých kroků se ve výrobní zakázce, dávkové objednávce nebo kanbanu odrazí zobrazením změny ve stavu výroby. Různé typy produktů vyžadují různé výrobní procesy.

Modul **Řízení výroby** je propojen s jinými moduly, jako je například **Řízení informací o produktech**, **Řízení zásob**, **Hlavní kniha**, **Řízení skladu**, **Účetnictví projektu** a **Správa organizace**. Tato integrace podporuje tok informací, který je požadován k dokončení výroby dokončené položky.

Výrobní proces je obvykle ovlivněn nákladovým účetnictvím a metodami ocenění zásob, které byly vybrány pro konkrétní výrobní proces. Aplikace Supply Chain Management podporuje metodu skutečných nákladů (model \[FIFO\]; model \[LIFO\]; klouzavý průměr a periodický vážený průměr) i standardních nákladů. Štíhlá výroba je implementována na základě pravidla pro zpětné účtování nákladů.

Výběr metod měření nákladů také definuje požadavky pro vytváření sestav o spotřebě materiálu a zdrojů během výrobního procesu. Obvykle metoda skutečných nákladů vyžaduje přesné vytváření sestav na úrovni úlohy, zatímco periodická metoda umožňuje méně podrobné vykazování spotřeby materiálu a zdrojů.

## <a name="mixed-mode-manufacturing"></a>Kombinovaný režim výroby

Jiné produkty a topologie výroby vyžadují použití různých typů objednávek. Supply Chain Management umožňuje použít různé typy objednávek ve smíšeném režimu. Jinými slovy ke všem objednávkám může dojít od začátku do konce při výrobě jednoho konečného produktu.

- **Výrobní zakázka** – jedná se o klasický typ objednávky umožňující vyprodukovat určitý produkt nebo variantu produktu v daném množství k určitému datu. Výrobní zakázky jsou založeny na kusovnících a postupech.
- **Dávková objednávka** – tento typ objednávky se používá pro odvětví zpracování a diskrétní procesy, kde je převod výroby založen na receptuře, nebo kde souběžné a vedlejší produkty mohou být konečné produkty jako doplněk nebo náhrada za hlavní produkt. Dávkové objednávky používají typ **Vzorec** pro kusovníky a postupy.
- **Kanban** – kanbany se používají pro signalizaci procesů štíhlé výroby, které jsou založeny na výrobních tocích kanbanových pravidlech a kusovnících.
- **Projekt** – výrobní projekt spojuje produkty a služby s daným plánem a rozpočtem. Výrobní část projektu lze poskytovat pomocí některého z jiných typů objednávek.

## <a name="manufacturing-principles"></a>Zásady výroby

Pokud chcete vybrat princip výroby, který se nejlépe hodí pro určitý výrobek a související trh, je nutné zvážit požadavky výroby a logistiky a také očekávání zákazníka v oblasti dodací lhůty.

- **Výroba na sklad** – tento princip klasické výroby, kde jsou produkty vytvořeny na sklad, vychází z prognózy nebo minimálních zásob a jejich doplnění (které je většinou vypočteno na základě prognózy nebo historické spotřeby).
- **Zhotovit na objednávku** – standardní výrobky jsou vytvořeny na objednávku nebo dokončenou objednávku. Ačkoli předvýroba může být provedena pomocí principu výroby na sklad, nákladné kroky hodnotového řetězce nebo postup, který vytváří varianty, jsou spuštěny prodejní objednávkou nebo převodním příkazem.
- **Konfigurovat pro objednávku** – stejně jako pro proces zhotovení na objednávku jsou konečné operace hodnotového řetězce vytvořeny na objednávku. Aktuální vyráběná varianta produktu není předdefinována, ale je vytvořena v době zadání objednávky na základě modelu konfigurace pro prodejní produkt. Princip Konfigurovat pro objednávku vyžaduje určitou úroveň sjednocení procesu pro danou produktovou řadu.
- **Technik na zakázku** – procesy Technik na zakázku jsou většinou určeny podle projektu a obvykle začínají fází analýzy. Během fáze analýzy jsou navrženy a popsány skutečné produkty, které jsou vyžadovány ke splnění objednávky. Výrobní zakázky, dávkové objednávky nebo kanbany bude možné vytvořit s cílem vyrábět výrobky.

## <a name="overview-of-the-production-life-cycle"></a>Přehled výrobního cyklu

Následující kroky ve výrobním cyklu mohou nastat pro všechny typy smíšeného režimu výrobní objednávky. Avšak ne všechny z nich jsou reprezentovány jako explicitní stav zakázky.

1. **Vytvořeno** – můžete vytvářet výrobní zakázky, dávkové objednávky nebo kanban ručně, nebo můžete nakonfigurovat systém tak, aby je generoval podle různých signálů poptávky. Hlavní plánování vytvoří výrobní zakázky, dávkové objednávky nebo kanbany potvrzením plánovaných objednávek. Další signály poptávky jsou prodejní objednávky nebo doložené signály dodávek z jiných výrobních zakázek nebo kanbanů. Pro kanbany s pevným množstvím jsou signály poptávky generovány při registraci kanbanů jako prázdných.
1. **Odhadováno** – Můžete vypočítat odhady spotřeby materiálu a zdrojů. Odhad generuje skladové transakce pro suroviny, které mají stav **Na objednávce**. Příjmy pro hlavní produkty, druhotné produkty a vedlejší produkty se generují při odhadu výrobních zakázek nebo dávkových objednávek. Pokud Kusovník obsahuje řádky typu **Doložená dodávka**, nákupní objednávky pro materiály nebo služby pro subdodavatelské operace jsou generovány a doloženy dávkovou objednávkou nebo výrobní zakázkou. Položky nebo objednávky se rezervují podle strategie rezervace výrobní zakázky a cena dokončeného zboží je založena na nastavení parametrů.
1. **Plánováno** – K plánování výroby můžete použít operace, jednotlivé úkoly nebo obojí.

    - **Plánování operací** – Tato metoda plánování poskytuje přibližný a dlouhodobý plán. Pomocí této metody můžete výrobním zakázkám přiřadit data zahájení a ukončení. Jsou-li výrobní zakázky připojeny k operacím postupu, můžete je přiřadit ke skupinám nákladových středisek.
    - **Plánování úlohy** – Tato metoda plánování poskytuje podrobný plán. Každá operace je rozčleněna na jednotlivé úkony s konkrétními daty, časy a přiřazenými provozními prostředky. Je-li použita omezená kapacita, jsou úkony přiřazeny provozním prostředkům na základě dostupnosti. Plán lze zobrazit a změnit v Ganttově diagramu.
    - **Plán kanbanu** – kanbanové úlohy jsou naplánovány v rozvrhu plánování kanbanu nebo automaticky naplánované podle konfigurace automatického plánování kanbanových pravidel.

1. **Vydáno** – můžete vydat výrobní zakázku nebo dávkovou objednávku při dokončení plánu, a když materiál je k dispozici k vyskladnění nebo přípravě. Kontrola dostupnosti materiálu pomáhá vedoucímu dílny posoudit dostupnost materiálu pro výrobní zakázky nebo dávkové objednávky. Můžete také vytisknout výrobní zakázky dokumentů, například výdejku, úkolový lístek, kartu postupu a technologický postup. Po uvolnění výrobní zakázky se stav objednávky změní, aby označoval, že může začít výroba. Při použití řízení skladu má uvolnění výrobní zakázky nebo dávkové objednávky za cíl uvolnění řádků kusovníku do správy skladu. Vlny pro sklad a skladová práce je poté vygenerována podle nastavení skladu.
1. **Připraveno**/**Vyskladněno** – po připravení všech materiálů a zdrojů na výrobním místě jsou aktualizovány řádky kusovníku výroby nebo řádky kanbanu na stav **Vyskladněno**. Doložené objednávky dodávky a související skladová práce je v této fázi obvykle dokončena. Kanbanové karty nebo úkolové karty, které jsou vyžadovány pro hlášení výrobního postupu, by měly být přiřazeny a vytištěny.
1. **Spuštěno** – při zahájení výrobní zakázky, dávkové objednávky nebo kanbanu můžete vykázat spotřebu materiálu a zdrojů oproti objednávce. Systém lze nakonfigurovat pro automatické zaúčtování spotřeby materiálu a zdrojů, které jsou přiřazeny k objednávce při zahájení objednávky. Přidělení se označuje jako vyprázdnění předem, předběžné vyprazdňování nebo automatická spotřeba. Vytvořením dalších deníků výdejek lze zařadit ručně materiál do výrobní zakázky nebo dávkové objednávky. Do objednávky můžete také ručně přidělit práci a další náklady na postup. Pokud používáte plánování operací, můžete tyto náklady přidělit vytvořením deníku karet postupů. Pokud používáte plánování úloh, můžete tyto náklady přidělit vytvořením deníku karet úloh. Výrobní zakázky nebo dávkové objednávky je možné spustit v dávkách konečného požadovaného množství. V rámci výrobní zakázky, dávkové objednávky nebo kanbanu lze spustit úlohy, které jsou vytvořeny, a vykazovat je odděleně skrze deníky, terminály pro provádění výroby (MES terminál) nebo kanbanové desky.
1. Hlášení průběhu/**dokončení** úloh – umožňuje MES terminálu, deníkům výroby, kanbanovým deskám nebo mobilním funkcím skenování ohlásit výrobní postup podle úlohy nebo zdroje. Spotřeba materiálu a zdrojů bude zaúčtována a stav souvisejícího kanbanu, výrobní zakázky nebo dávkové objednávky může být aktualizován na **Přijato** nebo **Ohlášeno jako dokončené**. Může být vytvořena práce vyskladnění v závislosti na konfiguraci skladu.
1. **Ohlášeno jako dokončené** (příjemka produktu) – Je-li výrobní zakázka nebo dávková objednávka vykázána jako dokončená, jsou v zásobách aktualizována množství dokončeného zboží. Toto množství obsahuje množství příslušných souběžných a vedlejších produktů. Pokud používáte účtování nedokončení výroby (NV), deník hlavní knihy sníží účty NV a zvýší zásoby dokončeného zboží. Při výpočtu nákladů výrobní zakázky jsou zaúčtovány skutečné náklady výroby. Pokud náklady na materiál a práci, které jsou přidruženy k dané výrobě, nejsou dosud přiděleny v deníku nebo na základě vyprázdnění předem, lze je automaticky přidělit pomocí zpětného vyprázdnění. Přiřazení pomocí zpětného vyprázdnění zahrnuje dodatečný odpočet procesů skladových transakcí. Je-li výrobní zakázka dokončena, zaškrtněte políčko **Koncová práce** a změňte stav na **Ukončeno**. V opačném případě je pole prázdné, aby bylo možné vykazovat dodatečné množství, které je vyrobeno.
1. **Hodnocení kvality** – příjemka produktu může spustit vytvoření objednávek kvality v závislosti na konfiguraci a procesů testu a pravidel kvality, která jsou vytvořena pro konkrétní produkty. Vzhledem k tomu, že objednávka kvality může aktualizovat stav zásob nebo atributy dávky u testovaných produktů, ocenění kvality je povinný proces v mnoha odvětvích.
1. **Odložení** a **Expedice do objednávky** – po vyhodnocení přijetí produktu a kvality přesměruje volitelná úloha přijaté produkty k dalším bodu spotřeby, do skladu dokončeného zboží nebo do zóny dodávky v případě, že existují požadavky na dodání objednávky.
1. **Ukončeno** – Před ukončením výroby jsou vypočteny skutečné náklady pro vyrobené množství. Všechny odhadované náklady na materiál, práci a režii jsou stornovány a nahrazeny skutečnými náklady. Pokud při spuštění výpočtu nákladů zaškrtnete políčko **Koncová práce**, bude stav výrobní zakázky změněn na **Ukončeno**. Nastavení tohoto stavu zabrání tomu, aby k dokončené výrobní zakázce byly zaúčtovány další náklady.
1. **Uzavření období** – některé zásady nákladového účetnictví, jako je například periodický průměr, náklady zpětného vyprázdnění, či metody FIFO a LIFO, vyžadují periodické aktivity pro uzávěrku zásob nebo fiskálního období. Obvykle se systém pokusí vytvořit sestavy všech materiálů a spotřeby zdrojů, a také provést opravy zásob a odpadu předtím, než je uzavřeno období. Toto oznámení se obvykle provádí pomocí deníků pohybů zásob nebo deníků úprav. Cílem je hodnocení ekonomické výkonnosti provozní jednotky za dané období. V některých případech při použití časově náročných výrobních objednávek, které pokrývají finanční období, se na konci období používají deníky výroby pro vykazování průběhu produkce a spotřeby zdrojů.

## <a name="additional-resources"></a>Další zdroje

- [Zpětná vazba z výroby](production-feedback.md)
- [Přehled modelů konfigurace produktu](../pim/product-configuration-models.md)
- [Lean manufacturing – přehled](lean-manufacturing-overview.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
