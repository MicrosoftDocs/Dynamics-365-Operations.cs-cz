---
title: Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky
description: Tento článek popisuje, jak vyloučit odlehlé hodnoty z historických dat, která se používají k výpočtu prognózy poptávky. Vyloučením odlehlých hodnot můžete zlepšit přesnost prognózy.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce8ebaf32b30c57b307f0d8799660ba6b42365a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "323610"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="369bd-104">Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="369bd-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="369bd-105">Tento článek popisuje, jak vyloučit odlehlé hodnoty z historických dat, která se používají k výpočtu prognózy poptávky.</span><span class="sxs-lookup"><span data-stu-id="369bd-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="369bd-106">Vyloučením odlehlých hodnot můžete zlepšit přesnost prognózy.</span><span class="sxs-lookup"><span data-stu-id="369bd-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="369bd-107">Přesnost prognózy můžete zlepšit vyloučením odlehlých hodnot.</span><span class="sxs-lookup"><span data-stu-id="369bd-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="369bd-108">Tato úloha je volitelná.</span><span class="sxs-lookup"><span data-stu-id="369bd-108">This is an optional task.</span></span> <span data-ttu-id="369bd-109">Přehled procesu:</span><span class="sxs-lookup"><span data-stu-id="369bd-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="369bd-110">Klikněte na **Hlavní plánování** &gt; **Nastavení** &gt; **Prognóza poptávky** &gt; **Odebrání odlehlé hodnoty**. Otevře se stránka **Odebrání odlehlé hodnoty**, na které můžete pomocí dotazu vybrat transakce k vyloučení.</span><span class="sxs-lookup"><span data-stu-id="369bd-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="369bd-111">Vyberte společnost, pro kterou se použije dotaz, a pak zadejte název a popis.</span><span class="sxs-lookup"><span data-stu-id="369bd-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="369bd-112">Pole **Datum dotazu** je automaticky nastaveno na aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="369bd-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="369bd-113">Zaškrtněte políčko **Aktivní**, chcete-li vyloučit transakce, které byly nalezeny dotazem, z historických dat.</span><span class="sxs-lookup"><span data-stu-id="369bd-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="369bd-114">Toto nastavení se projeví při vytváření základní prognózy.</span><span class="sxs-lookup"><span data-stu-id="369bd-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="369bd-115">Na stránce **Dotaz na odebrání odlehlé hodnoty** lze přidat, odebrat a vybrat kritéria, která definují transakce, které budou vyloučeny při výpočtu základní prognózy.</span><span class="sxs-lookup"><span data-stu-id="369bd-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="369bd-116">Například vyberte konkrétní položku nebo transakci zakázky, kterou chcete vyloučit.</span><span class="sxs-lookup"><span data-stu-id="369bd-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="369bd-117">Klikněte na možnost **Zobrazit transakce**.</span><span class="sxs-lookup"><span data-stu-id="369bd-117">Click **Display transactions**.</span></span> <span data-ttu-id="369bd-118">Stránka **Transakce odlehlé hodnoty** uvádí seznam transakcí, které splňují kritéria, která jste definovali v dotazu, a které budou vyloučeny z historických dat při výpočtu prognózy poptávky.</span><span class="sxs-lookup"><span data-stu-id="369bd-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="369bd-119">**Poznámka:** Můžete také vytvořit dotaz, který vychází z existujícího dotazu.</span><span class="sxs-lookup"><span data-stu-id="369bd-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="369bd-120">Vyberte dotaz, který se má kopírovat, a klikněte na možnost **Duplikovat**.</span><span class="sxs-lookup"><span data-stu-id="369bd-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="369bd-121">Pole **Datum dotazu** určuje verzi.</span><span class="sxs-lookup"><span data-stu-id="369bd-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="369bd-122">Můžete vybrat dotaz, jak je, nebo můžete kliknout na možnost **Upravit dotaz**, chcete-li změnit kritéria.</span><span class="sxs-lookup"><span data-stu-id="369bd-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="369bd-123">Volitelně můžete upravit název a popis nového dotazu.</span><span class="sxs-lookup"><span data-stu-id="369bd-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="369bd-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="369bd-124">Additional resources</span></span>
--------

[<span data-ttu-id="369bd-125">Úvod do prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="369bd-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="369bd-126">Měření přesnosti prognózy</span><span class="sxs-lookup"><span data-stu-id="369bd-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)



