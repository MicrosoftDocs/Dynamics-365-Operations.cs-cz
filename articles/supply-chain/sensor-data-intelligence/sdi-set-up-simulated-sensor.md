---
title: Nastaven simulovaného senzoru pro testování
description: Tento článek popisuje, jak nastavit simulátor, který můžete použít k Sensor Data Intelligence bez instalace jakýchkoli fyzických senzorů.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc8bd020a53214abab28ec51ffc6d6be74979932
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643969"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Nastaven simulovaného senzoru pro testování

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Pokud chcete otestovat Sensor Data Intelligence bez instalace jakýchkoli fyzických senzorů, můžete použít službu *Raspberry PI Azure IoT Online Simulator* k emulaci signály senzorů a jejich odesílání do řešení internetu věcí (IoT) v Microsoft Azure. Více informací o simulátoru viz [Připojení Raspberry Pi online simulator k Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Video s pokyny

Následující video ukazuje, jak nastavit simulovaný snímač pro testování. Zbývající části tohoto článku obsahují stejné pokyny v textovém formátu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Vytvoření zařízení v Azure IoT Hub

Nejprve musíte nastavit zařízení k ověřování signálů senzorů do Azure IoT Hub.

1. V Azure přejděte na seznam prostředků pro skupinu prostředků, kterou jste vytvořili pro použití se Sensor Data Intelligence. (Další informace viz [Nasazení řešení IoT v Azure](sdi-deploy-iot-solution-on-azure.md) .)
1. V seznamu zdrojů najděte záznam, kde je pole **Typ** nastaveno na *Centrum IoT*. Ve sloupci **Název** vyberte název k otevření stránky s údaji o prostředku.
1. V levém navigačním podokně vyberte položku **Zařízení**.
1. Na stránce **Zařízení** vyberte **Přidat zařízení**.
1. Na stránce **Vytvořit zařízení** nastavte následující pole:

    - **ID zařízení** – Zadejte název nového zařízení (např. *My-IoT-Device*).
    - **Typ ověřování** – Vyberte *Symetrické klíče*.
    - **Automaticky generovat klíče** – Zaškrtněte toto políčko.
    - **Připojit toto zařízení k centru IoT** – Vyberte *Aktivovat*.

1. Vyberte **Uložit** pro návrat na stránku **Zařízení**.
1. Najděte nové zařízení v seznamu. Ve sloupci **ID zařízení** vyberte název k otevření stránky s údaji o zařízení. Pokud nové zařízení v seznamu nevidíte, obnovte stránku.
1. Zkopírujte hodnotu **Primární připojovací řetězec** (například výběrem tlačítka **Zkopírovat do schránky**). Tuto hodnotu budete potřebovat později, až budete nastavovat simulátor Raspberry Pi IoT pro emulaci signálů senzorů. Zvažte proto prozatím jeho vložení do textového souboru.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Přidejte připojovací řetězec Azure do simulátoru Raspberry Pi IoT

Podle těchto kroků přidejte připojovací řetězec ze zařízení v Azure IoT Hub do skriptu ve službě Raspberry.

1. Otevřete [simulátor Raspberry Pi IoT](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. V podokně editoru kódu vyhledejte řádek obsahující následující příkaz.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Nahraďte text nápovědy včetně závorek hodnotou **Primární připojovací řetězec**, kterou jste zkopírovali v předchozí části. Výsledek by měl vypadat podobně jako v následujícím příkladu.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Přidejte ID a hodnoty senzorů k datové části v simulátoru Raspberry Pi IoT

Nyní musíte nastavit simulátor Raspberry Pi IoT se simulovanými senzory a hodnotami, které budou odesílat jako datová část.

- V editoru kódu simulátoru Raspberry Pi IoT najděte funkci `getMessage` a upravte ji tak, aby odpovídala následujícímu kódu. (Senzory jsou umístěny v řádcích `cb()`.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > ID senzorů, které jsou definovány v editoru kódu pro simulátor Raspberry Pi IoT, musí být totožné s ID senzorů, které zadáte později pro scénáře v Supply Chain Management. Předchozí ukázkový kód používá člověkem čitelné ID senzorů. Ve skutečném scénáři však budou ID senzorů hodnoty globálně jedinečných identifikátorů (GUID), které poskytuje výrobce senzoru. Člověkem čitelná ID senzorů, která jsou použita v tomto příkladu kódu, jsou také použita v příkladech v částech [Scénář kvality produktu](sdi-scenario-product-quality.md), [Scénář údržby majetku](sdi-scenario-asset-maintenance.md), [Scénář zpoždění výroby](sdi-scenario-production-delays.md) a [Scénář stavu stroje](sdi-scenario-equipment-downtime.md)). Proto použijte tento kód, pokud budete procházet těmito scénáři.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Upravte interval pro odesílání signálů senzoru

Nyní musíte nastavit interval, ve kterém má simulátor Raspberry Pi IoT odesílat emulované signály senzoru.

1. V editoru kódu simulátoru Raspberry Pi IoT najděte následující vyvolání funkce.

    `setInterval(sendMessage, 2000);`

2. Ve výchozím nastavení odesílá simulátor IoT Raspberry Pi signál senzoru každých 2000 milisekund (dvě sekundy). Hodnotu můžete podle potřeby měnit.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Spuštění simulátoru Raspberry Pi IoT

- Vyberte **Spustit** ke spuštění simulátoru a zahájení odesílání simulovaných dat senzoru.
