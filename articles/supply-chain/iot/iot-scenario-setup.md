---
title: Nastavení scénáře pro IoT Intelligence
description: Tohle téma vysvětluje, jak konfigurovat scénáře pro IoT Intelligence v Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 8adc65e26d78e229271eb427659a87ee5f371319
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814052"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="c795b-103">Nastavení scénáře pro IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="c795b-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c795b-104">Tohle téma vysvětluje, jak konfigurovat scénáře pro IoT Intelligence v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c795b-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c795b-105">Před vytvořením scénářů musíte [vytvořit Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="c795b-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="c795b-106">V tomto tématu nakonfigurujete scénář **Výpadky zařízení** pro generování oznámení v Supply Chain Management, když přestane fungovat stroj.</span><span class="sxs-lookup"><span data-stu-id="c795b-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="c795b-107">Tohle téma také ukazuje, jak konfigurovat scénář **Kvalita produktu**, takže je generováno oznámení, pokud je atribut položky mimo zadaný rozsah, a jak nakonfigurovat scénář **Zpoždění výroby** tak, aby se vygenerovalo oznámení, pokud výrobní kapacita klesne pod prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c795b-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="c795b-108">Konfigurace scénáře Výpadky zařízení v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c795b-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="c795b-109">Scénář **Výpadky zařízení** mapuje signál **PartOut** na prahovou hodnotu výstrahy stroje.</span><span class="sxs-lookup"><span data-stu-id="c795b-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="c795b-110">Stroj je monitorován, pouze pokud je vybrán pro scénář a je nastaven na **V provozu** v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c795b-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="c795b-111">Pokud doba od posledního přijatého signálu **PartOut** stroje přesahuje prahovou hodnotu výstrahy, spustí se oznámení **Stroj nepracuje**.</span><span class="sxs-lookup"><span data-stu-id="c795b-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="c795b-112">Pokud je stroj stále v chodu, při příštím obdržení signálu **PartOut** se spustí aktivuje **Stroj pracuje**.</span><span class="sxs-lookup"><span data-stu-id="c795b-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="c795b-113">Pokud stroj zůstane v nečinnosti po dobu 30 minut, spustí se nové oznámení **Stroj nepracuje**.</span><span class="sxs-lookup"><span data-stu-id="c795b-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="c795b-114">Scénář **Výpadky zařízení** má tyto závislosti:</span><span class="sxs-lookup"><span data-stu-id="c795b-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="c795b-115">Výstraha může být aktivována, pouze pokud je na mapovaném stroji spuštěna výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="c795b-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="c795b-116">Signál představující signál **PartOut** mapovaného stroje musí být odeslán do centra IoT se zadaným jedinečným názvem vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="c795b-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="c795b-117">Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v milisekundách (ms), musí být zahrnuta ve zprávě Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="c795b-118">Pro nakonfigurování scénáře postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c795b-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="c795b-119">Přihlaste se k aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c795b-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="c795b-120">Povolte příznak funkce IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="c795b-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="c795b-121">Další informace naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="c795b-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="c795b-122">Nakonfigurujte metriky.</span><span class="sxs-lookup"><span data-stu-id="c795b-122">Configure the metrics.</span></span> <span data-ttu-id="c795b-123">Další informace naleznete v části [Konfigurace metrik](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="c795b-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="c795b-124">Přejděte na **Řízení výroby \> Nastavení \> IoT Intelligence \> Správa scénářů**.</span><span class="sxs-lookup"><span data-stu-id="c795b-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="c795b-125">Na dlaždici **Výpadky zařízení** volbou **Konfigurovat** otevřete průvodce konfigurací.</span><span class="sxs-lookup"><span data-stu-id="c795b-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="c795b-126">První stránka průvodce je **Definice schématu senzoru zařízení**.</span><span class="sxs-lookup"><span data-stu-id="c795b-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="c795b-127">Na této stránce je vaším cílem nastavit schéma v Supply Chain Management tak, aby odpovídalo formátu JSON (JavaScript Object Notation) pro zprávy IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="c795b-128">Lze definovat více schémat zpráv.</span><span class="sxs-lookup"><span data-stu-id="c795b-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="c795b-129">Další informace viz [Formáty schémat pro zprávy IoT Hub](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="c795b-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="c795b-130">V tomto příkladu obsahuje datová část sadu zpráv v následujícím formátu.</span><span class="sxs-lookup"><span data-stu-id="c795b-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="c795b-131">Přidejte řádek do tabulky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c795b-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="c795b-132">Nastavte pole **Název schématu** na **ID**.</span><span class="sxs-lookup"><span data-stu-id="c795b-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="c795b-133">Nastavte pole **Název schématu** na **/payload\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="c795b-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="c795b-134">Nastavte pole **Popis** na **ID zprávy**.</span><span class="sxs-lookup"><span data-stu-id="c795b-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="c795b-135">Přidejte další řádek do tabulky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c795b-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="c795b-136">Nastavte pole **Název schématu** na **Časové razítko**.</span><span class="sxs-lookup"><span data-stu-id="c795b-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="c795b-137">Nastavte pole **Název schématu** na **/payload\[\*\]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="c795b-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="c795b-138">Nastavte pole **Popis** na **Časové razítko zprávy**.</span><span class="sxs-lookup"><span data-stu-id="c795b-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="c795b-139">Přidejte další řádek do tabulky a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c795b-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="c795b-140">Nastavte pole **Název schématu** na **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="c795b-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="c795b-141">Nastavte pole **Název schématu** na **/payload\[\*\]/value**.</span><span class="sxs-lookup"><span data-stu-id="c795b-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="c795b-142">Nastavte pole **Popis** na **Hodnota zprávy**.</span><span class="sxs-lookup"><span data-stu-id="c795b-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c795b-143">Ve zprávě nemusíte definovat všechny vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="c795b-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="c795b-144">Definujte pouze potřebné vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="c795b-144">Define only the properties that you require.</span></span> <span data-ttu-id="c795b-145">V předchozích krocích jste nevytvořili řádek pro **Kořenové časové razítko**.</span><span class="sxs-lookup"><span data-stu-id="c795b-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="c795b-146">Cesta pro **Kořenové časové razítko** by byla **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="c795b-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="c795b-147">Volbou **Další** a přejděte na stránku **Mapa schématu senzoru zařízení**.</span><span class="sxs-lookup"><span data-stu-id="c795b-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="c795b-148">V řádku pro **ID zdroje zařízení** v poli **Název schématu** vyberte **ID**.</span><span class="sxs-lookup"><span data-stu-id="c795b-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="c795b-149">V řádku pro **Čas UTC** v poli **Název schématu** vyberte **Časové razítko**.</span><span class="sxs-lookup"><span data-stu-id="c795b-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="c795b-150">V řádku pro **Díl vyvolal signál** v poli **Název schématu** vyberte **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="c795b-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="c795b-151">Volbou **Další** přejděte na stránku **Konfigurace ID zdroje zařízení**.</span><span class="sxs-lookup"><span data-stu-id="c795b-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="c795b-152">Podle těchto kroků namapujte hodnoty ve zprávě IoT Hub na zdroje Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="c795b-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="c795b-153">V tabulce **Hodnoty dat signálu** přidejte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="c795b-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="c795b-154">Do pole **Hodnota** zadejte **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="c795b-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="c795b-155">Tato hodnota pochází z vlastnosti **id** ve formátu JSON ve zprávě IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="c795b-156">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c795b-156">Select **Save**.</span></span>
    3. <span data-ttu-id="c795b-157">V tabulce **Mapování obchodních záznamů** vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c795b-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="c795b-158">Výchozí hodnota pro pole **Typ obchodního záznamu** je vyplněna automaticky a nemusíte ji měnit.</span><span class="sxs-lookup"><span data-stu-id="c795b-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="c795b-159">V poli **Obchodní záznam** vyberte zdroj stroje Supply Chain Management, ze kterého se odesílá hodnota signálu.</span><span class="sxs-lookup"><span data-stu-id="c795b-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="c795b-160">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c795b-160">Select **Save**.</span></span>
    6. <span data-ttu-id="c795b-161">Opakováním těchto kroků přidáte nové mapování obchodního záznamu pro **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="c795b-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="c795b-162">V aplikaci Supply Chain Management můžete namapovat více hodnot dat signálu na jeden záznam.</span><span class="sxs-lookup"><span data-stu-id="c795b-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="c795b-163">Použijte sloupec **Vybrané** pro výběr strojů, které chcete zpracovat.</span><span class="sxs-lookup"><span data-stu-id="c795b-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="c795b-164">Nemusíte definovat všechny hodnoty signálu a nemusíte vybírat všechny stroje.</span><span class="sxs-lookup"><span data-stu-id="c795b-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="c795b-165">Volbou **Další** přejděte na stránku **Konfigurace dílu který vyvolal signál**.</span><span class="sxs-lookup"><span data-stu-id="c795b-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="c795b-166">V tabulce **Hodnoty dat signálu** přidejte řádek a nastavte pole **Hodnota** na **True**.</span><span class="sxs-lookup"><span data-stu-id="c795b-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="c795b-167">Tato hodnota pochází z vlastnosti **hodnota** ve formátu JSON ve zprávě IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="c795b-168">Můžete přidat tolik hodnot, kolik potřebujete pro svůj scénář.</span><span class="sxs-lookup"><span data-stu-id="c795b-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="c795b-169">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c795b-169">Select **Save**.</span></span>
20. <span data-ttu-id="c795b-170">Volbou **Další** přejděte na stránku **Prahová hodnota zařízení výpadku**.</span><span class="sxs-lookup"><span data-stu-id="c795b-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="c795b-171">Uvedené stroje jsou stroje dříve namapované na hodnoty signálu.</span><span class="sxs-lookup"><span data-stu-id="c795b-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="c795b-172">Na této stránce definujete prahovou hodnotu pro určení, zda stroj nepracuje.</span><span class="sxs-lookup"><span data-stu-id="c795b-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="c795b-173">Pokud například nastavíte prahovou hodnotu na **10**, systém Supply Chain Management vygeneruje oznámení, pokud po dobu 10 minut není od stroje přijat signál **PartOut**.</span><span class="sxs-lookup"><span data-stu-id="c795b-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="c795b-174">Volbou **Další** přejděte na stránku **Povolit scénář**.</span><span class="sxs-lookup"><span data-stu-id="c795b-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="c795b-175">Nastavte možnost pro povolení scénáře.</span><span class="sxs-lookup"><span data-stu-id="c795b-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="c795b-176">Vyberte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="c795b-176">Select **Finish**.</span></span>

<span data-ttu-id="c795b-177">Nastavení scénáře je nyní dokončeno.</span><span class="sxs-lookup"><span data-stu-id="c795b-177">The scenario setup is now completed.</span></span> <span data-ttu-id="c795b-178">IoT Intelligence automaticky začne zpracovávat zprávy IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="c795b-179">Konfigurace scénáře Kvalita produktu v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c795b-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="c795b-180">Scénář **Kvalita produktu** generuje upozornění, pokud je atribut položky mimo určený rozsah.</span><span class="sxs-lookup"><span data-stu-id="c795b-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="c795b-181">Například senzor odešle váhu každé položky do služby IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="c795b-182">Pokud je položka příliš těžká nebo příliš lehká, v aplikaci Supply Chain Management se vygeneruje oznámení.</span><span class="sxs-lookup"><span data-stu-id="c795b-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="c795b-183">Scénář **Kvalita produktu** má tyto závislosti:</span><span class="sxs-lookup"><span data-stu-id="c795b-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="c795b-184">Aby byla výstraha aktivována, musí být na mapovaném stroji spuštěna výrobní zakázka a musí být vytvořen produkt s atributem mapované dávky.</span><span class="sxs-lookup"><span data-stu-id="c795b-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="c795b-185">Signál představující atribut dávky musí být odeslán do služby IoT Hub se zadaným jedinečným názvem vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="c795b-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="c795b-186">Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v ms, musí být zahrnuta ve zprávě IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="c795b-187">Konfigurace scénáře Zpoždění výroby v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c795b-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="c795b-188">Scénář **Zpoždění výroby** generuje oznámení, pokud výrobní kapacita klesne pod prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c795b-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="c795b-189">V tomto scénáři je signál **PartOut** odeslán do služby IoT Hub pro každou vyrobenou položku.</span><span class="sxs-lookup"><span data-stu-id="c795b-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="c795b-190">V aplikaci Supply Chain Management se zpoždění objednávky počítá na základě doby, po kterou je naplánováno spuštění výrobní zakázky, počtu položek, které by měly být vyrobeny, doby, po kterou byla úloha spuštěna, a počtu signálů **PartOut**, které byly přijaty.</span><span class="sxs-lookup"><span data-stu-id="c795b-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="c795b-191">Oznámení o zpoždění je generováno, pokud by počet signálů **PartOut** klesl pod prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c795b-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="c795b-192">Scénář **Zpoždění výroby** má tyto závislosti:</span><span class="sxs-lookup"><span data-stu-id="c795b-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="c795b-193">Výstraha může být aktivována, pouze pokud je na mapovaném stroji spuštěna výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="c795b-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="c795b-194">Signál představující signál **PartOut** mapovaného stroje musí být odeslán do centra Azure IoT se zadaným jedinečným názvem vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="c795b-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="c795b-195">Vlastnost **časového razítka** UNIX, kde je hodnota vyjádřena v ms, musí být zahrnuta ve zprávě IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c795b-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="c795b-196">Zákaz scénáře</span><span class="sxs-lookup"><span data-stu-id="c795b-196">Disable a scenario</span></span>

<span data-ttu-id="c795b-197">Pokud chcete zakázat scénář, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c795b-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="c795b-198">V aplikaci Supply Chain Management přejděte na **Řízení výroby \> Nastavení \> IoT Intelligence \> Správa scénářů**.</span><span class="sxs-lookup"><span data-stu-id="c795b-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="c795b-199">Na dlaždici scénáře vyberte **Konfigurovat**.</span><span class="sxs-lookup"><span data-stu-id="c795b-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="c795b-200">Volbou **Další** přejděte na poslední stránku průvodce.</span><span class="sxs-lookup"><span data-stu-id="c795b-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="c795b-201">Nastavte možnost pro zákaz scénáře.</span><span class="sxs-lookup"><span data-stu-id="c795b-201">Set the option to disable the scenario.</span></span>
