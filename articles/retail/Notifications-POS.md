---
title: "Zobrazení oznámení objednávek v pokladním místě (POS)"
description: "Toto téma popisuje postup povolení oznámení objednávek v pokladním místě a architekturu oznámení. Vývojáři budou moci rozšířit tato oznámení na operace kromě operací plnění objednávky."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41f16d13051f6095bdb04af1586ec06fe0ce93f6
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Zobrazení oznámení objednávek v pokladním místě (POS)

[!include [banner](includes/banner.md)]

V moderním prostředí maloobchodu jsou zaměstnancům obchodu přiřazovány různé úkoly, jako je pomoc zákazníkům, zadávání transakcí, provádění inventur a přijímání objednávek v obchodě. Klient pokladního místa poskytuje aplikaci, kde mohou zaměstnanci provádět provádět všechny tyto úlohy a mnohé další. Protože během dne je třeba provést různé úlohy, může být pro zaměstnance nutné dostávat oznámení, pokud cokoliv vyžaduje jejich pozornost. Architektura oznámení v POS pomáhá tak, že maloobchodní prodejci mohou nakonfigurovat oznámení na základě rolí. U aplikace Dynamics 365 for Retail s aktualizací Application update 5 lze tato oznámení konfigurovat pouze pro POS operace.

V současné době systém může zobrazit upozornění pouze pro operace plnění objednávky. Protože je však architektura navržena jako rozšiřitelná, vývojáři případně budou moci napsat obslužné rutiny oznámení pro veškeré operace a zobrazit oznámení pro danou operaci v POS.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Povolení oznámení pro operace plnění objednávky

Chcete-li povolit oznámení pro operace plnění objednávky, postupujte podle těchto kroků.

1. Přejděte do nabídky **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Operace**.
2. Vyhledejte operaci **Plnění objednávky** a vyberte zaškrtávací políčko **Povolit oznámení** k určení, že architektura oznámení musí pro tuto operaci naslouchat obslužné rutině. Pokud je obslužná rutina implementována, oznámení pro tuto operaci se zobrazí v POS.
3. Přejděte na **Maloobchod** &gt; **Zaměstnanci** &gt; **Pracovníci** &gt; a na kartě Maloobchod otevřete oprávnění POS přidružená k praovníkovi. Rozbalte pevnou záložku **Oznámení**, přidejte operaci **Plnění objednávky** a nastavte pole **Pořadí zobrazení** na **1**. Pokud je nakonfigurováno více než jedno oznámení, toto pole se používá k uspořádání oznámení. Oznámení, která mají nižší hodnotu **Pořadí zobrazení** se zobrazí nad oznámeními, která mají hodnotu vyšší. Oznámení, která mají hodnotu **Pořadí zobrazení** **1**, jsou nahoře.

    Upozornění se zobrazí pouze pro operace, které budou přidány na pevné záložce **Oznámení**, a můžete tam přidat pouze operace, pro které bylo na stránce **Operace POS** zaškrtnuto políčko **Povolit oznámení**. Kromě toho oznámení pro operaci se zobrazuje pracovníkům pouze v případě, že operace je přidána do oprávnění POS pro tyto pracovníky.

    > [!NOTE]
    > Oznámení mohou být přepsána na úrovni uživatele. Otevřít záznam pracovníka, vyberte **Oprávnění POS** a poté upravte uživatelský odběr oznámení.

4. Přejděte na **Maloobchod** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Funkční profily**. V poli **Interval oznámení** upřesněte, jak často mají být oznámení odesílána. U některých oznámení musí POS provádět volání v reálném čase do administrativní aplikace. Tato volání spotřebovávají výpočetní kapacitu administrativní aplikace. Proto při nastavení intervalu oznámení zvažte své obchodní požadavky a dopad volání administrativní aplikace v reálném čase. Hodnota **0** (nula) vypne oznámení.
5. Přejděte do nabídky **Maloobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**. Vyberte plán **1060** (**Zaměstnanci**) za účelem synchronizace nastavení odběru oznámení a poté zvolte na **Spustit**. Dále vyberte plán **1070** (**Konfigurace kanálu**) pro synchronizaci intervalu oprávnění a poté zvolte na **Spustit**.

