---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (19. března 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 19. březnu 2020.
author: Darinkramer
manager: AnnBe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0b961de23a76947440f6616176874dc6a86cc4c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712513"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (19. března 2020)

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3014. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Limity prostředí Human Resources jsou nyní založeny na aktualizovaném licencování (394595)

Byl změněn limit počtu prostředí na projekt v rámci Lifecycle Services (LCS). Předchozí limit byl dvě prostředí. Limit pro počet produkčních a sandboxových prostředí, které můžete vytvořit pro Human Resources v LCS, je nyní založen na aktualizovaném licencování. Nyní můžete pro projekt LCS vytvořit tolik prostředí, kolik je třeba, v závislosti na zakoupeném počtu licencí. Nové licencování aktualizované 1. února (2020) umožňuje zákazníkům zakoupit další prostředí. Další informace o licenčních požadavcích pro další prostředí naleznete v tématu [Průvodce licencováním Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Poskytnutí zobrazení dat kompenzace pro zaměstnance a manažery mezi společnostmi (403904)

Tuto funkci zapnete v pracovním prostoru **Správa funkcí**. Další informace naleznete v tématu [Povolení nebo zákaz funkcí ve verzi Preview](hr-admin-manage-features.md#enable-or-disable-preview-features).

Pokud tuto funkci povolíte, manažeři mohou zobrazit kompenzace přímých a dalších podřízených bez nutnosti přihlásit se ke společnosti poskytující zaměstnání. Úplná historie kompenzace je k dispozici ve všech přihlášených společnostech, ke kterým má manažer přístup. Další informace naleznete v tématu [Přehled samoobsluhy pro zaměstnance a manažery](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Povolení funkce sloučení globálního adresáře (427189)

Duplicitní položky adresáře lze nyní sloučit výběrem duplicitních záznamů a možnosti **Sloučit** na stránce **Globální adresář**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Nelze upravit zůstatek dovolené pro plán bez časového rozlišení, který byl vytvořen se zapnutou funkcí Více typů pracovního volna (419635)

Nyní můžete upravit zůstatky pro plány dovolené, které byly vytvořeny se zapnutou funkcí verze Preview **Více typů pracovního volna** ve správě funkcí.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Pole Primární pozice v entitě WorkerPositionAssignmentEntity při rozvázání pracovního poměru se zaměstnancem (420774)

U zaměstnanců s ukončeným zaměstnáním se v entitě zobrazí primární pozice, která byla aktivní v době ukončení. V případě integrace již nebude pro přiřazení pracovní pozice zaměstnance vytvořen duplicitní záznam. 

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

### <a name="platform-update-33"></a>Platform update 33

- Aplikace přes celou stránku (Preview) – Tato ukázková funkce, která vyžaduje povolení funkce Uložená zobrazení, umožňuje přidání aplikací Power Apps a aplikací třetích stran v zobrazení přes celou stránku prostřednictvím řídicího panelu.

- Uložená zobrazení (Preview) – Tato ukázková funkce povoluje uložená zobrazení, což je významné rozšíření podsystému individuálního nastavení. Tato funkce umožňuje uživatelům vlastnit více pojmenovaných sad individuálních nastavení na stránku. Zobrazení lze také publikovat v rolích zabezpečení.

- Optimalizovaná funkce filtrování „je jedna z“ – Tato funkce umožňuje optimalizaci funkce filtrování „je jedna z“, které usnadňuje zadání více hodnot filtru, má jednodušší mechanismus k odebrání jednotlivých nebo všech hodnot filtru a má kompaktnější a intuitivnější vizualizace hodnot filtru.

- Doporučená pole – Uživatelé často potřebují přidávat pole do mřížky nebo na stránku. To může být obtížné s tolika dostupnými poli. Tato funkce místo prohledávání rozsáhlého seznamu umožňuje systému vytáhnout sadu doporučených polí podle toho, co jiní uživatelé nejčastěji přidávají v podobných situacích.

- Výchozí akce jedním prstem v mřížkách – Touto funkcí je zajištěno, že výchozí akce v mřížce je propojena s určitým sloupcem v mřížce bez ohledu na to, zda je tento sloupec přesunut nebo skryt.

## <a name="new-production-release-cadence"></a>Četnost nových vydání

Počínaje dubnem se četnost vydání produktu Human Resources mění z týdenní aktualizace na čtrnáctidenní aktualizaci. Tím se zajistí sjednocení s postupy bezpečného nasazení a vysoké standardy stability a spolehlivosti ve službě. Zavádíme dodatečná testování a sledovaní pro ověření úspěšného nasazení v každé fázi procesu. Další informace o četnosti vydání naleznete v tématu [Aktualizace procesu](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>Náhled

Od 3. února 2020 jsou k dispozici následující funkce náhledu:

- **Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)