---
title: Zobrazení oznámení objednávek v pokladním místě (POS)
description: Toto téma popisuje postup povolení oznámení objednávek v pokladním místě a architekturu oznámení.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57f5d23533c2fd17593648a15745fa770fc01dc4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345201"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Zobrazení oznámení objednávek v pokladním místě (POS)

[!include [banner](includes/banner.md)]

Spolupracovníkům obchodu mohou být přiděleny různé úkoly v jejich obchodě, například plnění objednávek nebo provádění příjmu zásob nebo počítání zásob. Klient pokladního místa poskytuje aplikaci, kde mohou zaměstnanci být upozorňováni na tyto úkoly. Architektura oznámení v POS pomáhá tak, že maloobchodní prodejci mohou nakonfigurovat oznámení na základě rolí. Od Dynamics 365 Retail s aktualizací 5 lze tato oznámení nakonfigurovat pouze POS operace.

Systém může zobrazit oznámení pro operaci *vyřízení objednávky* a počínaje verzí Commerce 10.0.18 lze také zobrazit oznámení pro operaci *zrušit objednávku*. Protože je však architektura navržena jako rozšiřitelná, vývojáři mohou napsat obslužné [rutiny oznámení](dev-itpro/extend-pos-notification.md) pro veškeré operace a zobrazit oznámení pro danou operaci v POS.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Povolení oznámení pro operace plnění objednávky nebo zrušení objednávky

Chcete-li povolit oznámení pro operace plnění objednávky nebo zrušení objednávky, postupujte podle následujících kroků.

1. Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Operace**.
1. Vyhledejte operaci **Plnění objednávky** nebo **Zrušení objednávky** a vyberte zaškrtávací políčko **Povolit oznámení** pro operaci k určení, že architektura oznámení musí pro tuto operaci naslouchat obslužné rutině. Pokud je obslužná rutina implementována, oznámení pro tuto operaci se zobrazí v POS.
1. Přejděte na **Retail a Commerce \> Zaměstnanci \> Pracovníci**.
1. Vyberte kartu **Commerce** kartu, vyberte řádek pracovníka a poté vyberte **Oprávnění POS**. Vyberte kartu s náhledem **Oznámení**, rozbalte ji a poté přidejte operace, pro které jste povolili oznámení. Pokud konfigurujete jedno oznámení pro pracovníka, ujistěte se, že je hodnota **Zobrazit objednávku** nastavena na **1**. Pokud konfigurujete více než jednu operaci, nastavte hodnoty **Zobrazit objednávku**, aby označovaly pořadí, ve kterém by se oznámení měla zobrazovat. 

      Oznámení se zobrazují pouze pro operace, které jsou přidány na kartu s náhledem **Oznámení**. Můžete tam přidat operace, pouze pokud byla zaškrtnuta políčka **Povolit oznámení** pro tyto operace na stránce **POS operace**. Kromě toho oznámení pro operaci se zobrazuje pracovníkům pouze v případě, že operace je přidána do oprávnění POS pro tyto pracovníky.

    > [!NOTE]
    > Oznámení mohou být přepsána na úrovni uživatele. To uděláte tak, že otevřete záznam pracovníka, vyberete **Oprávnění POS** a poté upravíte uživatelský odběr oznámení.

1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. V poli **Interval oznámení** upřesněte, jak často mají být oznámení odesílána. U některých oznámení musí POS provádět volání v reálném čase do administrativní aplikace. Tato volání spotřebovávají výpočetní kapacitu administrativní aplikace. Proto při nastavení intervalu oznámení zvažte své obchodní požadavky a dopad volání administrativní aplikace v reálném čase. Hodnota **0** (nula) vypne oznámení.
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**. Vyberte plán **1060** (**Zaměstnanci**) za účelem synchronizace nastavení odběru oznámení a poté zvolte na **Spustit**. Dále vyberte plán **1070** (**Konfigurace kanálu**) pro synchronizaci intervalu oprávnění a poté zvolte na **Spustit**.

## <a name="view-notifications-in-the-pos"></a>Zobrazení oznámení v POS

Po dokončení předchozích kroků budou moci pracovníci zobrazit oznámení v POS. Chcete-li zobrazit oznámení, vyberte ikonu oznámení v pravém horním rohu POS. Zobrazí se oznamovací panel a zobrazí oznámení o operacích nakonfigurovaných pro pracovníka. 

Pro operace **plnění objednávky** panel oznámení zobrazí následující skupiny.

- **Vyzvednutí v obchodě** – Tato skupina zobrazí jednotlivé řádky objednávky, které jsou naplánovány k výdeji z aktuálního obchodu. Můžete vybrat číslo ve skupině a otevřít operaci **Plnění objednávky** s filtrem tak, že zobrazuje pouze aktivní řádky objednávky, které jsou nastaveny pro vyzvednutí z aktuálního obchodu.
- **Odeslat z obchodu** – Tato skupina zobrazuje počet jednotlivých řádků objednávky, které byly nakonfigurovány k odeslání z aktuálního obchodu uživatele. Můžete vybrat číslo ve skupině a otevřít operaci **Plnění objednávky** s filtrovaným pohledem tak, že se zobrazují pouze aktivní řádky objednávky, které jsou nastaveny pro odeslání z aktuálního obchodu.

