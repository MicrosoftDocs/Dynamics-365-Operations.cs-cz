---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 for Talent (27. srpna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529797"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 for Talent (27. srpna 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2447. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Funkce Preview jsou povoleny pouze v instancích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance Produkce nebo Sandbox. Instance typu Sandbox umožňují dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance Produkční. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance Sandbox, obraťte se na podporu a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Zobrazení rozšířených informací o výkonu v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Odstranění právnických osob není povoleno, pokud ve společnosti existují zaměstnanci (339849).

Na základě této změny nelze odebírat nebo odstraňovat společnosti v případě, že pro právnickou osobu existují zaměstnanci a další související data.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Analýza Business Intelligence správy kompenzace se v pracovním prostoru kompenzace (322493) neshoduje.

V této verzi byla analýza kompenzace upravena tak, aby přesně odpovídala plánům přiřazeným zaměstnancům.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Zástupný symbol workflowu %company% zobrazuje DAT při náboru zaměstnanců prostřednictvím workflowu (343905).

V této verzi aplikace zástupný symbol company zobrazuje právnickou osobu, která je spojena se zaměstnáním nového zaměstnance.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>Entita CDSJobPosition zobrazí chybu, pokud je nastaveno platné koncové datum (349387).

V této verzi umožňují zdroje dat **Podrobnosti o pozici** a **Doba trvání pozice** v entitě **CDSJobPosition** úpravy z polí Common Data Service do polí **Datum platnosti**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>V případě výpovědi od zaměstnance je poslední odpracovaný den zadán do pole Koncové datum přiřazení (332496).

Tato změna nyní nastaví pozici **Koncové datum přiřazení** ve výchozím nastavení na **Koncové datum zaměstnání**. Tato výchozí nastavení lze změnit při zadávání dat.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Právnické osoby nejsou omezeny nástupem do zaměstnání (338871).
 
Tato změna omezuje proces náboru tak, aby zobrazoval pouze právnické osoby, ke kterým má uživatel přístup.  

## <a name="in-preview"></a>Náhled

### <a name="streamlined-employee-entry-and-navigation"></a>Zjednodušené zadávání zaměstnance a navigace

Tato funkce je nyní k dispozici v prostředí izolovaného prostoru a zkušebním prostředí. Chcete-li tuto funkci zapnout, přejděte na **Správa systému > Odkazy > Nastavení > Systémové parametry > Funkce náhledu**. Vyberte **Rozšířený formulář pracovníka a navigace**. Tato možnost povolí tyto změny pro všechny uživatele. Tuto možnost můžete kdykoli vypnout.

Další informace naleznete v tématu [Zjednodušené zadání zaměstnance a navigace](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Již brzy

### <a name="platform-update-29"></a>Aktualizace platformy 29

Další podrobnosti o aktualizaci Platform Update 29 naleznete v tématu [Funkce Preview v aktualizaci Platform Update 29 aplikace Dynamics 365 for Finance and Operations (říjen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).


[!INCLUDE[footer-include](../includes/footer-banner.md)]