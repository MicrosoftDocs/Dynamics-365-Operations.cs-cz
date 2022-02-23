---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (23. října 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 27cb4a7c125cb2b330dff083c8ed0c1ee89c0e7e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527996"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (23. října 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2569. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Aktualizace platformy 30 pro aplikace Finance and Operations

Další informace naleznete v tématu [Co je nového nebo změněné v aktualizaci Platform update 30 pro aplikace Finance and Operations (listopad 2019)](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Odebrání výhod otevře funkci náhledu zahrnutí

V souladu s naším oznámením v příspěvku v blogu Strategické investice v [Core HR řídí provozní dokonalost](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) odebírá společnost Microsoft 18. října 2019 funkci registrace otevření výhod z veřejného náhledu. Místo toho bude v budoucnu vydána nová funkce. Produkční použití funkce pro registrace výhod, která je aktuálně ve veřejném náhledu, není podporováno.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Chyba při výběru země nebo oblasti ve formuláři pracovníka podruhé (350294)

Ve vydání tohoto týdne byl problém opraven při výběru země nebo oblasti ve formuláři **Pracovník**.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Výchozí hodnoty finanční dimenze pro pole kombinace zobrazené v případě, že ruční zadávání je nastaveno na hodnotu pravda (340097)

Na základě této změny platí, že při nastavování finančních dimenzí a použití možnosti nepovolení ručního zadávání bude systém správně nastavovat ve výchozím nastavení hodnotu dimenze na pole **Kombinované zobrazení**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Nové typy relací je třeba přidat do vyhledávání vztahů ve formuláři osobních kontaktů (347691).

Tato verze obsahuje nové funkce pro přidání nových typů vztahů v tabulce **Typy vztahů** a tyto změny se projeví ve vyhledávání vztahů pro osobní kontakty.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Další hodnoty seznamu ve vlastních polích se neodrazí v Common Data Service (379599)

Při vydání z tohoto týdne se po přidání nové hodnoty seznamu k existujícímu vlastnímu poli, které je již synchronizováno s aplikací Common Data Service, zobrazí nové hodnoty seznamu vyskladnění po uplatnění změn entity.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Na stránce Podmínky zaměstnání se zobrazí všechny podmínky zaměstnání po výběru možnosti Otevřít v aplikaci Excel (348073).

V tomto vydání budou v aplikaci Excel otevřeny pouze podmínky zaměstnání vybraného zaměstnance. Rovněž je třeba dodržovat všechna zabezpečení společnosti.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Přidružení mezi entitou Svátek v pracovním kalendáři a entitou pracovního kalendáře chybí v Common Data Service (324178).

Tento vztah byl v této verzi přidán. Tato změna umožní, aby se pracovní dny zaměstnance zobrazovaly v aplikaci PowerApps. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Chyba při použití workflowů samoobslužných stránek zaměstnanců s konfigurovatelnými hierarchiemi (370132)

V tomto vydání je k dispozici lepší zasílání zpráv o způsobu konfigurace workflowů pomocí konfigurovatelných hierarchií. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Systém umožňuje vytvoření nových pozic, kde je datum K dispozici pro přiřazení dřívější než datum aktivace (340103).

Tato změna zobrazí varování, když datum **Dostupné pro přiřazení** předchází datum **Aktivace** pozice.

## <a name="coming-soon"></a>Již brzy

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.

### <a name="feature-management-workspace"></a>Pracovní prostor Správa funkcí

Funkce se přidávají a aktualizují v každém vydání. Funkce Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.

Další informace o změnách přicházejících ve správě funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
