---
title: Nastavení scénáře pro IoT Intelligence
description: Tohle téma vysvětluje, jak konfigurovat scénáře pro IoT Intelligence v Microsoft Dynamics 365 Supply Chain Management.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e8c65cebe64f86dcf158668e8a4f5600c158a1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782420"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Nastavení scénáře pro IoT Intelligence

[!include [banner](../../includes/banner.md)]

Tohle téma vysvětluje, jak konfigurovat scénáře pro IoT Intelligence v Microsoft Dynamics 365 Supply Chain Management. Před vytvořením scénářů musíte [vytvořit Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

V tomto tématu nakonfigurujete scénář **Výpadky zařízení** pro generování oznámení v Supply Chain Management, když přestane fungovat stroj. Tohle téma také ukazuje, jak konfigurovat scénář **Kvalita produktu**, takže je generováno oznámení, pokud je atribut položky mimo zadaný rozsah, a jak nakonfigurovat scénář **Zpoždění výroby** tak, aby se vygenerovalo oznámení, pokud výrobní kapacita klesne pod prahovou hodnotu.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Konfigurace scénáře Výpadky zařízení v Supply Chain Management

Scénář **Výpadky zařízení** mapuje signál **PartOut** na prahovou hodnotu výstrahy stroje. Stroj je monitorován, pouze pokud je vybrán pro scénář a je nastaven na **V provozu** v aplikaci Supply Chain Management. Pokud doba od posledního přijatého signálu **PartOut** stroje přesahuje prahovou hodnotu výstrahy, spustí se oznámení **Stroj nepracuje**. Pokud je stroj stále v chodu, při příštím obdržení signálu **PartOut** se spustí aktivuje **Stroj pracuje**. Pokud stroj zůstane v nečinnosti po dobu 30 minut, spustí se nové oznámení **Stroj nepracuje**.

Scénář **Výpadky zařízení** má tyto závislosti:

+ Výstraha může být aktivována, pouze pokud je na mapovaném stroji spuštěna výrobní zakázka.
+ Signál představující signál **PartOut** mapovaného stroje musí být odeslán do centra IoT se zadaným jedinečným názvem vlastnosti.
+ Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v milisekundách (ms), musí být zahrnuta ve zprávě Azure IoT Hub.

Pro nakonfigurování scénáře postupujte takto.

1. Přihlaste se k aplikaci Supply Chain Management.
2. Povolte příznak funkce IoT Intelligence. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Nakonfigurujte metriky. Další informace naleznete v části [Konfigurace metrik](iot-metrics-setup.md#configure-metrics).
4. Přejděte na **Řízení výroby \> Nastavení \> IoT Intelligence \> Správa scénářů**.
6. Na dlaždici **Výpadky zařízení** volbou **Konfigurovat** otevřete průvodce konfigurací.

   První stránka průvodce je **Definice schématu senzoru zařízení**. Na této stránce je vaším cílem nastavit schéma v Supply Chain Management tak, aby odpovídalo formátu JSON (JavaScript Object Notation) pro zprávy IoT Hub. Lze definovat více schémat zpráv. Další informace viz [Formáty schémat pro zprávy IoT Hub](iot-schema-format.md). V tomto příkladu obsahuje datová část sadu zpráv v následujícím formátu.

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

7. Přidejte řádek do tabulky a nastavte následující hodnoty:

    1. Nastavte pole **Název schématu** na **ID**.
    2. Nastavte pole **Název schématu** na **/payload\[\*\]/id**.
    3. Nastavte pole **Popis** na **ID zprávy**.

8. Přidejte další řádek do tabulky a nastavte následující hodnoty:

    1. Nastavte pole **Název schématu** na **Časové razítko**.
    2. Nastavte pole **Název schématu** na **/payload\[\*\]/timestamp**.
    3. Nastavte pole **Popis** na **Časové razítko zprávy**.

9. Přidejte další řádek do tabulky a nastavte následující hodnoty:

    1. Nastavte pole **Název schématu** na **Hodnota**.
    2. Nastavte pole **Název schématu** na **/payload\[\*\]/value**.
    3. Nastavte pole **Popis** na **Hodnota zprávy**.

    > [!NOTE]
    > Ve zprávě nemusíte definovat všechny vlastnosti. Definujte pouze potřebné vlastnosti. V předchozích krocích jste nevytvořili řádek pro **Kořenové časové razítko**. Cesta pro **Kořenové časové razítko** by byla **/timestamp**.

10. Volbou **Další** a přejděte na stránku **Mapa schématu senzoru zařízení**.
11. V řádku pro **ID zdroje zařízení** v poli **Název schématu** vyberte **ID**.
12. V řádku pro **Čas UTC** v poli **Název schématu** vyberte **Časové razítko**.
13. V řádku pro **Díl vyvolal signál** v poli **Název schématu** vyberte **Hodnota**.
14. Volbou **Další** přejděte na stránku **Konfigurace ID zdroje zařízení**.
15. Podle těchto kroků namapujte hodnoty ve zprávě IoT Hub na zdroje Supply Chain Management:

    1. V tabulce **Hodnoty dat signálu** přidejte nový řádek. Do pole **Hodnota** zadejte **IoTInt.Machine1225.PartOut**. Tato hodnota pochází z vlastnosti **id** ve formátu JSON ve zprávě IoT Hub.
    2. Zvolte **Uložit**.
    3. V tabulce **Mapování obchodních záznamů** vyberte **Nové**. Výchozí hodnota pro pole **Typ obchodního záznamu** je vyplněna automaticky a nemusíte ji měnit.
    4. V poli **Obchodní záznam** vyberte zdroj stroje Supply Chain Management, ze kterého se odesílá hodnota signálu.
    5. Zvolte **Uložit**.
    6. Opakováním těchto kroků přidáte nové mapování obchodního záznamu pro **Machine1226**. V aplikaci Supply Chain Management můžete namapovat více hodnot dat signálu na jeden záznam.

16. Použijte sloupec **Vybrané** pro výběr strojů, které chcete zpracovat. Nemusíte definovat všechny hodnoty signálu a nemusíte vybírat všechny stroje.
17. Volbou **Další** přejděte na stránku **Konfigurace dílu který vyvolal signál**.
18. V tabulce **Hodnoty dat signálu** přidejte řádek a nastavte pole **Hodnota** na **True**. Tato hodnota pochází z vlastnosti **hodnota** ve formátu JSON ve zprávě IoT Hub. Můžete přidat tolik hodnot, kolik potřebujete pro svůj scénář.
19. Zvolte **Uložit**.
20. Volbou **Další** přejděte na stránku **Prahová hodnota zařízení výpadku**. Uvedené stroje jsou stroje dříve namapované na hodnoty signálu. Na této stránce definujete prahovou hodnotu pro určení, zda stroj nepracuje. Pokud například nastavíte prahovou hodnotu na **10**, systém Supply Chain Management vygeneruje oznámení, pokud po dobu 10 minut není od stroje přijat signál **PartOut**.
21. Volbou **Další** přejděte na stránku **Povolit scénář**. Nastavte možnost pro povolení scénáře.
22. Vyberte **Dokončit**.

Nastavení scénáře je nyní dokončeno. IoT Intelligence automaticky začne zpracovávat zprávy IoT Hub.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Konfigurace scénáře Kvalita produktu v Supply Chain Management

Scénář **Kvalita produktu** generuje upozornění, pokud je atribut položky mimo určený rozsah. Například senzor odešle váhu každé položky do služby IoT Hub. Pokud je položka příliš těžká nebo příliš lehká, v aplikaci Supply Chain Management se vygeneruje oznámení.

Scénář **Kvalita produktu** má tyto závislosti:

+ Aby byla výstraha aktivována, musí být na mapovaném stroji spuštěna výrobní zakázka a musí být vytvořen produkt s atributem mapované dávky.
+ Signál představující atribut dávky musí být odeslán do služby IoT Hub se zadaným jedinečným názvem vlastnosti.
+ Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v ms, musí být zahrnuta ve zprávě IoT Hub.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Konfigurace scénáře Zpoždění výroby v Supply Chain Management

Scénář **Zpoždění výroby** generuje oznámení, pokud výrobní kapacita klesne pod prahovou hodnotu. V tomto scénáři je signál **PartOut** odeslán do služby IoT Hub pro každou vyrobenou položku. V aplikaci Supply Chain Management se zpoždění objednávky počítá na základě doby, po kterou je naplánováno spuštění výrobní zakázky, počtu položek, které by měly být vyrobeny, doby, po kterou byla úloha spuštěna, a počtu signálů **PartOut**, které byly přijaty. Oznámení o zpoždění je generováno, pokud by počet signálů **PartOut** klesl pod prahovou hodnotu.

Scénář **Zpoždění výroby** má tyto závislosti:

+ Výstraha může být aktivována, pouze pokud je na mapovaném stroji spuštěna výrobní zakázka.
+ Signál představující signál **PartOut** mapovaného stroje musí být odeslán do centra Azure IoT se zadaným jedinečným názvem vlastnosti.
+ Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v ms, musí být zahrnuta ve zprávě IoT Hub.

## <a name="disable-a-scenario"></a>Zákaz scénáře

Pokud chcete zakázat scénář, postupujte takto.

1. V aplikaci Supply Chain Management přejděte na **Řízení výroby \> Nastavení \> IoT Intelligence \> Správa scénářů**.
2. Na dlaždici scénáře vyberte **Konfigurovat**.
3. Volbou **Další** přejděte na poslední stránku průvodce.
4. Nastavte možnost pro zákaz scénáře.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]