---
title: Použití analytických sestav v aplikaci Microsoft Dynamics 365 Talent– Attract
description: V tomto tématu je popsána analytická sestava pro přehled procesu náboru v aplikaci Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009998"
---
# <a name="use-analytic-reports"></a>Použití analytických sestav

Analytické sestavy v aplikaci Microsoft Dynamics 365 Talent: Attract poskytují vestavěné řešení (OOTB) pro přehledy náborových procesů. Mezi dostupné funkce patří:

- **Analytika práce** – Klikněte na kartu **Analytika** v rámci práce pro metriky na uchazečích o práci.
- **Centrum analýz:** Klikněte na **Analytika** na levém navigačním panelu pro agregované metriky napříč pracemi.
- **Zabezpečení specifické pro uživatele** – Přístup k sestavám je ovládán [rolí](security-attract.md) aplikace Attract a rolí účastníka na práci.
- **Křížové filtrování:** Klikněte na vizuální prvky v rámci sestavy a zobrazte další metriky filtrované podle zvoleného data.

>[!NOTE] 
>- Tato funkce je aktuálně v [náhledu](access-preview-feature.md). Chcete-li to vyzkoušet, musíte mít [**doplněk komplexního náboru**](attract-comprehensive-hiring.md)pronájem.
>- Všechny sestavy veřejné verze Preview jsou zobrazeny v angličtině.
>- Sestavy se obnovují každé 3 hodiny. Čas poslední aktualizace (v místním časovém pásmu) je umístěn v horní části sestavy. Časy aktualizace jsou přibližné a liší se v závislosti na objemu dat a vytížení zdrojů ve vaší oblasti.

## <a name="job-analytics"></a>Analytika práce

Sestavy analytiky práce jsou snímkem procesu náboru pro práci.  Mezi klíčové metriky patří:

- Aktivní uchazeči podle fáze
- Zdroj uchazečů
- Typ uchazeče (interní nebo externí)

## <a name="analytics-hub"></a>Centrum analytiky

Sestavy centra analytiky agregují data napříč pracemi za účelem odhalení trendů v náborovém procesu. Attract zahrnuje dvě OOTB sestavy: Souhrn profilace a trychtýřovou analýzu.

### <a name="pipeline-summary"></a>Souhrn profilace

Sestava souhrnu profilace agreguje data pro otevřené práce. Mezi klíčové metriky patří:

- Uchazeči napříč všemi pracemi podle fáze
- Zdroj uchazečů
- Otevřené pracovní pozice podle úrovně služebního věku

### <a name="funnel-analysis"></a>Trychtýřová analýza

Sestava trychtýřové analýzy agreguje data pro úlohy, které byly uzavřeny jako vyplněné. Mezi klíčové metriky patří:

- Čas do náboru
- Metriky převodu (při najetí myší)
- Míra přijetí nabídky

Poznámka: Chcete-li získat nejpřesnější vykazování doby do náboru, doporučujeme používat [správu nabídek](offer-setup.md), která je k dispozici jako součást doplňku komplexního náboru.

>[!TIP] 
>Zkuste přejít myší nad vizuální prvky pro získání dalších informací. Například při přechodu myší na vizuální prvky **Aktivní uchazeči** se zobrazí průměrné dny ve fázi. Analýza těchto informací může poskytovat přehledy důležité pro snížení doby do náboru a umožnit náborovým pracovníkům zaměřit se na způsoby snížení času stráveného v jednotlivých fázích.

## <a name="user-specific-security"></a>Zabezpečení specifické pro uživatele

Sestavy Attract jsou přístupné pro [role](security-attract.md) správce, čtení všech, náborových pracovníků a náborových manažerů. Nepřiřazení uživatelé nemají přístup k žádné ze stránek analytických sestav (Analytika práce a Centrum analytiky).

Sestavy Analytika práce zobrazují data pro vybranou práci. Sestavy centra analýz agregují data napříč všemi pracemi, které může zobrazit uživatel. Uživatelé, kteří mohou zobrazit jak Moje úlohy, tak Všechny úlohy, na stránce úloh, mají k dispozici stejná zobrazení v centru analýz.

## <a name="cross-filter"></a>Křížové filtrování

Jednou z skvělých funkcí aplikace Power BI je způsob, jakým jsou vzájemně propojeny všechny vizuální prvky na stránce sestavy. Pokud vyberete datový bod na jednom z vizuálních prvků, změní se na základě tohoto výběru všechny ostatní vizuální prvky na stránce, které obsahují tato data. Další informace a příklady naleznete v tématu [Jak se vizuální prvky křížově filtrují navzájem v sestavě Power BI](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Export do aplikace Excel

Chcete-li zobrazit data sestav v aplikaci Excel, můžete kliknout na nabídku možností (tři tečky) na vizuálním prvku a zvolit **Exportovat podkladová data**. Exportovaná data budou exportována jako filtrovaná s ohledem na uživatelská oprávnění v aplikaci Attract. Další informace naleznete v tématu [Export dat z vizualizací](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
