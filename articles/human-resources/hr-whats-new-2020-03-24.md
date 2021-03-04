---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (24. března 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 24. březnu 2020.
author: Darinkramer
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87b7ea660d94c6d564a8f09d4133b098e0ecedf9
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526900"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (24. března 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3073. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Limity prostředí Human Resources jsou nyní založeny na aktualizovaném licencování (394595)

Byl změněn limit počtu prostředí na projekt v rámci Lifecycle Services (LCS). Předchozí limit byl dvě prostředí. Limit pro počet produkčních a sandboxových prostředí, které můžete vytvořit pro Human Resources v LCS, je nyní založen na aktualizovaném licencování. Nyní můžete pro projekt LCS vytvořit tolik prostředí, kolik je třeba, v závislosti na zakoupeném počtu licencí. Nové licencování aktualizované 1. února (2020) umožňuje zákazníkům zakoupit další prostředí. Další informace o licenčních požadavcích pro další prostředí naleznete v tématu [Průvodce licencováním Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="platform-changes"></a>Změny platformy

- Aplikace přes celou stránku (Preview) – Tato ukázková funkce, která vyžaduje povolení funkce Uložená zobrazení, umožňuje přidání aplikací Power Apps a aplikací třetích stran v zobrazení přes celou stránku prostřednictvím řídicího panelu.

- Uložená zobrazení (Preview) – Tato ukázková funkce povoluje uložená zobrazení, což je významné rozšíření podsystému individuálního nastavení. Tato funkce umožňuje uživatelům vlastnit více pojmenovaných sad individuálních nastavení na stránku. Zobrazení lze také publikovat v rolích zabezpečení.

- Optimalizovaná funkce filtrování „je jedna z“ – Tato funkce umožňuje optimalizaci funkce filtrování „je jedna z“, které usnadňuje zadání více hodnot filtru, má jednodušší mechanismus k odebrání jednotlivých nebo všech hodnot filtru a má kompaktnější a intuitivnější vizualizace hodnot filtru.

- Doporučená pole – Uživatelé často potřebují přidávat pole do mřížky nebo na stránku. To může být obtížné s tolika dostupnými poli. Tato funkce místo prohledávání rozsáhlého seznamu umožňuje systému vytáhnout sadu doporučených polí podle toho, co jiní uživatelé nejčastěji přidávají v podobných situacích.

- Výchozí akce jedním prstem v mřížkách – Touto funkcí je zajištěno, že výchozí akce v mřížce je propojena s určitým sloupcem v mřížce bez ohledu na to, zda je tento sloupec přesunut nebo skryt.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Nelze upravit zůstatek dovolené pro plán bez časového rozlišení, který byl vytvořen se zapnutou funkcí "Více typů pracovního volna" (419635)

S touto změnou nyní můžete upravit zůstatky pro plány dovolené, které byly vytvořeny se zapnutou funkcí verze Více typů pracovního volna (náhled) ve správě funkcí.

## <a name="in-preview"></a>Náhled

Od 3. února 2020 budou k dispozici následující ukázkové funkce:

- **Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Řešení Common Data Service je nyní k dispozici s následujícími změnami:

| popis | Vrácená hotovost |
| --- | --- |
| Změny entity **práce/pozice** | <ul><li>Přidána **Oblast kompenzace**</li>|
| Byla přidána entita **Dimenze pracovní pozice** | <ul><li>Přidání **finančních dimenzí**</li>
| Změny entity **pracovníka** | <ul><li>Přidání **sekvence jmen**</li><li>Přidaná možnost **Práce z domova**</li><li>Přidán **jazyk**</li><li>Přidáno **Datum služebního věku**</li><li>Přidáno **Datum výročí**</li><li>Přidáno **Datum původního přijetí**</li></ul> |
| Změny **entity zaměstnání** | <ul><li>Přidání **finančních dimenzí**</li><li>Přidán **Důvod pro výpověď**</li><li>**Datum ukončení** přejmenováno z **data přechodu**</li><li>Přidáno **datum zkušební doby**</li></ul> |
| Změny entity **adresy pracovníka** | <ul><li>Přidána **Adresa ulice**</li><li>**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis</li></ul> |
| Nové entity nastavení s nastavením variabilní kompenzace | <ul><li>**Typ plánu variabilní kompenzace**</li><li>**Plán variabilní kompenzace**</li><li>**Pravidla připsání**</li><li>**Úroveň plánu variabilní kompenzace**</li></ul> |
| Nová entita **Zaměstnání dle kalendáře pracovníka** | <ul><li>Byla přidána **entita pracovního kalendáře**</li></ul> |
| Nová entita **Mzdové podrobnosti o pozici** | <ul><li>Byla přidána položka **Mzdové podrobnosti o pozici**.</li></ul> |
| Nová entita **Pozice** | <ul><li>Přidána položka **Pozice**</li></ul>Nová entity **Pozice** je zahrnuta do Common Data Service, ale tentokrát neodkazuje z entit **Pracovní pozice** nebo **Práce**. |

> [!NOTE]
> Finanční dimenze pro pracovní pozice i zaměstnanost poskytují integraci jedním směrem pro aktualizace z modulu Human Resources do Common Data Service. Aktualizace finančních dimenzí nejsou v současné době synchronizovány z Common Data Service do modulu Human Resources.

Během příštích několika týdnů budou tyto změny entit k dispozici ve všech prostředích. Postup při ruční instalaci nejnovějšího řešení Common Data Service pro Human Resources:

1.  Přejděte do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2.  Vyberte **Prostředí**.

3.  Vyhledjete prostředí, která chcete upgradovat. Prostředí by mělo odpovídat poli **Název prostředí** v sekci **Informace o Common Data Service** ve formuláři **O aplikaci** v modulu Human Resources.

4.  Vyberte prostředí pro zobrazení podrobností o prostředí.

5.  Vyberte možnost **Správa řešení** na panelu akcí nahoře. Otevře se nové okno prohlížeče a přejde do **Centra pro správu Dynamics 365** v kontextu vašeho prostředí.

6.  Na seznamu **Řešení** vyberte možnost **Kotva Dynamics 365 Human Resources**.

7.  Chcete-li použít poslední řešení, vyberte možnost **Upgrade**.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>V některých prostředích nefunguje náhled služby SharePoint

Pokud nefunguje náhled dokumentů uložených ve službě SharePoint, postupujte následujícím způsobem:

1. Ověřte, zda má uživatelský účet Správce přidružen e-mail k záznamu uživatele. Tyto informace můžete zobrazit na stránce **Uživatel**. Není-li e-mail nastaven, je nutné přidat e-mail a poskytovatele pomocí doplňku OData Excel. Ve výchozím nastavení není v návrhu aplikace Excel e-mailová adresa k dispozici. Je nutné upravit návrh aplikace Excel, přidat všechna pole, použít a aktualizovat. Po dokončení těchto kroků můžete aktualizovat účet správce.

2. Poté, co má účet správce přidružen e-mailový účet, přihlaste se k modulu Human Resources s pověřeními správce.

3. Ve službě SharePoint přistupte k příloze a zobrazte náhled dokumentu.

4. Přihlaste se s jiným uživatelským účtem, který má přístup k přílohám, a ověřte, že náhled funguje očekávaným způsobem.

## <a name="coming-soon"></a>Již brzy

## <a name="new-production-release-cadence"></a>Četnost nových vydání

Počínaje dubnem se četnost vydání produktu Human Resources mění z týdenní aktualizace na čtrnáctidenní aktualizaci. Abychom zajistili sbližování s postupy bezpečného nasazení a udržovat ve službě vysoké standardy stability a spolehlivosti, proces nasazení aktualizací služeb do všech regionů bude nyní tvořen dvěma týdny. Dodatečná testování a sledovaní budou zavedena pro ověření úspěšného nasazení v každé fázi procesu. Další informace o četnosti vydání naleznete v tématu [Aktualizace procesu](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Známé problémy

## <a name="employment-detail-entity"></a>Entita Podrobnosti o zaměstnání

Entita **Podrobnosti o zaměstnání** byla aktualizována pomocí následujících polí: **PayFrequency**, **ID kategorie zaměstnání**, **Typ zaměstnání**, **EmploymentType ID** a **tav zaměstnaneckých výhod zaměstnání**. Data nastavení pro tato pole spoléhají na správu výhod, která je povolena ve Správě funkcí. Tato pole v entitě **Podrobností o zaměstnání** by neměla být naplňována ani aktualizována, protože během importu způsobí chyby.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]