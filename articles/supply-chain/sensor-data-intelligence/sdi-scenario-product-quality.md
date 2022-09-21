---
title: Scénář kvality produktu
description: Tento článek obsahuje informace o scénáři kvality produktu. Tento scénář používá senzor k měření kvality šarže produktu a generuje výstrahu, pokud měření překročí definovanou prahovou hodnotu.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 8c4808ea3a0389c2a8699f0e11ea154705a6916d
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428312"
---
# <a name="the-product-quality-scenario"></a>Scénář kvality produktu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Ve scénáři *kvalita produktu* se nastaví senzor pro měření kvality produktové šarže v dílně. Pokud měření spadá mimo definovanou prahovou hodnotu pro produkt, na řídicím panelu se zobrazí upozornění. Senzor například měří vlhkost potravinářského produktu, který vychází z výrobní linky. Pokud je měření mimo povolenou minimální nebo maximální hodnotu vlhkosti pro produkt, je vygenerováno upozornění.

## <a name="scenario-dependencies"></a>Závislosti scénáře

Scénář *Kvalita produktu* má tyto závislosti:

- Aby byla výstraha aktivována, musí být na mapovaném stroji spuštěna výrobní zakázka a stroj musí vyrábět produkt s atributem mapované dávky.
- Signál představující atribut dávky musí být odeslán do služby IoT Hub se zadaným jedinečným názvem vlastnosti.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Příprava ukázkových dat pro scénář kvality produktu

Pokud chcete použít ukázkový systém k testování scénáře *kvalita produktu*, použijte systém, kde jsou [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md) nainstalována, vyberte právnickou osobu *USMF* (společnost) a připravte další ukázková data, jak je popsáno v této části. Pokud používáte vlastní senzory a data, můžete tuto část přeskočit.

V této sekci nastavíte ukázková data, abyste mohli používat vydaný produkt *P0111* (*Kompozitní pouzdro*) se scénářem *kvalita produktu*. V tomto scénáři systém sleduje, zda hodnota atributu dávky měřená senzorem je mimo definovanou prahovou hodnotu pro atribut dávky, který je přidružen k produktu.

### <a name="set-up-a-sensor-simulator"></a>Nastavení simulátoru senzoru

