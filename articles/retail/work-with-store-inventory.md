---
title: "Správa skladových zásob"
description: "Tento článek popisuje typy dokumentů, které můžete použít ke správě zásob."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: e61dc863169d70fd4d383120a6ebcebb8682b33c
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="store-inventory-management"></a><span data-ttu-id="9717c-103">Správa skladových zásob</span><span class="sxs-lookup"><span data-stu-id="9717c-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9717c-104">Tento článek popisuje typy dokumentů, které můžete použít ke správě zásob.</span><span class="sxs-lookup"><span data-stu-id="9717c-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="9717c-105">Typy následující dokumentů slouží ke správě skladových zásob v organizaci.</span><span class="sxs-lookup"><span data-stu-id="9717c-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="9717c-106">Nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="9717c-106">Purchase orders</span></span>

<span data-ttu-id="9717c-107">Nákupní objednávky se vytvářejí v ústředí.</span><span class="sxs-lookup"><span data-stu-id="9717c-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="9717c-108">Pokud je maloobchodní sklad zahrnut v záhlaví nákupní objednávky, objednávku lze přijmout v obchodě pomocí řešení Modern POS (MPOS) nebo Cloud POS v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="9717c-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="9717c-109">Po zadání množství, která jsou přijata v obchodě, mohou být tato množství místně uložena pro další úpravy.</span><span class="sxs-lookup"><span data-stu-id="9717c-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9717c-110">Množství lze také potvrdit a odeslat do ústředí.</span><span class="sxs-lookup"><span data-stu-id="9717c-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9717c-111">V ústředí se množství, které bylo přijato v obchodě, zobrazuje v aplikaci Microsoft Dynamics 365 for Retail, v poli **Přijmout nyní** v nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="9717c-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="9717c-112">Převodní příkazy</span><span class="sxs-lookup"><span data-stu-id="9717c-112">Transfer orders</span></span>

<span data-ttu-id="9717c-113">Převodní příkaz může stanovit, že určitý obchod je místo, ze kterého mohou být položky expedovány.</span><span class="sxs-lookup"><span data-stu-id="9717c-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="9717c-114">V tomto případě se převodní příkaz zobrazí v obchodě jako požadavek vyskladnění v MPOS nebo Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="9717c-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9717c-115">Jakmile jsou požadovaná množství vyskladněna, jsou potvrzena a odeslána do ústředí.</span><span class="sxs-lookup"><span data-stu-id="9717c-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="9717c-116">V ústředí se množství, které bylo vyzvednuto v obchodě, zobrazuje v aplikaci Microsoft Dynamics 365 for Retail v poli **Expedovat nyní** v převodním příkazu.</span><span class="sxs-lookup"><span data-stu-id="9717c-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="9717c-117">Převodní příkaz může stanovit, že určitý obchod je místo, do kterého mohou být položky expedovány.</span><span class="sxs-lookup"><span data-stu-id="9717c-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="9717c-118">V tomto případě se převodní příkaz zobrazí v obchodě jako příjmová žádanka v MPOS nebo Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="9717c-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9717c-119">Po zadání množství, která jsou přijata v obchodě, mohou být tato množství místně uložena pro další úpravy.</span><span class="sxs-lookup"><span data-stu-id="9717c-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9717c-120">Množství lze také potvrdit a odeslat do ústředí.</span><span class="sxs-lookup"><span data-stu-id="9717c-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9717c-121">V ústředí se množství, které bylo přijato v obchodě, zobrazuje v aplikaci Microsoft Dynamics 365 for Retail, v poli **Přijmout nyní** v převodní objednávce.</span><span class="sxs-lookup"><span data-stu-id="9717c-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="9717c-122">Počty na skladě</span><span class="sxs-lookup"><span data-stu-id="9717c-122">Stock counts</span></span>

<span data-ttu-id="9717c-123">Inventury mohou být plánované nebo neplánované.</span><span class="sxs-lookup"><span data-stu-id="9717c-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="9717c-124">Plánované inventury zahajuje ústředí, které také určuje, které položky musí být spočítány.</span><span class="sxs-lookup"><span data-stu-id="9717c-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="9717c-125">Ústředí vytvoří dokument inventury skladu, který lze přijmout v obchodě, kde jsou množství skutečných zásob na skladě zadána v MPOS nebo Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="9717c-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="9717c-126">Neplánované maloobchodní inventury jsou zahájeny v obchodě a množství skutečných zásob na skladě jsou aktualizována v MPOS nebo Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="9717c-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="9717c-127">Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek.</span><span class="sxs-lookup"><span data-stu-id="9717c-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="9717c-128">Po dokončení obou typů inventury budou potvrzeny a odeslány do ústředí.</span><span class="sxs-lookup"><span data-stu-id="9717c-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="9717c-129">V ústředí bude inventura ověřena a zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="9717c-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="9717c-130">Vyhledávání zásob</span><span class="sxs-lookup"><span data-stu-id="9717c-130">Inventory lookup</span></span>

<span data-ttu-id="9717c-131">Na stránce vyhledávání zásob lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů.</span><span class="sxs-lookup"><span data-stu-id="9717c-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="9717c-132">Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod.</span><span class="sxs-lookup"><span data-stu-id="9717c-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="9717c-133">Chcete-li tak učinit, vyberte obchod, pro který chcete zobrazit ATP, a klikněte na **Zobrazit dostupnost obchodu**.</span><span class="sxs-lookup"><span data-stu-id="9717c-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>

