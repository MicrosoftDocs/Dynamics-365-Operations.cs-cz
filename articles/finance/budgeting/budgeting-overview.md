---
title: Domovská stránka Rozpočtování
description: V tomto tématu najdete přehled o součástech funkce rozpočtování, rozpočtových nástrojích a možnostech vykazování v aplikaci Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b56f56f5307c292ced30ec94d178244268c5e68
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935435"
---
# <a name="budgeting-home-page"></a>Domovská stránka Rozpočtování

[!include [banner](../includes/banner.md)]

V tomto tématu najdete přehled o součástech funkce rozpočtování, rozpočtových nástrojích a možnostech vykazování. 

<a name="components-of-budgeting-functionality"></a>Součásti funkce rozpočtování
-------------------------------------

Cyklus plánování zdrojů pro společnost se obvykle skládá z plánování, sestavování rozpočtu a prognózování.

[![Komponenty funkce rozpočtování](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

Procesy pro dlouhodobé strategické plánování a plánování ročního rozpočtu jsou podporovány prostřednictvím dokumentu plánu rozpočtu. Dokumenty plánu rozpočtu jsou úzce integrovány s aplikací Microsoft Excel. Uživatelé mohou konfigurovat neomezené peněžní a množstevní scénáře a také definovat rozpočtování organizační hierarchie k podpoře rozpočtování metodami shora dolů a zdola nahoru. Po stanovení a schválení rozpočtu v aplikaci převedete plán rozpočtu na položku registru rozpočtu. Položky registru rozpočtu poskytují nástroje pro správu rozpočtu a udržování přehledu o částkách prostřednictvím kódů rozpočtu. Položky registru rozpočtu umožňují opravit původní rozpočty, provést převody a přenést částky z rozpočtu z předchozího roku. Na základě stanoveného rozpočtu může společnost povolit řízení rozpočtu. Úroveň řízení závisí na kultuře organizace a úrovni vyspělosti organizace. Organizace, které mají nízkou úroveň vyspělosti, mohou ponechat rozpočet bez dalších úprav a mohou být více reaktivní než proaktivní v případě, že rozpočet neodpovídá očekávání. Jiné organizace mohou povolit zásady kontroly rozpočtu, které uživatelům zabrání v nákupech, pokud rozpočtové prostředky nejsou k dispozici.

Velmi vyspělé organizace mohou vytvořit organizační kulturu, ve které se zaměstnanci vzdělávají v otázkách organizačních cílů a postupují podle cílů prostřednictvím pravidel, jako je „Zvažte online schůzky namísto cest.” Aplikace zahrnuje architekturu kontroly rozpočtu, která umožňuje vedoucím pracovníkům společnosti zvolit buď důslednou kontrolu (ta zabraňuje zaúčtování, která by překročila rozpočet), nebo uvolněnou kontrolu (ta uživatele upozorní, že překročí dostupné rozpočtové prostředky, ale oni sami určí další postup). Můžete použít také postupné prognózy. Postupná prognóza je pravidelné porovnání rozpočtu a skutečných hodnot a slouží k určení míry, do jaké společnost operuje oproti rozpočtu. Postupná prognóza se také používá k identifikaci trendů. V aplikaci Finance and Operations jsou podporovány postupné prognózy pomocí dokumentu plánu rozpočtu jako počáteční aktivity plánování. Postupné prognózy lze provádět současně s plánováním nadcházejícího rozpočtového cyklu.

-   [Přehled rozpočtování](basic-budgeting-overview-configuration.md)
-   [Přehled kontroly rozpočtu](budget-control-overview-configuration.md)
-   [Přehled plánování rozpočtu](budget-planning-overview-configuration.md)
-   [Prognóza pozice](position-forecasting.md)
-   [Dokumenty odůvodnění plánování rozpočtu](budget-planning-justification-docs.md)
-   [Šablony plánování rozpočtu pro Excel](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a>Nástroje pro rozpočtování
[![Nástroje pro rozpočtování](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Další funkce plánování a sestavování rozpočtu jsou k dispozici a jsou integrovány do rozpočtů hlavní knihy.

-   **Rozpočty zaměstnanců** – Rozpočtování zaměstnanců obsahuje podrobné rozpočtové náklady na pracovní pozice, skupiny kompenzací a tak dále.
-   **Rozpočty dlouhodobého majetku** – Na základě informací o dlouhodobém majetku můžete vypočítat plánovaný odpis a zaznamenat jiné plánované transakce související s dlouhodobým majetkem.
-   **Rozpočty projektu** – V modulu projektů můžete vytvořit podrobné prognózy projektu. Prognózy projektů budou obsahovat podrobnosti o plánovaných hodinách, výdajích, poplatcích a položkách.
-   **Prognóza poptávky** – Na základě historických dat transakcí můžete odhadovat budoucí poptávku po zásobách a vytvářet prognózy poptávky.

Informace o přenesení dat plánování z jiných modulů do plánů rozpočtu najdete v tématu [Integrace plánování rozpočtu s jinými moduly](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Uživatelské rozhraní a možnosti vykazování
Uživatelé mohou vytvářet plány rozpočtu buď přímo v klientovi (pomocí přizpůsobitelné stránky dokumentu plánu rozpočtu) nebo prostřednictvím aplikace Excel. Excel obsahuje několik dalších funkcí. Můžete například použít externí data jako zdroj pro plán rozpočtu, provádět vlastní výpočty a používat kontingenční tabulky a grafy společnosti Microsoft. Většinu proměnných v procesu plánování rozpočtu lze konfigurovat. 

Například můžete definovat, kdo provádí rozpočtování, co se rozpočtuje a jak proces vypadá. Přestože lze pro plánování rozpočtu použít Excel, aplikace zůstává zachována jako autoritativní zdroj a pomáhá zabránit problémům kontroly rozpočtu. Periodické procesy lze použít k přenosu počátečních dat pro rozpočtování do plánu rozpočtu. Pro vytváření sestav nabízí aplikace standardní sadu stránek s dotazy, které umožňují zobrazení a analýzu dat rozpočtování. K datům plánu rozpočtu lze přistupovat prostřednictvím aplikace Management Reporter a samostatné scénáře plánu rozpočtu lze zobrazit jako sloupce v sestavě aplikace Management Reporter.