## <a name="view-notifications-in-the-pos"></a>Zobrazení oznámení v POS

Po dokončení předchozích kroků budou moci pracovníci zobrazit oznámení v POS. Chcete-li zobrazit oznámení, klikněte na ikonu oznámení v pravém horním rohu POS. Zobrazí se centrum oznámení s oznámeními pro operaci plnění objednávky. Centrum oznámení má zobrazit následující skupiny v rámci operace plnění objednávky:

- **Vyzvednutí v obchodě** -Tato skupina zobrazí počet objednávek, které mají způsob dodání **Výdej** a jsou naplánovány k výdeji z aktuálního obchodu. Můžete stisknout číslo ve skupině pro otevření stránky **Plnění objednávky**. V tomto případě stránka bude filtrována tak, aby se zobrazily pouze aktivní objednávky, které jsou nastaveny pro výdej v aktuálním obchodě.
- **Expedovat z obchodu** -Tato skupina zobrazí počet objednávek, které mají způsob dodání **Expedice** a expedice je naplánována z aktuálního obchodu. Můžete stisknout číslo ve skupině pro otevření stránky **Plnění objednávky**. V tomto případě stránka bude filtrována tak, aby se zobrazily pouze aktivní objednávky, které jsou nastaveny pro expedici z aktuálního obchodu.

Pokud jsou nové objednávky přiřazené k obchodu pro plnění, změní se ikona oznámení za účelem označení, že existují nová oznámení a počet odpovídajících skupin je aktualizován. I když jsou skupiny obnovovány v pravidelných intervalech, mohou uživatelé POS ručně aktualizovat skupiny kdykoliv pomocí tlačítka **Obnovit** vedle dané skupiny. Pokud má skupina novou položku, kterou aktuální pracovník nezobrazil, pak skupina zobrazuje symbol výbuchu, který označuje nový obsah.

## <a name="enable-live-content-on-pos-buttons"></a>Povolení aktivního obsahu na tlačítkách POS

Tlačítka POS mohou nyní zobrazit počet, což pracovníkům usnadňuje určit úkoly, které vyžadují jejich okamžitou pozornost. Chcete-li zobrazit toto číslo na POS tlačítku, je nutné dokončit nastavení oznámení popsané dříve v tomto tématu (musíte povolit oznámení pro operaci, nastavit interval upozornění a aktualizovat skupinu oprávnění POS pro daného pracovníka). Dále musíte otevřít návrháře mřížky tlačítek, zobrazit vlastnosti tlačítka a vybrat zaškrtávací políčko **Povolit aktivní obsah**. V poli **Zarovnání obsahu** můžete určit, zda se počet zobrazí v pravém horním rohu tlačítka (**Vpravo nahoře**) nebo uprostřed (**Na střed**).

> [!NOTE]
> Aktivní obsah lze povolit pro operace pouze v případě, kdy je zaškrtnuto políčko **Povolit oznámení** na stránce **Operace POS**, jak bylo popsáno dříve v tomto tématu.

Následující obrázek znázorňuje nastavení aktivního obsahu v návrháři mřížky tlačítek.

![Nastavení aktivního obsahu v návrháři mřížky tlačítek](./media/ButtonGridDesigner.png "Nastavení aktivního obsahu v návrháři mřížky tlačítek")

Následující obrázek znázorňuje účinek výběru **Vpravo nahoře** oproti možnosti **Na střed** v poli **Zarovnání obsahu** pro tlačítka různých velikostí.

![Aktivní obsah na tlačítkách POS](./media/ButtonsWithLiveContent.png "Aktivní obsah na tlačítkách POS")

