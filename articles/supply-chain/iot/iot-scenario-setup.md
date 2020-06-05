---
title: Nastavení scénáře pro IoT Intelligence
description: Toto téma popisuje, jak nakonfigurovat scénář v aplikaci Supply Chain Management pro IoT Intelligence.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386494"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Nastavení scénáře pro IoT Intelligence

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nakonfigurovat scénář v aplikaci Supply Chain Management pro IoT Intelligence. Než budete moci scénáře nastavit, musíte [nastavit LCS](iot-lcs-setup.md).

V tomto tématu nakonfigurujete scénář **Výpadky zařízení** pro generování oznámení v Supply Chain Management, když stroj přestane fungovat.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurace scénáře **Výpadky zařízení** v Supply Chain Management

Scénář **Výpadky zařízení** mapuje signál Part Out na prahovou hodnotu výstrahy stroje. Stroj je monitorován, pouze pokud je vybrán pro scénář a je nastaven na běh v aplikaci Supply Chain Management. Pokud je doba od posledního přijatého signálu Part Out zařízení delší než prahová hodnota výstrahy, spustí se oznámení **Stroj nepracuje**. Pokud je stroj stále v chodu, při příštím obdržení signálu **PartOut** se spustí oznámení **Stroj pracuje**. Pokud stroj zůstane v nečinnosti po dobu 30 minut, spustí se nové oznámení **Stroj nepracuje**.

Scénář **Výpadky zařízení** má tyto závislosti:

+ Aby byla výstraha spuštěna, musí být na mapovaném stroji spuštěna výrobní zakázka.
+ Signál představující signál Part Out mapovaného stroje musí být odeslán do centra IoT s jedinečným názvem vlastnosti.
+ Ve zprávě centra IoT musí být přítomna vlastnost časového razítka v milisekundách Unixu.

Pro nakonfigurování scénáře postupujte takto:

1. Přihlaste se do Supply Chain Management.
2. Povolte příznak funkce IoT Intelligence. Další informace naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Nakonfigurujte metriky. Další informace naleznete v části [Konfigurace metrik](iot-metrics-setup.md#configure-metrics).
4. Přejděte na **Řízení výroby**.
5. Přejděte na **Nastavit \> IoT Intelligence \> Správa scénářů**.
6. Klikněte na **Konfigurovat** na dlaždici **Výpadky zařízení**. Průvodce konfigurací začíná na stránce **Definice schématu senzoru zařízení**. Cílem je nastavit schéma v Supply Chain Management tak, aby odpovídalo formátu JSON zpráv IoT. Lze definovat více schémat zpráv. Další informace viz [Formáty schémat zpráv pro centrum IoT](iot-schema-format.md). V tomto příkladu obsahuje datová část sadu zpráv v tomto formátu:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Přidejte do tabulky řádek.

    1. Nastavte **Název schématu** na **ID**.
    2. Nastavte **Název schématu** na **/payload[\*]/id**.
    3. Nastavte **Popis** na **ID zprávy**.

8. Přidejte do tabulky řádek.

    1. Nastavte **Název schématu** na **Časové razítko**.
    2. Nastavte **Název schématu** na **/payload[\*]/timestamp**.
    3. Nastavte **Popis** na **Časové razítko zprávy**.

9. Přidejte do tabulky řádek.

    1. Nastavte **Název schématu** na **Hodnota**.
    2. Nastavte **Název schématu** na **/payload[\*]/value**.
    3. Nastavte **Popis** na **Hodnota zprávy**.

    Nemusíte definovat všechny vlastnosti ve zprávě, ale jen ty, které potřebujete. V tomto příkladu jste nevytvořili řádek pro **Kořenové časové razítko**. Cesta pro **Kořenové časové razítko** by byla **/timestamp**.
  
10. Klikněte na **Další** a přejděte na stránku **Mapa schématu senzoru zařízení**.
11. V řádku pro **ID zdroje zařízení** nastavte **Název schématu** na **ID**. Platné hodnoty jsou zobrazeny v rozbalovací tabulce.
12. V řádku pro **Čas UTC** nastavte **Název schématu** na **Časové razítko**. Platné hodnoty jsou zobrazeny v rozbalovací tabulce.
13. V řádku pro **Díl vyvolal signál** nastavte **Název schématu** na **Hodnota**. Platné hodnoty jsou zobrazeny v rozbalovací tabulce.
14. Klikněte na **Další** pro stránku **Konfigurace ID zdroje zařízení**.
15. V tomto kroku namapujete hodnoty zpráv centra IoT na zdroje Supply Chain Management.

    1. V tabulce **Hodnoty dat signálu** přidejte nový řádek a zadejte **IoTInt.Machine1225.PartOut** do sloupce **Hodnota**. Hodnota **IoTInt.Machine1225.PartOut** pochází z vlastnosti **ID** JSON ve zprávě centra IoT.
    2. Klikněte na možnost **Uložit**.
    3. V tabulce **Mapování obchodních záznamů** klikněte na **Nový**. Výchozí hodnota pro **Typ obchodního záznamu** je vyplněna automaticky a nemusíte ji měnit.
    4. Ve sloupci **Obchodní záznam** vyberte zdroj stroje Supple Chain Management, ze kterého se odesílá hodnota signálu.
    5. Klikněte na možnost **Uložit**.
    6. Tyto kroky opakujte a přidejte nové mapování obchodních záznamů pro **Machine1226**. V aplikaci Supply Chain Management můžete namapovat více hodnot dat signálu na jeden záznam.

16. Použijte sloupec **Vybrané** pro výběr strojů, které chcete zpracovat. Nemusíte definovat všechny hodnoty signálu a nemusíte vybírat všechny stroje.
17. Klikněte na **Další** a přejděte na stránku **Konfigurace dílu který vyvolal signál**.
18. V tabulce **Hodnoty dat signálu** přidejte řádek a nastavte pole **Hodnota** na **True**. Hodnota **True** pochází z vlastnosti **hodnota** JSON ve zprávě centra IoT. Můžete přidat tolik hodnot, kolik potřebujete pro svůj scénář.
19. Klikněte na možnost **Uložit**.
20. Klikněte na **Další** a přejděte na stránku **Prahová hodnota zařízení výpadku**. Uvedené stroje jsou stroje dříve namapované na hodnoty signálu. V tomto kroku definujete prahovou hodnotu pro určení, zda stroj nepracuje. Pokud například nastavíte prahovou hodnotu na 10, systém Supply Chain Management vygeneruje oznámení, pokud po dobu 10 minut negeneruje stroj zprávu o dokončeném dílu.
21. Kliknutím na tlačítko **Další** přejděte na stránku **Povolit scénář**. Přepněte posuvník pro povolení scénáře.
22. Klikněte na **Dokončit**.

Nastavení scénáře je dokončeno. IoT Intelligence automaticky začne zpracovávat zprávy centra IoT.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurace scénáře **Kvalita produktu** v Supply Chain Management

Scénář **Kvalita produktu** generuje upozornění, pokud je atribut položky mimo určený rozsah. Například senzor mohl poslat váhu každé položky do centra IoT. V aplikaci Supply Chain Management by bylo vygenerováno oznámení, pokud by položka byla příliš těžká nebo příliš lehká.

Scénář má tyto závislosti:

+ Aby byla výstraha spuštěna, musí být na mapovaném stroji spuštěna výrobní zakázka a musí být vytvořen produkt s atributem mapované dávky.
+ Signál představující atribut dávky musí být odeslán do centra IoT s jedinečným názvem vlastnosti.
+ Ve zprávě centra IoT musí být přítomna vlastnost časového razítka v milisekundách Unixu.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurace scénáře **Zpoždění výroby** v Supply Chain Management

Scénář **Zpoždění výroby** generuje oznámení, pokud výrobní kapacita klesne pod prahovou hodnotu. V tomto scénáři je signál **PartOut** odeslán do centra IoT pro každou vyrobenou položku. V aplikaci Supply Chain Management se zpoždění objednávky počítá na základě toho, jak dlouho je naplánována spuštění výrobní zakázky, kolik položek by mělo být vyrobeno, jak dlouho byla úloha spuštěna a kolik signálů **PartOut** je přijato. Oznámení o zpoždění by bylo generováno, pokud by počet signálů **PartOut** klesl pod prahovou hodnotu očekávané hodnoty.

Scénář má tyto závislosti:

+ Aby byla výstraha spuštěna, musí být na mapovaném stroji spuštěna výrobní zakázka.
+ Signál představující signál Part Out mapovaného stroje musí být odeslán do centra IoT s jedinečným názvem vlastnosti.
+ Ve zprávě centra IoT musí být přítomna vlastnost časového razítka v milisekundách Unixu.

## <a name="how-to-disable-a-scenario"></a>Jak zakázat scénář

Pokud chcete zakázat scénář, postupujte takto:

1. V aplikaci Supply Chain Management přejděte na **Řízení výroby \> Nastavit \> IoT Intelligence \> Správa scénářů**.
2. Klikněte na **Konfigurovat** ve scénáři.
3. Klikněte na **Další** a dostanete se na poslední kartu průvodce.
4. Přepněte posuvník pro zakázání scénáře.
