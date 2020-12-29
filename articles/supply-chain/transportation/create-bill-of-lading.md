---
title: Vytvoření přepravního dokladu
description: Toto téma popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd014f5804681936920b47e999709f153def11bc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424232"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="42280-103">Vytvoření přepravního dokladu</span><span class="sxs-lookup"><span data-stu-id="42280-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42280-104">Toto téma popisuje, jak vytvořit přepravní doklad při používání procesů pro řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="42280-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="42280-105">Přepravní doklad je právním dokumentem mezi společností, která dodává položky, a dopravcem.</span><span class="sxs-lookup"><span data-stu-id="42280-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="42280-106">Dokument doprovází dodané položky a slouží jako potvrzení expedice při dodání položek do cílového umístění.</span><span class="sxs-lookup"><span data-stu-id="42280-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="42280-107">Jestliže používáte řízení skladu, existují dva způsoby, jak přepravní doklad generovat:</span><span class="sxs-lookup"><span data-stu-id="42280-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="42280-108">Vytvoření sestavy ručně pomocí stránky **Přepravní doklad**.</span><span class="sxs-lookup"><span data-stu-id="42280-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="42280-109">Generování sestavy z **pracovní plochy plánování vytížení**.</span><span class="sxs-lookup"><span data-stu-id="42280-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="42280-110">Pokud generujete přepravní doklad z **pracovní plochy plánování vytížení**, stav vytížení musí být **Expedováno**.</span><span class="sxs-lookup"><span data-stu-id="42280-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="42280-111">Pokud existuje více než jedna dodávka v nákladu, u každé dodávky dojde k vytvoření jednoho přepravního dokladu.</span><span class="sxs-lookup"><span data-stu-id="42280-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="42280-112">Poté, co byl přepravní doklad vytvořen, můžete provést jeho změny na stránce **Přepravní doklad**.</span><span class="sxs-lookup"><span data-stu-id="42280-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="42280-113">Hlavní přepravní doklad</span><span class="sxs-lookup"><span data-stu-id="42280-113">Master bill of lading</span></span>
<span data-ttu-id="42280-114">Pokud je ve vytížení více než jedna dodávka, můžete vygenerovat hlavní přepravní doklad.</span><span class="sxs-lookup"><span data-stu-id="42280-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="42280-115">Ten má stejné rozvržení a obsahuje stejné informace jako přepravní doklad, ale obsahuje souhrnný obsah všech dodávek.</span><span class="sxs-lookup"><span data-stu-id="42280-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="42280-116">Pokud možnost **Vytvořit hlavní přepravní doklad, když je ve vytížení více než jedna dodávka** nastavíte na **Ano** na stránce **Parametry správy přepravy**, hlavní přepravní doklad bude vygenerován automaticky po vytvoření přepravního dokladu z **pracovní plochy plánování vytížení**, existuje-li více než jedna dodávka.</span><span class="sxs-lookup"><span data-stu-id="42280-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="42280-117">Seznam přepravních dokladů získáte rovněž kliknutím na **Související informace** &gt; **Přepravní doklad**.</span><span class="sxs-lookup"><span data-stu-id="42280-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="42280-118">Pokud vytváříte přepravní doklad ručně, můžete hlavní přepravní doklad vytvořit na stránce **Přepravní doklad**.</span><span class="sxs-lookup"><span data-stu-id="42280-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



