---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (23. dubna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527169"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (23. dubna 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR
Změny popsané v této části se vztahují na číslo sestavení 8.1.2253. Čísla v závorkách se vztahují na čísla podpory v Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Podpora entity Common Data Service pro vlastní pole
Ve vydání z tohoto týdne následující entity podporují vlastní pole: úroveň kompenzace, možnost zaměstnaneckých výhod, typ dovednosti a oblast kompenzace.

### <a name="additional-odata-entities-302992"></a>Další entity OData (302992)
Následující entity jsou nyní podporovány v rámci OData: odborné zkušenosti pracovníka a vzdělání pracovníka.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Přílohy deníku výkonnosti pro manažery a zaměstnance (308248)
V tomto vydání jsou nyní k dispozici přílohy pro manažery i zaměstnance při vytváření a aktualizaci položek deníku výkonnosti.

### <a name="employee-rehire-flag-always-available-310047"></a>Příznak opětovného náboru zaměstnance je vždy k dispozici (310047)
Možnost opětovného náboru zaměstnance je nyní k dispozici pro aktualizaci mimo proces ukončení. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Nelze změnit název **mého způsobu platby** (308815)
Individuální nastavení bylo povoleno, aby byla umožněna změna popisku **mého způsobu platby** v samoobsluze zaměstnanců.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Finanční dimenze proti pozici nelze odstranit (293908)
Finanční dimenze lze nyní odebrat při požadavku na změnu existující pozice a mezipodnikových hranic finančních dimenzí. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Odběratel nemůže publikovat data zpět do aplikace Talent při otevření dat z aplikace Excel (302955)
Tato změna opravuje problém publikování při použití souvisejících tabulek.

## <a name="in-preview"></a>Náhled

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Povolení určení kódů důvodů na typech pracovního volna
Organizace mohou potřebovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro určité typy pracovního volna na požadavcích na volno
Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Může to být způsobeno zásadami společnosti nebo právními požadavky. Nyní můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Poskytnutí seznamu transakcí pracovního volna a absencí pro oddělení lidských zdrojů
Sledování volna zaměstnanců a pochopení toho, jak se počítá volno, nejenže pomáhá oddělení lidských zdrojů odpovídat na otázky zaměstnanců, ale také zajišťuje přesné odměny za volno pro zaměstnance. Oddělení lidských zdrojů má nyní nový pohled na transakce (granty, časové rozlišení, úpravy a požadavky), aby vidělo příčiny zůstatků.

## <a name="coming-soon"></a>Již brzy

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Vylepšení uživatelského rozhraní pro duplicitní kontrolu zaměstnanců
S touto změnou se při zadávání polí názvů zjistí duplicity a stav zobrazí počet nalezených duplicit. Chcete-li otevřít novou stránku, můžete vybrat poskytnutý odkaz a vyhodnotit, zda chcete použít detekovanou shodu. Aby nedošlo k přerušení zadávání dat, formulář duplicit se neotevře automaticky.
## <a name="known-issues"></a>Známé problémy

### <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy
S aktualizací Platform Update 26 Finance and Operations mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěny událostí.


[!INCLUDE[footer-include](../includes/footer-banner.md)]