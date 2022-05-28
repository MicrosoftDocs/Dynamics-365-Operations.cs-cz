---
title: Domovská stránka IoT Intelligence
description: Toto téma obsahuje odkazy na informace o IoT Intelligence.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674414"
---
# <a name="iot-intelligence-home-page"></a>Domovská stránka IoT Intelligence

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Tato funkce je momentálně k dispozici pouze v následujících zemích/oblastech:
>
> - US (Spojené státy americké)
> - EU (Evropská unie)
> - AU (Austrálie)
> - CA (Kanada)
> - UK (Spojené království)

IoT Intelligence je doplněk pro Microsoft Dynamics 365 Supply Chain Management. Integruje signály internetu věcí (IoT) s daty v Supply Chain Management a vytváří užitečné informace.

IoT Intelligence podporuje následující scénáře:

- **Zpoždění výroby** – Tento scénář porovnává skutečnou dobu cyklu s plánovanou dobou cyklu. Supply Chain Management vás upozorní, když výroba není podle plánu, takže můžete zasáhnout, abyste maximalizovali provozní efektivitu a předešli zpoždění objednávek.
- **Odstávka zařízení** – Tento scénář porovnává naměřenou dobu provozuschopnosti s uživatelem definovanými parametry. Supply Chain Management vás upozorní, když je překročena prahová hodnota výpadku, takže můžete provést akce, jako je přeplánování výrobního pracovního příkazu nebo vytvoření pracovního příkazu údržby.
- **Kvalita produktu** – Tento scénář porovnává údaje ze senzorů, jako je vlhkost a teplota, s uživatelem definovanými metrikami kvality. Supply Chain Management vás upozorní, když dojde k odchylce, abyste mohli zasáhnout, abyste udrželi standardy kvality a minimalizovali plýtvání.

Následující obrázek ukazuje interakci Azure IoT Hub, IoT Intelligence a Supply Chain Management.

![IoT Hub, IoT Intelligence a Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Sledování a údržba

- [Scénáře monitorování v Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Zákaz scénáře](iot-scenario-setup.md#disable-a-scenario)
- [Úprava běžícího scénáře IoT Intelligence](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Možnosti simulace](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]