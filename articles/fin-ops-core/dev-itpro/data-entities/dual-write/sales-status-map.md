---
title: Nastavení mapování pro pole stavu prodejní objednávky
description: Toto téma vysvětluje, jak nastavit pole stavu prodejní objednávky pro duální zápis.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829278"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="2b062-103">Nastavení mapování pro pole stavu prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="2b062-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b062-104">Pole, která označují stav prodejní objednávky, mají různé hodnoty výčtu v Microsoft Dynamics 365 Supply Chain Management a Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="2b062-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="2b062-105">K mapování těchto polí při duálním zápisu je nutné další nastavení.</span><span class="sxs-lookup"><span data-stu-id="2b062-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="2b062-106">Pole v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2b062-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="2b062-107">V aplikaci Supply Chain Management dvě pole odrážejí stav prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b062-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="2b062-108">Pole, která musíte mapovat, jsou **Stav** a **Stav dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="2b062-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="2b062-109">Výčet **Stav** určuje celkový stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b062-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="2b062-110">Tento stav se zobrazuje v záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b062-110">This status is shown on the order header.</span></span>

<span data-ttu-id="2b062-111">Výčet **Stav** má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2b062-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="2b062-112">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-112">Open Order</span></span>
- <span data-ttu-id="2b062-113">Dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-113">Delivered</span></span>
- <span data-ttu-id="2b062-114">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-114">Invoiced</span></span>
- <span data-ttu-id="2b062-115">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-115">Cancelled</span></span>

<span data-ttu-id="2b062-116">Výčet **Stav dokumentu** určuje nejnovější dokument, který byl vygenerován pro objednávku.</span><span class="sxs-lookup"><span data-stu-id="2b062-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="2b062-117">Například pokud je objednávka potvrzena, tento dokument je potvrzením prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b062-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="2b062-118">Pokud je prodejní objednávka částečně vyfakturována a poté je potvrzen zbývající řádek, zůstane stav dokladu **Faktura**, protože faktura je generována později v procesu.</span><span class="sxs-lookup"><span data-stu-id="2b062-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="2b062-119">Výčet **Stav dokumentu** má následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2b062-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="2b062-120">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="2b062-120">Confirmation</span></span>
- <span data-ttu-id="2b062-121">Výdejka</span><span class="sxs-lookup"><span data-stu-id="2b062-121">Picking List</span></span>
- <span data-ttu-id="2b062-122">Dodací list</span><span class="sxs-lookup"><span data-stu-id="2b062-122">Packing Slip</span></span>
- <span data-ttu-id="2b062-123">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b062-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="2b062-124">Pole v aplikaci Sales</span><span class="sxs-lookup"><span data-stu-id="2b062-124">Fields in Sales</span></span>

<span data-ttu-id="2b062-125">V aplikaci Sales dvě pole označují stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b062-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="2b062-126">Pole, která musíte mapovat, jsou **Stav** a **Stav zpracování**.</span><span class="sxs-lookup"><span data-stu-id="2b062-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="2b062-127">Výčet **Stav** určuje celkový stav objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b062-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="2b062-128">Má následujícími hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2b062-128">It has the following values:</span></span>

- <span data-ttu-id="2b062-129">Aktivní</span><span class="sxs-lookup"><span data-stu-id="2b062-129">Active</span></span>
- <span data-ttu-id="2b062-130">Odesláno</span><span class="sxs-lookup"><span data-stu-id="2b062-130">Submitted</span></span>
- <span data-ttu-id="2b062-131">Splněno</span><span class="sxs-lookup"><span data-stu-id="2b062-131">Fulfilled</span></span>
- <span data-ttu-id="2b062-132">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-132">Invoiced</span></span>
- <span data-ttu-id="2b062-133">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-133">Cancelled</span></span>

