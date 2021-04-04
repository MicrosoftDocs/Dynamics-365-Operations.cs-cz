---
title: Nastavení mapování pro sloupce stavu prodejní objednávky
description: Toto téma vysvětluje, jak nastavit sloupce stavu prodejní objednávky pro duální zápis.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: ecf26a2a697fa4d0485c1904041692a6c10ce9c3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560402"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="4a0a8-103">Nastavení mapování pro sloupce stavu prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="4a0a8-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a0a8-104">Sloupce, které označují stav prodejní objednávky, mají různé hodnoty výčtu v Microsoft Dynamics 365 Supply Chain Management a Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="4a0a8-105">K mapování těchto sloupců při duálním zápisu je nutné další nastavení.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="4a0a8-106">sloupce v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4a0a8-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="4a0a8-107">V aplikaci Supply Chain Management dva sloupce odrážejí stav prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="4a0a8-108">Sloupce, které musíte mapovat, jsou **Stav** a **Stav dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="4a0a8-109">Výčet **Stav** určuje celkový stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="4a0a8-110">Tento stav se zobrazuje v záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-110">This status is shown on the order header.</span></span>

<span data-ttu-id="4a0a8-111">Výčet **Stav** má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4a0a8-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="4a0a8-112">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-112">Open Order</span></span>
- <span data-ttu-id="4a0a8-113">Dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-113">Delivered</span></span>
- <span data-ttu-id="4a0a8-114">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-114">Invoiced</span></span>
- <span data-ttu-id="4a0a8-115">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-115">Cancelled</span></span>

<span data-ttu-id="4a0a8-116">Výčet **Stav dokumentu** určuje nejnovější dokument, který byl vygenerován pro objednávku.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="4a0a8-117">Například pokud je objednávka potvrzena, tento dokument je potvrzením prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="4a0a8-118">Pokud je prodejní objednávka částečně vyfakturována a poté je potvrzen zbývající řádek, zůstane stav dokladu **Faktura**, protože faktura je generována později v procesu.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="4a0a8-119">Výčet **Stav dokumentu** má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4a0a8-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="4a0a8-120">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="4a0a8-120">Confirmation</span></span>
- <span data-ttu-id="4a0a8-121">Výdejka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-121">Picking List</span></span>
- <span data-ttu-id="4a0a8-122">Dodací list</span><span class="sxs-lookup"><span data-stu-id="4a0a8-122">Packing Slip</span></span>
- <span data-ttu-id="4a0a8-123">Faktura</span><span class="sxs-lookup"><span data-stu-id="4a0a8-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="4a0a8-124">sloupce v aplikaci Prodej</span><span class="sxs-lookup"><span data-stu-id="4a0a8-124">columns in Sales</span></span>

<span data-ttu-id="4a0a8-125">V aplikaci Sales dva sloupce označují stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="4a0a8-126">Sloupce, které musíte mapovat, jsou **Stav** a **Stav zpracování**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="4a0a8-127">Výčet **Stav** určuje celkový stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="4a0a8-128">Má následujícími hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4a0a8-128">It has the following values:</span></span>

- <span data-ttu-id="4a0a8-129">Aktivní</span><span class="sxs-lookup"><span data-stu-id="4a0a8-129">Active</span></span>
- <span data-ttu-id="4a0a8-130">Odesláno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-130">Submitted</span></span>
- <span data-ttu-id="4a0a8-131">Splněno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-131">Fulfilled</span></span>
- <span data-ttu-id="4a0a8-132">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-132">Invoiced</span></span>
- <span data-ttu-id="4a0a8-133">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-133">Cancelled</span></span>

