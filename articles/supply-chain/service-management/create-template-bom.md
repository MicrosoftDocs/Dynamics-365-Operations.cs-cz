---
title: Vytvoření šablony kusovníku
description: Šablonu kusovníku lze vytvořit pomocí mnoha metod.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470755"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="d32a3-103">Vytvoření šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="d32a3-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d32a3-104">Šablonu kusovníku lze vytvořit pomocí kterékoli z následujících metod.</span><span class="sxs-lookup"><span data-stu-id="d32a3-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="d32a3-105">U všech těchto metod jsou pole **Od data** a **Do data** nepovinná a slouží pouze pro informaci.</span><span class="sxs-lookup"><span data-stu-id="d32a3-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="d32a3-106">Ruční vytvoření šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="d32a3-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="d32a3-107">Přejděte na **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d32a3-108">Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d32a3-109">Ve skupinovém rámečku **Kopírovat řádky kusovníku z odkazu** vyberte možnost **ruční**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="d32a3-110">Do pole **Číslo položky** zadejte položku typu **Kusovník**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="d32a3-111">Do pole **Název** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="d32a3-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d32a3-112">Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d32a3-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-113">Select **OK**.</span></span>

<span data-ttu-id="d32a3-114">Je vytvořena nová prázdná šablona kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="d32a3-115">Vytvoření šablony kusovníku na základě jiné šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="d32a3-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="d32a3-116">Vyberte **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d32a3-117">Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d32a3-118">Ve skupinovém rámečku **Kopírovat řádky kusovníku z odkazu** vyberte možnost **Šablona kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="d32a3-119">V poli **Referenční číslo** vyberte stávající šablonu kusovníku, kterou chcete zkopírovat do nové šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="d32a3-120">Do pole **Název** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="d32a3-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d32a3-121">Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d32a3-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-122">Select **OK**.</span></span>

<span data-ttu-id="d32a3-123">Je vytvořena nová šablona kusovníku pomocí řádků odpovídajících řádkům původní šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="d32a3-124">Vytvoření šablony kusovníku na základě kusovníku položky</span><span class="sxs-lookup"><span data-stu-id="d32a3-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="d32a3-125">Vyberte **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d32a3-126">Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d32a3-127">Ve skupinovém rámečku **Kopírování řádků kusovníku z odkazu** vyberte **Kusovník**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="d32a3-128">V poli **referenční číslo** vyberte verzi Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="d32a3-129">Položka typu kusovníku je zkopírována do **číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="d32a3-130">Do pole **Název** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="d32a3-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d32a3-131">Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d32a3-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-132">Select **OK**.</span></span>

<span data-ttu-id="d32a3-133">Je vytvořena nová šablona kusovníku s využitím řádků odpovídajících řádkům kusovníku uvedeného v poli **Kusovník**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="d32a3-134">Vytvoření šablony kusovníku na základě kusovníku výroby</span><span class="sxs-lookup"><span data-stu-id="d32a3-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="d32a3-135">Vyberte **Správa servisu** \> **Nastavení** \> **Servisní objekty** \> **Šablony kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="d32a3-136">Výběrem možnosti **Nový** otevřete formulář **Vytvořit šablonu kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="d32a3-137">Ve skupinovém rámečku **Kopírování řádků kusovníku z odkazu** vyberte **Výroba**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="d32a3-138">V poli **referenční číslo** vyberte kusovník výroby.</span><span class="sxs-lookup"><span data-stu-id="d32a3-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="d32a3-139">Do pole **Název** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="d32a3-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="d32a3-140">Do polí **Od data** a **Do data** zadejte datový interval platnosti této šablony kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d32a3-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="d32a3-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-141">Select **OK**.</span></span>

<span data-ttu-id="d32a3-142">Je vytvořena nová šablona kusovníku s využitím řádků odpovídajících řádkům kusovníku uvedeného v poli **BOM**.</span><span class="sxs-lookup"><span data-stu-id="d32a3-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d32a3-143">Viz také</span><span class="sxs-lookup"><span data-stu-id="d32a3-143">See also</span></span>

[<span data-ttu-id="d32a3-144">Kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="d32a3-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]