<span data-ttu-id="2b062-134">Výčet **Stav zpracování** byl zaveden, aby bylo možné stav přesněji mapovat pomocí aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2b062-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="2b062-135">Následující tabulka ukazuje mapování **stavu zpracování** v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2b062-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="2b062-136">Stav zpracování</span><span class="sxs-lookup"><span data-stu-id="2b062-136">Processing Status</span></span>   | <span data-ttu-id="2b062-137">Stav v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2b062-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="2b062-138">Dokument v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2b062-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="2b062-139">Aktivní</span><span class="sxs-lookup"><span data-stu-id="2b062-139">Active</span></span>              | <span data-ttu-id="2b062-140">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-140">Open Order</span></span>                        | <span data-ttu-id="2b062-141">Není</span><span class="sxs-lookup"><span data-stu-id="2b062-141">None</span></span>                                       |
| <span data-ttu-id="2b062-142">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="2b062-142">Confirmed</span></span>           | <span data-ttu-id="2b062-143">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-143">Open Order</span></span>                        | <span data-ttu-id="2b062-144">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="2b062-144">Confirmation</span></span>                               |
| <span data-ttu-id="2b062-145">Vydáno</span><span class="sxs-lookup"><span data-stu-id="2b062-145">Picked</span></span>              | <span data-ttu-id="2b062-146">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-146">Open Order</span></span>                        | <span data-ttu-id="2b062-147">Výdejka</span><span class="sxs-lookup"><span data-stu-id="2b062-147">Picking List</span></span>                               |
| <span data-ttu-id="2b062-148">Částečně dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-148">Partially Delivered</span></span> | <span data-ttu-id="2b062-149">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-149">Open Order</span></span>                        | <span data-ttu-id="2b062-150">Dodací list</span><span class="sxs-lookup"><span data-stu-id="2b062-150">Packing Slip</span></span>                               |
| <span data-ttu-id="2b062-151">Dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-151">Delivered</span></span>           | <span data-ttu-id="2b062-152">Dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-152">Delivered</span></span>                         | <span data-ttu-id="2b062-153">Dodací list</span><span class="sxs-lookup"><span data-stu-id="2b062-153">Packing Slip</span></span>                               |
| <span data-ttu-id="2b062-154">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-154">Partially Invoiced</span></span>  | <span data-ttu-id="2b062-155">Dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-155">Delivered</span></span>                         | <span data-ttu-id="2b062-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b062-156">Invoice</span></span>                                    |
| <span data-ttu-id="2b062-157">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-157">Invoiced</span></span>            | <span data-ttu-id="2b062-158">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-158">Invoiced</span></span>                          | <span data-ttu-id="2b062-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b062-159">Invoice</span></span>                                    |
| <span data-ttu-id="2b062-160">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-160">Cancelled</span></span>           | <span data-ttu-id="2b062-161">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-161">Cancelled</span></span>                         | <span data-ttu-id="2b062-162">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="2b062-162">Not applicable</span></span>                             |

<span data-ttu-id="2b062-163">Následující tabulka ukazuje mapování **stavu zpracování** mezi aplikacemi Sales a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2b062-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="2b062-164">Stav zpracování</span><span class="sxs-lookup"><span data-stu-id="2b062-164">Processing Status</span></span>   | <span data-ttu-id="2b062-165">Stav v Sales</span><span class="sxs-lookup"><span data-stu-id="2b062-165">Status in Sales</span></span> | <span data-ttu-id="2b062-166">Stav v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2b062-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="2b062-167">Aktivní</span><span class="sxs-lookup"><span data-stu-id="2b062-167">Active</span></span>              | <span data-ttu-id="2b062-168">Aktivní</span><span class="sxs-lookup"><span data-stu-id="2b062-168">Active</span></span>          | <span data-ttu-id="2b062-169">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-169">Open Order</span></span>                        |
| <span data-ttu-id="2b062-170">Potvrzeno</span><span class="sxs-lookup"><span data-stu-id="2b062-170">Confirmed</span></span>           | <span data-ttu-id="2b062-171">Odesláno</span><span class="sxs-lookup"><span data-stu-id="2b062-171">Submitted</span></span>       | <span data-ttu-id="2b062-172">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-172">Open Order</span></span>                        |
| <span data-ttu-id="2b062-173">Vydáno</span><span class="sxs-lookup"><span data-stu-id="2b062-173">Picked</span></span>              | <span data-ttu-id="2b062-174">Odesláno</span><span class="sxs-lookup"><span data-stu-id="2b062-174">Submitted</span></span>       | <span data-ttu-id="2b062-175">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-175">Open Order</span></span>                        |
| <span data-ttu-id="2b062-176">Částečně dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-176">Partially Delivered</span></span> | <span data-ttu-id="2b062-177">Aktivní</span><span class="sxs-lookup"><span data-stu-id="2b062-177">Active</span></span>          | <span data-ttu-id="2b062-178">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-178">Open Order</span></span>                        |
| <span data-ttu-id="2b062-179">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-179">Partially Invoiced</span></span>  | <span data-ttu-id="2b062-180">Aktivní</span><span class="sxs-lookup"><span data-stu-id="2b062-180">Active</span></span>          | <span data-ttu-id="2b062-181">Otevřená objednávka</span><span class="sxs-lookup"><span data-stu-id="2b062-181">Open Order</span></span>                        |
| <span data-ttu-id="2b062-182">Částečně fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-182">Partially Invoiced</span></span>  | <span data-ttu-id="2b062-183">Splněno</span><span class="sxs-lookup"><span data-stu-id="2b062-183">Fulfilled</span></span>       | <span data-ttu-id="2b062-184">Dodáno</span><span class="sxs-lookup"><span data-stu-id="2b062-184">Delivered</span></span>                         |
| <span data-ttu-id="2b062-185">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-185">Invoiced</span></span>            | <span data-ttu-id="2b062-186">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-186">Invoiced</span></span>        | <span data-ttu-id="2b062-187">Fakturováno</span><span class="sxs-lookup"><span data-stu-id="2b062-187">Invoiced</span></span>                          |
| <span data-ttu-id="2b062-188">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-188">Cancelled</span></span>           | <span data-ttu-id="2b062-189">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-189">Cancelled</span></span>       | <span data-ttu-id="2b062-190">Zrušeno</span><span class="sxs-lookup"><span data-stu-id="2b062-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="2b062-191">Nastavení</span><span class="sxs-lookup"><span data-stu-id="2b062-191">Setup</span></span>

