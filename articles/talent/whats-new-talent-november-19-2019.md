---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (19. listopadu 2019)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527137"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (19. listopadu 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2621. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Aktualizace platformy 31 pro aplikace Finance and Operations

Další informace naleznete v tématu [Funkce Preview v aktualizaci Platform update 31 pro aplikace Finance and Operations (leden 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Pracovní prostor Správa funkcí (383856)

Pracovní prostor **Správa funkcí** uvádí seznam funkcí dodaných v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace. Další informace o aktivaci správy funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru **Správa funkcí** zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.
 
V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor **Správa funkcí**).
 
Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor **Správa funkcí** označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Zpráva se zobrazí, pokud zrušená akce existuje pro pozici (382887)

Následující zpráva se již nezobrazí, pokud vyberete určitou pozici a je k dispozici zrušená akce pro danou pozici: **Probíhá nedokončená akce pro pozici xxxxxx.**

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>V rámci analýzy studia zobrazuje typ a stav kurzu nesprávná data (381151).

Verze z tohoto týdne aktualizovala analytiku studia tak, aby správně zobrazovala **Typ kurzu** a **Stav**.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>V banneru formuláře Nový pracovník by se mělo zobrazovat číslo pracovníka (383832)

Ve formuláři **Nový pracovník** zobrazuje **Číslo personálu** nyní banner pro rychlou referenci.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Počáteční datum pozice určuje záznam úlohy, který se má použít při načítání úrovně kompenzace během pronájmu (350361).

V této verzi aplikace **počáteční datum kompenzace** určuje úroveň přiřazenou nové práci.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Pole vlastního seznamu vyskladnění v tabulce pozic nejsou synchronizována s Common Data Service (387503).

V rámci této verze jsou položky seznamu vyskladnění synchronizovány s aplikací Common Data Service.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Entita adresy pracovníka není synchronizovaná s aplikací Common Data Service při importu nových dat (349673).

V tomto týdnu jsou data adres synchronizována s aplikací Common Data Service při importu nových dat.

## <a name="in-preview"></a>Náhled

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.


[!INCLUDE[footer-include](../includes/footer-banner.md)]