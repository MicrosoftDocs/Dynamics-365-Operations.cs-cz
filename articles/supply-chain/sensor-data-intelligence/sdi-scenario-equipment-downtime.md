---
title: Scénář stavu stroje
description: Tento článek popisuje scénář stavu stroje, který vám umožňuje používat data ze senzorů ke sledování dostupnosti vašeho zařízení.
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
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689632"
---
# <a name="the-machine-status-scenario"></a>Scénář stavu stroje

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Scénář *stavu stroje* vám umožňuje používat data ze senzorů ke sledování dostupnosti vašeho zařízení. Pokud nastavíte senzor, který odešle signál, když produkční úloha na strojovém zdroji vytvoří výstup, ale během zadaného intervalu není přijat žádný signál senzoru, na řídicím panelu se zobrazí upozornění.

## <a name="scenario-dependencies"></a>Závislosti scénáře

Scénář *stav stroje* má tyto závislosti:

- Oznámení může být aktivováno, pouze pokud je na mapovaném stroji spuštěna úloha.
- Signál, který představuje signál *part-out*, musí být odeslán do centra IoT.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Příprava ukázkových dat pro scénář stavu stroje

Pokud chcete použít ukázkový systém k testování scénáře *stav stroje*, použijte systém, kde jsou [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md) nainstalována, vyberte právnickou osobu *USMF* (společnost) a připravte další ukázková data, jak je popsáno v této části. Pokud používáte vlastní senzory a data, můžete tuto část přeskočit.

### <a name="set-up-a-sensor-simulator"></a>Nastavení simulátoru senzoru

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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Konfigurace rozhraní pro provádění výrobního provozu

Ke spuštění úlohy, která byla naplánována a uvolněna pro číslo položky *P0111* v předchozí části, použijete rozhraní provádění výrobní dílny. Konfiguraci rozhraní pro provádění výrobního provozu provedete následovně.

1. Přejděte do nabídky **Řízení výroby \> Provádění výroby \> Provádění výrobního provozu**.
1. Pokud jste rozhraní ještě nenastavili, zobrazí se přihlašovací stránka. Zadejte své přihlašovací údaje.
1. Na úvodní stránce vyberte **Konfigurovat** k otevření průvodce **Konfigurace zařízení**.
1. Na stránce **Konfigurace zařízení – Krok 1 – Vybrat konfiguraci** vyberte konfiguraci *Výchozí*.
1. Zvolte **Další**.
1. Na stránce **Konfigurace zařízení – Krok 2 – Definovat výrobní dílnu** nastavte pole **Prostředek** na *3118*.
1. Vyberte **OK**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Aktivace možnosti hledání pro rozhraní ke spuštění výrobního provozu

Chcete-li usnadnit nalezení produkční úlohy pro výrobní zakázku, která byla vydána dříve, povolte pomocí těchto kroků možnost vyhledávání v rozhraní provádění produkční dílny.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**.
1. Vyberte konfiguraci *Výchozí*.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Obecné** nastavte možnost **Aktivovat vyhledávání** na *Ano*.
1. Zavřete stránku.

### <a name="start-the-first-job-in-the-batch-order"></a>Spuštění první úlohy v dávkovém příkazu

Chcete-li spustit úlohu naplánovanou na prostředek *3118*, postupujte podle těchto kroků.

1. Přejděte do nabídky **Řízení výroby \> Provádění výroby \> Provádění výrobního provozu**.
1. V poli **ID oznámení** zadejte *123*. Pak vyberte **Přihlásit se**.
1. Pokud se zobrazí výzva k zadání důvodu nepřítomnosti, vyberte jednu z karet nepřítomnosti a poté vyberte **OK**.
1. Do pole **Vyhledávání** zadejte číslo dávkového příkazu, které jste si předtím poznamenali. Poté vyberte klíč **Vrátit**.
1. Vyberte objednávku a poté vyberte **Spustit úlohu**.
1. V dialogovém okně **Spustit úlohu** vyberte **Spustit**.

## <a name="set-up-the-machine-status-scenario"></a>Nastavení scénáře stavu stroje

Chcete-li nastavit scénář *stav stroje* v Supply Chain Management, postupujte takto.

1. Přejděte na **Řízení výroby \> Nastavení \> Sensor Data Intelligence \> Scénáře**.
1. V poli scénáře **Stav stroje** vyberte **Konfigurovat** a otevřete průvodce nastavením pro tento scénář.
1. Na stránce **Senzory** přidejte senzor do mřížky výběrem možnosti **Nový**. Poté pro něj nastavte následující pole:

    - **ID senzoru** – Zadejte ID senzoru, který používáte. (Pokud používáte Raspberry PI Azure IoT Online Simulator a nastavili jste ho podle popisu v části [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md), zadejte *MachineStatus*.)
    - **Popis senzoru** – zadejte popis senzoru.