<span data-ttu-id="2b062-192">Chcete-li nastavit mapování pro pole stavu prodejní objednávky, musíte povolit atributy **IsSOPIntegrationEnabled** a **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="2b062-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="2b062-193">Chcete-li povolit atribut **IsSOPIntegrationEnabled**, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2b062-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="2b062-194">Přejděte v prohlížeči na `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="2b062-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="2b062-195">Nahraďte **\<test-name\>** odkazem vaší společnosti na aplikaci Prodej.</span><span class="sxs-lookup"><span data-stu-id="2b062-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="2b062-196">Na otevřené stránce najděte **organizationid** a poznamenejte si hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2b062-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Nalezení organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="2b062-198">V aplikaci Sales otevřete konzolu prohlížeče a spusťte následující skript.</span><span class="sxs-lookup"><span data-stu-id="2b062-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="2b062-199">Použijte hodnotu **organizationid** z kroku 2.</span><span class="sxs-lookup"><span data-stu-id="2b062-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Kód JavaScript v konzole prohlížeče](media/sales-map-script.png)

4. <span data-ttu-id="2b062-201">Ověřte, zda je **IsSOPIntegrationEnabled** nastaveno na **true**.</span><span class="sxs-lookup"><span data-stu-id="2b062-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="2b062-202">Použijte URL adresu z kroku 1 pro ověření hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2b062-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled nastaveno na true](media/sales-map-integration-enabled.png)

<span data-ttu-id="2b062-204">Chcete-li povolit atribut **isIntegrationUser**, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2b062-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="2b062-205">V aplikaci Sales přejděte na **Nastavení \> Přizpůsobení \> Přizpůsobit systém**, vyberte **Entita uživatele** a poté otevřete **Formulář \> Uživatel**.</span><span class="sxs-lookup"><span data-stu-id="2b062-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Otevření formuláře uživatele](media/sales-map-user.png)

2. <span data-ttu-id="2b062-207">V prohlížeči polí najděte **Uživatelský režim integrace** a dvojitým kliknutím ho přidejte do formuláře.</span><span class="sxs-lookup"><span data-stu-id="2b062-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="2b062-208">Uložte změnu.</span><span class="sxs-lookup"><span data-stu-id="2b062-208">Save your change.</span></span>

    ![Přidání pole uživatelského režimu integrace do formuláře](media/sales-map-field-explorer.png)

3. <span data-ttu-id="2b062-210">V aplikaci Sales přejděte na **Nastavení \> Zabezpečeno \> Uživatelé** a změňte zobrazení z **Povolení uživatelé** na **Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="2b062-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Změna zobrazení z povolených uživatelů na uživatele aplikace](media/sales-map-enabled-users.png)

4. <span data-ttu-id="2b062-212">Vyberte dvě položky pro **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="2b062-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Seznam uživatelů aplikací](media/sales-map-user-mode.png)

5. <span data-ttu-id="2b062-214">Změňte hodnotu pole **Uživatelský režim integrace** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2b062-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Změna hodnoty pole uživatelského režimu integrace](media/sales-map-user-mode-yes.png)

<span data-ttu-id="2b062-216">Vaše prodejní objednávky jsou nyní mapovány.</span><span class="sxs-lookup"><span data-stu-id="2b062-216">Your sales orders are now mapped.</span></span>
