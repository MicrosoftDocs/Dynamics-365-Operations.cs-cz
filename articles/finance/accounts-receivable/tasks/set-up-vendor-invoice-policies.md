---
title: Nastavení zásad faktur dodavatele
description: Toto téma vysvětluje, jak nastavit zásady pro fakturu dodavatele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143354"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="e3baa-103">Nastavení zásad faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="e3baa-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3baa-104">Toto téma vysvětluje, jak nastavit zásady pro fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e3baa-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="e3baa-105">Zásady faktur dodavatele se spouští při zaúčtování faktury dodavatele na stránce Faktura dodavatele, a při otevření stránky s porušením zásad faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e3baa-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="e3baa-106">Můžete také konfigurovat workflow faktury dodavatele tak, aby spustila zásady faktury dodavatele při každém odeslání faktury do workflowu.</span><span class="sxs-lookup"><span data-stu-id="e3baa-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="e3baa-107">Zásady faktur dodavatele se nevztahují na faktury, které byly vytvořeny v registru faktur a deníku faktur.</span><span class="sxs-lookup"><span data-stu-id="e3baa-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="e3baa-108">Ověření párování faktur nepoužívá zásady faktur dodavatele, ale namísto toho nastaví údaje na stránce s parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="e3baa-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="e3baa-109">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="e3baa-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="e3baa-110">Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.</span><span class="sxs-lookup"><span data-stu-id="e3baa-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="e3baa-111">Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur.</span><span class="sxs-lookup"><span data-stu-id="e3baa-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="e3baa-112">Příprava na vytvoření zásad faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="e3baa-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="e3baa-113">Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení > Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="e3baa-114">Zvolte kartu **Ověření faktury**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="e3baa-115">Zaškrtněte nebo zrušte označení pole **Automaticky aktualizovat stav záhlaví faktury**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="e3baa-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-116">Select **OK**.</span></span>
5. <span data-ttu-id="e3baa-117">V poli **Zaúčtovat fakturu s odchylkami** vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="e3baa-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="e3baa-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e3baa-118">Close the page.</span></span>
7. <span data-ttu-id="e3baa-119">Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení zásad > Zásady faktur dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="e3baa-120">Vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="e3baa-121">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-121">Select **Add**.</span></span>
10. <span data-ttu-id="e3baa-122">Zavřete stránku a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="e3baa-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="e3baa-123">Vytvoření nebo aktualizace typů pro faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="e3baa-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="e3baa-124">Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení zásad > Typy zásad faktur dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="e3baa-125">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-125">Select **New**.</span></span>
3. <span data-ttu-id="e3baa-126">Zadejte hodnoty do polí **Název pravidla** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="e3baa-127">V poli **Název dotazu** klepnutím na rozevírací tlačítko otevřete vyhledávání a poté vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="e3baa-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="e3baa-128">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-128">Select **Save**.</span></span>
6. <span data-ttu-id="e3baa-129">Zavřete stránku a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="e3baa-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="e3baa-130">Definování zásad faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="e3baa-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="e3baa-131">Přejděte na **Navigační podokno > Moduly > Závazky > Nastavení zásad > Zásady faktur dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="e3baa-132">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-132">Select **New**.</span></span>
3. <span data-ttu-id="e3baa-133">Zadejte hodnoty do polí **Název** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="e3baa-134">Rozbalte nebo sbalte část **Organizace zásad**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="e3baa-135">Ve stromovém zobrazení vyberte **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="e3baa-136">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-136">Select **Add**.</span></span>
7. <span data-ttu-id="e3baa-137">Rozbalte nebo sbalte část **Pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="e3baa-138">Vyberte **Vytvořit pravidlo zásad**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="e3baa-139">Zadejte hodnotu do pole **Popis pravidla zásad**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="e3baa-140">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-140">Select **Filter**.</span></span>
11. <span data-ttu-id="e3baa-141">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-141">Select **Add**.</span></span> <span data-ttu-id="e3baa-142">Vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="e3baa-142">Select the desired record.</span></span>
12. <span data-ttu-id="e3baa-143">V polích **Tabulka**, **Odvozená tabulka** a **Pole** vyberte nebo zadejte možnosti z rozevíracích nabídek.</span><span class="sxs-lookup"><span data-stu-id="e3baa-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="e3baa-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e3baa-144">Close the page.</span></span>
14. <span data-ttu-id="e3baa-145">Zadejte hodnotu do pole **Kritéria**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="e3baa-146">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-146">Select **OK**.</span></span>
16. <span data-ttu-id="e3baa-147">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3baa-147">Select **OK**.</span></span>
17. <span data-ttu-id="e3baa-148">Zavřete stránky a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="e3baa-148">Close the pages to return to the home page.</span></span>

