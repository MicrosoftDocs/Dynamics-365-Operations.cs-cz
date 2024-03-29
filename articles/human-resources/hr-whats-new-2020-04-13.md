---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (13. dubna 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 13. dubnu 2020.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9219e3f2da4d398ed7e8bb27337835d42403925
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692800"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (13. dubna 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3136. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="new-production-release-cadence"></a>Četnost nových vydání

S vydáním tohoto týdne se četnost vydání produktu Human Resources mění z týdenní aktualizace na čtrnáctidenní aktualizaci. Abychom zajistili sbližování s postupy bezpečného nasazení a udržovat ve službě vysoké standardy stability a spolehlivosti, proces nasazení aktualizací služeb do všech regionů je nyní tvořen dvěma týdny. Dodatečná testování a sledovaní jsou zavedena pro ověření úspěšného nasazení v každé fázi procesu. Další informace o četnosti vydání naleznete v tématu [Aktualizace procesu](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Pole přesnosti zaokrouhlení nelze upravit po zadání typu zaokrouhlení (435616)

Tato změna má nyní k dispozici pole **Přesnost zaokrouhlení** po aktualizaci pole **Typ zaokrouhlení**.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Nelze upravit datum ukončení přihlášení, pokud plán volna neobsahuje období časového rozlišení (413628)

Nyní můžete upravit koncové datum přihlášení, aniž by došlo k chybě "Je nutné vyplnit základ data časového rozlišení".

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>Entita zaměstnání se nesynchronizuje do Dataverse (430834)

Tato změna opravuje problém, kdy se data zaměstnání nesynchronizují do Dataverse po přidání finančních dimenzí. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Odebrat pro entitu časového intervalu pracovního kalendáře více nadřazenosti (431775)

Tato změna odstraňuje více nadřazenosti pro entitu **Časový interval pracovního kalenáře**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filtr s funkcí CAST nefunguje na volání OData entity Přiřazení pozice pracovníka (431699)

Tato aktualizace obsahuje změnu pro povolení filtru s funkcí CAST v rámci OData pro entitu **Přiřazení pozice pracovníka**.

## <a name="in-preview"></a>Náhled

## <a name="leave-suspension"></a>Pozastavit pracovní volno

Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance. Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna. Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance. Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Pravidla pro převod do dalšího období

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Známé problémy

## <a name="employment-details-entity"></a>Entita Podrobnosti o zaměstnání

Entita **podrobností o zaměstnání** byla aktualizována pomocí následujících polí:

- **PayFrequency**
- **ID Kategorie zaměstnání**
- **Typ zaměstnání**
- **EmploymentType ID**
- **Stav zaměstnaneckých výhod zaměstnání**

Data nastavení pro tato pole spoléhají na správu výhod, která je povolena v pracovním prostoru **Správa funkcí**. Tato pole v entitě **podrobností o zaměstnání** se nezaplňují ani neaktualizují, protože během importu způsobí chyby.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>V některých prostředích nefunguje náhled služby SharePoint

Pokud nefunguje náhled dokumentů uložených ve službě SharePoint, postupujte následujícím způsobem:

1. Ověřte, zda má uživatelský účet Správce přidružen e-mail k záznamu uživatele. Tyto informace můžete zobrazit na stránce **Uživatel**. Není-li e-mail nastaven, je nutné přidat e-mail a poskytovatele pomocí doplňku OData Excel. Ve výchozím nastavení není v návrhu aplikace Excel e-mailová adresa k dispozici. Je nutné upravit návrh aplikace Excel, přidat všechna pole, použít a aktualizovat. Po dokončení těchto kroků můžete aktualizovat účet správce.

2. Poté, co má účet správce přidružen e-mailový účet, přihlaste se k modulu Human Resources s pověřeními správce.

3. Ve službě SharePoint přistupte k příloze a zobrazte náhled dokumentu.

4. Přihlaste se s jiným uživatelským účtem, který má přístup k přílohám, a ověřte, že náhled funguje očekávaným způsobem.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]