Pro operaci **zrušit objednávky** panel oznámení zobrazí následující skupiny.

- **Objednávky k plnění** – Tato skupina zobrazuje počet objednávek, které jsou nakonfigurovány pro vyzvednutí nebo odeslání pro aktuální obchod uživatele. Můžete vybrat číslo ve skupině a otevřít operaci **Zrušení objednávky** operace s filtrovaným pohledem, který zobrazuje pouze otevřené objednávky, které musí plnit aktuální obchod uživatele pro scénáře vyzvednutí v obchodě nebo odeslání ze skladu.
- **Objednávky k vyzvednutí** – Tato skupina zobrazí počet objednávek, které jsou naplánovány k výdeji z aktuálního obchodu. Můžete vybrat číslo ve skupině a otevřít operaci **Zrušení objednávky** operace s filtrovaným pohledem, který zobrazuje pouze otevřené objednávky, které musí plnit aktuální obchod uživatele pro scénáře vyzvednutí v aktuálním obchodě.
- **Objednávky k odeslání** – Tato skupina zobrazuje počet objednávek, které mají být odeslány z aktuálního obchodu uživatele. Můžete vybrat číslo ve skupině a otevřít operaci **Zrušení objednávky** operace s filtrovaným pohledem, který zobrazuje pouze otevřené objednávky, které musí plnit aktuální obchod uživatele pro scénáře odeslání z aktuálního obchodu.

U oznámení o plnění objednávky i zrušení objednívky se při zpracování objednávek procesem změní ikona oznámení za účelem označení, že existují nová oznámení a počet odpovídajících skupin je aktualizován. I když jsou skupiny obnovovány v pravidelných intervalech, mohou uživatelé POS ručně aktualizovat skupiny kdykoliv pomocí tlačítka **Obnovit** vedle dané skupiny. Pokud má skupina novou položku, kterou aktuální pracovník nezobrazil, pak skupina zobrazuje symbol výbuchu, který označuje nový obsah.

## <a name="enable-live-content-on-pos-buttons"></a>Povolení aktivního obsahu na tlačítkách POS

Tlačítka POS mohou nyní zobrazit počet, což pracovníkům usnadňuje určit úkoly, které vyžadují jejich okamžitou pozornost. Chcete-li zobrazit toto číslo na POS tlačítku, je nutné dokončit nastavení oznámení popsané dříve v tomto tématu (musíte povolit oznámení pro operaci, nastavit interval upozornění a aktualizovat skupinu oprávnění POS pro daného pracovníka). Dále musíte otevřít návrháře mřížky tlačítek, zobrazit vlastnosti tlačítka a vybrat zaškrtávací políčko **Povolit aktivní obsah**. V poli **Zarovnání obsahu** můžete určit, zda se počet zobrazí v pravém horním rohu tlačítka (**Vpravo nahoře**) nebo uprostřed (**Na střed**).

> [!NOTE]
> Aktivní obsah lze povolit pro operace pouze v případě, kdy je zaškrtnuto políčko **Povolit oznámení** na stránce **Operace POS**, jak bylo popsáno dříve v tomto tématu.

Následující obrázek znázorňuje nastavení aktivního obsahu v návrháři mřížky tlačítek.

![Nastavení živého obsahu v Návrháři mřížky tlačítek.](./media/ButtonGridDesigner.png "Nastavení živého obsahu v Návrháři mřížky tlačítek")

Chcete-li zobrazit počet oznámení na tlačítku, je nutné zajistit, aby bylo aktualizováno správné rozvržení obrazovky. Chcete-li určit rozvržení obrazovky, které používá POS, vyberte ikonu **Nastavení** v pravém horním rohu a poznamenejte si **ID rozvržení obrazovky** a **Rozlišení rozvržení**. Nyní pomocí prohlížeče Edge přejděte na stránku **Rozvržení obrazovky**, najděte výše uvedené **ID rozvržení obrazovky** a **Rozlišení rozvržení** a zaškrtněte políčko **Povolit živý obsah**. Přejděte na **Maloobchod a velkoobchod \> IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu 1090 (Registry) pro synchronizaci změn rozvržení.

![Najít rozvržení obrazovky použité POS.](./media/Choose_screen_layout.png "Vyhledání rozložení obrazovky")

Následující obrázek znázorňuje účinek výběru **Vpravo nahoře** oproti možnosti **Na střed** v poli **Zarovnání obsahu** pro tlačítka různých velikostí.

![Aktivní obsah na tlačítkách POS.](./media/ButtonsWithLiveContent.png "Aktivní obsah na tlačítkách POS")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
