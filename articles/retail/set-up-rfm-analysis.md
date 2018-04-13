---
title: "Nastavení analýzy RFM"
description: "Toto téma vysvětluje, jak nastavit analýzu RFM (Recency, Frequency, and Monetary) odběratelů."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: e66208ccceb4c248c2704bb7358d77447e032205
ms.openlocfilehash: c59d12c54563b883ae6d8ea8594f423f02797f4f
ms.contentlocale: cs-cz
ms.lasthandoff: 12/14/2017

---

# <a name="set-up-rfm-analysis"></a>Nastavení analýzy RFM

[!INCLUDE [banner](includes/banner.md)]

Toto téma vysvětluje, jak nastavit analýzu RFM (Recency, Frequency, and Monetary) odběratelů.

Analýza RFM je marketingový nástroj, který vaše organizace může používat k vyhodnocení dat, která je vygenerována nákupy odběratelů. Po nastavení analýzy RFM je odběratelů přiřazeno hodnocení RFM, jak nakupují. Hodnocení RFM může být trojmístné hodnocení nebo celkové číslo v závislosti na konfiguraci analýzy RFM ve vaší organizaci. Zde je princip hodnocení, pokud vaše organizace používá trojmístné hodnocení pro výsledek:

- První číslice je hodnocení aktuálnosti odběratele, což znamená, kdy naposledy odběratel provedl nákup od vaší organizace. 
- Druhá číslice je hodnocení frekvence zákazníka, což znamená, jak často odběratel provádí nákupy od vaší organizace. 
- Třetí číslice je ohodnocení peněžní částky zákazníka, což znamená, kolik odběratel utratí při nákupech od vaší organizace. 

Například vaše organizace má nastavená hodnocení v rozsahu 1 až 5, kde 5 je nejvyšší hodnocení. V tomto případě hodnocení 535 odběratelů informuje následujících informace o zákazníkovi:

-   **Skóre aktuálnosti 5** – zákazník nedávno provedl nákup.
-   **Hodnocení četnosti 3** – odběratel středně často nakupuje produkty od vaší organizace.
-   **Peněžní hodnocení 5** – když zákazník provede nákup, utratí značné množství peněz.

Pokud vaše organizace používá agregaci těchto čísel, individuální hodnocení se sečtou. Například má zákazník ohodnocení 13 (5 + 3 + 5).

## <a name="to-set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Chcete-li nastavit analýzu RFM pro odběratele v dané organizaci.

1.  Přejít na **Kontaktní středisko** > **Periodicky** > **Analýza RFM**.

2.  Na stránce **Analýza RFM** vyberte **Nový**. V poli **Definice RFM** zadejte název definice RFM. Můžete například definici nazvat RFM-A.

3.  Zadejte počáteční a koncové datum pro tuto definici RFM.

4.  Na pevné záložce **Obecné** proveďte následující kroky: 
    - Pokud každý oddíl skóre RFM musí obsahovat stejný počet odběratelů, zaškrtněte políčko **Rovnoměrná distribuce**. 
    - Zaškrtnutím políčka **Přidat hodnocení** budete agregovat tři hodnocení. To dá například odběrateli hodnocení RFM 13 namísto 535. 
    - Zaškrtněte políčko **Uložit historii**, aby systém musela ukládat statistická data pro odběratele, aby bylo data možné použít k výpočtu hodnocení RFM.

5.  Na pevné záložce **Recency** proveďte následující kroky: 
    - Do pole **Divize** zadejte počet divizí nebo skupin, které budou použity pro výpočet skóre recency pro odběratele. Pokud například máte 100 odběratelů, rozdělení po 5 znamená, že pro každé hodnocení je 20 odběratelů. 20 zákazníků, kteří naposledy provedli nákup, mají skóre recency 5. Další 20 zákazníků má skóre recency 4 atd. Pokud máte 50 odběratelů, 10 odběratelů má hodnocení recency 5, 10 má hodnocení recency 4 atd. 
    - V poli **Priorita** vyberte, jakou váhu chcete přiřadit parametru recency ve vztahu k ostatním parametrům při výpočtu hodnocení RFM pro odběratele. Například můžete chtít dát větší hodnotu hodnocení recency než peněžnímu hodnocení. 
    - V poli **Multiplikátor** zadejte hodnotu, kterou se má hodnocení recency násobit. Pokud nezadáte hodnotu, hodnocení nebude vynásobeno. 
    - V poli **Období** vyberte časové období, podle kterého se vypočítá skóre recency. Například podle týdne nebo měsíce.

6.  Na pevné záložce **Frekvence** proveďte následující kroky: 
    - Do pole **Divize** zadejte počet divizí nebo skupin, které budou použity pro výpočet skóre frekvence pro odběratele. 
    - V poli **Priorita** vyberte, jakou váhu chcete přiřadit parametru frekvence ve vztahu k ostatním parametrům při výpočtu hodnocení RFM pro odběratele. 
    - V poli **Multiplikátor** zadejte hodnotu, kterou se má hodnocení frekvence násobit. Pokud nezadáte hodnotu, hodnocení nebude vynásobeno.

7.  Na pevné záložce **Peněžní** proveďte následující kroky: 
    - Do pole **Divize** zadejte počet divizí nebo skupin, které budou použity pro výpočet peněžního skóre pro odběratele. 
    - V poli **Priorita** vyberte, jakou váhu chcete přiřadit peněžnímu parametru ve vztahu k ostatním parametrům při výpočtu hodnocení RFM pro odběratele. 
    - V poli **Multiplikátor** zadejte hodnotu, kterou se má peněžní hodnocení násobit. Pokud nezadáte hodnotu, hodnocení nebude vynásobeno. 
    - V poli **Hrubý/čistý** vyberte, zda má být peněžní hodnocení odběratele vypočteno pomocí hrubé nebo čisté částky faktury. 
    - Pokud mají být vrácené částky odběratele odečteny od výpočtu celkové fakturované částky odběratele, zaškrtněte políčko **Odečíst vrácení**. 

## <a name="view-a-customers-rfm-score"></a>Zobrazení hodnocení RFM odběratele
Tento postup použijte k zobrazení hodnocení RFM odběratele. 

1.  Přejděte na **Kontaktní středisko** > **Deníky** > **Odběratelský servis**. 

2.  Na stránce **Odběratelský servis** v podokně **Odběratelský servis** v polích pro vyhledávání vyberte typ klíčového slova, které chcete hledat, a zadejte text vyhledávání.

3.  Vyberte **Vyhledat**.

4.  Na stránce **Hledat zákazníka** vyberte požadovaný záznam odběratele, a klikněte na tlačítko **Vybrat zákazníka**. 

Hodnocení RFM se zobrazí ve skupině **Historie objednávek** na pravé straně stránky **Odběratelský servis**. 

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Zobrazení nebo vymazání historie záznamu analýzy RFM
Tento postup použijte pro zobrazení nebo vymazání historie záznamu analýzy RFM. 

1.  Přejít na **Kontaktní středisko** > **Periodicky** > **Analýza RFM**.

2.  Na stránce **Analýza RFM** vyberte záznam, který chcete zobrazit.

3.  Pro zobrazení historie záznamů zvolte pevnou záložku **Historie**.

4.  Chcete-li vymazat historii záznamu, zvolte **Vymazat historii**.

