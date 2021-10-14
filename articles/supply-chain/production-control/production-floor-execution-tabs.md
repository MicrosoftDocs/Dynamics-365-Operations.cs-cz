---
title: Návrh rozhraní pro provádění výrobního provozu
description: Toto téma popisuje, jak navrhnout obsah uživatelského rozhraní pro každou konfiguraci.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 6752d79a71a673fedb0caff7b6ad1023093269c0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570170"
---
# <a name="design-the-production-floor-execution-interface"></a>Návrh rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Můžete navrhnout obsah uživatelského rozhraní pro každou konfiguraci používanou rozhraním pro provádění výrobního provozu. Například pracovníci v jedné pracovní buňce možná budou muset být schopni otevřít pracovní pokyny ve výrobním provozu, zatímco v jiné pracovní buňce nejsou pokyny potřeba. V takovém případě by měly být vytvořeny dvě konfigurace, jedna s tlačítkem pro otevírání příloh dokumentů a druhá bez tohoto tlačítka.

## <a name="design-a-tab"></a>Návrh karty

Na stránce **Konfigurace provádění výrobního provozu** můžete vytvářet a konfigurovat karty výběrem **Návrh karet** v podokně akcí.

Každá karta je rozdělena do čtyř částí, jak je znázorněno na následujícím obrázku.

![Rozložení karty.](media/pfe-tab-layout.png "Rozložení karty")

Na obrázku jsou zobrazeny následující prvky:

1. Primární panel nástrojů
1. Sekundární panel nástrojů
1. Hlavní zobrazení
1. Podrobné zobrazení

Chcete-li vytvořit a konfigurovat novou kartu, postupujte dle těchto kroků:

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**.

1. Vyberte **Návrh karet** na panelu akcí a otevřete stránku **Návrh karet**.

    ![Stránka Návrh karet.](media/pfe-design-tabs.png "Stránka Návrh karet")

1. V podokně akcí zvolte **Nový**.

1. V záhlaví stránky proveďte následující nastavení:

    - **Název karty** - Zadejte název karty.
    - **Hlavní zobrazení** - Vyberte mezi dvěma předdefinovanými seznamy úloh (*Aktivní úlohy*, *Všechny úlohy* nebo *Můj počítač*).
    - **Zobrazení podrobností** - Vyberte mezi prázdnou hodnotou nebo **Podrobnosti o úloze**. Pokud vyberete prázdnou hodnotu, na kartě nebude žádné podrobné zobrazení. Pokud vyberete **Podrobnosti o úloze**, podrobné zobrazení bude obsahovat podrobný popis úlohy vybrané v seznamu úloh v hlavním zobrazení.

1. V části **Primární panel nástrojů** vyberte, která tlačítka by měla být k dispozici na primárním panelu nástrojů. Sloupec **Dostupné akce** zobrazuje seznam všech tlačítek, která lze přidat. Sloupec **Vybrané akce** zobrazuje seznam všech tlačítek, která jsou součástí aktuální konfigurace. Pomocí tlačítek mezi sloupci můžete podle potřeby přesouvat vybrané položky mezi sloupci. Použijte tlačítka nahoru a dolů vedle sloupce **Vybrané akce** pro ovládání pořadí, v jakém jsou tlačítka zobrazena v uživatelském rozhraní.

1. V části **Sekundární** **panel nástrojů** vyberte, která tlačítka by měla být k dispozici na sekundárním panelu nástrojů. Sloupec **Dostupné akce** zobrazuje seznam všech tlačítek, která lze přidat. Sloupec **Vybrané akce** zobrazuje seznam všech tlačítek, která jsou součástí aktuální konfigurace. Pomocí tlačítek mezi sloupci můžete podle potřeby přesouvat vybrané položky mezi sloupci. Použijte tlačítka nahoru a dolů vedle sloupce **Vybrané akce** pro ovládání pořadí, v jakém jsou tlačítka zobrazena v uživatelském rozhraní.

## <a name="associate-a-tab-with-a-configuration"></a>Přiřazení karty ke konfiguraci

Poté, co jste navrhli všechny karty, které potřebujete, můžete je přidružit ke konfiguraci.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**.

    ![Konfigurovat provedení výrobního provozu.](media/pfe-config-prod-floor-execution.png "Konfigurovat provedení výrobního provozu")

1. Na záložce s náhledem **Volba karty** vyberte **Přidat**.

1. Do mřížky je přidán nový řádek. U tohoto nového řádku vyberte název karty, kterou chcete přidat do konfigurace.

1. Podle potřeby pokračujte v přidávání dalších karet.

1. Použijte tlačítka **Nahoru** a **Dolů** na panelu nástrojů a uspořádejte karty podle potřeby. Karty se budou zobrazovat zleva doprava v pořadí uvedeném na výše uvedeném snímku obrazovky (karta nahoře je zobrazena vlevo).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]