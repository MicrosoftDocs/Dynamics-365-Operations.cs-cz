---
title: Scénář zpoždění výroby
description: Tento článek popisuje scénář zpoždění výroby, který generuje oznámení, pokud výrobní kapacita klesne pod zadanou mezní hodnotu.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 073762581d84646ba12b570e57327b7cab8efd3b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428311"
---
# <a name="the-production-delays-scenario"></a>Scénář zpoždění výroby

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Scénář *zpoždění výroby* generuje oznámení, pokud výrobní kapacita klesne pod zadanou mezní hodnotu. V tomto scénáři je signál *part-out* odeslán do služby Microsoft Azure IoT Hub pro každou vyrobenou položku. V aplikaci Dynamics 365 Supply Chain Management se zpoždění objednávky počítá na základě doby, po kterou je naplánováno spuštění výrobní zakázky, počtu položek, které by měly být vyrobeny, doby, po kterou byla úloha spuštěna, a počtu signálů *part-out*, které byly přijaty. Oznámení o zpoždění je generováno, pokud by počet signálů *part-out* klesl pod prahovou hodnotu.

## <a name="scenario-dependencies"></a>Závislosti scénáře

Scénář *zpoždění výroby* má tyto závislosti:

- Výstraha může být aktivována, pouze pokud je na mapovaném stroji spuštěna výrobní zakázka.
- Signál představující signál *part-out* mapovaného stroje musí být odeslán do centra IoT se zadaným jedinečným názvem vlastnosti.
- Vlastnost časového razítka UNIX, kde je hodnota vyjádřena v milisekundách (ms), musí být zahrnuta ve zprávě Azure IoT Hub.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Příprava ukázkových dat pro scénář zpoždění výroby

Pokud chcete použít ukázkový systém k testování scénáře *zpoždění výroby*, použijte systém, kde jsou [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md) nainstalována, vyberte právnickou osobu *USMF* (společnost) a připravte další ukázková data, jak je popsáno v této části. Pokud používáte vlastní senzory a data, můžete tuto část přeskočit.

### <a name="set-up-sensor-simulator"></a>Nastavení simulátoru senzoru

Pokud si chcete tento scénář vyzkoušet bez použití fyzického senzoru, můžete nastavit simulátor pro generování požadovaných signálů. Další informace viz [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Ověřte, zda je pro produkt P0111 použit prostředek 3118

Bude naplánována a uvolněna výrobní zakázka. Proto je produkční úloha uvolněna do zdroje *3118* (*Stroj na řezání pěny*). K ověření, že se prostředek *3118* používá pro produkt *P0111* ve vašich ukázkových datech, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Najděte a vyberte produkt, kde je pole **Číslo položky** nastaveno na *P0111*.
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

## <a name="set-up-the-production-delays-scenario"></a>Nastavení scénáře zpoždění výroby

Chcete-li nastavit scénář *zpoždění výroby* v Supply Chain Management, postupujte takto.

1. Přejděte na **Řízení výroby \> Nastavení \> Sensor Data Intelligence \> Scénáře**.
1. V poli scénáře **Zpoždění výroby** vyberte **Konfigurovat** a otevřete průvodce nastavením pro tento scénář.
1. Na stránce **Senzory** přidejte senzor do mřížky výběrem možnosti **Nový**. Poté pro něj nastavte následující pole:

    - **ID senzoru** – Zadejte ID senzoru, který používáte. (Pokud používáte Raspberry PI Azure IoT Online Simulator a nastavili jste ho podle popisu v části [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md), zadejte *ProductionDelay*.)
    - **Popis senzoru** – zadejte popis senzoru.

1. Opakujte předchozí krok pro každý senzor, který teď chcete přidat. Kdykoli se můžete vrátit a přidat další senzory.
1. Zvolte **Další**.
1. Na stránce **Mapování obchodních záznamů** v části **Senzory** vyberte záznam pro jeden ze senzorů, které jste právě přidali.
1. V části **Mapování obchodního záznamu** vyberte **Nový** pro přidání řádku do mřížky.
1. Na novém řádku nastavte **Obchodní záznam** na zdroj, který používáte ke sledování vybraného senzoru. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, nastavte ho na *3118, Stroj na řezání pěny*.)
1. Zvolte **Další**.
1. Na stránce **Mezné hodnota odchylky zpoždění výroby**, pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, postupujte takto:

    1. Vyberte záhlaví sloupce **Vztah položky** pro otevření rozevíracího dialogového okna, které obsahuje vyhledávací filtry pro daný sloupec. Zadejte do vyhledávacího pole *P0111* a poté vyberte **Použít**.
    2. Vyberte řádek, kde je pole **Operace** nastaveno hodnotu *Oříznout/vyjmout*. Nastavte pole **Mezní hodnota oznámení pro zpoždění (%)** na mezní hodnotu (v procentech), na kterou má být oznámení zasláno.

1. Zvolte **Další**.
1. Na stránce **Aktivovat senzory** v mřížce vyberte senzor, který jste přidali, a poté vyberte **Aktivovat**. Pro každý aktivovaný senzor v mřížce se objeví zaškrtnutí ve sloupci **Aktivní**.
1. Vyberte **Dokončit**.

## <a name="work-with-the-production-delays-scenario"></a>Práce se scénářem zpoždění výroby

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Zobrazení dat zpoždění výroby na stránce stavu zdrojů

Na stránce **Stav zdroje** mohou nadřízení sledovat časovou osu signálů, které jsou přijímány ze senzorů, které jsou mapovány na každý strojový zdroj. Pro nakonfigurování časové osy postupujte takto.

1. Přejděte na **Řízení výroby \> Provádění výroby \> Stav prostředku**.
1. V dialogovém okně **Konfigurovat** nastavte následující pole:

    - **Prostředek** – Vyberte prostředky, které chcete monitorovat. (Pokud pracujete s ukázkovými daty, vyberte *3118*.)
    - **Časová řada 1** – Vyberte záznam (metrický klíč), jehož název má následující formát: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Zobrazovaný název** – Zadejte *Signál výstupu dílů*.
