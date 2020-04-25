---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.6. (listopad 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac1
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 319ba09184c087a194b664ca87076d57c6ba0c66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201541"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.6. (listopad 2019)

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.6. Tato verze má číslo sestavení 10.0.234. Zatímco datum všeobecné dostupnosti je v listopadu, nové funkce jsou k dispozici pro dřívější vydání v říjnu. Další informace o verzi 10.0.6 viz [Další zdroje](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Přehled modelů konfigurace datovou entitu V2

Druhá verze pro datovou entitu „modely konfigurace produktu“ je uvolněna (s názvem „modely konfigurace produktu V2“). Výchozí šablona „418 – modely konfigurace produktu“ také musí používat novou datovou entitu „modely konfigurace produktu V2“ v šablonách platformy importu/exportu. Šablona nebude automaticky aktualizována, takže bude nutné šablonu načíst z výchozího nastavení ručně. Entita V2 exportuje jeden řádek jako samostatný soubor přílohy namísto vloženého a vyřeší omezení velikosti entity V1. 
 
Jakým způsobem je nutné provést tuto změnu?
-    Protože se entita V1 již nepoužívá, měli byste zahájit migraci z V1 na v2. Používáte-li šablonu „418 – modely konfigurace produktu“, můžete kliknout na tlačítko „načíst výchozí šablony“ a znovu načíst šablonu s „418 – modely konfigurace produktu“.
-    Potřebujete-li zachovat kompatibilitu s existujícími systémy, můžete nyní nadále používat stávající šablonu a (zastaralou) entitu V1, dokud nepřesunete integrace do nové šablony. 

## <a name="feature-management-enhancements"></a>Vylepšení správy funkcí
Správa funkcí nyní umožňuje povolit všechny nové funkce ve výchozím nastavení, vyžadovat potvrzení povolení funkce a povolit všechny funkce, které dosud nebyly povoleny. 


## <a name="purchase-agreement-responsible-party"></a>Odpovědná strana nákupní smlouvy
Nyní máte možnost definovat primární a sekundární odpovědné osoby ve formuláři klasifikace nákupní smlouvy a výsledných nákupních smlouvách.  To poskytuje uživateli přístup k aplikaci, která tyto smlouvy dohlíží.

## <a name="rfq-link-on-the-purchase-order-line"></a>Odkaz na požadavek na nabídku na řádku nákupní objednávky
Můžete přidat referenční odkaz z řádků nákupní objednávky zpět na odpovídající řádky požadavku na nabídku, odkud pocházejí, a jednoduše poskytnout uživateli podpůrnou žádost o dokument nabídky.

## <a name="additional-resources"></a>Další prostředky

### <a name="bug-fixes"></a>Opravy chyb
Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.6, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Platform update 30
Aplikace Microsoft Dynamics 365 Supply Chain Management 10.0.6 zahrnuje aktualizaci Platform Update 30. Další informace o aktualizaci Platform Update 30 naleznete v tématu [Co je nového a co se změnilo v aktualizaci Platform Update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: plán 2. vlny vydání v r. 2019
Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si téma [Dynamics 365: plán 2. vlny vydání v r. 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.
