---
title: Uložení sestavy stáří zásob
description: V tomto tématu je popsána funkce, která umožňuje spustit sestavu sledování splatnosti zásob a zpřístupnit výstup jako formulář a graf.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40b15448677f319c650c667cd7c4981c343f7a02
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205339"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="20e68-103">Uložení sestavy stáří zásob</span><span class="sxs-lookup"><span data-stu-id="20e68-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20e68-104">V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete spustit sestavu **Úložiště sestavy prodlení zásob** a zpřístupnit výstup jako formulář a graf.</span><span class="sxs-lookup"><span data-stu-id="20e68-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="20e68-105">Ve formuláři jsou sloupce a agregované zůstatky v závislosti na konfigurovaném rozvržení dynamicky upravovány.</span><span class="sxs-lookup"><span data-stu-id="20e68-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="20e68-106">Graf poskytuje vizuální přehled, který podporuje filtrování a umožňuje důkladné procházení podrobností.</span><span class="sxs-lookup"><span data-stu-id="20e68-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="20e68-107">Dále vám datová entita nazvaná **Sestava zastarávání zásad** umožňuje exportovat výsledky sestavy **Úložiště sestavy prodlení zásob** spuštění ve formátu, jako je soubor Microsoft Excel nebo PDF.</span><span class="sxs-lookup"><span data-stu-id="20e68-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="20e68-108">Tato metoda spuštění sestavy **Úložiště sestavy prodlení zásob** je užitečná v případech, kdy výstup obsahuje mnoho řádků.</span><span class="sxs-lookup"><span data-stu-id="20e68-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="20e68-109">Výstup bude například obsahovat mnoho řádků, pokud máte 50 000 položek a 300 obchodů, které jsou vytvořeny jako sklady, a požadujete splatnost zásob podle položky, pracoviště a skladu.</span><span class="sxs-lookup"><span data-stu-id="20e68-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="20e68-110">Povolení funkce sestavy úložiště hodnot zásob</span><span class="sxs-lookup"><span data-stu-id="20e68-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="20e68-111">Než můžete použít tuto funkci, musíte ji povolit ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="20e68-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="20e68-112">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="20e68-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="20e68-113">Tato funkce je uvedena jako:</span><span class="sxs-lookup"><span data-stu-id="20e68-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="20e68-114">**Modul** - Správa nákladů</span><span class="sxs-lookup"><span data-stu-id="20e68-114">**Module** - Cost management</span></span>
- <span data-ttu-id="20e68-115">**Název funkce** - Úložiště sestavy prodlení zásob</span><span class="sxs-lookup"><span data-stu-id="20e68-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="20e68-116">Spuštění úložiště sestavy prodlení zásob</span><span class="sxs-lookup"><span data-stu-id="20e68-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="20e68-117">Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy zastarávání zásob**.</span><span class="sxs-lookup"><span data-stu-id="20e68-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="20e68-118">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="20e68-118">Select **New**.</span></span>
1. <span data-ttu-id="20e68-119">V poli **Identifikátor procesu - název** zadejte jedinečný název sestavy.</span><span class="sxs-lookup"><span data-stu-id="20e68-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="20e68-120">Vyberte sestavu **Identifikace – ID** a filtrujte ji podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="20e68-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="20e68-121">Spuštění sestavy je vždy provedeno v dávkové úloze.</span><span class="sxs-lookup"><span data-stu-id="20e68-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="20e68-122">Po dokončení dávkové úlohy se výstup zobrazí na stránce **Úložiště sestavy prodlení zásob**.</span><span class="sxs-lookup"><span data-stu-id="20e68-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="20e68-123">Chcete-li zobrazit výstup jako formulář s tradičním rozvržením mřížky, vyberte možnost **zobrazit podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="20e68-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="20e68-124">Chcete-li zobrazit výstup jako agregovaný graf, vyberte možnost **zobrazit graf**.</span><span class="sxs-lookup"><span data-stu-id="20e68-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="20e68-125">Ve formuláři nebudou zahrnuty mezisoučty definované v rozvržení sestavy.</span><span class="sxs-lookup"><span data-stu-id="20e68-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="20e68-126">Datová entita **Sestava prodlení zásob** umožňuje exportovat výstup sestavy **Úložiště sestavy prodlení zásob** použitím filtru pro pole **Identifikátor procesu – název** na libovolný formát, který správa dat podporuje.</span><span class="sxs-lookup"><span data-stu-id="20e68-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]