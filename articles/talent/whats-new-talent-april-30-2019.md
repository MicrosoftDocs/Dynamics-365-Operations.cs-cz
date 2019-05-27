---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent (30. dubna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 112146ac46193e37b33bf429dc5a359f8cfaca94
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505361"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-30-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent (30. dubna 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2270. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Poskytnout zpětnou vazbu

Možnost pro poskytnutí zpětné vazby je umístěna v nabídce **Nápověda** (**?**) v aplikaci Talent. Tato nabídka poskytuje přístup k následujícím zdrojům:

- Zpětná vazba
- Nápověda
- Začínáme
- Podpora
- Nápady
- O aplikaci

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Vylepšení uživatelského rozhraní pro detekci duplicitních zaměstnanců

Díky této změně jsou nyní duplicity detekovány při nastavování polí názvu a indikátor stavu zobrazuje počet zjištěných duplicit. Poskytnutý odkaz otevře stránku, na které je možné zjistit, zda je třeba použít jednu z duplicitních hodnot. Aby nedošlo k přerušení zadávání dat, stránka duplicit se neotevře automaticky. Chcete-li otevřít stránku, je nutné vybrat odkaz.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Podpora entity Common Data Service pro vlastní pole

Ve verzi z tohoto týdne nyní následující entity podporují vlastní pole: zaměstnání, typ zaměstnanecké výhody a cyklus plateb.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Při přiřazení kontrolního seznamu odchodu zaměstnance dochází k chybě (299877)

Tato změna opravuje chybovou zprávu, která se zobrazí při přiřazení kontrolního seznamu odchodu zaměstnanci mimo proces ukončení.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Odkaz na ukončené pracovníky otevře nesprávného pracovníka (309939)

Tato změna opravuje problém, ke kterému dojde při opětovném náboru zaměstnance z jiné právnické osoby a pokusu o přechod na zaměstnance ze seznamu ukončených pracovníků.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Karta kompenzace samoobsluhy zaměstnance nezobrazuje souhrnné hodnoty, pokud je zapnuto rozšířené zabezpečení (315231)

Tato změna opravuje problém, ke kterému dojde při použití rozšířeného zabezpečení kompenzace. Je-li rozšířené zabezpečení zapnuto, samoobsluha zaměstnance nyní zobrazí souhrnné částky kompenzace pro zaměstnance i manažery. Před provedením této změny se souhrnné hodnoty zobrazily jako 0 (nula).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Pokud je v aplikaci Common Data Service vytvořena pozice bez názvu, nevytvoří se v aplikaci Talent žádná pozice (314562)

Změny z tohoto týdne opravují problém, ke kterému dochází při vytváření pozic v Common Data Service bez zadání názvu.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Chybová zpráva v položkách deníku výkonnosti v samoobsluze zaměstnanců (314134)

Tato změna opravuje problém, ke kterému dojde při připojení výkonnostních cílů k položkám deníku výkonnosti v samoobsluze zaměstnanců.

## <a name="in-preview"></a>Náhled

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Povolení určení kódů důvodů na typech pracovního volna

Organizace mohou vyžadovat další informace o požadavcích na pracovní volno. Nyní můžete určit kódy důvodu pro typy pracovního volna a umožnit zaměstnancům vybrat kód důvodu v jejich požadavcích na volno.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vyžádání kódů důvodu pro konkrétní typy pracovního volna na požadavcích na volno

Organizace mohou vyžadovat kódy důvodu pro konkrétní typy pracovního volna, když o něj zaměstnanci žádají. Tento požadavek může existovat v důsledku zásad společnosti nebo předpisů. Nyní můžete určit, které typy pracovního volna vyžadují kód důvodu, a můžete požadovat, aby zaměstnanci poskytli na svých žádostech o volno kód důvodu pracovního volna.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Poskytnutí seznamu transakcí pracovního volna a absencí pro oddělení lidských zdrojů

Možnost sledování volna zaměstnanců a pochopení toho, jak se počítá volno, nejenže pomáhá oddělení lidských zdrojů odpovídat na otázky zaměstnanců, ale také zajišťuje přesné odměny za volno pro zaměstnance. Oddělení lidských zdrojů má nyní nový pohled na transakce (granty, časové rozlišení, úpravy a požadavky), aby jeho členové viděli příčiny zůstatků.

## <a name="coming-soon"></a>Již brzy

### <a name="email-support-for-alerts"></a>Podpora e-mailu pro výstrahy

V aktualizaci Platform Update 26 mohou uživatelé vytvářet pravidla výstrah, která automaticky odesílají e-mailová oznámení kontaktům, pokud jsou spuštěna událostí.
