---
title: Odstraněné nebo zastaralé funkce v Dynamics 365 Finance
description: Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.
author: kfend
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 070c61df14db4d2538b129b01defd4b82db0b8a7
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462294"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Odstraněné nebo zastaralé funkce v Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Finance.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v finančních a provozních aplikacích lze nalézt v části [Sestavy technických informací](/dynamics/s-e/global/axtechrefrep_61). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí finančních a provozních aplikací.

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.30

### <a name="revenue-recognition"></a>Uznání výnosů

[Uznání výnosů](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Důvod pro zrušení/odstranění** |Nahrazeno vylepšenou funkčností [fakturace předplatného](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu** | Aplikace |
| **Možnost nasazení** | Vše |
| **Stav** | Zastaráno: Po dubnu 2023 již nebude funkce uznávání příjmů v Dynamics 365 Finance dostávat podporu s opravami chyb. Zákazníci budou požádáni, aby používali vylepšenou funkci [fakturace předplatného](../../finance/accounts-receivable/subscription-billing-summary.md). V říjnu 2023 již nebude k dispozici funkce rozpoznávání výnosů. Zákazníci budou požádáni, aby používali vylepšenou funkci fakturace předplatného. Pro funkci balíčku jako součást účtování výnosů není v tuto chvíli plánována žádná náhradní funkce.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Skladové převodní příkazy s daní na mezipodnikové ceně

[Skladové převodní příkazy s daní na mezipodnikové ceně](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Důvod pro zrušení/odstranění** | Nahrazeno vylepšenou funkcí [Příkazy k převodu akcií pro Indii](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu** | Aplikace |
| **Možnost nasazení** | Vše |
| **Stav** | Zastaralé: Po dubnu 2023 funkce **Příkazy k převodu akcií, které mají daň z převodní ceny** již nebude podporována opravami chyb a bezpečnostními opravami. Zákazníci budou požádáni, aby používali vylepšenou funkci [Příkazy k převodu akcií pro Indii](../../finance/localizations/apac-ind-stock-transfer.md). Po říjnu 2023 nebude funkce **Příkazy k převodu akcií, které mají daň z převodní ceny** již k dispozici a zákazníci budou požádáni, aby přešli na vylepšenou funkci. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Import a export souboru pozitivních plateb z bankovního výpisu

| &nbsp;  | &nbsp;  |
|---|---|
| **Důvod pro zrušení/odstranění** |Nahrazeno vylepšenou funkčností, importem bankovních výpisů a exportem souborů pozitivních plateb.| 
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Aplikace |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaráno: Funkce XSLT pro import a export souborů již nebude podporována opravami chyb a opravami zabezpečení. Zákazníci budou požádáni, aby používali vylepšené funkce: [Nastavte soubory kladných plateb pomocí elektronického výkaznictví](../../finance/accounts-payable/set-up-positive-pay-er.md) a[Nastavte pokročilý import bankovního odsouhlasení pomocí elektronického výkaznictví](../../finance/accounts-payable/import-bai2-er.md). Po září 2022 již nebude funkce XSLT dostupná a zákazníci budou požádáni, aby přešli na vylepšenou funkcionalitu.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.26

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Sestava DPH pro Finsko (design založený na kódech vykazování)

[Sestava DPH pro Finsko](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým designem přiznání k DPH, [Přiznání k DPH pro Finsko](../localizations/emea-fin-vat-declaration.md). |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Aplikace |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. března 2023 plánujeme přestat podporovat sestavu DPH pro Finsko (rozložení sestavy pro Finsko). Místo toho jsou v rámci modelu **Daňové přiznání** zavedeny nové formáty elektronického výkaznictví **Přiznání k DPH v XML (FI**) a **Přiznání k DPH pro Excel (FI)**. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.24

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Sestava DPH pro Švédsko (design založený na kódech vykazování)

[Sestava DPH pro Švédsko](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým designem přiznání k DPH, [Přiznání k DPH pro Švédsko](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. prosince 2022 plánujeme přestat podporovat sestavu DPH pro Švédsko (rozložení sestavy pro Švédsko). Místo toho jsou v rámci modelu **Daňové přiznání** zavedeny nové formáty elektronického výkaznictví **Přiznání k DPH v XML (SE**) a **Přiznání k DPH pro Excel (SE)**. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Výkaz DPH pro Rakousko (design založený na kódech vykazování)

[Podrobnosti výkazu DPH pro Rakousko](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým designem přiznání k DPH, [Přiznání k DPH pro Rakousko](../localizations/emea-aut-vat-declaration-austria.md) |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. prosince 2022 plánujeme přestat podporovat formát elektronického výkaznictví **Přiznání k DPH (AT)** v sekci **Model přiznání k DPH**. Místo toho jsou v rámci modelu **Daňové přiznání** zavedeny nové formáty elektronického výkaznictví **Přiznání k DPH v XML (AT)** a **Přiznání k DPH pro Excel (AT)**. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>Přiznání ELSTER pro Německo (design založený na kódech vykazování)

[Výkaz DPH](../localizations/emea-de-vat-declaration.md)</br>
[Nastavení elektronického daňového přiznání pro Německo](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[Elektronický přenos přiznání k DPH (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým designem přiznání k DPH, [Přiznání k DPH pro Německo](../localizations/emea-deu-vat-declaration-germany.md) |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. prosince 2022 plánujeme přestat podporovat formát elektronického výkaznictví **Elster (DE)** a **Model Elster**. Místo toho jsou v rámci modelu **Daňové přiznání** zavedeny nové formáty elektronického výkaznictví **Přiznání k DPH v XML (DE)** a **Přiznání k DPH pro Excel (DE)**. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>Přiznání OB pro Nizozemsko (design založený na kódech vykazování)

[Přiznání OB](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým designem přiznání k DPH, [Přiznání k DPH pro Nizozemsko](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. prosince 2022 plánujeme přestat podporovat formáty elektronického výkaznictví **Přiznání OB (NL)** a **Model přiznání OB**. Místo toho jsou v rámci modelu **Daňové přiznání** zavedeny nové formáty elektronického výkaznictví **Přiznání k DPH v XML (NL)** a **Přiznání k DPH pro Excel (NL)**. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.20

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Konfigurace formátu požadavku na data faktur dotazu "RTIR Query Invoice Data Request (HU)"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Vyloučeno ze zpracování elektronických zpráv o spolupráci s maďarským online fakturačním systémem |
| **Nahrazeno jinou funkcí?**   | Ne |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 15. dubna 2022 plánujeme, že již nebudeme podporovat konfiguraci formátu „požadavek na data faktur dotazu RTIR (HU)“. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>„Francouzský soubor auditu FEC“ Formát elektronického hlášení (ER) pro Francii ve formátu „Výstup německého souboru auditu“

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým formátem „FEC audit file (FR)“ |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: do 1. května 2022, plánujeme, že již nebudeme podporovat formát „francouzského souboru auditu FEC“ ve formátu elektronického výkaznictví (ER) pro Francii ve formátu „výstup německého souboru auditu“. V části „Model exportu dat“ je místo toho zaveden nový formát souboru auditu FEC (FR). |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Odebrané nebo zastaralé funkce v aplikaci Finance verze 10.0.17

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>Úložiště LCS jako možnost úložiště pro konfigurace elektronických zpráv

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Nahrazeno novým globálním úložištěm Regulatory Configuration Service (RCS) |
| **Nahrazeno jinou funkcí?**   | Ano |
| **Ovlivněné oblasti produktu**         | Dynamics 365 Finance, produkty Supply Chain Management a Project Operations|
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Do 1. dubna 2022 plánujeme přestat podporovat úložiště Microsoft Dynamics Lifecycle Services (LCS) jako možnost úložiště pro konfigurace elektronického vykazování (ER). Nové konfigurace Microsoft ER budou publikovány ke stažení výhradně z globálního úložiště. Globální úložiště je přístupné z produktů Dynamics 365 a RCS. Další informace viz témata [Import konfigurací ER z RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) a [Regulatory Configuration Service – ukončení podpory úložiště Lifecycle Services](../localizations/rcs-lcs-repo-dep-faq.md). |

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

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Nezastaralé: Polské sestavy SSRS: registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Není vyžadováno zákonem.  |
| **Nahrazeno jinou funkcí?**   | Ano (formát aplikace Excel pro standardní soubor auditu s přiznáním k DPH – JPK_VDEK) |
| **Ovlivněné oblasti produktu**         | Přihláška |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Nezastaralé: Od 27. dubna 2021 plánujeme dále podporovat sestavy SSRS: **registr DPH na výstupu, registr DPH na vstupu, souhrnný registr DPH v EU – odkaz na funkci PL-00014**. Uveden byl také příklad formátu aplikace Excel pro standardní soubor auditu s přiznáním k DPH (JPK_VDEK). |

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

