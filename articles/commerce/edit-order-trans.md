---
title: Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků
description: Toto téma popisuje, jak upravit a auditovat online objednávky a asynchronní transakce objednávek zákazníků v Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458647"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="ca5af-103">Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="ca5af-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca5af-104">Toto téma popisuje, jak upravit a auditovat online objednávky a asynchronní transakce objednávek zákazníků v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ca5af-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="ca5af-105">Overview</span></span>

<span data-ttu-id="ca5af-106">Mezi verzemi Commerce 10.0.5 a 10.0.6 byla přidána podpora pro úpravy transakcí cash and carry (jako jsou prodeje a vrácení) a transakcí řízení hotovosti (jako je zadání plovoucího zůstatku a odstranění úhrad).</span><span class="sxs-lookup"><span data-stu-id="ca5af-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="ca5af-107">V Commerce verze 10.0.7 byla přidána podpora pro úpravy transakcí online objednávek a asynchronních transakcí objednávek zákazníků.</span><span class="sxs-lookup"><span data-stu-id="ca5af-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="ca5af-108">Úprava a audit transakcí objednávek</span><span class="sxs-lookup"><span data-stu-id="ca5af-108">Edit and audit order transactions</span></span>

<span data-ttu-id="ca5af-109">Chcete-li upravit a auditovat transakce objednávek v Commerce Headquarters, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ca5af-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ca5af-110">Nainstalujte [doplněk Microsoft Dynamics Office](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="ca5af-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="ca5af-111">Na stránce **Parametry maloobchodu** na záložce **Objednávky zákazníků** na záložce s náhledem **Objednávka** zadejte kód blokování pro **Kód blokování pro chyby synchronizace objednávky**.</span><span class="sxs-lookup"><span data-stu-id="ca5af-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="ca5af-112">Otevřete pracovní prostor **Finance obchodu**.</span><span class="sxs-lookup"><span data-stu-id="ca5af-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="ca5af-113">Dlaždice **Chyby synchronizace online objednávek** a **Chyby synchronizace objednávek zákazníka** poskytují předfiltrované zobrazení stránky maloobchodních transakcí.</span><span class="sxs-lookup"><span data-stu-id="ca5af-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="ca5af-114">Každé z nich zobrazuje záznamy transakcí, u kterých se nezdařila synchronizace pro odpovídající typ objednávky.</span><span class="sxs-lookup"><span data-stu-id="ca5af-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="ca5af-115">Otevřete buď stránku **Chyby synchronizace online objednávek** nebo stránku **Chyby synchronizace objednávek zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="ca5af-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="ca5af-116">Vyberte záznam a zobrazte podrobnosti chyby synchronizace.</span><span class="sxs-lookup"><span data-stu-id="ca5af-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="ca5af-117">Záložka s náhledem **Stav synchronizace** poskytuje následující podrobnosti o chybě:</span><span class="sxs-lookup"><span data-stu-id="ca5af-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="ca5af-118">Stav čekající objednávky</span><span class="sxs-lookup"><span data-stu-id="ca5af-118">Pending order status</span></span>
    - <span data-ttu-id="ca5af-119">Podrobnosti chyby objednávky</span><span class="sxs-lookup"><span data-stu-id="ca5af-119">Order error details</span></span>
    - <span data-ttu-id="ca5af-120">Datum a čas úpravy</span><span class="sxs-lookup"><span data-stu-id="ca5af-120">Modified date and time</span></span>
    - <span data-ttu-id="ca5af-121">Počet opakování</span><span class="sxs-lookup"><span data-stu-id="ca5af-121">Retry count</span></span>

