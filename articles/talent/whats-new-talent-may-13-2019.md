---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (13. května 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591495"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (13. května 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.

## <a name="coming-soon-in-attract"></a>Již brzy v aplikaci Attract

### <a name="job-approvals-on-home-page"></a>Schválení práce na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou zkontrolovat svá schválení v části **Přiřazeno vám**, která zobrazuje ID práce, název, ostatní schvalovatele a datum přiřazení. Uživatelé, kteří odesílají práci ke schválení, mohou revidovat své práce v části **Vyžádáno vámi**, která zobrazuje schvalovatele, kteří potřebují schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2297. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Označení typu instance při zřizování aplikace Talent

Při zřizování nové instance aplikace Talent můžete označit, zda je typem instance **Produkční** nebo **Sandbox**, což umožňuje včasné testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typu instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Podpora entity Common Data Service pro vlastní pole

Ve verzi z tohoto týdne následující entity Common Data Service nyní podporují vlastní pole: zaměstnání, frekvenci výpočtu zaměstnaneckých výhod, sazbu výpočtu zaměstnaneckých výhod, svátek pracovního kalendáře a typ identifikace.

### <a name="common-data-service-integration-page"></a>Stránka integrace s aplikací Common Data Service

Tato verze poskytuje novou možnost v nastavení **Správa systému > Odkazy > Integrace > Konfigurace Common Data Service.** Možnost **Konfigurace Common Data Service** umožňuje správci nebo správci dat určitou flexibilitu a vhled se službou Common Data Service. Pomocí této možnosti můžete povolit nebo zakázat integraci Common Data Service s instancí aplikace Talent a zobrazit podrobnosti o synchronizaci mezi instancí aplikace Talent a službou Common Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Import dat o výkonnosti s konečným hodnocením zaměstnanců (316710)

V této verzi můžete importovat historická data hodnocení zaměstnanců. Pole **FinalEmployeeRatingId** má nyní oprávnění k zápisu.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>V Common Data Service nelze vytvořit adresu pracovníka a synchronizovat ji s aplikací Talent (317555)

Tato změna umožňuje synchronizaci dat adres vytvořených v Common Data Service s aplikací Talent.

## <a name="in-preview"></a>Náhled

### <a name="new-page-to-validate-position-hierarchy-data"></a>Nová stránka pro ověření dat hierarchie pozic

Lidské zdroje (HR) a správci mohou nyní ověřit manažerskou hierarchii pro všechny cyklické odkazy, které by mohly být nechtěně importovány. K této nové stránce můžete přistupovat z možností **Správa organizace > Propojení > Pozice > Ověření hierarchie pozice**.

### <a name="specify-reason-codes-on-leave-types"></a>Zadání kódů důvodu u typů pracovního volna

Organizace mohou vyžadovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro konkrétní typy pracovního volna na požadavcích na volno

Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Tento požadavek může existovat v důsledku zásad společnosti nebo předpisů. Můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Poskytnutí seznamu transakcí pracovního volna a absencí pro oddělení lidských zdrojů

Možnost sledování volna zaměstnanců a pochopení toho, jak se počítá volno, nejenže pomáhá oddělení lidských zdrojů odpovídat na otázky zaměstnanců, ale také zajišťuje přesné odměny za volno pro zaměstnance. Oddělení lidských zdrojů má nyní nový pohled na transakce (granty, časové rozlišení, úpravy a požadavky), aby jeho členové viděli příčiny zůstatků volna.
