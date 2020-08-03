---
title: Nastavení scénáře pro IoT Intelligence
description: Toto téma popisuje, jak nakonfigurovat scénář v aplikaci Supply Chain Management pro IoT Intelligence.
author: robinarh
manager: tfehr
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
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597161"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="0d65c-103">Nastavení scénáře pro IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="0d65c-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d65c-104">Toto téma popisuje, jak nakonfigurovat scénář v aplikaci Supply Chain Management pro IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="0d65c-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="0d65c-105">Než budete moci scénáře nastavit, musíte [nastavit LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="0d65c-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="0d65c-106">V tomto tématu nakonfigurujete scénář **Výpadky zařízení** pro generování oznámení v Supply Chain Management, když stroj přestane fungovat.</span><span class="sxs-lookup"><span data-stu-id="0d65c-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="0d65c-107">Konfigurace scénáře **Výpadky zařízení** v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d65c-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="0d65c-108">Scénář **Výpadky zařízení** mapuje signál Part Out na prahovou hodnotu výstrahy stroje.</span><span class="sxs-lookup"><span data-stu-id="0d65c-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="0d65c-109">Stroj je monitorován, pouze pokud je vybrán pro scénář a je nastaven na běh v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d65c-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="0d65c-110">Pokud je doba od posledního přijatého signálu Part Out zařízení delší než prahová hodnota výstrahy, spustí se oznámení **Stroj nepracuje**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="0d65c-111">Pokud je stroj stále v chodu, při příštím obdržení signálu **PartOut** se spustí oznámení **Stroj pracuje**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="0d65c-112">Pokud stroj zůstane v nečinnosti po dobu 30 minut, spustí se nové oznámení **Stroj nepracuje**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="0d65c-113">Scénář **Výpadky zařízení** má tyto závislosti:</span><span class="sxs-lookup"><span data-stu-id="0d65c-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="0d65c-114">Aby byla výstraha spuštěna, musí být na mapovaném stroji spuštěna výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="0d65c-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="0d65c-115">Signál představující signál Part Out mapovaného stroje musí být odeslán do centra IoT s jedinečným názvem vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="0d65c-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="0d65c-116">Ve zprávě centra IoT musí být přítomna vlastnost časového razítka v milisekundách Unixu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="0d65c-117">Pro nakonfigurování scénáře postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0d65c-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="0d65c-118">Přihlaste se do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d65c-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="0d65c-119">Povolte příznak funkce IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="0d65c-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="0d65c-120">Další informace naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0d65c-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="0d65c-121">Nakonfigurujte metriky.</span><span class="sxs-lookup"><span data-stu-id="0d65c-121">Configure the metrics.</span></span> <span data-ttu-id="0d65c-122">Další informace naleznete v části [Konfigurace metrik](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="0d65c-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="0d65c-123">Přejděte na **Řízení výroby**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="0d65c-124">Přejděte na **Nastavit \> IoT Intelligence \> Správa scénářů**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="0d65c-125">Klikněte na **Konfigurovat** na dlaždici **Výpadky zařízení**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="0d65c-126">Průvodce konfigurací začíná na stránce **Definice schématu senzoru zařízení**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="0d65c-127">Cílem je nastavit schéma v Supply Chain Management tak, aby odpovídalo formátu JSON zpráv IoT.</span><span class="sxs-lookup"><span data-stu-id="0d65c-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="0d65c-128">Lze definovat více schémat zpráv.</span><span class="sxs-lookup"><span data-stu-id="0d65c-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="0d65c-129">Další informace viz [Formáty schémat zpráv pro centrum IoT](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="0d65c-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="0d65c-130">V tomto příkladu obsahuje datová část sadu zpráv v tomto formátu:</span><span class="sxs-lookup"><span data-stu-id="0d65c-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="0d65c-131">Přidejte do tabulky řádek.</span><span class="sxs-lookup"><span data-stu-id="0d65c-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="0d65c-132">Nastavte **Název schématu** na **ID**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="0d65c-133">Nastavte **Název schématu** na **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="0d65c-134">Nastavte **Popis** na **ID zprávy**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="0d65c-135">Přidejte do tabulky řádek.</span><span class="sxs-lookup"><span data-stu-id="0d65c-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="0d65c-136">Nastavte **Název schématu** na **Časové razítko**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="0d65c-137">Nastavte **Název schématu** na **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="0d65c-138">Nastavte **Popis** na **Časové razítko zprávy**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="0d65c-139">Přidejte do tabulky řádek.</span><span class="sxs-lookup"><span data-stu-id="0d65c-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="0d65c-140">Nastavte **Název schématu** na **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="0d65c-141">Nastavte **Název schématu** na **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="0d65c-142">Nastavte **Popis** na **Hodnota zprávy**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="0d65c-143">Nemusíte definovat všechny vlastnosti ve zprávě, ale jen ty, které potřebujete.</span><span class="sxs-lookup"><span data-stu-id="0d65c-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="0d65c-144">V tomto příkladu jste nevytvořili řádek pro **Kořenové časové razítko**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="0d65c-145">Cesta pro **Kořenové časové razítko** by byla **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="0d65c-146">Klikněte na **Další** a přejděte na stránku **Mapa schématu senzoru zařízení**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="0d65c-147">V řádku pro **ID zdroje zařízení** nastavte **Název schématu** na **ID**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="0d65c-148">Platné hodnoty jsou zobrazeny v rozbalovací tabulce.</span><span class="sxs-lookup"><span data-stu-id="0d65c-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="0d65c-149">V řádku pro **Čas UTC** nastavte **Název schématu** na **Časové razítko**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="0d65c-150">Platné hodnoty jsou zobrazeny v rozbalovací tabulce.</span><span class="sxs-lookup"><span data-stu-id="0d65c-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="0d65c-151">V řádku pro **Díl vyvolal signál** nastavte **Název schématu** na **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="0d65c-152">Platné hodnoty jsou zobrazeny v rozbalovací tabulce.</span><span class="sxs-lookup"><span data-stu-id="0d65c-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="0d65c-153">Klikněte na **Další** pro stránku **Konfigurace ID zdroje zařízení**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="0d65c-154">V tomto kroku namapujete hodnoty zpráv centra IoT na zdroje Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d65c-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="0d65c-155">V tabulce **Hodnoty dat signálu** přidejte nový řádek a zadejte **IoTInt.Machine1225.PartOut** do sloupce **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="0d65c-156">Hodnota **IoTInt.Machine1225.PartOut** pochází z vlastnosti **ID** JSON ve zprávě centra IoT.</span><span class="sxs-lookup"><span data-stu-id="0d65c-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="0d65c-157">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-157">Click **Save**.</span></span>
    3. <span data-ttu-id="0d65c-158">V tabulce **Mapování obchodních záznamů** klikněte na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="0d65c-159">Výchozí hodnota pro **Typ obchodního záznamu** je vyplněna automaticky a nemusíte ji měnit.</span><span class="sxs-lookup"><span data-stu-id="0d65c-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="0d65c-160">Ve sloupci **Obchodní záznam** vyberte zdroj stroje Supple Chain Management, ze kterého se odesílá hodnota signálu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="0d65c-161">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-161">Click **Save**.</span></span>
    6. <span data-ttu-id="0d65c-162">Tyto kroky opakujte a přidejte nové mapování obchodních záznamů pro **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="0d65c-163">V aplikaci Supply Chain Management můžete namapovat více hodnot dat signálu na jeden záznam.</span><span class="sxs-lookup"><span data-stu-id="0d65c-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="0d65c-164">Použijte sloupec **Vybrané** pro výběr strojů, které chcete zpracovat.</span><span class="sxs-lookup"><span data-stu-id="0d65c-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="0d65c-165">Nemusíte definovat všechny hodnoty signálu a nemusíte vybírat všechny stroje.</span><span class="sxs-lookup"><span data-stu-id="0d65c-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="0d65c-166">Klikněte na **Další** a přejděte na stránku **Konfigurace dílu který vyvolal signál**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="0d65c-167">V tabulce **Hodnoty dat signálu** přidejte řádek a nastavte pole **Hodnota** na **True**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="0d65c-168">Hodnota **True** pochází z vlastnosti **hodnota** JSON ve zprávě centra IoT.</span><span class="sxs-lookup"><span data-stu-id="0d65c-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="0d65c-169">Můžete přidat tolik hodnot, kolik potřebujete pro svůj scénář.</span><span class="sxs-lookup"><span data-stu-id="0d65c-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="0d65c-170">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-170">Click **Save**.</span></span>
20. <span data-ttu-id="0d65c-171">Klikněte na **Další** a přejděte na stránku **Prahová hodnota zařízení výpadku**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="0d65c-172">Uvedené stroje jsou stroje dříve namapované na hodnoty signálu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="0d65c-173">V tomto kroku definujete prahovou hodnotu pro určení, zda stroj nepracuje.</span><span class="sxs-lookup"><span data-stu-id="0d65c-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="0d65c-174">Pokud například nastavíte prahovou hodnotu na 10, systém Supply Chain Management vygeneruje oznámení, pokud po dobu 10 minut negeneruje stroj zprávu o dokončeném dílu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="0d65c-175">Kliknutím na tlačítko **Další** přejděte na stránku **Povolit scénář**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="0d65c-176">Přepněte posuvník pro povolení scénáře.</span><span class="sxs-lookup"><span data-stu-id="0d65c-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="0d65c-177">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-177">Click **Finish**.</span></span>

<span data-ttu-id="0d65c-178">Nastavení scénáře je dokončeno.</span><span class="sxs-lookup"><span data-stu-id="0d65c-178">The scenario setup is complete.</span></span> <span data-ttu-id="0d65c-179">IoT Intelligence automaticky začne zpracovávat zprávy centra IoT.</span><span class="sxs-lookup"><span data-stu-id="0d65c-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="0d65c-180">Konfigurace scénáře **Kvalita produktu** v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d65c-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="0d65c-181">Scénář **Kvalita produktu** generuje upozornění, pokud je atribut položky mimo určený rozsah.</span><span class="sxs-lookup"><span data-stu-id="0d65c-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="0d65c-182">Například senzor mohl poslat váhu každé položky do centra IoT.</span><span class="sxs-lookup"><span data-stu-id="0d65c-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="0d65c-183">V aplikaci Supply Chain Management by bylo vygenerováno oznámení, pokud by položka byla příliš těžká nebo příliš lehká.</span><span class="sxs-lookup"><span data-stu-id="0d65c-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="0d65c-184">Scénář má tyto závislosti:</span><span class="sxs-lookup"><span data-stu-id="0d65c-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="0d65c-185">Aby byla výstraha spuštěna, musí být na mapovaném stroji spuštěna výrobní zakázka a musí být vytvořen produkt s atributem mapované dávky.</span><span class="sxs-lookup"><span data-stu-id="0d65c-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="0d65c-186">Signál představující atribut dávky musí být odeslán do centra IoT s jedinečným názvem vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="0d65c-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="0d65c-187">Ve zprávě centra IoT musí být přítomna vlastnost časového razítka v milisekundách Unixu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="0d65c-188">Konfigurace scénáře **Zpoždění výroby** v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d65c-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="0d65c-189">Scénář **Zpoždění výroby** generuje oznámení, pokud výrobní kapacita klesne pod prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="0d65c-190">V tomto scénáři je signál **PartOut** odeslán do centra IoT pro každou vyrobenou položku.</span><span class="sxs-lookup"><span data-stu-id="0d65c-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="0d65c-191">V aplikaci Supply Chain Management se zpoždění objednávky počítá na základě toho, jak dlouho je naplánována spuštění výrobní zakázky, kolik položek by mělo být vyrobeno, jak dlouho byla úloha spuštěna a kolik signálů **PartOut** je přijato.</span><span class="sxs-lookup"><span data-stu-id="0d65c-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="0d65c-192">Oznámení o zpoždění by bylo generováno, pokud by počet signálů **PartOut** klesl pod prahovou hodnotu očekávané hodnoty.</span><span class="sxs-lookup"><span data-stu-id="0d65c-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="0d65c-193">Scénář má tyto závislosti:</span><span class="sxs-lookup"><span data-stu-id="0d65c-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="0d65c-194">Aby byla výstraha spuštěna, musí být na mapovaném stroji spuštěna výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="0d65c-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="0d65c-195">Signál představující signál Part Out mapovaného stroje musí být odeslán do centra IoT s jedinečným názvem vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="0d65c-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="0d65c-196">Ve zprávě centra IoT musí být přítomna vlastnost časového razítka v milisekundách Unixu.</span><span class="sxs-lookup"><span data-stu-id="0d65c-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="0d65c-197">Jak zakázat scénář</span><span class="sxs-lookup"><span data-stu-id="0d65c-197">How to disable a scenario</span></span>

<span data-ttu-id="0d65c-198">Pokud chcete zakázat scénář, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0d65c-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="0d65c-199">V aplikaci Supply Chain Management přejděte na **Řízení výroby \> Nastavit \> IoT Intelligence \> Správa scénářů**.</span><span class="sxs-lookup"><span data-stu-id="0d65c-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="0d65c-200">Klikněte na **Konfigurovat** ve scénáři.</span><span class="sxs-lookup"><span data-stu-id="0d65c-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="0d65c-201">Klikněte na **Další** a dostanete se na poslední kartu průvodce.</span><span class="sxs-lookup"><span data-stu-id="0d65c-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="0d65c-202">Přepněte posuvník pro zakázání scénáře.</span><span class="sxs-lookup"><span data-stu-id="0d65c-202">Toggle the slider to disable the scenario.</span></span>
