---
title: Scénář odstávky majetku
description: Tento článek popisuje scénář odstávky majetku, který vám umožňuje používat data ze senzorů ke sledování dostupnosti vašeho majetku.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 944818557deebed06c02c00fd69de6e8f08bda83
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428322"
---
# <a name="the-asset-downtime-scenario"></a>Scénář odstávky majetku

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Scénář odstávky majetku generuje záznam o prostoji údržby, pokud není přijat žádný signál ze stroje v rámci definovaného časového prahu od posledního přijetí signálu. Scénář vyžaduje, abyste svůj počítač vybavili senzorem, který pravidelně odesílá signál do vašeho Azure IoT Hub, když je počítač v provozu, ale neodesílá signál, když stroj nepracuje.

## <a name="set-up-the-asset-downtime-scenario"></a>Nastavení scénáře odstávky majetku

Chcete-li nastavit scénář *odstávky majetku* v Supply Chain Management, postupujte takto.

1. Přejděte na **Správa majetku \> Nastavení \> Sensor Data Intelligence \> Scénáře** k otevření stránky **Scénáře**.
2. V poli scénáře **Odstávka majetku** vyberte **Konfigurovat** a otevřete průvodce nastavením pro tento scénář.
3. Na stránce **Senzory** přidejte senzor do mřížky výběrem možnosti **Nový**. Poté pro něj nastavte následující pole:

    - **ID senzoru** – Zadejte ID senzoru, který používáte. (Pokud používáte Raspberry PI Azure IoT Online Simulator a nastavili jste ho podle popisu v části [Nastavení simulovaného senzoru pro testování](sdi-set-up-simulated-sensor.md), zadejte *AssetDownTime*.)
    - **Popis senzoru** – zadejte popis senzoru.

4. Opakujte předchozí krok pro každý senzor, který teď chcete přidat. Kdykoli se můžete vrátit a přidat další senzory.
5. Zvolte **Další**.
6. Na stránce **Mapování obchodních záznamů** v části **Senzory** vyberte záznam pro jeden ze senzorů, které jste právě přidali.
7. V části **Mapování obchodního záznamu** vyberte **Nový** pro přidání řádku do mřížky.
8. Na novém řádku nastavte pole **Obchodní záznam** na zdroj, který používáte ke sledování vybraného senzoru. (Pokud používáte ukázková data, vyberte *AK-101, Vzduchový nůž pro řádek 1*.)
9. Zvolte **Další**.
10. Na stránce **mezní hodnota doby odstávky majetku** definujte, jak dlouho po posledním signálu má systém čekat, než odešle oznámení o výpadku zařízení. Existují dva způsoby, jak mezní hodnotu definovat:

    - **Výchozí mezní hodnota (minuty)** – Nastavením tohoto pole definujete výchozí mezní hodnotu. Tato hodnota platí pro všechny zdroje, kde je pole **Mezní hodnota oznámení (minuty)** nastaveno na dvě minuty nebo méně. Minimální hodnota je *2* (minuty).
    - **Mezní hodnota pro zjištění, že stroj nereaguje (minuty)** – Pro každý zdroj v mřížce, kde nechcete použít výchozí mezní hodnotu, zadejte do tohoto pole hodnotu přepsání. Prostředky, které jsou nastaveny na použití mezní hodnoty dvou minut nebo méně, budou používat nastavení **Výchozí mezní hodnota (minuty)**.
11. Zvolte **Další**.
12. Na stránce **Aktivovat senzory** v mřížce vyberte senzor, který jste nastavili, a poté vyberte **Aktivovat**. Pro každý aktivovaný senzor v mřížce se objeví zaškrtnutí ve sloupci **Aktivní**.
13. Vyberte **Dokončit**.

## <a name="work-with-the-asset-downtime-scenario"></a>Práce se scénářem odstávky majetku

Pokud není přijat žádný signál senzoru z majetku v rámci mezní hodnoty definované v konfiguraci scénáře, systém pro tento majetek vytvoří záznam o prostoji údržby. Manažeři by měli pravidelně kontrolovat záznamy o prostojích (například jednou během každé pracovní směny) a používat vhodné kódy příčiny a časy ukončení pro každou registraci prostojů. Chcete-li zobrazit záznamy o prostojích údržby pro majetek, postupujte takto:

1. Přejděte na **Správa majetku > Majetek > Všechen majetek**.
2. Najděte a vyberte majetek, který chcete prozkoumat. (Pokud pracujete s ukázkovými daty, vyberte *AK-101*.)
3. V podokně akcí otevřete kartu **Majetek** a ze skupiny **Pracovní příkaz** vyberte **Prostoj údržby** k otevření stránky pro záznamy o prostojích údržby pro vybraný majetek.
