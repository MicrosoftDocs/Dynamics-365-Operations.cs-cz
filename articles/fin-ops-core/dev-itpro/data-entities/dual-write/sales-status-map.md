---
title: Nastavení mapování pro sloupce stavu prodejní objednávky
description: Toto téma vysvětluje, jak nastavit sloupce stavu prodejní objednávky pro duální zápis.
author: dasani-madipalli
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
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750707"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="176f4-103">Nastavení mapování pro sloupce stavu prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="176f4-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="176f4-104">Sloupce, které označují stav prodejní objednávky, mají různé hodnoty výčtu v Microsoft Dynamics 365 Supply Chain Management a Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="176f4-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="176f4-105">K mapování těchto sloupců při duálním zápisu je nutné další nastavení.</span><span class="sxs-lookup"><span data-stu-id="176f4-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="176f4-106">sloupce v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="176f4-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="176f4-107">V aplikaci Supply Chain Management dva sloupce odrážejí stav prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="176f4-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="176f4-108">Sloupce, které musíte mapovat, jsou **Stav** a **Stav dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="176f4-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="176f4-109">Výčet **Stav** určuje celkový stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="176f4-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="176f4-110">Tento stav se zobrazuje v záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="176f4-110">This status is shown on the order header.</span></span>

<span data-ttu-id="176f4-111">Výčet **Stav** má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="176f4-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="176f4-112">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-112">Open Order</span></span>
- <span data-ttu-id="176f4-113">Dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-113">Delivered</span></span>
- <span data-ttu-id="176f4-114">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-114">Invoiced</span></span>
- <span data-ttu-id="176f4-115">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-115">Cancelled</span></span>

<span data-ttu-id="176f4-116">Výčet **Stav dokumentu** určuje nejnovější dokument, který byl vygenerován pro objednávku.</span><span class="sxs-lookup"><span data-stu-id="176f4-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="176f4-117">Například pokud je objednávka potvrzena, tento dokument je potvrzením prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="176f4-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="176f4-118">Pokud je prodejní objednávka částečně vyfakturována a poté je potvrzen zbývající řádek, zůstane stav dokladu **Faktura**, protože faktura je generována později v procesu.</span><span class="sxs-lookup"><span data-stu-id="176f4-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="176f4-119">Výčet **Stav dokumentu** má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="176f4-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="176f4-120">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="176f4-120">Confirmation</span></span>
- <span data-ttu-id="176f4-121">Výdejka</span><span class="sxs-lookup"><span data-stu-id="176f4-121">Picking List</span></span>
- <span data-ttu-id="176f4-122">Dodací list</span><span class="sxs-lookup"><span data-stu-id="176f4-122">Packing Slip</span></span>
- <span data-ttu-id="176f4-123">Faktura</span><span class="sxs-lookup"><span data-stu-id="176f4-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="176f4-124">sloupce v aplikaci Prodej</span><span class="sxs-lookup"><span data-stu-id="176f4-124">columns in Sales</span></span>

<span data-ttu-id="176f4-125">V aplikaci Sales dva sloupce označují stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="176f4-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="176f4-126">Sloupce, které musíte mapovat, jsou **Stav** a **Stav zpracování**.</span><span class="sxs-lookup"><span data-stu-id="176f4-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="176f4-127">Výčet **Stav** určuje celkový stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="176f4-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="176f4-128">Má následujícími hodnoty:</span><span class="sxs-lookup"><span data-stu-id="176f4-128">It has the following values:</span></span>

- <span data-ttu-id="176f4-129">Aktivní</span><span class="sxs-lookup"><span data-stu-id="176f4-129">Active</span></span>
- <span data-ttu-id="176f4-130">Odesláno</span><span class="sxs-lookup"><span data-stu-id="176f4-130">Submitted</span></span>
- <span data-ttu-id="176f4-131">Splněno</span><span class="sxs-lookup"><span data-stu-id="176f4-131">Fulfilled</span></span>
- <span data-ttu-id="176f4-132">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-132">Invoiced</span></span>
- <span data-ttu-id="176f4-133">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-133">Cancelled</span></span>

