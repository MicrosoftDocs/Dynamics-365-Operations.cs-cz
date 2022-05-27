---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (23. července 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 23. červenci 2020.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: baf92234bc63449435324cc2d199a0529e53857a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692023"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (23. července 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3416. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Odstranění finančních dimenzí na pozici nefunguje podle očekávání (445476)

Odstranění dimenzí z pozice nyní odstraní stejné pozice z Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Pozice, které nejsou v hierarchii, ukazují neaktivní pozice (397257)

Pozice, které jsou neaktivní (jejichž platnost vypršela), se již v hierarchii pozic nezobrazují jako **Pozice, které nejsou v hierarchii**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Ověření, které nastane mezi importem LeaveEnrollmentEntity a HcmWorkerEntity na importu architektury pro správu dat (DMF), způsobuje pomalé načítání dat (442324)

Změny v této verzi zvyšují výkon **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Nelze provádět přizpůsobení ve správě organizace (447490)

Díky této změně si nyní můžete přizpůsobit odkazy ve **Správě organizace**.

## <a name="in-preview"></a>Náhled

## <a name="mandatory-fields"></a>Povinná pole 

Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů. Tato funkce vyžaduje **Uložená zobrazení**.

## <a name="human-resources-application-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace viz [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod
 
Zvýhodněné účetní jednotky se uvolňují. Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod. K přesunutí dat bude k dispozici šablona správy výhod. Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti.

## <a name="buy-and-sell-leave"></a>Nákup a prodej pracovního volna 

Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou. Tento proces je často řízen ručně. Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů. Usnadňuje proces správy dovolených a pomáhá eliminovat chyby. Další informace naleznete zde:

- [Správa zásad nákupu a prodeje pracovního volna](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Nákup a prodej pracovního volna](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán

Zákazníci mohou zpracovat časové rozlišení pro jednu společnost nebo jeden plán dovolené a nepřítomnosti. Tato schopnost objasňuje proces časového rozlišení pro zákazníky s různými roky dovolené nebo zásadami časového rozlišení dovolené. Další informace získáte v části [Časové rozlišení dovolené podle společnosti nebo plánu dovolených](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Přidání příloh k požadavkům na volno

Schopnost přidávat přílohy ke schváleným požadavkům na dovolenou je v současném prostředí COVID-19 kritická. Zaměstnanci nyní mohou tyto přílohy přidávat. Mají také podrobnější přehled o tom, jak jsou aktualizovány žádosti o dovolenou. Další informace získáte v části [Přidání přílohy k existující žádosti](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Přidání kódu důvodu k časově rozlišeným pozastavením 

K akruálnímu pozastavení byly přidány kódy důvodů.

## <a name="carry-forward-rules"></a>Pravidla pro převod do dalšího období 

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Časové rozlišení pozastavení dovolené pro zadané typy dovolené

Můžete vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou. Neplacená dovolená může být zadána, ale nemusí. Dovolenou můžete pozastavit na základě jiného typu dovolené.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>Entita DMF dostupná pro pozastavení časového rozlišení 

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="coming-soon"></a>Již brzy

## <a name="checklist-entities-included-in-dataverse"></a>Položky kontrolního seznamu zahrnuté do Dataverse

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.

## <a name="platform-changes"></a>Změny platformy

Platform update 10.0.12 (36)

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]