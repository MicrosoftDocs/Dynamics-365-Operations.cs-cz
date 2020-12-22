---
title: Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí
description: Toto téma popisuje, jak vytvořit sešit aplikace Excel, abyste mohli upravovat maloobchodní transakce v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458649"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="7c85d-103">Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="7c85d-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c85d-104">Toto téma popisuje, jak vytvořit sešit aplikace Excel, abyste mohli upravovat maloobchodní transakce v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c85d-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7c85d-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="7c85d-105">Overview</span></span>

<span data-ttu-id="7c85d-106">K dispozici je předdefinovaná šablona aplikace Excel, ke které mají zákazníci přístup z různých částí systému a používají ji k úpravám a auditu maloobchodních transakcí.</span><span class="sxs-lookup"><span data-stu-id="7c85d-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="7c85d-107">Zákazníci si však pro tento účel mohou také vytvořit vlastní sešit aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="7c85d-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="7c85d-108">Vytvoření a konfigurace sešitu aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="7c85d-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="7c85d-109">Chcete-li vytvořit a konfigurovat sešit aplikace Excel, abyste mohli upravovat maloobchodní transakce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="7c85d-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="7c85d-110">Otevřete Excel a vytvořte prázdný sešit.</span><span class="sxs-lookup"><span data-stu-id="7c85d-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="7c85d-111">Na kartě **Vložit** vyberte **Moje doplňky**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="7c85d-112">V pravém podokně vyberte odkaz **Přidat informace o serveru**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="7c85d-113">Zadejte adresu URL serveru a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="7c85d-114">Pokud se zobrazí chybová zpráva „Nebyly nalezeny žádné registrace appletů“, problém vyřešíte takto:</span><span class="sxs-lookup"><span data-stu-id="7c85d-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="7c85d-115">V Commerce přejděte na **Správa systému \> Nastavení \> Parametry aplikace Office**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="7c85d-116">Na záložce s náhledem **Parametry aplikace** vyberte **Inicializovat parametry aplikace**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="7c85d-117">V okně s potvrzovací zprávou vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="7c85d-118">Na záložce s náhledem **Registrované applety** vyberte **Inicializovat registraci appletu**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="7c85d-119">Podle potřeby opakujte předchozí tři kroky.</span><span class="sxs-lookup"><span data-stu-id="7c85d-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="7c85d-120">Vyberte **Návrh** a potom vyberte **Přidat tabulku**.</span><span class="sxs-lookup"><span data-stu-id="7c85d-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="7c85d-121">Na základě dat, která je třeba upravit, vyberte entity, které je nutné přidat do sešitu aplikace Excel pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="7c85d-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="7c85d-122">Jako referenci použijte následující tabulku.</span><span class="sxs-lookup"><span data-stu-id="7c85d-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="7c85d-123">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="7c85d-123">Transaction type</span></span> | <span data-ttu-id="7c85d-124">Datové entity, které mají být použity</span><span class="sxs-lookup"><span data-stu-id="7c85d-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="7c85d-125">Transakce cash and carry, online objednávky, asynchronní objednávky zákazníka, asynchronní nabídky zákazníka</span><span class="sxs-lookup"><span data-stu-id="7c85d-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="7c85d-126">Transakce (auditovatelné), prodejní transakce (auditovatelné), platební transakce (auditovatelné), daňové transakce (auditovatelné), slevové transakce (auditovatelné), nákladové transakce (auditovatelné)</span><span class="sxs-lookup"><span data-stu-id="7c85d-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="7c85d-127">Odvod do banky</span><span class="sxs-lookup"><span data-stu-id="7c85d-127">Bank drop</span></span> | <span data-ttu-id="7c85d-128">Transakce (auditovatelné), transakce bankovních úhrad (auditovatelné)</span><span class="sxs-lookup"><span data-stu-id="7c85d-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="7c85d-129">Odvod do trezoru</span><span class="sxs-lookup"><span data-stu-id="7c85d-129">Safe drop</span></span> | <span data-ttu-id="7c85d-130">Transakce (auditovatelné), transakce odvodu úhrad do trezoru (auditovatelné)</span><span class="sxs-lookup"><span data-stu-id="7c85d-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="7c85d-131">Výkaz úhrad</span><span class="sxs-lookup"><span data-stu-id="7c85d-131">Tender declaration</span></span> | <span data-ttu-id="7c85d-132">Transakce (auditovatelné), transakce výkazu úhrad (auditovatelné)</span><span class="sxs-lookup"><span data-stu-id="7c85d-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="7c85d-133">Příjem, výdaj</span><span class="sxs-lookup"><span data-stu-id="7c85d-133">Income, Expense</span></span> | <span data-ttu-id="7c85d-134">Transakce (auditovatelné), příjmové/výdajové transakce (auditovatelné), platební transakce (auditovatelné)</span><span class="sxs-lookup"><span data-stu-id="7c85d-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="7c85d-135">Deklarace počáteční částky, odstranění úhrady, zadání plovoucího zůstatku, změna úhrady, platba faktury, vklad zákazníka</span><span class="sxs-lookup"><span data-stu-id="7c85d-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="7c85d-136">Transakce (auditovatelné), platební transakce (auditovatelné)</span><span class="sxs-lookup"><span data-stu-id="7c85d-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="7c85d-137">Je důležité, abyste do každého sešitu aplikace Excel přidali pouze jednu datovou entitu.</span><span class="sxs-lookup"><span data-stu-id="7c85d-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="7c85d-138">Všechna pole, která jsou označena symbolem klíče, musí být navíc přidána do příslušného sešitu.</span><span class="sxs-lookup"><span data-stu-id="7c85d-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="7c85d-139">Po nakonfigurování sešitu použijte požadované filtry.</span><span class="sxs-lookup"><span data-stu-id="7c85d-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="7c85d-140">Nezapomeňte použít stejné filtry na všechny listy v souboru.</span><span class="sxs-lookup"><span data-stu-id="7c85d-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="7c85d-141">Vyvarujte se načítání velkého množství dat do souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="7c85d-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="7c85d-142">Jinak může být ovlivněn výkon a Excel a váš systém se mohou zpomalit.</span><span class="sxs-lookup"><span data-stu-id="7c85d-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="7c85d-143">Jako filtry pro váš soubor doporučujeme vždy použít „Společnost“ a „Číslo výkazu“ nebo „Číslo transakce“.</span><span class="sxs-lookup"><span data-stu-id="7c85d-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="7c85d-144">Po nakonfigurování filtrů vyberte **Obnovit** pro načtení dat.</span><span class="sxs-lookup"><span data-stu-id="7c85d-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="7c85d-145">Upravte požadovaná data a poté je publikujte.</span><span class="sxs-lookup"><span data-stu-id="7c85d-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="7c85d-146">Pokud tlačítko **Publikovat** není k dispozici, některá klíčová pole pravděpodobně nebyla do sešitu aplikace Excel přidána.</span><span class="sxs-lookup"><span data-stu-id="7c85d-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c85d-147">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7c85d-147">Additional resources</span></span>

[<span data-ttu-id="7c85d-148">Úpravy a audit transakcí cash and carry a řízení hotovosti</span><span class="sxs-lookup"><span data-stu-id="7c85d-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="7c85d-149">Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="7c85d-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="7c85d-150">Úprava finančních dimenzí pro maloobchodní transakce</span><span class="sxs-lookup"><span data-stu-id="7c85d-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="7c85d-151">Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="7c85d-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
