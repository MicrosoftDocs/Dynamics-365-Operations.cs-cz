---
title: Monitorování a správa IoT Intelligence
description: Toto téma vysvětluje, jak monitorovat a spravovat IoT Intelligence.
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
ms.openlocfilehash: 97a87b78a0178424f00e464262bb7f69e8a5b4a0
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386492"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="7699e-103">Monitorování a správa IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="7699e-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7699e-104">Toto téma vysvětluje, jak monitorovat a spravovat IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="7699e-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="7699e-105">Scénáře monitorování v Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7699e-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="7699e-106">Můžete monitorovat zpracování IoT Intelligence z několika míst:</span><span class="sxs-lookup"><span data-stu-id="7699e-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="7699e-107">**Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Oznámení** - Zobrazit seznam nevyřešených oznámení.</span><span class="sxs-lookup"><span data-stu-id="7699e-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="7699e-108">**Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Uzavřená oznámení** - Zobrazit seznam oznámení, která byla vyřešena nebo zamítnuta.</span><span class="sxs-lookup"><span data-stu-id="7699e-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="7699e-109">**Moduly \> Řízení výroby \> Dotazy a sestavy \> IoT Intelligence \> Klíče metrik** – Zobrazit klíče metrik pro grafy časových řad **Stav zdroje**.</span><span class="sxs-lookup"><span data-stu-id="7699e-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="7699e-110">**Moduly \> Řízení výroby \> Provádění výroby \> Stav zdroje** - Sledovat konkrétní metriky pomocí dialogového okna **Konfigurovat**.</span><span class="sxs-lookup"><span data-stu-id="7699e-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="7699e-111">Pokud scénář detekuje výjimku, oznámení zobrazí podrobnosti o výjimce.</span><span class="sxs-lookup"><span data-stu-id="7699e-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="7699e-112">**Pracovní prostory \> Správa výrobního provozu \> Oznámení** - Zobrazit seznam nevyřešených oznámení.</span><span class="sxs-lookup"><span data-stu-id="7699e-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="7699e-113">Úprava běžícího scénáře IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="7699e-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="7699e-114">Když je spuštěn scénář, můžete provést tyto změny:</span><span class="sxs-lookup"><span data-stu-id="7699e-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="7699e-115">Přidat nové definice schématu senzoru.</span><span class="sxs-lookup"><span data-stu-id="7699e-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="7699e-116">Vybrat nové hodnoty dat signálu.</span><span class="sxs-lookup"><span data-stu-id="7699e-116">Select new signal data values.</span></span>
+ <span data-ttu-id="7699e-117">Zrušit výběr existujících hodnot dat signálu.</span><span class="sxs-lookup"><span data-stu-id="7699e-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="7699e-118">Přidat a mapovat nové hodnoty dat signálu.</span><span class="sxs-lookup"><span data-stu-id="7699e-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="7699e-119">Aktualizovat prahové hodnoty.</span><span class="sxs-lookup"><span data-stu-id="7699e-119">Update threshold values.</span></span>

<span data-ttu-id="7699e-120">Když je spuštěn scénář, tyto změny jsou zakázané:</span><span class="sxs-lookup"><span data-stu-id="7699e-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="7699e-121">Odstranit nebo upravit všechny definice schématu, které aktuálně spotřebovává povolený scénář.</span><span class="sxs-lookup"><span data-stu-id="7699e-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="7699e-122">Změnit vybrané cesty schématu povoleného scénáře.</span><span class="sxs-lookup"><span data-stu-id="7699e-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="7699e-123">Možnosti simulace</span><span class="sxs-lookup"><span data-stu-id="7699e-123">Simulation options</span></span>

<span data-ttu-id="7699e-124">Můžete simulovat signály výrobního stroje.</span><span class="sxs-lookup"><span data-stu-id="7699e-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="7699e-125">Další informace naleznete v tématech:</span><span class="sxs-lookup"><span data-stu-id="7699e-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="7699e-126">Připojení IoT DevKit AZ3166 k centru Azure IoT</span><span class="sxs-lookup"><span data-stu-id="7699e-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="7699e-127">Připojení online simulátoru Raspberry Pi k centru Azure IoT (Node.js)</span><span class="sxs-lookup"><span data-stu-id="7699e-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="7699e-128">Přehled akcelerátoru řešení simulace zařízení</span><span class="sxs-lookup"><span data-stu-id="7699e-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
