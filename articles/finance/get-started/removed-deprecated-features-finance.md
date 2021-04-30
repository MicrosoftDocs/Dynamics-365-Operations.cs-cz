---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Finance
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: e0db5c35e58ab7a7cbf31642072d25ee5d8ba868
ms.sourcegitcommit: 04817103dc8e87a679d371575927284b8ce080b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/15/2021
ms.locfileid: "5898280"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](/dynamics/s-e/global/axtechrefrep_61). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.20

### <a name="rtir-query-invoice-data-request-hu-format-configuration"></a>Konfigurace formátu požadavku na data faktur dotazu RTIR (HU)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Vyloučeno ze zpracování elektronických zpráv o spolupráci s maďarským online fakturačním systémem |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 15. dubna 2022 plánujeme, že již nebudeme podporovat konfiguraci formátu „požadavek na data faktur dotazu RTIR (HU)“. |


## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.17

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>Úložiště LCS jako možnost úložiště pro konfigurace elektronických zpráv

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým globálním úložištěm Regulatory Configuration Service (RCS) |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Dynamics 365 Finance, produkty Supply Chain Management a Project Operations|
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. dubna 2022 plánujeme přestat podporovat úložiště Microsoft Dynamics Lifecycle Services (LCS) jako možnost úložiště pro konfigurace elektronického vykazování (ER). Nové konfigurace Microsoft ER budou publikovány ke stažení výhradně z globálního úložiště. Globální úložiště je přístupné z produktů Dynamics 365 a RCS. Další informace získáte v tématu [Import konfigurací ER z RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.16

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Formáty elektronického hlášení „Přiznání DPH (CZ)“ a „Export kontrolního hlášení (CZ)“ pro Českou republiku

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novými formáty |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 22. ledna 2022 plánujeme nadále nepodporovat formáty elktronických výkazů (ER) „Přiznání DPH (CZ)“, „Export kontrolního hlášení (CZ)“. Místo toho jsou v rámci modelu „Daňové přiznání“ zavedeny nové formáty XML přiznání DPH (CZ), Excel přiznání DPH (CZ), XML kontrolního hlášení DPH (CZ). |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>„Formát exportu transakcí hlavní knihy (BE)“ Formát elektronického hlášení a příslušný model „Export transakcí hlavní knihy (BE)“ pro Belgii

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým formátem ER v modelu „Standardní soubor auditu (SAF-T)“.  |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. prosince 2021 plánujeme, že již nebudeme podporovat formát elektronického výkaznictví (ER) „Formát exportu transakcí hlavní knihy (BE)“ a příslušný model „Export transakcí hlavní knihy (BE)“. V rámci modelu „Standardní soubor auditu (SAF-T)“ je místo toho zaveden nový formát „Export dat hlavní knihy (BE)“ spolu s „Mapováním datového modelu hlavní knihy“. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>Sestava "VAT 100" pro spojené království ve formátu SSRS

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým formátem ER - formát „Declaration VAT Excel (UK)“ pod „Model daňového přiznání“.  |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. prosince 2021 plánujeme, že již nebudeme podporovat „přehled 100 DPH“ ve formátu SSRS. Pro EU byl zaveden nový formát "Prohlášení o DPH Excel (UK)" v sekci "Model daňového přiznání" [Funkce DPH MTD](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je podpora aplikace Microsoft Internet Explorer 11 zastaralá pro všechny produkty Dynamics 365 a Internet Explorer 11 nebude podporován po srpnu 2021.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Internet Explorer 11 nebude podporován po srpnu 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.12

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Polské sestavy SSRS: registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Není vyžadováno zákonem.  |
| **Nahrazeno jinou funkcí?**   | Ano (formát aplikace Excel pro standardní soubor auditu s přiznáním k DPH – JPK_VDEK) |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od 1. července 2021 plánujeme již dále nepodporovat sestavy SSRS: **registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014**. Namísto toho bude zaveden příklad formátu aplikace Excel pro standardní soubor auditu s přiznáním k DPH (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.11

### <a name="norwegian-standard-main-accounts"></a>Standardní hlavní účty pro Norsko

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Změnit návrh  |
| **Nahrazeno jinou funkcí?**   | Ano (nahrazeno parametry specifickými pro aplikaci formátu ER) |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: od 1. dubna 2021 nebude možné podporovat funkce související se standardními hlavními účty: referenční pole, související tabulka, entita dat. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Změněno na funkci s výběrem skupiny účtů.  |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Workflow |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: do 1. prosince 2020 plánujeme nadále nepodporovat nastavení čínských typů dokladů bez výběru skupin účtů. Další informace o novém designu najdete v části [Co je nového ve verzi 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
