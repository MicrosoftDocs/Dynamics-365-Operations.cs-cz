---
title: "Simulace změn nákladů pomocí nákladové verze pro plánované náklady"
description: "Tento článek popisuje simulaci účinků změn nákladů na vypočtené náklady vyráběné položky za použití samostatné nákladové verze pro plánované náklady."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8bdea0ae201ffbf805707cdfda2489c316779e5f
ms.lasthandoff: 03/31/2017


---

# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Simulace změn nákladů pomocí nákladové verze pro plánované náklady

[!include[banner](../includes/banner.md)]


Tento článek popisuje simulaci účinků změn nákladů na vypočtené náklady vyráběné položky za použití samostatné nákladové verze pro plánované náklady.

Účinky změn nákladů na vypočtené náklady vyráběné položky můžete pro plánované náklady simulovat s použitím samostatné nákladové verze. Použijte tuto samostatnou nákladovou verzi pro zadání nevyřízených záznamů nákladů, které odrážejí přírůstkové změny nákladů, a pro výpočet dopadu nákladů na vyráběné položky. Ve výpočtech kusovníku bude použit záložní princip aktivních nákladů, takže je nutno zadat pouze přírůstkové změny nákladů.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Pokyny k definování nákladové verze simulace
Při definování nákladové verze pro simulace postupujte podle následujících pokynů:

-   Přiřaďte nákladový typ **plánovaných nákladů**.
-   Přiřaďte popisný identifikátor pro nákladovou verzi, například **Simulace**.
-   Ověřte, že obsah zahrnuje záznamy o nákladech.
-   Povolte zadávání záznamů nákladů. Neblokujte zadávání čekajících nákladů.
-   Povolte zadávání záznamů nákladů pro všechna pracoviště. Přiřazením pracoviště omezíte zadávání záznamů nákladů na toto pracoviště.
-   Zabránění aktivace čekajících nákladů. V rámci nákladové verze simulace musíte pro nákladové záznamy zadat pouze nevyřízené náklady.
-   Nezadávejte počáteční datum (Od). Pro každý výpočet kusovníku, který používá nákladovou verzi simulace, bude zadáno datum výpočtu.
-   Určete záložní princip pro možnost **Aktuálně aktivní**. Záložní princip umožňuje zadání přírůstkových změn nákladů pro účely simulace, přičemž jako zdroj jsou pro všechny ostatní nákladové záznamy použity aktuální aktivní náklady. Předpokládáme se, že pro všechny ostatní nákladové záznamy existují aktuální aktivní náklady.
-   Určete model nákladových cen pro **nákladovou cenu verze**, avšak neomezujte výpočty. Při simulacích může být například také použit model nákladových cen **skupiny výpočtů kusovníku** pro určení zdroje dat příspěvků nákladů pro zakoupené položky.
-   Určete režim rozpadu pro **více úrovní**, avšak neomezujte výpočty. Při simulacích lze použít jiné režimy rozpadu.

## <a name="costing-versions"></a>Nákladové verze
V následujícím scénáři je znázorněno, jak je použita nákladová verze simulace k simulaci dopadu změn nákladů. Před zadáním simulované změny nákladů odstraňte nevyřízené nákladové záznamy v rámci nákladové verze simulace, aby byla operace zahájena z čistého počátečního bodu. Prostřednictvím stránky **Cena položky** můžete zobrazit a odstranit nevyřízené nákladové záznamy, které souvisí s cenami položek a cenami nákladové kategorie.

-   Proveďte simulaci změny nákladů pro zakoupenou položku. Změna nákladů může například odrážet očekávané zvýšení nebo snížení nákladů zakoupeného kriticky důležitého materiálu. Chcete-li pro zakoupenou položku definovat různé náklady, zadejte na stránce **Cena položky** nevyřízený nákladový záznam v rámci nákladové verze simulace.
-   Proveďte simulaci změny nákladů pro nákladovou kategorii. Změna nákladů může například odrážet očekávané zvýšení nebo snížení sazeb za práci nebo hodinových sazeb pro provozní prostředky. Chcete-li pro nákladovou kategorii definovat různé náklady, zadejte na stránce **Cena nákladové kategorie** nevyřízený nákladový záznam v rámci nákladové verze simulace.
-   Proveďte simulaci změny nákladů ve vzorci pro výpočet nepřímých nákladů. Změna nákladů může například odrážet předpokládané zvýšení nebo snížení režijních nákladů. Chcete-li definovat změnu ve vzorci pro výpočet nepřímých nákladů, na stránce **Nastavení nákladového formuláře** zadejte nevyřízený nákladový záznam v simulaci nákladové verze a ověřte a uložte změnu.

Po zadání simulovaných změn nákladů vypočtěte náklady pro vyráběné položky, které jsou ovlivněny změnami nákladů. Použijte stránku **Výpočet** pro simulaci nákladové verze a určete vybrané vyráběné položky, které budou ovlivněny změnami nákladů. Pokud nevyberete konkrétní položky, budou pro všechny vyráběné položky použity výpočty kusovníku. Jinou možností je použití volby výpočtu kusovníku pro případně použité aktualizace. Zobrazte nákladové záznamy položky v nákladové verzi simulace k analýze způsobu, jakým simulované změny nákladů ovlivnily náklady pro vybrané vyráběné položky. Pomocí stránky **Cena položky** a **Vypočítat náklady na zboží** můžete zobrazit a analyzovat náklady.



