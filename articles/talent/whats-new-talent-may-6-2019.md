---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (6. května 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c04af27bcc446b516f14125e71fb707bfd1d7708
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529701"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (6. května 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Výběr volitelných dokumentů při tvorbě nabídky

Když vyberete šablonu balíčku nabídek, zobrazí se výzva aplikace Attract k výběru použitelných, volitelných dokumentů z dané šablony balíčku. Při přípravě nabídky můžete přidat další volitelné dokumenty.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2282. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Aktualizace Platform 26 pro Finance and Operations

Další podrobnosti o aktualizaci Platform Update 26 pro Finance and Operations naleznete v tématu [Funkce Preview v aktualizaci Platform Update 26 aplikace Dynamics 365 Finance and Operations (květen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Podpora entity Common Data Service pro vlastní pole

Ve verzi z tohoto týdne následující entity nyní podporují vlastní pole: Frekvenci výpočtu zaměstnaneckých výhod, sazbu výpočtu zaměstnaneckých výhod, typ výhod, pracovní kalendář, svátky pracovního kalendáře, cyklus plateb a typy identifikace pracovníka.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Opuštění hromadného zápisu a změna základu úrovně na Datum služebního věku neaktualizuje počáteční sazbu časového rozlišení (318526)

Když hromadně zapíšete zaměstnance a změníte základ úrovně, původní časové rozlišení nyní odpovídá vybranému základu úrovně.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Workflow zobrazuje duplicitní zástupné hodnoty (313636)

Změny v této verzi eliminují duplicitu zástupných hodnot při odeslání oznámení workflow.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Pole dimenzí nejsou aktualizována při použití položky Otevřít v aplikaci Excel (176261)

V této verzi můžete nyní aktualizovat finanční dimenzi pomocí možnosti **Otevřít v aplikaci Excel** na stránce **Pracovník**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Adresa pracovníka vytvořená v Common Data Service není synchronizovaná do aplikace Talent (317555)

S touto změnou se adresy vytvořené v Common Data Service aktualizují v aplikace Talent: Core HR.


## <a name="in-preview"></a>Náhled

### <a name="new-page-to-validate-position-hierarchy-data"></a>Nová stránka pro ověření dat hierarchie pozic

Lidské zdroje (HR) a správci mohou nyní ověřit manažerskou hierarchii pro všechny cyklické odkazy, které by mohly být nechtěně importovány. K této nové stránce můžete přistupovat z možností **Správa organizace > Propojení > Pozice > Ověření hierarchie pozice**.

### <a name="specify-reason-codes-on-leave-types"></a>Zadání kódů důvodu u typů pracovního volna

Organizace mohou vyžadovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro konkrétní typy pracovního volna na požadavcích na volno

Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Tento požadavek může existovat v důsledku zásad společnosti nebo předpisů. Nyní můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Poskytnutí seznamu transakcí pracovního volna a absencí pro oddělení lidských zdrojů

Možnost sledování volna zaměstnanců a pochopení toho, jak se počítá volno, nejenže pomáhá oddělení lidských zdrojů odpovídat na otázky zaměstnanců, ale také zajišťuje přesné odměny za volno pro zaměstnance. Oddělení lidských zdrojů má nyní nový pohled na transakce (granty, časové rozlišení, úpravy a požadavky), aby jeho členové viděli příčiny zůstatků.

## <a name="coming-soon"></a>Již brzy

### <a name="indicate-instance-type-when-provisioning-talent"></a>Označení typu instance při zřizování aplikace Talent

Při zřizování nové instance aplikace Talent budete moci označit, zda je typem instance **Produkční** nebo **Sandbox**, což umožňuje včasné testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ produkční instance. Chcete-li, aby byla jedna z existujících instancí aktualizována na typu instance sandbox, obraťte se na podporu a inicializujte požadavek na změnu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]