Pokud si chcete tento scénář vyzkoušet bez použití fyzického senzoru, můžete nastavit simulátor pro generování požadovaných signálů. Další informace viz [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Přiřazení atributu dávky a zdroje k produktu P0111

Chcete-li k produktu *P0111* (*Kompozitní pouzdro*) přiřadit atribut dávky, postupujte podle těchto kroků a ověřte, že zdroj *3118* (*Stroj na řezání pěny*) se k tomu používá.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Najděte a vyberte produkt, kde je pole **Číslo položky** nastaveno na *P0111*.
1. Na podokně Akce, na kartě **Správa skladu** ve skupině **Atributy dávky** vyberte tlačítko **Specifika produktu**.
1. Na stránce **Specifika produktu** vyberte **Nový** k vytvoření atributu šarže specifického pro produkt.
1. V záhlaví nastavte následující pole:

    - **Kód atributu** – Vyberte rozsah atributů, které budete sledovat (*Tabulka*, *Skupina* nebo *Všechno*). Pro tento scénář vyberte *Tabulka*, protože budete vždy sledovat jeden atribut.
    - **Vztah atributu** – Vyberte atribut, jehož hodnotu budete pomocí scénáře *kvalita produktu* monitorovat. Pro tento příklad vyberte *Koncentrace*, což je atribut, který je součástí standardních ukázkových dat.

1. Na pevné záložce **Hodnoty** v polích **Minimum** a **Maximum** definujte rozsah přijatelných hodnot, které musí atribut hlásit, aby prošel kontrolou kvality. Pokud senzor hlásí hodnotu mimo tento rozsah, systém to identifikuje jako porušení kvality. Ostatní pole na této pevné záložce nejsou pro scénář *kvalita produktu* relevantní. Výchozí hodnoty, které aktuálně vidíte, pocházejí z ukázkových dat. Proto je nechte tak, jak jsou, a zavřete stránku **Specifika produktu** pro návrat na stránku **Zveřejněné údaje o produktu** pro položku *P0111*.
1. V podokně akcí na kartě **Analyzovat** ve skupině **Zobrazit** zvolte **Trasa**.
1. Na stránce **Trasa** stránce, na kartě **Přehled** ve spodní části stránky vyberte řádek, na kterém je pole **Č. oper.** nastaveno na *30*.
1. Na kartě **Požadavky na zdroje** ve spodní části stránky zkontrolujte, že zdroj *3118* (*Stroj na řezání pěny*) je přiřazen k operaci.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Vytvoření a uvolnění výrobní zakázky pro produkt P0111

Chcete-li vytvořit a uvolnit výrobní zakázku pro produkt *P0111*, postupujte podle těchto kroků.

1. Přejděte na **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky**.
1. Na stránce **Všechny výrobní objednávky** v podokně Akce vyberte **Nová dávková objednávka**.
1. V dialogovém okně **Vytvořit dávku** nastavte následující hodnoty:

    - **Číslo položky:** *P0111*
    - **Množství:** *10*

1. Vyberte **Vytvořit** pro vytvoření zakázky a přejdete zpět na stránku **Všechny výrobní zakázky**.
1. Použijte pole **Filtr** pro vyhledávání výrobních zakázek, kde je pole **Číslo položky** nastaveno na *P0111*. Poté najděte a vyberte výrobní zakázku, kterou jste právě vytvořili.
1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Odhad**.
1. V dialogovém okně **Odhad** vyberte **OK** a spusťte odhad.
1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Uvolnit**.
1. V dialogovém okně **Uvolnit** si poznamenejte číslo dávkového příkazu, který jste právě vytvořili.
1. Výběrem **OK** objednávku uvolníte.

### <a name="configure-the-production-floor-execution-interface"></a>Konfigurace rozhraní pro provádění výrobního provozu

Pokud jste tak ještě neučinili, nakonfigurujte rozhraní provádění produkční dílny tak, aby zobrazovalo úlohy, které jsou přiřazeny ke zdroji *3118* (*Stroj na řezání pěny*). Pokyny naleznete v následujících částech:

- [Konfigurace rozhraní pro provádění výrobního provozu](sdi-scenario-equipment-downtime.md#config-pfe)
- [Aktivace možnosti hledání pro rozhraní ke spuštění výrobního provozu](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Spuštění první úlohy v dávkovém příkazu

Chcete-li zahájit první úlohu v dávkovém pořadí, postupujte podle těchto kroků.

1. Přejděte do nabídky **Řízení výroby \> Provádění výroby \> Provádění výrobního provozu**.
1. V poli **ID oznámení** zadejte *123*. Pak vyberte **Přihlásit se**.
1. Pokud se zobrazí výzva k zadání důvodu nepřítomnosti, vyberte jednu z karet nepřítomnosti a poté vyberte **OK**.
1. Do pole **Vyhledávání** zadejte číslo dávkového příkazu, které jste si předtím poznamenali. Poté vyberte klíč **Vrátit**.
1. Vyberte objednávku a poté vyberte **Spustit úlohu**.
1. V dialogovém okně **Spustit úlohu** vyberte **Spustit**.

## <a name="set-up-the-product-quality-scenario"></a>Nastavení scénáře kvality produktu

Chcete-li nastavit scénář *kvality produktu* v Supply Chain Management, postupujte takto.

1. Přejděte na **Řízení výroby \> Nastavení \> Sensor Data Intelligence \> Scénáře**.
1. V poli scénáře **Kvalita produktu** vyberte **Konfigurovat** a otevřete průvodce nastavením pro tento scénář.
1. Na stránce **Senzory** přidejte senzor do mřížky výběrem možnosti **Nový**. Poté pro něj nastavte následující pole:

    - **ID senzoru** – Zadejte ID senzoru, který používáte. (Pokud používáte Raspberry PI Azure IoT Online Simulator a nastavili jste ho podle popisu v části [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md), zadejte *Kvalita*.)
    - **Popis senzoru** – zadejte popis senzoru.

1. Opakujte předchozí krok pro každý senzor, který teď chcete přidat. Kdykoli se můžete vrátit a přidat další senzory.
1. Zvolte **Další**.
1. Na stránce **Mapování obchodních záznamů** v části **Senzory** vyberte záznam pro jeden ze senzorů, které jste právě přidali.
1. V části **Mapování obchodního záznamu** vyberte **Nový** pro přidání řádku do mřížky.
1. Na novém řádku by pole **Typ obchodního záznamu** mělo být automaticky nastaveno na *Resources(WrkCtrTable)*. Nastavte pole **Obchodní záznam** na zdroj, který používáte ke sledování vybraného senzoru. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, nastavte ho na *3118, Stroj na řezání pěny*.)
1. Ihned poté, co vyberete typ obchodního záznamu pro řádek, který jste přidali v předchozím kroku, se do mřížky automaticky přidá druhý řádek. Na tomto řádku je třeba pole **Typ obchodního záznamu** nastavit na *Batch attributes(PdsBatchAttrib)*. Nastavte pole **Obchodní záznam** na atribut dávky, který používáte ke sledování vybraného senzoru. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, nastavte ho na *Koncentrace, procento koncentrace*.)
1. Zvolte **Další**.
1. Na stránce **Aktivovat senzory** v mřížce vyberte senzor, který jste přidali, a poté vyberte **Aktivovat**. Pro každý aktivovaný senzor v mřížce se objeví zaškrtnutí ve sloupci **Aktivní**.
1. Vyberte **Dokončit**.

## <a name="work-with-the-product-quality-scenario"></a>Práce se scénářem kvality produktu

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Zobrazení údajů o kvalitě produktu na stránce stavu zdrojů

Na stránce **Stav zdroje** mohou nadřízení sledovat časovou osu signálu kvality produktu, který je přijímán ze senzorů, které jsou mapovány na každý strojový zdroj. Pro nakonfigurování časové osy postupujte takto.

1. Přejděte na **Řízení výroby \> Provádění výroby \> Stav prostředku**.
1. V dialogovém okně **Konfigurovat** nastavte následující pole:

    - **Prostředek** – Vyberte prostředky, které chcete monitorovat. (Pokud pracujete s ukázkovými daty, vyberte *3118*.)
    - **Časová řada 1** – Vyberte záznam (metrický klíč), jehož název má následující formát: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Zobrazovaný název** – Zadejte *Hodnoty dávkového atributu*.

Následující obrázek ukazuje příklad údajů o kvalitě produktu na stránce **Stav zdroje**, když je hodnota v rozsahu přijatelných hodnot.

![Údaje o kvalitě produktu na stránce stavu zdrojů, když je hodnota v rozsahu.](media/sdi-product-quality-in-range.png "Údaje o kvalitě produktu na stránce stavu zdrojů, když je hodnota v rozsahu")

Následující obrázek ukazuje příklad údajů o kvalitě produktu, když je zjištěna hodnota mimo rozsah.

![Údaje o kvalitě produktu na stránce stavu zdrojů, když je zjištěna hodnota mimo rozsah.](media/sdi-product-quality-out-of-range.png "Údaje o kvalitě produktu na stránce stavu zdrojů, když je zjištěna hodnota mimo rozsah")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Zobrazení údajů o kvalitě produktu na stránce Oznámení

Na stránce **Oznámení** mohou nadřízení zobrazit oznámení, která jsou generována, když senzor změří hodnotu atributu dávky, která spadá mimo definovanou prahovou hodnotu pro atribut dávky. Každé oznámení poskytuje přehled o produkční úloze, která je postižena výpadkem, a dává možnost přeřadit postiženou úlohu k jinému zdroji.

K otevření stránky **Oznámení** přejděte na **Řízení výroby \> Dotazy a sestavy \> Sensor Data Intelligence \> Oznámení**.

Následující obrázek znázorňuje příklad stránky s oznámením kvality produktu.

![Příklad oznámení kvality produktu.](media/sdi-product-quality-notification.png "Příklad oznámení kvality produktu")