<span data-ttu-id="176f4-134">Výčet **Stav zpracování** byl zaveden, aby bylo možné stav přesněji mapovat pomocí aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="176f4-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="176f4-135">Následující tabulka ukazuje mapování **stavu zpracování** v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="176f4-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="176f4-136">Stav zpracování</span><span class="sxs-lookup"><span data-stu-id="176f4-136">Processing Status</span></span>   | <span data-ttu-id="176f4-137">Stav v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="176f4-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="176f4-138">Dokument v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="176f4-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="176f4-139">Aktivní</span><span class="sxs-lookup"><span data-stu-id="176f4-139">Active</span></span>              | <span data-ttu-id="176f4-140">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-140">Open Order</span></span>                        | <span data-ttu-id="176f4-141">Není</span><span class="sxs-lookup"><span data-stu-id="176f4-141">None</span></span>                                       |
| <span data-ttu-id="176f4-142">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="176f4-142">Confirmed</span></span>           | <span data-ttu-id="176f4-143">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-143">Open Order</span></span>                        | <span data-ttu-id="176f4-144">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="176f4-144">Confirmation</span></span>                               |
| <span data-ttu-id="176f4-145">Vydáno</span><span class="sxs-lookup"><span data-stu-id="176f4-145">Picked</span></span>              | <span data-ttu-id="176f4-146">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-146">Open Order</span></span>                        | <span data-ttu-id="176f4-147">Výdejka</span><span class="sxs-lookup"><span data-stu-id="176f4-147">Picking List</span></span>                               |
| <span data-ttu-id="176f4-148">Částečně dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-148">Partially Delivered</span></span> | <span data-ttu-id="176f4-149">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-149">Open Order</span></span>                        | <span data-ttu-id="176f4-150">Dodací list</span><span class="sxs-lookup"><span data-stu-id="176f4-150">Packing Slip</span></span>                               |
| <span data-ttu-id="176f4-151">Dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-151">Delivered</span></span>           | <span data-ttu-id="176f4-152">Dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-152">Delivered</span></span>                         | <span data-ttu-id="176f4-153">Dodací list</span><span class="sxs-lookup"><span data-stu-id="176f4-153">Packing Slip</span></span>                               |
| <span data-ttu-id="176f4-154">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-154">Partially Invoiced</span></span>  | <span data-ttu-id="176f4-155">Dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-155">Delivered</span></span>                         | <span data-ttu-id="176f4-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="176f4-156">Invoice</span></span>                                    |
| <span data-ttu-id="176f4-157">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-157">Invoiced</span></span>            | <span data-ttu-id="176f4-158">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-158">Invoiced</span></span>                          | <span data-ttu-id="176f4-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="176f4-159">Invoice</span></span>                                    |
| <span data-ttu-id="176f4-160">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-160">Cancelled</span></span>           | <span data-ttu-id="176f4-161">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-161">Cancelled</span></span>                         | <span data-ttu-id="176f4-162">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="176f4-162">Not applicable</span></span>                             |

<span data-ttu-id="176f4-163">Následující tabulka ukazuje mapování **stavu zpracování** mezi aplikacemi Sales a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="176f4-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="176f4-164">Stav zpracování</span><span class="sxs-lookup"><span data-stu-id="176f4-164">Processing Status</span></span>   | <span data-ttu-id="176f4-165">Stav v Sales</span><span class="sxs-lookup"><span data-stu-id="176f4-165">Status in Sales</span></span> | <span data-ttu-id="176f4-166">Stav v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="176f4-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="176f4-167">Aktivní</span><span class="sxs-lookup"><span data-stu-id="176f4-167">Active</span></span>              | <span data-ttu-id="176f4-168">Aktivní</span><span class="sxs-lookup"><span data-stu-id="176f4-168">Active</span></span>          | <span data-ttu-id="176f4-169">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-169">Open Order</span></span>                        |
| <span data-ttu-id="176f4-170">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="176f4-170">Confirmed</span></span>           | <span data-ttu-id="176f4-171">Odesláno</span><span class="sxs-lookup"><span data-stu-id="176f4-171">Submitted</span></span>       | <span data-ttu-id="176f4-172">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-172">Open Order</span></span>                        |
| <span data-ttu-id="176f4-173">Vydáno</span><span class="sxs-lookup"><span data-stu-id="176f4-173">Picked</span></span>              | <span data-ttu-id="176f4-174">Odesláno</span><span class="sxs-lookup"><span data-stu-id="176f4-174">Submitted</span></span>       | <span data-ttu-id="176f4-175">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-175">Open Order</span></span>                        |
| <span data-ttu-id="176f4-176">Částečně dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-176">Partially Delivered</span></span> | <span data-ttu-id="176f4-177">Aktivní</span><span class="sxs-lookup"><span data-stu-id="176f4-177">Active</span></span>          | <span data-ttu-id="176f4-178">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-178">Open Order</span></span>                        |
| <span data-ttu-id="176f4-179">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-179">Partially Invoiced</span></span>  | <span data-ttu-id="176f4-180">Aktivní</span><span class="sxs-lookup"><span data-stu-id="176f4-180">Active</span></span>          | <span data-ttu-id="176f4-181">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="176f4-181">Open Order</span></span>                        |
| <span data-ttu-id="176f4-182">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-182">Partially Invoiced</span></span>  | <span data-ttu-id="176f4-183">Splněno</span><span class="sxs-lookup"><span data-stu-id="176f4-183">Fulfilled</span></span>       | <span data-ttu-id="176f4-184">Dodáno</span><span class="sxs-lookup"><span data-stu-id="176f4-184">Delivered</span></span>                         |
| <span data-ttu-id="176f4-185">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-185">Invoiced</span></span>            | <span data-ttu-id="176f4-186">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-186">Invoiced</span></span>        | <span data-ttu-id="176f4-187">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="176f4-187">Invoiced</span></span>                          |
| <span data-ttu-id="176f4-188">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-188">Cancelled</span></span>           | <span data-ttu-id="176f4-189">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-189">Cancelled</span></span>       | <span data-ttu-id="176f4-190">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="176f4-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="176f4-191">Nastavení</span><span class="sxs-lookup"><span data-stu-id="176f4-191">Setup</span></span>

