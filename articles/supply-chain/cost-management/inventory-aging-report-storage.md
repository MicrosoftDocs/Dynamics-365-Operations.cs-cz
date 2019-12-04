---
title: Sestava prodlení zásob
description: V tomto tématu je popsána funkce, která umožňuje spustit sestavu sledování splatnosti zásob a zpřístupnit výstup jako formulář a graf.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810244"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="1601a-103">Sestava prodlení zásob</span><span class="sxs-lookup"><span data-stu-id="1601a-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1601a-104">V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete spustit sestavu **Prodlení zásob** a zpřístupnit výstup jako formulář a graf.</span><span class="sxs-lookup"><span data-stu-id="1601a-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="1601a-105">Ve formuláři jsou sloupce a agregované zůstatky v závislosti na konfigurovaném rozvržení dynamicky upravovány.</span><span class="sxs-lookup"><span data-stu-id="1601a-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="1601a-106">Graf poskytuje vizuální přehled, který podporuje filtrování a umožňuje důkladné procházení podrobností.</span><span class="sxs-lookup"><span data-stu-id="1601a-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="1601a-107">Dále vám datová entita nazvaná **Sestava zastarávání zásad** umožňuje exportovat výsledky sestavy **Prodlení zásob** spuštění ve formátu, jako je soubor Microsoft Excel nebo PDF.</span><span class="sxs-lookup"><span data-stu-id="1601a-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="1601a-108">Tato metoda spuštění sestavy **Prodlení zásob** je užitečná v případech, kdy výstup obsahuje mnoho řádků.</span><span class="sxs-lookup"><span data-stu-id="1601a-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="1601a-109">Výstup bude například obsahovat mnoho řádků, pokud máte 50 000 položek a 300 obchodů, které jsou vytvořeny jako sklady, a požadujete splatnost zásob podle položky, pracoviště a skladu.</span><span class="sxs-lookup"><span data-stu-id="1601a-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="1601a-110">Spuštění sestavy prodlení zásob</span><span class="sxs-lookup"><span data-stu-id="1601a-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="1601a-111">Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy zastarávání zásob**.</span><span class="sxs-lookup"><span data-stu-id="1601a-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="1601a-112">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="1601a-112">Select **New**.</span></span>
1. <span data-ttu-id="1601a-113">V poli **Identifikátor procesu - název** zadejte jedinečný název sestavy.</span><span class="sxs-lookup"><span data-stu-id="1601a-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="1601a-114">Vyberte sestavu **Identifikace – ID** a filtrujte ji podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="1601a-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="1601a-115">Spuštění sestavy je vždy provedeno v dávkové úloze.</span><span class="sxs-lookup"><span data-stu-id="1601a-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="1601a-116">Po dokončení dávkové úlohy se výstup zobrazí na stránce **Úložiště sestavy prodlení zásob**.</span><span class="sxs-lookup"><span data-stu-id="1601a-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="1601a-117">Chcete-li zobrazit výstup jako formulář s tradičním rozvržením mřížky, vyberte možnost **zobrazit podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="1601a-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="1601a-118">Chcete-li zobrazit výstup jako agregovaný graf, vyberte možnost **zobrazit graf**.</span><span class="sxs-lookup"><span data-stu-id="1601a-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1601a-119">Ve formuláři nebudou zahrnuty mezisoučty definované v rozvržení sestavy.</span><span class="sxs-lookup"><span data-stu-id="1601a-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="1601a-120">Datová entita **Sestava prodlení zásob** umožňuje exportovat výstup sestavy **Zastarávání zásob** použitím filtru pro pole **Identifikátor procesu – název** na libovolný formát, který správa dat podporuje.</span><span class="sxs-lookup"><span data-stu-id="1601a-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
