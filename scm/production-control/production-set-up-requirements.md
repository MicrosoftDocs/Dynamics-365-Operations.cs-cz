---
title: "Požadavky na nastavení výroby"
description: "V tomto článku jsou informace o požadavcích na nastavení předtím, než bude možné pracovat s modulem řízení výroby."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2e39173ef6a27296a20d5f6e44ff6c728aa49c09
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="production-setup-requirements"></a>Požadavky na nastavení výroby

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace o požadavcích na nastavení předtím, než bude možné pracovat s modulem řízení výroby. 

Modul Řízení výroby je integrován s funkcemi v ostatních modulech. Díky této propojenosti můžete měnit výrobní zakázky a spolehnout se na to, že tyto zakázky budou automaticky aktualizovány ve všech souvisejících procesech a výpočtech v daném systému. Následující procesy nastavení by měly být provedeny v pořadí, v jakém jsou uvedeny.

## <a name="required-baseline-setup-in-other-modules"></a>Vyžadované základní nastavení v jiných modulech
Před prací s modulem Řízení výroby je nutné nastavit informace v jiných modulech. Tato nastavení zahrnuje následující úlohy:

-   Nastavení obecných informací o společnosti
-   Nastavení hlavní knihy
-   Definování skupin položek
-   Nastavení účtů hlavní knihy pro skupiny položek
-   Nastavení tabulky položek zásob v modulu Řízení zásob.
-   V modulu Řízení zásob vytvořte kusovníky (BOM) a verze kusovníku.

## <a name="required-calendar-and-resource-setup"></a>Potřebné nastavení kalendáře a prostředků
Před použitím modulu Řízení výroby otevřete modul Správa organizace a v následujícím pořadí vytvořte a definujte kalendář a provozní prostředky:

1.  **Šablony pracovní doby** – Nastavením šablon pracovní doby definujte doby, které jsou k dispozici pro plánování výroby.
2.  **Kalendáře** – Nastavením kalendářů pracovní doby definujte dny v roce, které jsou k dispozici pro plánování výroby.
3.  **Skupiny prostředků** – Nastavením skupiny prostředků seskupte provozní prostředky, abyste mohli při spuštění plánování získat přehled o všech volných kapacitách. Není nutné nastavovat provozní prostředky ještě před nastavením skupin prostředků. Doporučujeme však, abyste se seznámili se způsobem, jakým se při nastavování v modulu Řízení výroby seskupují prostředky.
4.  **Zdroje** – Nastavením provozních prostředků definujte zdroje používané k provedení výrobního procesu a k plánování kapacity.

## <a name="required-production-parameters-setup"></a>Vyžadovaná nastavení parametrů výroby
**Parametry řízení výroby** – Nastavením základních parametrů výroby definujte způsob, jakým systém zpracovává výrobní zakázky. Určete způsob, jakým jsou výrobní zakázky vytvářeny, odhadovány, plánovány a spotřebovávány. Dále je možné vybrat požadovaný druh zpětné vazby a způsob provádění nákladového účetnictví.

## <a name="required-journal-name-identification"></a>Vyžadovaná identifikace názvu deníku
**Názvy deníků výroby** - Určete názvy deníků výroby používaných k zaznamenání a zaúčtování transakcí.

## <a name="setup-if-you-use-operations"></a>Nastavení při použití operací
Operace reprezentují specifické aktivity prováděné za účelem výroby hotového výrobku. **Poznámka:** Je nutné znát typy aktivit, které jsou zapotřebí k výrobě položky, a také pořadí a priority těchto aktivit. Také musíte vědět, které prostředky jsou zapojeny a kolik jich je.

1.  **Operace** – Nastavte operace reprezentující úkoly, které je nutné dokončit při výrobě hotové položky.
2.  **Vztahy** – Nastavením vztahů operací vytvořte podrobné vlastnosti. Vztahy operací můžete definovat kliknutím na tlačítko **Vztahy** na stránce **Operace**.

## <a name="setup-if-you-use-routes"></a>Nastavení při použití postupů
Pokud pracujete s postupy, je nutné definovat operaci pro každý nastavený výrobní postup. Postup reprezentuje cestu, kterou položka urazí mezi operacemi od počátku procesu výroby až po jeho konec.

1.  **Nákladové kategorie** – Nastavením nákladových kategorií definujte náklady na hodinu pro stanované procesy a přípravné časy.
2.  **Nákladové skupiny** – Nastavením nákladových skupin můžete vytvořit a udržovat různé typy nákladů.
3.  **Skupiny postupů** – Nastavením skupin postupů můžete definovat parametry týkající se skupin postupů. Skupiny postupů je nutné nastavit před vytvořením výrobních postupů.
4.  **Postupy** – Nastavením výrobních postupů a definováním výchozích nastavení můžete řídit plánování, náklady a oceňování operací postupů a hlášení průběhu.
5.  **Postupy** – Nastavením verzí postupů povolíte odchylky položek ve výrobě.

## <a name="optional-advanced-settings"></a>Volitelná rozšířená nastavení
1.  **Skupiny výroby** – Nastavením skupin výroby vytvoříte vztahy mezi výrobní zakázkou a účty hlavní knihy. Účty hlavní knihy jsou používány k zaúčtování nebo seskupení objednávek pro vykazování.
2.  **Skupiny produktů** – Vytvořením skupin výrobků můžete seskupit výrobní zakázky tak, že bude možné zpracovat naléhavé výrobní zakázky nebo odstranit a zaúčtovat skupiny objednávek.
3.  **Vlastnosti** – Definováním vlastností můžete vytvořit speciální atributy, které lze přiřadit zdrojům a řídit tak pořadí výroby. Tyto atributy jsou spojeny se šablonou pracovní doby.





