---
title: Scénář údržby majetku
description: Tento článek popisuje scénář údržby majetku, který umožňuje používat data ze senzorů k vytváření záznamů počítadel, které sledují využití strojového majetku.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: fcd16d09b4293046c457b602857ef8950e8259c6
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644050"
---
# <a name="the-asset-maintenance-scenario"></a>Scénář údržby majetku

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Scénář *údržba majetku* umožňuje použít data senzoru k vytvoření záznamů čítačů. Záznamy počítadel sledují využití strojového majetku a používají se jako vstup pro generování plánu údržby strojového majetku.

## <a name="video-instructions"></a>Video s pokyny

Následující video ukazuje, jak nastavit a vyzkoušet scénář údržby majetku pomocí standardních [ukázkových dat](../../fin-ops-core/fin-ops/get-started/demo-data.md). Zbývající části tohoto článku obsahují stejné pokyny v textovém formátu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Příprava ukázkových dat pro scénář údržby majetku

Pokud chcete použít ukázkový systém k testování scénáře *údržba majetku*, použijte systém, kde jsou [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md) nainstalována, vyberte právnickou osobu *USMF* (společnost) a připravte další ukázková data, jak je popsáno v této části. Pokud používáte vlastní senzory a data, můžete tuto část přeskočit.

V této sekci nastavíte majetek *AK-101, Vzduchový nůž* v ukázkových datech jako příklad. Poté uvidíte, jak lze předvídat nadcházející údržbové práce na základě signálů senzorů, které měří počet hodin, po které byl vzduchový nůž v provozu. Nastavíte si také plán údržby, kde musí být vzduchový nůž udržován každých 10 000 hodin.

### <a name="set-up-a-sensor-simulator"></a>Nastavení simulátoru senzoru

Pokud si chcete tento scénář vyzkoušet bez použití fyzického senzoru, můžete nastavit simulátor pro generování požadovaných signálů. Další informace viz [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Vytvoření počítadla majetku pro sledování výrobních hodin

Následujícím postupem vytvořte počítadlo majetku pro sledování výrobních hodin.

1. Přejděte na **Správa majetku \> Nastavení \> Typy majetku \> Čítače**.
1. V podokně Akce vyberte možnost **Nový** a vytvořte počítadlo.
1. V záhlaví nastavte následující hodnoty:

    - **Počítadlo:** *ProductionHr*
    - **Název:** *Výrobní hodiny*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Jednotka:** *h*
    - **Aktualizace:** *Ruční*
    - **Celkový souhrn:** *Součet*

1. Na pevné záložce **Typy majetku** vyberte tlačítko **Přidat řádek**.
1. Na novém řádku nastavte pole **Typ majetku** na *Vzduchový nůž*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Vytvoření plánu údržby pro majetek

Pro vytvoření pánu údržby pro majetek postupujte následovně.

1. Klikněte na **Správa majetku \> Nastavení \> Preventivní údržba \> Plán údržby**.
1. V podokně Akce vyberte možnost **Nový** a vytvořte plán údržby.
1. V záhlaví nastavte následující hodnoty:

    - **Plán údržby:** *AirKnife*
    - **Název:** *Plán pro vzduchové nože*

1. Na pevné záložce **Obecné** nastavte následující hodnoty:

    - **Datum plánu:** Zadejte dnešní datum.
    - **Aktivní:** *Ano*

1. Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Přidat řádek čítače majetku**. Pro tento řádek nastavte následující hodnoty:

    - **Popis pracovního příkazu:** *Údržba vzduchového nože*
    - **Typ úlohy údržby:** *Preventivní*
    - **Typ intervalu:** *Opakuje z posledního pracovního příkazu*
    - **Frekvence období:** *10000*
    - **Počítadlo:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Nastavení scénáře údržby majetku

Chcete-li nastavit scénář *údržby majetku* v Supply Chain Management, postupujte takto.

1. Přejděte na **Správa majetku \> Nastavení \> Sensor Data Intelligence \> Scénáře**.
1. V poli scénáře **Údržba majetku** vyberte **Konfigurovat** a otevřete průvodce nastavením pro tento scénář.
1. Na stránce **Senzory** přidejte senzor do mřížky výběrem možnosti **Nový**. Poté pro něj nastavte následující pole:

    - **ID senzoru** – Zadejte ID senzoru, který používáte. (Pokud používáte Raspberry PI Azure IoT Online Simulator a nastavili jste ho podle popisu v části [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md), zadejte *AssetMaintenance*.)
    - **Popis senzoru** – zadejte popis senzoru.

1. Opakujte předchozí krok pro každý senzor, který teď chcete přidat. Kdykoli se můžete vrátit a přidat další senzory.
1. Zvolte **Další**.
1. Na stránce **Mapování obchodních záznamů** v části **Senzory** vyberte záznam pro jeden ze senzorů, které jste právě přidali.
1. V části **Mapování obchodního záznamu** vyberte **Nový** pro přidání řádku do mřížky.
1. Na novém řádku by pole **Typ obchodního záznamu** mělo být automaticky nastaveno na *Assets(EntAssetObjectTable)*. Nastavte pole **Obchodní záznam** na zdroj, který používáte ke sledování vybraného senzoru. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, nastavte ho na *AK-101, AK-101, Vzduchový nůž pro řádek 1*.)
1. Ihned poté, co vyberete typ obchodního záznamu pro řádek, který jste přidali v předchozím kroku, se do mřížky automaticky přidá druhý řádek. Na tomto řádku je třeba pole **Typ obchodního záznamu** nastavit na *Counters(EntAssetCounterType)*. Nastavte pole **Obchodní záznam** na počítadlo aktiv, které aktualizujete na základě signálů z vybraného senzoru. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, nastavte ho na *ProductionHr, výrobní hodiny*.)
1. Zvolte **Další**.
1. Na stránce **Aktivovat senzory** v mřížce vyberte senzor, který jste přidali, a poté vyberte **Aktivovat**. Pro každý aktivovaný senzor v mřížce se objeví zaškrtnutí ve sloupci **Aktivní**.
1. Vyberte **Dokončit**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Práce se scénářem údržby majetku

### <a name="view-counter-values"></a>Zobrazení hodnot čítače

Poté, co jsou data připravena, a scénář *údržba majetku* je scénář nakonfigurován a aktivován, můžete vidět, jak jsou vkládány záznamy pro počítadlo majetku na základě dat senzoru.

1. Přejděte na **Správa majetku \> Majetek \> Všechen majetek**.
1. Najděte a vyberte majetek, který chcete prozkoumat. (Pokud používáte ukázková data, která jste vytvořili dříve v tomto článku, vyberte *AK-101*.)
1. V podokně akcí na kartě **Majetek** ve skupině **Preventivní** vyberte **Čítače** a otevřete stránku pro záznamy čítače pro majetek *AK-101*.

### <a name="generate-maintenance-work-orders"></a>Generování pracovních příkazů údržby

Poté, co aktivujete scénář *údržba majetku* a nastavíte plán údržby, můžete spustit plán údržby a generovat pracovní příkazy údržby. Další informace o práci s preventivní údržbou najdete v části [Přehled preventivní údržby](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
