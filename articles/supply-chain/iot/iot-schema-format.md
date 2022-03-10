---
title: Formáty schémat pro zprávy IoT Hub
description: Toto téma vysvětluje, jak byste měli navrhnout schéma zpráv, které můžete použít v IoT Intelligence.
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
ms.openlocfilehash: b24a6e14182baa91299abad0da2987b2dca92601
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781605"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Formáty schémat pro zprávy IoT Hub

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak byste měli navrhnout schéma zpráv, které můžete použít v IoT Intelligence.

## <a name="message-requirements"></a>Požadavky na zprávy

Následující pravidla platí pro monitorování zpráv v IoT Intelligence:

+ Schémata zpráv musí být ve formátu JavaScript Object Notation (JSON).
+ Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v milisekundách (ms), musí být zahrnuta ve zprávě Microsoft Azure IoT Hub.
+ Zpráva je sledována pouze v případě, že obsahuje všechny vlastnosti, které jsou definovány v nastavení scénáře. Například pokud definujete vlastnosti **id**, **timestamp** a **value**, je sledována následující zpráva.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Tato zpráva není monitorována, protože vlastnost **value** chybí.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT Intelligence ignoruje vlastnosti ve zprávě, které nejsou definovány v konfiguraci scénáře. Například pokud definujete vlastnosti **id**, **timestamp** a **value**, IoT Intelligence bude monitorovat následující zprávy.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT Intelligence tiše ignoruje zprávy, které neodpovídají kritériím konfigurace scénáře.
+ Můžete definovat a používat více typů schémat zpráv.
+ Ne každý typ schématu zprávy musí být definován. Musí být definována pouze schémata, která budou použita pro scénáře IoT Intelligence.

## <a name="id-value-pair-schema"></a>Schéma páru ID-hodnota

Pár id-hodnota je běžný vzor pro schémata zpráv IoT Intelligence. Použitím páru id-hodnota zajistíte, že schéma zprávy bude ve všech scénářích stejné. Zde je například zpráva pro scénář **Odstávka zařízení** nebo **Zpoždění výroby**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Zde je zpráva pro scénář **Kvalita produktu**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Obě předchozí zprávy obsahují vlastnosti **id** a **value**. Hodnoty **id** hodnoty lze mapovat v tabulce **Hodnoty dat signálu** během nastavování scénáře. Pro scénář **Odstávka zařízení** budete mapovat hodnotu **IoTInt.Machine1225.PartOut**. Pro scénář **Kvalita produktu** budete mapovat hodnotu **IoTInt.Machine1225.Temperature**.

Další informace naleznete v [Dokumentace centra IoT Azure](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]