<span data-ttu-id="4a0a8-134">Výčet **Stav zpracování** byl zaveden, aby bylo možné stav přesněji mapovat pomocí aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="4a0a8-135">Následující tabulka ukazuje mapování **stavu zpracování** v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="4a0a8-136">Stav zpracování</span><span class="sxs-lookup"><span data-stu-id="4a0a8-136">Processing Status</span></span>   | <span data-ttu-id="4a0a8-137">Stav v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4a0a8-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="4a0a8-138">Dokument v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4a0a8-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="4a0a8-139">Aktivní</span><span class="sxs-lookup"><span data-stu-id="4a0a8-139">Active</span></span>              | <span data-ttu-id="4a0a8-140">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-140">Open Order</span></span>                        | <span data-ttu-id="4a0a8-141">Není</span><span class="sxs-lookup"><span data-stu-id="4a0a8-141">None</span></span>                                       |
| <span data-ttu-id="4a0a8-142">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-142">Confirmed</span></span>           | <span data-ttu-id="4a0a8-143">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-143">Open Order</span></span>                        | <span data-ttu-id="4a0a8-144">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="4a0a8-144">Confirmation</span></span>                               |
| <span data-ttu-id="4a0a8-145">Vydáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-145">Picked</span></span>              | <span data-ttu-id="4a0a8-146">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-146">Open Order</span></span>                        | <span data-ttu-id="4a0a8-147">Výdejka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-147">Picking List</span></span>                               |
| <span data-ttu-id="4a0a8-148">Částečně dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-148">Partially Delivered</span></span> | <span data-ttu-id="4a0a8-149">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-149">Open Order</span></span>                        | <span data-ttu-id="4a0a8-150">Dodací list</span><span class="sxs-lookup"><span data-stu-id="4a0a8-150">Packing Slip</span></span>                               |
| <span data-ttu-id="4a0a8-151">Dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-151">Delivered</span></span>           | <span data-ttu-id="4a0a8-152">Dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-152">Delivered</span></span>                         | <span data-ttu-id="4a0a8-153">Dodací list</span><span class="sxs-lookup"><span data-stu-id="4a0a8-153">Packing Slip</span></span>                               |
| <span data-ttu-id="4a0a8-154">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-154">Partially Invoiced</span></span>  | <span data-ttu-id="4a0a8-155">Dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-155">Delivered</span></span>                         | <span data-ttu-id="4a0a8-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="4a0a8-156">Invoice</span></span>                                    |
| <span data-ttu-id="4a0a8-157">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-157">Invoiced</span></span>            | <span data-ttu-id="4a0a8-158">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-158">Invoiced</span></span>                          | <span data-ttu-id="4a0a8-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="4a0a8-159">Invoice</span></span>                                    |
| <span data-ttu-id="4a0a8-160">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-160">Cancelled</span></span>           | <span data-ttu-id="4a0a8-161">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-161">Cancelled</span></span>                         | <span data-ttu-id="4a0a8-162">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="4a0a8-162">Not applicable</span></span>                             |

<span data-ttu-id="4a0a8-163">Následující tabulka ukazuje mapování **stavu zpracování** mezi aplikacemi Sales a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="4a0a8-164">Stav zpracování</span><span class="sxs-lookup"><span data-stu-id="4a0a8-164">Processing Status</span></span>   | <span data-ttu-id="4a0a8-165">Stav v Sales</span><span class="sxs-lookup"><span data-stu-id="4a0a8-165">Status in Sales</span></span> | <span data-ttu-id="4a0a8-166">Stav v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4a0a8-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="4a0a8-167">Aktivní</span><span class="sxs-lookup"><span data-stu-id="4a0a8-167">Active</span></span>              | <span data-ttu-id="4a0a8-168">Aktivní</span><span class="sxs-lookup"><span data-stu-id="4a0a8-168">Active</span></span>          | <span data-ttu-id="4a0a8-169">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-169">Open Order</span></span>                        |
| <span data-ttu-id="4a0a8-170">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-170">Confirmed</span></span>           | <span data-ttu-id="4a0a8-171">Odesláno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-171">Submitted</span></span>       | <span data-ttu-id="4a0a8-172">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-172">Open Order</span></span>                        |
| <span data-ttu-id="4a0a8-173">Vydáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-173">Picked</span></span>              | <span data-ttu-id="4a0a8-174">Odesláno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-174">Submitted</span></span>       | <span data-ttu-id="4a0a8-175">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-175">Open Order</span></span>                        |
| <span data-ttu-id="4a0a8-176">Částečně dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-176">Partially Delivered</span></span> | <span data-ttu-id="4a0a8-177">Aktivní</span><span class="sxs-lookup"><span data-stu-id="4a0a8-177">Active</span></span>          | <span data-ttu-id="4a0a8-178">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-178">Open Order</span></span>                        |
| <span data-ttu-id="4a0a8-179">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-179">Partially Invoiced</span></span>  | <span data-ttu-id="4a0a8-180">Aktivní</span><span class="sxs-lookup"><span data-stu-id="4a0a8-180">Active</span></span>          | <span data-ttu-id="4a0a8-181">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="4a0a8-181">Open Order</span></span>                        |
| <span data-ttu-id="4a0a8-182">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-182">Partially Invoiced</span></span>  | <span data-ttu-id="4a0a8-183">Splněno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-183">Fulfilled</span></span>       | <span data-ttu-id="4a0a8-184">Dodáno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-184">Delivered</span></span>                         |
| <span data-ttu-id="4a0a8-185">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-185">Invoiced</span></span>            | <span data-ttu-id="4a0a8-186">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-186">Invoiced</span></span>        | <span data-ttu-id="4a0a8-187">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-187">Invoiced</span></span>                          |
| <span data-ttu-id="4a0a8-188">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-188">Cancelled</span></span>           | <span data-ttu-id="4a0a8-189">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-189">Cancelled</span></span>       | <span data-ttu-id="4a0a8-190">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="4a0a8-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="4a0a8-191">Nastavení</span><span class="sxs-lookup"><span data-stu-id="4a0a8-191">Setup</span></span>

