---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (28. května 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 28. květnu 2020.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 00a5881ea88749c8553e4c810fb57070f217b01c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712005"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (28. května 2020)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3287. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>Entita LeaveRequest nefunguje, když povolíte více typů plánů volna (447498)

S touto změnou **LeaveEnrollmentV2Entity** je nyní k dispozici k opravě chyby, ke které dochází, když povolíte více typů dovolené.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Funkce omezení obsahu dávky (náhled) (446619)

Pokud tuto funkci povolíte, můžete při výběru úkolů a dokončení úloh očekávat snížení blokování v tabulkách dávkových rámců.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict při ukládání pracovníka zabraňuje úpravám záznamu v aplikaci People (427915)

Tato změna opravuje chybu při přidávání nového pracovníka, aktualizaci informací o adrese a změně jazykových preferencí. V tomto jedinečném scénáři se zobrazila chyba označující, že záznam nelze aktualizovat. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Nelze přidat přílohu ke schválené žádosti o pracovní volno a znovu ji odeslat (425407)

Tato změna nyní umožňuje přílohy ke schváleným žádostem o dovolenou.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Uživatel může zadat náhradu za zaměstnance v jiném formuláři právnické osoby (409529)

Tato změna zakáže možnosti kompenzace, aby se zabránilo neúmyslnému zápisu záznamů o kompenzaci pro nesprávnou právnickou osobu.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Chyba při převodu zaměstnance a datum přiřazení pracovní pozice je před trváním pozice (429402)

Chybové zprávy při převodu zaměstnance v tomto scénáři byly aktualizovány, aby lépe popisovaly změny potřebné k odstranění problému.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Funkce příloh v samoobslužném zápisu zaměstnaneckých výhod zaměstnance
 
Nyní můžete přidávat přílohy během procesu zápisu výhod pro každý plán, do kterého se zaměstnanec zapisuje. Poté si můžete zobrazit přílohy ve formuláři **Registrované zaměstnanecké výhody pracovníka**.

## <a name="in-preview"></a>Náhled

## <a name="human-resources-application-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>Pozastavit pracovní volno

Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance. Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna. Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance. Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Aktualizujte uživatelské prostředí, abyste naznačili, že akruální účet je pozastaven (429550)

Uživatelská zkušenost nyní naznačuje, že přírůstek byl pro plán pozastaven.

## <a name="coming-soon"></a>Již brzy

## <a name="database-logging-in-preview-in-june"></a>Protokolování databáze (v náhledu v červnu)

Funkce protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány. Umožňuje také určit události, které by měly spustit sledování změn. K dispozici jsou možnosti dotazů, které tyto změny v průběhu času uvidí.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Koupit a prodat volno (v náhledu 1. června)

Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou. Tento proces je často řízen ručně. Tato funkce poskytuje automatizovanější způsob správy zásad a požadavků oddělení lidských zdrojů a pomáhá eliminovat chyby a zefektivnit proces správy dovolené. Další informace naleznete zde:

- [Správa zásad nákupu a prodeje pracovního volna](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Nákup a prodej pracovního volna](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod
 
Zvýhodněné účetní jednotky se uvolňují. Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod. K přesunutí dat bude k dispozici také šablona správy výhod. Šablona exportuje a importuje data sekvenčním způsobem, aby respektovala datové závislosti.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Přidejte kód příčiny pro akruální pozastavení (1. červen)

K akruálnímu pozastavení byly přidány kódy důvodů.

## <a name="carry-forward-rules-june-1"></a>Pravidla pro převod do dalšího období (1. červen)

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Pozastavení časového limitu pro vybrané typy dovolené (1. červen)

V této verzi může HR vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou. Neplacená dovolená může být zadána, ale nemusí. Dovolenou můžete pozastavit na základě jiného typu dovolené.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>Entita DMF je k dispozici pro akruální pozastavení (1. červen)

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)