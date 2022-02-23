---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Talent (4. června 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4a42a3b817024447e2ff26cfcb3cdd0df1351158
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528026"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Talent (4. června 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Již brzy v aplikaci Attract

### <a name="job-approvals-on-the-home-page"></a>Schválení práce na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou svá schválení zkontrolovat pod možností **Přiřazeno vám**. V tomto oddílu se zobrazuje ID práce, pracovní pozice, ostatní schvalovatelé a datum, kdy byla práce přiřazena. Uživatelé, kteří odesílají práci ke schválení, si mohou své práce zkontrolovat pod možností **Vyžádáno vámi**. Tato část zobrazuje schvalovatele, kteří potřebují schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Nová stránka pro ověření dat hierarchie pozic

Personál lidských zdrojů (HR) a správci mohou nyní ověřit manažerskou hierarchii pro všechny cyklické odkazy, které byly nechtěně importovány. K této nové stránce můžete přistupovat z možností **Správa organizace \> Propojení \> Pozice \> Ověření hierarchie pozice**.

### <a name="specify-reason-codes-on-leave-types"></a>Zadání kódů důvodu u typů pracovního volna

Organizace mohou vyžadovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro konkrétní typy pracovního volna na požadavcích na volno

Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Tento požadavek může existovat v důsledku zásad společnosti nebo předpisů. Můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Poskytnutí seznamu transakcí pracovního volna a absencí pro oddělení lidských zdrojů

Možnost sledování volna zaměstnanců a pochopení toho, jak se počítá volno, nejenže pomáhá oddělení lidských zdrojů odpovídat na otázky zaměstnanců, ale také zajišťuje přesné odměny za volno pro zaměstnance. Oddělení lidských zdrojů má nyní nový pohled na transakce (granty, časové rozlišení, úpravy a požadavky), aby jeho členové viděli příčiny zůstatků volna.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Při odstranění záznamu z aplikace Talent nedojde k odebrání záznamu z aplikace Common Data Service

Záznamy, které jsou odebrány z aplikace Talent: Core HR, jsou nyní také odebrány z aplikace Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Plány variabilní kompenzace platné od/do data nejsou dodrženy.

V této verzi nelze zaměstnance zařadit do plánu variabilní kompenzace, pokud počáteční datum předchází počátečnímu datu plánu nebo koncové datum je po koncovém datu plánu. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Komentáře k revizím výkonu jsou odebrány, když uživatel vybere možnost Zrušit

Tato verze opravuje problém, kdy jsou odstraněny komentáře revize, pokud uživatel začne měnit komentář, ale poté vybere **Zrušit**. 

## <a name="in-preview"></a>Náhled

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Funkce Preview jsou povoleny pouze v instancích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance **Produkce** nebo **Sandbox**. Instance typu **Sandbox** umožňují dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Omezení typů pracovního volna v žádostech o volno

Organizace mohou nabízet mnoho různých typů volna svým zaměstnancům. Pro zaměstnance však nemusí být vhodné odesílat požadavky na volno u některých typů pracovního volna. Tyto typy pracovního volna mohou být namísto toho spravovány oddělením HR. V této verzi můžete konfigurovat, pro které typy pracovního volna mohou zaměstnanci odesílat žádosti o volno. 

## <a name="coming-soon-in-core-hr"></a>Již brzy v Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Zobrazení rozšířených informací o výkonu v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize, na kterých jejich zaměstnanci spolupracují. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými. 

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Zaměstnanci, manažeři a HR budou moci vytisknout hodnocení výkonnosti zaměstnance.
