---
title: Monitorování a správa IoT Intelligence
description: Toto téma vysvětluje, jak monitorovat a spravovat IoT Intelligence.
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
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803058"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="e3482-103">Monitorování a správa IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="e3482-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3482-104">Toto téma vysvětluje, jak monitorovat a spravovat IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="e3482-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="e3482-105">Scénáře monitorování v Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e3482-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="e3482-106">Můžete monitorovat zpracování IoT Intelligence z několika míst:</span><span class="sxs-lookup"><span data-stu-id="e3482-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="e3482-107">**Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Oznámení** - Zobrazit seznam nevyřešených oznámení.</span><span class="sxs-lookup"><span data-stu-id="e3482-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="e3482-108">**Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Uzavřená oznámení** - Zobrazit seznam oznámení, která byla vyřešena nebo zamítnuta.</span><span class="sxs-lookup"><span data-stu-id="e3482-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="e3482-109">**Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Klíče metrik** – Zobrazit klíče metrik pro grafy časových řad **Stav zdroje**.</span><span class="sxs-lookup"><span data-stu-id="e3482-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="e3482-110">**Moduly \> Řízení výroby \> Provádění výroby \> Stav zdroje** - Sledovat konkrétní metriky pomocí dialogového okna **Konfigurovat**.</span><span class="sxs-lookup"><span data-stu-id="e3482-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="e3482-111">Pokud scénář detekuje výjimku, oznámení zobrazí podrobnosti o výjimce.</span><span class="sxs-lookup"><span data-stu-id="e3482-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="e3482-112">**Pracovní prostory \> Správa výrobního provozu \> Oznámení** - Zobrazit seznam nevyřešených oznámení.</span><span class="sxs-lookup"><span data-stu-id="e3482-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="e3482-113">Úprava běžícího scénáře IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="e3482-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="e3482-114">Když je spuštěn scénář, můžete provést tyto změny:</span><span class="sxs-lookup"><span data-stu-id="e3482-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="e3482-115">Přidat nové definice schématu senzoru.</span><span class="sxs-lookup"><span data-stu-id="e3482-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="e3482-116">Vybrat nové hodnoty dat signálu.</span><span class="sxs-lookup"><span data-stu-id="e3482-116">Select new signal data values.</span></span>
+ <span data-ttu-id="e3482-117">Zrušit výběr existujících hodnot dat signálu.</span><span class="sxs-lookup"><span data-stu-id="e3482-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="e3482-118">Přidat a mapovat nové hodnoty dat signálu.</span><span class="sxs-lookup"><span data-stu-id="e3482-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="e3482-119">Aktualizovat prahové hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e3482-119">Update threshold values.</span></span>

<span data-ttu-id="e3482-120">Když je spuštěn scénář, tyto změny jsou zakázané:</span><span class="sxs-lookup"><span data-stu-id="e3482-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="e3482-121">Odstranit nebo upravit všechny definice schématu, které aktuálně spotřebovává povolený scénář.</span><span class="sxs-lookup"><span data-stu-id="e3482-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="e3482-122">Změnit vybrané cesty schématu povoleného scénáře.</span><span class="sxs-lookup"><span data-stu-id="e3482-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="e3482-123">Možnosti simulace</span><span class="sxs-lookup"><span data-stu-id="e3482-123">Simulation options</span></span>

<span data-ttu-id="e3482-124">Můžete simulovat signály výrobního stroje.</span><span class="sxs-lookup"><span data-stu-id="e3482-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="e3482-125">Další informace naleznete v tématech:</span><span class="sxs-lookup"><span data-stu-id="e3482-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="e3482-126">Připojení IoT DevKit AZ3166 k centru Azure IoT</span><span class="sxs-lookup"><span data-stu-id="e3482-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="e3482-127">Připojení online simulátoru Raspberry Pi k centru Azure IoT (Node.js)</span><span class="sxs-lookup"><span data-stu-id="e3482-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="e3482-128">Přehled akcelerátoru řešení simulace zařízení</span><span class="sxs-lookup"><span data-stu-id="e3482-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
