---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (14. března 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 79bb8c0ed3c3f3bee62a8bc384a9d3a15cfe881a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897596"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (14. března 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract
V této verzi existuje několik menších oprav chyb.

## <a name="changes-in-onboarding"></a>Změny v aplikaci Onboarding
V této verzi existuje několik menších oprav chyb.

## <a name="changes-in-core-hr"></a>Změny v Core HR
**Sestavení 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Správa výkonu nefunguje ve všech scénářích při použití duplicitních rolí zabezpečení
Změny provedené v této verzi umožňují scénáře správy výkonu při použití výchozích nebo duplicitních rolí.

### <a name="mass-assign-checklists-to-workers"></a>Hromadné přiřazení kontrolních seznamů pracovníkům
S touto změnou můžete nyní vybrat více zaměstnanců a hromadně jim přidělit jeden nebo více kontrolních seznamů. 

### <a name="platform-update-24-for-finance-and-operations"></a>Ajtzakuzace Platform Update 24 for Finance and Operations
Další podrobnosti o aktualizaci Platform Update 24 for Finance and Operations naleznete v tématu [Co je nového a co se změnilo v aplikaci Finance and Operations, Platform Update 24 (březen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Podstatné změny v aktualizaci Platform Update 24 obsahují: 

- V aplikaci Talent jsou povoleny výstrahy.
- Aktualizovaný navigační panel je nyní zarovnán se záhlavím Office.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Aktualizace umístění kanceláře přepne kontext na horní část seznamu pracovníků
Se současným vydáním již nepřepne změna umístění kanceláře kontext pracovníka, který prohlížíte při přiřazování umístění kanceláře.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Datum ukončení přiřazení pozice se nezobrazuje správně na akcích náboru a převodu pracovníka
Koncová data přiřazení pozice se nyní správně zobrazují na základě uživatelem preferovaného časového pásma při použití akcí.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Entita práce Common Data Service nepovoluje aktualizaci polí Typ práce a Pracovní funkce
Entity Common Data Service se nyní synchronizují správně při aktualizaci pomocí Common Data Service.

## <a name="coming-soon"></a>Již brzy

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Rozšířené zabezpečení kompenzace (fixní a variabilní)
V mnoha organizacích mohou mít manažeři kompenzací a zaměstnaneckých výhod přístup pouze k určitým záznamům o kompenzacích. Tyto záznamy mohou být pro vedoucí pracovníky nebo regionální zaměstnance. Díky této změně může oddělení lidských zdrojů spravovat a udržovat plány kompenzace pro různé skupiny zaměstnanců v organizaci. Fixním a variabilním plánům lze přiřadit role zabezpečení, které určí přístup k plánům a údajům zaměstnance souvisejících s plány, jako jsou například záznamy o mzdě nebo bonusech. Kompenzace pro tyto zaměstnance mohou zpracovávat pouze role, kterým byl udělen přístup.

###  <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy
V aktualizaci Platform Update 24 for Finance and Operations mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěna událostí.

### <a name="duplicate-employee-check-interface-changes"></a>Kontrola duplicitních zaměstnanců: změny rozhraní
S touto změnou se při zadávání polí názvů zjistí duplicity a stav zobrazí počet nalezených duplicit. Chcete-li otevřít novou stránku, můžete vybrat poskytnutý odkaz a vyhodnotit, zda chcete použít detekovanou shodu. Aby nedošlo k přerušení zadávání dat, formulář duplicit se neotevře automaticky.