<span data-ttu-id="4a0a8-192">Chcete-li nastavit mapování pro sloupce stavu prodejní objednávky, musíte povolit atributy **IsSOPIntegrationEnabled** a **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="4a0a8-193">Chcete-li povolit atribut **IsSOPIntegrationEnabled**, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="4a0a8-194">Přejděte v prohlížeči na `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="4a0a8-195">Nahraďte **\<test-name\>** odkazem vaší společnosti na aplikaci Prodej.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="4a0a8-196">Na otevřené stránce najděte **organizationid** a poznamenejte si hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Nalezení organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="4a0a8-198">V aplikaci Sales otevřete konzolu prohlížeče a spusťte následující skript.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="4a0a8-199">Použijte hodnotu **organizationid** z kroku 2.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Kód JavaScript v konzole prohlížeče](media/sales-map-script.png)

4. <span data-ttu-id="4a0a8-201">Ověřte, zda je **IsSOPIntegrationEnabled** nastaveno na **true**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="4a0a8-202">Použijte URL adresu z kroku 1 pro ověření hodnoty.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled nastaveno na true](media/sales-map-integration-enabled.png)

<span data-ttu-id="4a0a8-204">Chcete-li povolit atribut **isIntegrationUser**, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="4a0a8-205">V aplikaci Sales přejděte na **Nastavení \> Přizpůsobení \> Přizpůsobit systém**, vyberte **Tabulka uživatele** a poté otevřete **Formulář \> Uživatel**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Otevření formuláře uživatele](media/sales-map-user.png)

2. <span data-ttu-id="4a0a8-207">V prohlížeči polí najděte **Uživatelský režim integrace** a dvojitým kliknutím ho přidejte do formuláře.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="4a0a8-208">Uložte změnu.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-208">Save your change.</span></span>

    ![Přidání sloupce uživatelského režimu integrace do formuláře](media/sales-map-field-explorer.png)

3. <span data-ttu-id="4a0a8-210">V aplikaci Sales přejděte na **Nastavení \> Zabezpečeno \> Uživatelé** a změňte zobrazení z **Povolení uživatelé** na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Změna zobrazení z povolených uživatelů na uživatele aplikace](media/sales-map-enabled-users.png)

4. <span data-ttu-id="4a0a8-212">Vyberte dvě položky pro **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Seznam uživatelů aplikací](media/sales-map-user-mode.png)

5. <span data-ttu-id="4a0a8-214">Změňte hodnotu sloupce **Uživatelský režim integrace** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Změna hodnoty sloupce uživatelského režimu integrace](media/sales-map-user-mode-yes.png)

<span data-ttu-id="4a0a8-216">Vaše prodejní objednávky jsou nyní mapovány.</span><span class="sxs-lookup"><span data-stu-id="4a0a8-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]