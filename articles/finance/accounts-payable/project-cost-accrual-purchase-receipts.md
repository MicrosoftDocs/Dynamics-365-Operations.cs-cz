---
title: Časové rozlišení nákladů projektu na nákupních příjemkách
description: Tento článek popisuje, jak lze sledovat časově rozlišené náklady na projekt z nákupních příjemek v aplikaci Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a138fd41269fad2e9ac489664ca81c3ee12f830d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856850"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Časové rozlišení nákladů projektu na nákupních příjemkách

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak lze sledovat časově rozlišené náklady na projekt z nákupních příjemek v aplikaci Microsoft Dynamics 365 Finance. 

Faktury pro projekt často přicházejí později než zboží a služby, což může mít významný dopad na projekt klíčové ukazatele výkonu (KPI). Je důležité, aby bylo možné sledovat tyto transakce ve finančních i projektových sestavách.

Ilustruje to následující vzorový scénář. 

Společnost Contoso Consulting zahájila nový projekt nasazení do cloudu. Je vytvořena nákupní objednávka pro nákup počítače pro projekt. Počítač bude stát 1 500 USD a instalační služba 150 USD. Dodavatel má dodat a nainstalovat počítač, ale fakturu ještě nedošla do společnosti Contoso Consulting. Vedoucí projektu by chtěl vidět poměrné rozložení nákladů na 1650 USD před dodáním faktury. Tyto náklady by se projevily také ve finančních výkazech společnosti ke konci měsíce. 

Časově rozlišené náklady musí být zaznamenány na finanční úrovni i na úrovni projektu pro účely vykazování. V aplikaci Finance and Operations lze sledovat finanční aktualizaci příjemky produktu pro kategorie zboží a zakázek. 

U zboží na stránce **Parametry závazků** vyberte možnost **Zaúčtování příjemky produktu do knihy**.
[![Stránka Parametry závazků.](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Pro kategorie zásobování na stránce **Pravidlo zásad kategorie** vyberte zásady **Zásobování** a potom vyberte **Časově rozlišený nákupní výdaj na příjemce** pro každou kategorii zásobování.
[![Stránka Pravidlo zásad kategorie.](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Účty **Nákupní výdaj nefakturovaný** a **Časově rozlišený nákup** v **nastavení účtování** budou použity k zaúčtování dokladů, které jsou spojené s touto příjemkou produktu

Pomocí stejného scénáře se podíváme na to, jaký vliv bude mít zaúčtování příjemky produktu na hlavní knihu a informace o projektu. 

**Krok 1:** Vytvořte a potvrďte novou nákupní objednávku pro projekt k zaznamenání nákupu počítače za 1500 USD a instalační služby za 150 USD.
[![Vytvoření nové nákupní objednávky.](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Při potvrzení nákupní objednávky jsou pro projekt vytvořeny transakce pro potvrzené náklady. 
[![Vytvořené transakce.](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Transakce pro potvrzené náklady bude mít v poli **Původ transakce** nastavenou hodnotu **Nákupní objednávka**. Vytvoření a potvrzení nákupní objednávky nevytváří transakce pro projekt. 

**Krok 2:** Doručení zboží a služeb proběhne a je registrována příjemka produktu. 

Zaúčtování příjemky produktu bude generovat a zaúčtuje doklad do hlavní knihy. Doklad bude připsán na stranu nákupních výdajů, nefakturovaného účtu a poměrně rozloženého účtu nákupního kreditu. 
[![Transakce dokladu.](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Zaúčtování příjemky produktu bude používat nastavení účtování pro kategorie zásobování a produkty a nikoli nastavení účtování pro kategorie projektu. Aby se správně projevil finanční dopad na časově rozlišený nákup, je nutné toto nastavení vyrovnat. 

Je možné mapovat kategorie zásobování na kategorie projektu na stránce **Kategorie zásobování**.
[![Stránka Kategorie zásobování.](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Krok 3:** Vytvořte standardní fakturu dodavatele. 

Zaúčtování příjemky produktu nemá vliv na informace o projektu. Tento problém odstraníte vygenerováním návrhu faktury dodavatele přímo po zaúčtování nákupní příjemky. Přejděte na stránku **Nákupní objednávka** &gt; **karta Faktura** &gt; **Generovat** &gt; **Faktura**. Tím se vytvoří dokument čekající faktury, který aktualizuje informace o projektu. 

Vytvoření návrhu faktury dodavatele bude generovat čekající transakce projektu. 
[![Čekající transakce projektu.](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Na stránce **Potvrzené náklady** se záznamy vytvořené v kroku 1 uzavřou a nové záznamy budou vytvořeny tak, aby odrážely náklady závazků pocházející z nevyřízené faktury dodavatele. Pole **Původ transakce** pro potvrzené náklady bude nastaveno na hodnotu **faktura dodavatele**.
[![Stránka Potvrzené náklady.](./media/accruals9-1024x200.png)](./media/accruals9.png)

Faktura dodavatele zůstane v nevyřízeném stavu, dokud nepřijde skutečná dodavatelská faktura.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
