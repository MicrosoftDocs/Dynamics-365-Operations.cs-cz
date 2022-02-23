---
title: Zjednodušené zadávání zaměstnance a navigace
description: Zadávání dat pro pracovníky v aplikaci Dynamics 365 Talent bylo rozšířeno tak, aby umožňovalo rychlé zadání pro všechny zaměstnance, minulé, aktivní nebo budoucí. Byl aktualizován zjednodušený nebo konsolidovaný navigační model s cílem rychlého vyhledání souvisejících informací a zobrazení a provedení nezbytných aktualizací.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/26/2020
ms.locfileid: "4460628"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Zjednodušené zadávání zaměstnance a navigace

Dynamics 365 Talent umožňuje efektivní zadávání údajů o zaměstnancích a zaměstnání. Informace o historii práce můžete rychle aktualizovat pro minulé, aktivní a budoucí zaměstnance a dodavatele.

Můžete také povolit zjednodušenou navigaci s rychlým vyhledáváním informací souvisejících s uživatelem a provést potřebné změny. Tato funkce je nyní k dispozici ve všech prostředích. Chcete-li tuto funkci zapnout, přejděte na položku **Správa systému > Správa funkcí > Nová > Zjednodušené zadávání zaměstnance > Povolit**. To povolí tyto změny pro všechny uživatele. Tuto možnost můžete kdykoli vypnout.

## <a name="view-options"></a>Možnosti zobrazení

Pomocí příkazu **Možnosti zobrazení** ve formuláři pracovníka můžete vybrat libovolnou kombinaci zaměstnanců a dodavatelů z jednoho seznamu. Tyto možnosti umožňují zobrazit pracovníky mezi právnickými osobami nebo pro právnickou osobu, ke které jste právě přihlášeni. Můžete také zobrazit aktivní, čekající a ukončené pracovníky a můžete omezit výsledky na základě typu pracovníka (zaměstnanec nebo dodavatel). Je-li povoleno rozšířené zabezpečení, zobrazí se pouze zaměstnanci a dodavatelé v právnických osobách, ke kterým máte přístup.

Sloupce v seznamu se změní na základě vašeho výběru. Například při zobrazení ukončených zaměstnanců se kódy data ukončení a důvodu zobrazí jako další sloupce v seznamu. 

[![Možnosti zobrazení](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Navigace a banner

V tomto banneru jsou zobrazeny klíčové informace pro každého pracovníka. V banneru aktivních pracovníků se zobrazí následující pole:

- **Titul**
- **Oddělení**
- **Typ pozice**
- **Typ pracovníka**
- **Manažer**
- **Právnická osoba**

V banneru ukončených pracovníků se zobrazí následující pole:

- **Datum ukončení**
- **Důvod**

V banneru čekajících zaměstnanců se zobrazí následující pole:

- **Titul**
- **Oddělení**
- **Typ pozice**
- **Manažer**
- **Počáteční datum**
- **Právnická osoba**

Podokno akcí na stránce pracovníka bylo znovu uspořádáno tak, aby obsahovalo méně možností. Informace jsou nyní uspořádány do následujících kategorií: 

- Práce
- Osoba
- Pracovní volno
- Kompenzace
- Zam. výhody
- Dodržování předpisů

Kromě toho nová karta **Odkazy** na hlavní stránce pracovníka poskytuje uživatelům centrální umístění pro přístup ke všem souvisejícím informacím pro daného pracovníka.

Z důvodu těchto změn se mohou informace zobrazit na jiném místě, než na jaké jste zvyklí. Například informace o mzdách, které se dříve zobrazily ve formuláři pracovníka, se nyní zobrazí v podokně akcí pod položkou **Kompenzace > mzdy** a karta **Osobní údaje** má nyní tlačítko **Další informace** pro pole, která často nepoužíváte.

[![Banner](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Historie práce

Karta **Historie práce** zobrazuje historii práce pro všechny právnické osoby a je k dispozici pro ukončené, aktivní a čekající zaměstnance a dodavatele. Nyní můžete zobrazit celou historie práce pro právnické osoby, ke kterým máte přístup. Kromě toho můžete upravit informace pro každou z položek historie práce, aniž byste změnili kontext dat. Všechny informace lze aktualizovat přímo na stránce. 

[![Historie práce](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Historie pozic

Karta **Pozice** na hlavní stránce pracovníka poskytuje kompletní přehled o všech pozicích zastávaných v rámci organizace, včetně předchozích, současných a budoucích přiřazení. V podokně akcí lze nadále přejít přímo na historii pozic pracovníka.

[![Pozice](./media/Worker-position-history.png)](./media/Worker-position-history.png)

