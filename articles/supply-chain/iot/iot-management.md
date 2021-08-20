---
title: Monitorování a správa IoT Intelligence
description: Toto téma vysvětluje, jak monitorovat a spravovat IoT Intelligence.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9d0bea8fb434e4733715da7ec88e33d3f25733339e4987df8f704227dc387ab9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736836"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Monitorování a správa IoT Intelligence

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak monitorovat a spravovat IoT Intelligence.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Scénáře monitorování v Microsoft Dynamics 365 Supply Chain Management

Můžete monitorovat zpracování IoT Intelligence z několika míst:

+ **Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Oznámení** - Zobrazit seznam nevyřešených oznámení.
+ **Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Uzavřená oznámení** - Zobrazit seznam oznámení, která byla vyřešena nebo zamítnuta.
+ **Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Klíče metrik** – Zobrazit klíče metrik pro grafy časových řad **Stav zdroje**.
+ **Moduly \> Řízení výroby \> Provádění výroby \> Stav zdroje** - Sledovat konkrétní metriky pomocí dialogového okna **Konfigurovat**. Pokud scénář detekuje výjimku, oznámení zobrazí podrobnosti o výjimce.
+ **Pracovní prostory \> Správa výrobního provozu \> Oznámení** - Zobrazit seznam nevyřešených oznámení.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Úprava běžícího scénáře IoT Intelligence

Když je spuštěn scénář, můžete provést tyto změny:

+ Přidat nové definice schématu senzoru.
+ Vybrat nové hodnoty dat signálu.
+ Zrušit výběr existujících hodnot dat signálu.
+ Přidat a mapovat nové hodnoty dat signálu.
+ Aktualizovat prahové hodnoty.

Když je spuštěn scénář, tyto změny jsou zakázané:

+ Odstranit nebo upravit všechny definice schématu, které aktuálně spotřebovává povolený scénář.
+ Změnit vybrané cesty schématu povoleného scénáře.

## <a name="simulation-options"></a>Možnosti simulace

Můžete simulovat signály výrobního stroje. Další informace naleznete v tématech:

+ [Připojení IoT DevKit AZ3166 k centru Azure IoT](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Připojení online simulátoru Raspberry Pi k centru Azure IoT (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Přehled akcelerátoru řešení simulace zařízení](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]