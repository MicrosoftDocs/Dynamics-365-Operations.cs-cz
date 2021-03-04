---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (1. října 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529653"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (1. října 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2509. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="streamlined-employee-entry-and-navigation"></a>Zjednodušené zadávání zaměstnance a navigace

Tato funkce je nyní k dispozici ve všech prostředích. Chcete-li tuto funkci zapnout, přejděte na **Správa systému > Odkazy > Nastavení > Systémové parametry > Funkce náhledu**. Vyberte **Rozšířený formulář pracovníka a navigace**. Tato možnost povolí tyto změny pro všechny uživatele. Tuto možnost můžete kdykoli vypnout.

Další informace naleznete v tématu [Zjednodušené zadání zaměstnance a navigace](./streamlined-employee-entry.md). Chcete-li se podívat na video k těmto změnám, viz [Přehled vlny 2 verze Dynamics 365 for Talent 2019](https://aka.ms/ROGT19RW2ROV).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Můžete povolit funkce náhledu v izolovaném prostoru a zkušebních prostředích.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance Produkce nebo Sandbox. Instance typu Sandbox umožňují dřívější zkoušení nových funkcí. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance Sandbox, obraťte se na podporu a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>Výchozí datum kompenzace je nastaveno na jiné datum, než je přiřazení pozice (337694)

Tato změna nyní nastaví výchozí hodnoty počátečního data kompenzace na počáteční datum přiřazení pozice.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>Nelze ukončit kompenzaci spolu s přiřazením pozice (328993).

Tato změna umožňuje ukončit kompenzaci při ukončení přiřazení pozice pomocí funkce **koncové přiřazení** na stránce **přiřazení pozice pracovníka** s povolenými akcemi personálu.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>Ověření bankovního účtu vyžaduje směrové číslo účtu ve všech skladových místech (340403).

Při změně tohoto týdne byla přidána nová možnost konfigurace, která zakazuje **číslo postupu** a **číslo účtu**, které je vyžadováno ověřením. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>Pro zpětnou vazbu k výkonu nejsou povoleny přílohy ve výkonnostních denících MSS (341794).

Při vydání tohoto týdne jsou přílohy pro položky zpětné vazby povoleny na stránce deník výkonnosti.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>Podrobnosti žádosti o dovolenou se nesynchronizují z Common Data Service do Talent (369608)

S těmito změnami se budou podrobnosti o žádosti o dovolenou, které jsou aktualizovány v Common Data Service, synchronizovat zpět do aplikace Talent.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>Popis úlohy se pro úlohu na stránce analýzy mezer dovedností (369398) nezobrazí.

V sestavení tohoto týdne se popis zobrazí při výběru úlohy na stránce analýzy **Analýza mezer dovedností**.

## <a name="coming-soon"></a>Již brzy

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Zaměstnanci, manažeři a odborníci v oblasti HR budou moci vytisknout hodnocení výkonnosti zaměstnance.


[!INCLUDE[footer-include](../includes/footer-banner.md)]