1. Opakujte předchozí krok pro každý senzor, který teď chcete přidat. Kdykoli se můžete vrátit a přidat další senzory.
1. Zvolte **Další**.
1. Na stránce **Mapování obchodních záznamů** v části **Senzory** vyberte záznam pro jeden ze senzorů, které jste právě přidali.
1. V části **Mapování obchodního záznamu** vyberte **Nový** pro přidání řádku do mřížky.
1. Na novém řádku nastavte pole **Obchodní záznam** na zdroj, který používáte ke sledování vybraného senzoru. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, nastavte ho na *3118, Stroj na řezání pěny*.)
1. Zvolte **Další**.
1. Na stránce **Mezní hodnota stavu stroje** definujte, jak dlouho po posledním signálu *part-out* by systém měl odeslat oznámení o stavu stroje. Existují dva způsoby, jak mezní hodnotu definovat:

    - **Výchozí mezní hodnota (minuty)** – Nastavením tohoto pole definujete výchozí mezní hodnotu. Hodnota se pak použije na všechny zdroje, kde je pole **Mezní hodnota pro zjištění, že stroj nereaguje (minuty)** je nastaveno na dvě minuty nebo méně. Minimální hodnota je *2* (minuty).
    - **Mezní hodnota pro zjištění, že stroj nereaguje (minuty)** – Pro každý zdroj v mřížce, pro který nechcete použít výchozí mezní hodnotu, zadejte do tohoto pole hodnotu přepsání. Prostředky, které jsou nastaveny na použití mezní hodnoty dvou minut nebo méně, budou používat nastavení **Výchozí mezní hodnota (minuty)**.

    > [!NOTE]
    > Obvykle budete používat signál *part-out* pro sledování stavu stroje. Proto byste měli ověřit, že práh pro každý prostředek stroje je delší, než stroj potřebuje k výrobě každé součásti.

1. Zvolte **Další**.
1. Na stránce **Aktivovat senzory** v mřížce vyberte senzor, který jste přidali, a poté vyberte **Aktivovat**. Pro každý aktivovaný senzor v mřížce se objeví zaškrtnutí ve sloupci **Aktivní**.
1. Vyberte **Dokončit**.

## <a name="work-with-the-machine-status-scenario"></a>Práce se scénářem stavu stroje

Poté, co nainstalujete senzory a nakonfigurujete scénář, můžete zobrazit události stavu stroje v Supply Chain Management. Tato část popisuje, kde a jak tyto informace zobrazit.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Zobrazení stavu stroje na stránce stavu zdrojů

Na stránce **Stav zdroje** mohou nadřízení sledovat časovou osu signálu *part-out*, který je přijímán ze senzorů, které jsou mapovány na každý strojový zdroj. Pro nakonfigurování časové osy postupujte takto.

1. Přejděte na **Řízení výroby \> Provádění výroby \> Stav prostředku**.
1. V dialogovém okně **Konfigurovat** nastavte následující pole:

    - **Prostředek** – Vyberte prostředky, které chcete monitorovat. (Pokud pracujete s ukázkovými daty, vyberte *3118*.)
    - **Časová řada 1** – Vyberte záznam (metrický klíč), jehož název má následující formát:: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Zobrazovaný název** – Zadejte *Signál výstupu dílů*.

Následující obrázek ukazuje příklad údajů o stavu stroje na stránce **Stav zdroje** při standardním provozu.

![Data stavu stroje na stránce stavu zdrojů během standardního provozu.](media/sdi-resource-status-downtime-up.png "Data stavu stroje na stránce stavu zdrojů během standardního provozu")

Následující obrázek ukazuje příklad údajů o stavu stroje při zjištění prostoje.

![Údaje o stavu stroje na stránce stavu prostředků, když je zjištěn výpadek.](media/sdi-resource-status-downtime-down.png "Údaje o stavu stroje na stránce stavu prostředků, když je zjištěn výpadek")

### <a name="view-machine-status-on-the-notifications-page"></a>Zobrazení stavu stroje na stránce Oznámení

Na stránce **Oznámení** mohou nadřízení zobrazit oznámení, která jsou generována, když od posledního vydání signálu *part-out* senzorem uplynulo příliš mnoho času. Každé oznámení poskytuje přehled o produkční úloze, která je postižena výpadkem, a dává možnost přeřadit postiženou úlohu k jinému zdroji.

K otevření stránky **Oznámení** přejděte na **Řízení výroby \> Dotazy a sestavy \> Sensor Data Intelligence \> Oznámení**.

Následující obrázek znázorňuje příklad stránky s oznámením stavu stroje.

![Příklad oznámení stavu stroje.](media/sdi-resource-status-downtime-notification.png "Příklad oznámení stavu stroje")
