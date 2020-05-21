---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (1. května 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a0cfd1c1b0dcc9defaad7e4cce22ebe1e91fae
ms.sourcegitcommit: cc5dc0bd90277f1ba684dd310da3274886ce573c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2020
ms.locfileid: "3320912"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (1. května 2020)

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3196. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Nové entity správy výkonu dostupné v architektuře pro správu dat (DMF)

K dispozici jsou následující entity. Pokud tyto entity nejsou uvedeny v seznamu entity, použijte možnost **aktualizovat entity** v **Parametrech rozhraní > Nastavení entit > Aktualizovat seznam entit**.

- **Způsobilost k diskusi**
- **Cíle diskuse**
- **Měření diskuse**
- **Téma diskuse**
- **Deník výkonnosti**
- **Měření**
- **Měření cíle**

Kromě toho byly do entity **diskuse** přidány volby **Celkové skóre** a **Průměrné skóre**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Zvětšit délku komentářů k žádosti o dovolenou (275641)

Komentáře k žádostem o dovolenou nyní umožňují více než 100 znaků.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Závěrečné komentáře k revizím se nezobrazí, když je manažer nebo zaměstnanec přihlášen do jiné společnosti (431688)

Všechny komentáře se nyní zobrazí při prohlížení recenzí.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>U nového formuláře pracovníka nejsou uživatelem definované odkazy podporovány (390374)

Uživatelem definované odkazy jsou nyní povoleny na zjednodušeném formuláři **Pracovník**.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity způsobuje selhání rozhraní API OData (439476)

Tato změna opravuje selhání rozhraní API. Tuto chybu způsobil duplicitní název.

## <a name="in-preview"></a>Náhled

## <a name="leave-suspension"></a>Pozastavit pracovní volno

Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance. Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna. Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance. Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Aktualizujte uživatelské prostředí, abyste naznačili, že akruální účet je pozastaven (429550)

Uživatelská zkušenost nyní naznačuje, že přírůstek byl pro plán pozastaven.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Pozastavení časového limitu pro vybrané typy dovolené (272447)

V této verzi může HR vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou. Neplacená dovolená může být zadána, ale nemusí. Dovolenou můžete pozastavit na základě jiného typu dovolené.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>Entita DMF je k dispozici pro akruální pozastavení (429549)

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Přidejte kód příčiny pro akruální pozastavení (429547)

K akruálnímu pozastavení byly přidány kódy důvodů.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Začněte přechod z parametrů lidských zdrojů na parametry dovolené a nepřítomnosti

Tato verze začíná kombinovat parametry lidských zdrojů s parametry dovolené a nepřítomnosti.

## <a name="carry-forward-rules"></a>Pravidla pro převod do dalšího období

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Známé problémy

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>V některých prostředích nefunguje náhled služby SharePoint

Pokud nefunguje náhled dokumentů uložených ve službě SharePoint, postupujte následujícím způsobem:

1. Ověřte, zda má uživatelský účet Správce přidružen e-mail k záznamu uživatele. Tyto informace můžete zobrazit na stránce **Uživatel**. Není-li e-mail nastaven, je nutné přidat e-mail a poskytovatele pomocí doplňku OData Excel. Ve výchozím nastavení není v návrhu aplikace Excel e-mailová adresa k dispozici. Je nutné upravit návrh aplikace Excel, přidat všechna pole, použít a aktualizovat. Po dokončení těchto kroků můžete aktualizovat účet správce.

2. Poté, co má účet správce přidružen e-mailový účet, přihlaste se k modulu Human Resources s pověřeními správce.

3. Ve službě SharePoint přistupte k příloze a zobrazte náhled dokumentu.

4. Přihlaste se s jiným uživatelským účtem, který má přístup k přílohám, a ověřte, že náhled funguje očekávaným způsobem.