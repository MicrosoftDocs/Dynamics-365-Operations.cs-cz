---
title: Domovská stránka IoT Intelligence
description: Toto téma obsahuje odkazy na informace o IoT Intelligence.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782674"
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

+ **Zpoždění výroby** – Tento scénář porovnává skutečnou dobu cyklu s plánovanou dobou cyklu. Supply Chain Management vás upozorní, když výroba není podle plánu, takže můžete zasáhnout, abyste maximalizovali provozní efektivitu a předešli zpoždění objednávek.
+ **Odstávka zařízení** – Tento scénář porovnává naměřenou dobu provozuschopnosti s uživatelem definovanými parametry. Supply Chain Management vás upozorní, když je překročena prahová hodnota výpadku, takže můžete provést akce, jako je přeplánování výrobního pracovního příkazu nebo vytvoření pracovního příkazu údržby.
+ **Kvalita produktu** – Tento scénář porovnává údaje ze senzorů, jako je vlhkost a teplota, s uživatelem definovanými metrikami kvality. Supply Chain Management vás upozorní, když dojde k odchylce, abyste mohli zasáhnout, abyste udrželi standardy kvality a minimalizovali plýtvání.

Následující obrázek ukazuje interakci Azure IoT Hub, IoT Intelligence a Supply Chain Management.

![IoT Hub, IoT Intelligence a Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Nastavení

IoT Intelligence můžete nastavit a nakonfigurovat bez psaní kódu. Zde jsou základní kroky.

1. [Nastavení prostředků Azure](iot-azure-setup.md) – Vytvořte centrum IoT, mezipaměť Redis a trezor klíčů, ke kterým lze přistupovat ze Supply Chain Management.
2. [Formáty schématu zpráv pro IoT Hub](iot-schema-format.md) – Nakonfigurujte svá zařízení k odesílání zpráv do IoT Hub a definujte formát zpráv JavaScript Object Notation (JSON).
3. Ve správě funkcí povolte příznak funkce IoT Intelligence. 
4. [Nainstalovat doplněk IoT Intelligence do Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Nainstalujte doplněk do LCS a nakonfigurujte tajné klíče Azure.
5. [Nastavit metriku](iot-metrics-setup.md) – Nastavte metriku v Supply Chain Management.
6. [Nastavení scénáře](iot-scenario-setup.md) – Nastavte scénáře v Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Sledování a údržba

+ [Scénáře monitorování v Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Zákaz scénáře](iot-scenario-setup.md#disable-a-scenario)
+ [Odinstalace doplňku](iot-lcs-setup.md#uninstall-addin)
+ [Úprava běžícího scénáře IoT Intelligence](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Možnosti simulace](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]