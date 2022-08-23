---
title: Monitorování a správa IoT Intelligence
description: Tento článek vysvětluje, jak monitorovat a spravovat inteligenci IoT.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f1804e8b9cfa407f6549dc146df17338c4d51572
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228852"
---
# <a name="monitor-and-manage-iot-intelligence"></a>Monitorování a správa IoT Intelligence

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Tento článek vysvětluje, jak monitorovat a spravovat inteligenci IoT.

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

Můžete simulovat signály výrobního stroje. Další informace naleznete v článcích:

+ [Připojení IoT DevKit AZ3166 k centru Azure IoT](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Připojení online simulátoru Raspberry Pi k centru Azure IoT (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
