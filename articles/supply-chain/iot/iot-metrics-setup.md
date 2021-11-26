---
title: Nastavení metriky pro IoT Intelligence
description: Toto téma vysvětluje, jak nastavit metriku pro IoT Intelligence.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85db0211c32ad4e27c3a9a65d2c74c5a39687f9c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783091"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Nastavení metriky pro IoT Intelligence

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Konfigurace metriky

Pokud chcete zobrazit grafy časových řad vašich zpráv v Microsoft Dynamics 365 Supply Chain Management, musíte nastavit metriku podle následujících kroků.

1. Zkopírujte připojovací řetězec pro Redis Cache:

    1. Na portálu Azure přejděte na Redis Cache.
    2. Přejděte na **Nastavení** \> **Přístupové klíče**.
    3. Zkopírujte hodnotu do pole **Primární připojovací řetězec**.

2. V aplikaci Supply Chain Management přejděte na **Řízení výroby \> Nastavení \> IoT Intelligence \> Parametry scénáře**.
3. Na stránce **Parametry scénáře** na kartě **Časové řady** v poli **Připojovací řetězec úložiště metriky Redis** vložte připojovací řetězec, který jste zkopírovali dříve. Tento krok umožňuje vizualizaci metriky z Azure IoT Hub v Supply Chain Management. Když hodnotu vložíte do pole, zobrazí se jako **\*\*\*\*\*\***.

    > [!NOTE]
    > Kdykoli aktualizujete připojovací řetězec Redis Cache, musíte také aktualizovat toto pole.

4. Přejděte na **Kontrola produkce \> Dotazy a zprávy \> IoT Intelligence \> Klíče metriky**.
5. Na stránce **Klíče metriky** vyberte **Aktualizovat**.
6. V dialogovém okně **Aktualizovat klíče metriky** si všimněte, že je v poli vybrána možnost **Spustit na pozadí**. Vyberte **OK**.

Všechny klíče metriky v Redis Cache jsou načteny a přidány do seznamu **Klíče metriky**. Metrické hodnoty se zobrazí, až [aktivujete scénáře](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Konfigurace časové řady stavu prostředku

Chcete-li nakonfigurovat časovou řadu **Stav prostředku**, postupujte takto.

1. V Supply Chain Management přejděte na **Kontrola produkce \> Výrobní provedení \> Stav prostředku**.
2. Na stránce **Stav prostředku** vyberte **Konfigurovat**.
2. V dialogovém okně **Konfigurovat** v seznamu **Prostředek** vyberte položku, kterou chcete sledovat.
3. Vyberte tlačítko **Upravit** pro **Časová řada 1**.
4. V dialogovém okně **Vybrat časovou řadu** vyberte metriku v mřížce. (Můžete také použít odkaz **Aktualizovat klíče metriky** pro aktualizaci klíčů metriky z tohoto dialogového okna.)
5. Výběrem **OK** se vraťte do dialogového okna **Konfigurovat**.
6. Zadejte zobrazovaný název.
7. V poli **Zobrazit data z** vyberte časový rámec.
8. Vyberte **OK**.

Zobrazí se graf.

## <a name="delete-a-metric-key"></a>Odstranění klíče metriky

1. V Supply Chain Management přejděte na **Kontrola produkce \> Dotazy a zprávy \> IoT Intelligence \> Klíče metriky**.
2. Na stránce **Klíče metriky** vyberte klíč metriky, který chcete odstranit.
3. Zvolte **Odstranit**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]