<span data-ttu-id="176f4-192">Chcete-li nastavit mapování pro sloupce stavu prodejní objednávky, musíte povolit atributy **IsSOPIntegrationEnabled** a **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="176f4-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="176f4-193">Chcete-li povolit atribut **IsSOPIntegrationEnabled**, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="176f4-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="176f4-194">Přejděte v prohlížeči na `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="176f4-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="176f4-195">Nahraďte **\<test-name\>** odkazem vaší společnosti na aplikaci Prodej.</span><span class="sxs-lookup"><span data-stu-id="176f4-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="176f4-196">Na otevřené stránce najděte **organizationid** a poznamenejte si hodnotu.</span><span class="sxs-lookup"><span data-stu-id="176f4-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Nalezení organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="176f4-198">V aplikaci Sales otevřete konzolu prohlížeče a spusťte následující skript.</span><span class="sxs-lookup"><span data-stu-id="176f4-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="176f4-199">Použijte hodnotu **organizationid** z kroku 2.</span><span class="sxs-lookup"><span data-stu-id="176f4-199">Use the **organizationid** value from step 2.</span></span>

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

4. <span data-ttu-id="176f4-201">Ověřte, zda je **IsSOPIntegrationEnabled** nastaveno na **true**.</span><span class="sxs-lookup"><span data-stu-id="176f4-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="176f4-202">Použijte URL adresu z kroku 1 pro ověření hodnoty.</span><span class="sxs-lookup"><span data-stu-id="176f4-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled nastaveno na true](media/sales-map-integration-enabled.png)

<span data-ttu-id="176f4-204">Chcete-li povolit atribut **isIntegrationUser**, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="176f4-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="176f4-205">V aplikaci Sales přejděte na **Nastavení \> Přizpůsobení \> Přizpůsobit systém**, vyberte **Tabulka uživatele** a poté otevřete **Formulář \> Uživatel**.</span><span class="sxs-lookup"><span data-stu-id="176f4-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Otevření formuláře uživatele](media/sales-map-user.png)

2. <span data-ttu-id="176f4-207">V prohlížeči polí najděte **Uživatelský režim integrace** a dvojitým kliknutím ho přidejte do formuláře.</span><span class="sxs-lookup"><span data-stu-id="176f4-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="176f4-208">Uložte změnu.</span><span class="sxs-lookup"><span data-stu-id="176f4-208">Save your change.</span></span>

    ![Přidání sloupce uživatelského režimu integrace do formuláře](media/sales-map-field-explorer.png)

3. <span data-ttu-id="176f4-210">V aplikaci Sales přejděte na **Nastavení \> Zabezpečeno \> Uživatelé** a změňte zobrazení z **Povolení uživatelé** na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="176f4-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Změna zobrazení z povolených uživatelů na uživatele aplikace](media/sales-map-enabled-users.png)

4. <span data-ttu-id="176f4-212">Vyberte dvě položky pro **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="176f4-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Seznam uživatelů aplikací](media/sales-map-user-mode.png)

5. <span data-ttu-id="176f4-214">Změňte hodnotu sloupce **Uživatelský režim integrace** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="176f4-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Změna hodnoty sloupce uživatelského režimu integrace](media/sales-map-user-mode-yes.png)

<span data-ttu-id="176f4-216">Vaše prodejní objednávky jsou nyní mapovány.</span><span class="sxs-lookup"><span data-stu-id="176f4-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]