1. <span data-ttu-id="ca5af-122">Pokud podrobnosti o chybě označují, že záznam musí být opraven, vyberte **Doplněk Office** a potom vyberte **Upravit vybranou transakci**.</span><span class="sxs-lookup"><span data-stu-id="ca5af-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="ca5af-123">Otevře se soubor aplikace Excel, který zobrazuje podrobnosti vybrané transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="ca5af-124">Pokud je upravovanou transakcí transakce online objednávky, soubor Excel obsahuje následující listy:</span><span class="sxs-lookup"><span data-stu-id="ca5af-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="ca5af-125">**Transakce** - Tento list obsahuje podrobnosti záhlaví transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-126">**Prodejní transakce** - Tento list obsahuje podrobnosti řádku transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-127">**Platební transakce** - Tento list obsahuje podrobnosti o řádcích platby dané transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="ca5af-128">**Slevové transakce** - Tento list obsahuje podrobnosti transakce související se slevami.</span><span class="sxs-lookup"><span data-stu-id="ca5af-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-129">**Daňové transakce** - Tento list obsahuje podrobnosti transakce související s daněmi.</span><span class="sxs-lookup"><span data-stu-id="ca5af-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-130">**Transakce nákladů** - Tento list obsahuje data transakce související s náklady.</span><span class="sxs-lookup"><span data-stu-id="ca5af-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="ca5af-131">Pokud je upravovanou transakcí asynchronní transakce objednávek zákazníků, soubor Excel obsahuje následující listy:</span><span class="sxs-lookup"><span data-stu-id="ca5af-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="ca5af-132">**Řádky** - Tento list obsahuje podrobnosti záhlaví a řádku transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-133">**Platby** - Tento list obsahuje podrobnosti o řádcích platby dané transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="ca5af-134">**Slevy** - Tento list obsahuje podrobnosti transakce související se slevami.</span><span class="sxs-lookup"><span data-stu-id="ca5af-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-135">**Daně** - Tento list obsahuje podrobnosti transakce související s daněmi.</span><span class="sxs-lookup"><span data-stu-id="ca5af-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="ca5af-136">**Náklady** - Tento list obsahuje data transakce související s náklady.</span><span class="sxs-lookup"><span data-stu-id="ca5af-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="ca5af-137">V souboru Excel v poli **Čekající stav objednávky** zadejte **Úpravy** a poté publikujte změnu.</span><span class="sxs-lookup"><span data-stu-id="ca5af-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="ca5af-138">Tímto způsobem zabráníte, aby úloha **Synchronizovat objednávku**, která běží v dávkovém režimu, přeskočila tento záznam během zpracování.</span><span class="sxs-lookup"><span data-stu-id="ca5af-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="ca5af-139">V souboru aplikace Excel upravte příslušná pole a poté odešlete data zpět do Commerce Headquarters pomocí funkce publikování doplňku Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="ca5af-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="ca5af-140">Po publikování dat se změny projeví v systému.</span><span class="sxs-lookup"><span data-stu-id="ca5af-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="ca5af-141">Během publikování se neprovádí žádné ověření u změn, které uživatelé provedou.</span><span class="sxs-lookup"><span data-stu-id="ca5af-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="ca5af-142">Úplný záznam auditu změn lze zobrazit výběrem možnosti **Zobrazit záznam auditu** v záhlaví **Maloobchodní transakce** pro změny na úrovni záhlaví a v příslušné sekci a provést záznam na příslušné stránce transakce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="ca5af-143">Například všechny změny související s řádky prodeje se zobrazí na stránce **Prodejní transakce** a všechny změny související s platbami se zobrazí na stránce **Platební transakce**.</span><span class="sxs-lookup"><span data-stu-id="ca5af-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="ca5af-144">Pro změny jsou zachovány následující podrobnosti auditu:</span><span class="sxs-lookup"><span data-stu-id="ca5af-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="ca5af-145">Datum a čas úpravy</span><span class="sxs-lookup"><span data-stu-id="ca5af-145">Modified date and time</span></span>
    - <span data-ttu-id="ca5af-146">Pole</span><span class="sxs-lookup"><span data-stu-id="ca5af-146">Field</span></span>
    - <span data-ttu-id="ca5af-147">Stará hodnota</span><span class="sxs-lookup"><span data-stu-id="ca5af-147">Old value</span></span>
    - <span data-ttu-id="ca5af-148">Nová hodnota</span><span class="sxs-lookup"><span data-stu-id="ca5af-148">New value</span></span>
    - <span data-ttu-id="ca5af-149">Změnil/a</span><span class="sxs-lookup"><span data-stu-id="ca5af-149">Modified by</span></span>

1. <span data-ttu-id="ca5af-150">Po provedení a publikování změn vyberte **Synchronizovat objednávku** okamžitě zahájíte proces synchronizace.</span><span class="sxs-lookup"><span data-stu-id="ca5af-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="ca5af-151">Alternativně můžete počkat, až proces synchronizace, který běží v dávkovém režimu, zpracuje transakci.</span><span class="sxs-lookup"><span data-stu-id="ca5af-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="ca5af-152">Ve výchozím nastavení se po úspěšné synchronizaci objednávek tyto objednávky dostanou do stavu blokace na základě kódu blokování, který je definován v parametrech Commerce.</span><span class="sxs-lookup"><span data-stu-id="ca5af-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="ca5af-153">Blokování objednávek musí být odstraněno, než mohou být objednávky dále zpracovány pro plnění nebo jiné operace.</span><span class="sxs-lookup"><span data-stu-id="ca5af-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca5af-154">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ca5af-154">Additional resources</span></span>

[<span data-ttu-id="ca5af-155">Úpravy a audit transakcí cash and carry a řízení hotovosti</span><span class="sxs-lookup"><span data-stu-id="ca5af-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="ca5af-156">Úprava finančních dimenzí pro maloobchodní transakce</span><span class="sxs-lookup"><span data-stu-id="ca5af-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="ca5af-157">Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="ca5af-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="ca5af-158">Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="ca5af-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)