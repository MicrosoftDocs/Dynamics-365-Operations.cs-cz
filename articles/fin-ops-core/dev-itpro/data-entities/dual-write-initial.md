---
title: Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service
description: Toto téma popisuje pořadí synchronizace, které je nutné provést při vytváření počátečních dat.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184501"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="8ee8a-103">Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8ee8a-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="8ee8a-104">Před použitím integrace dat je nutné vytvořit počáteční data potřebná pro zákazníky, dodavatele a kontakty.</span><span class="sxs-lookup"><span data-stu-id="8ee8a-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="8ee8a-105">Chcete například vytvořit novou položku **Skupina dodavatelů** a nastavit její hodnotu **Platebních podmínek** na **Net30**.</span><span class="sxs-lookup"><span data-stu-id="8ee8a-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="8ee8a-106">V takovém případě se před pokusem o vytvoření položky **Skupiny dodavatelů** ujistěte, že **Net30** existuje v aplikaci a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8ee8a-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="8ee8a-107">(V budoucnu vydá Microsoft funkce platformy pro duální zápis nazvanou Počáteční synchronizace. Ta bude provádět jednočasovou synchronizaci dat mezi aplikací a Common Data Service jako součást nastavení pro duální zápis.)</span><span class="sxs-lookup"><span data-stu-id="8ee8a-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="8ee8a-108">Microsoft vydává mapu dvojího zápisu pro všechna referenční data, včetně **platebních podmínek** (podmínek platby).</span><span class="sxs-lookup"><span data-stu-id="8ee8a-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="8ee8a-109">Pokud již máte počáteční data v jednom systému, může malá operace aktualizace na záznamu spustit pro tento záznam dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="8ee8a-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="8ee8a-110">Je nutné postupovat podle následujícího pořadí priorit a zajistit, aby počáteční data byla k dispozici jak pro aplikaci, tak pro Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8ee8a-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="8ee8a-111">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="8ee8a-111">Vendor</span></span>

<span data-ttu-id="8ee8a-112">Zde je pořadí provádění entity **Dodavatel**:</span><span class="sxs-lookup"><span data-stu-id="8ee8a-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="8ee8a-113">Skupina dodavatelů</span><span class="sxs-lookup"><span data-stu-id="8ee8a-113">Vendor group</span></span>

    1. <span data-ttu-id="8ee8a-114">Platební podmínky</span><span class="sxs-lookup"><span data-stu-id="8ee8a-114">Terms of payment</span></span>

        1. <span data-ttu-id="8ee8a-115">Den a řádky platby</span><span class="sxs-lookup"><span data-stu-id="8ee8a-115">Payment day and lines</span></span>
        2. <span data-ttu-id="8ee8a-116">Platební kalendář</span><span class="sxs-lookup"><span data-stu-id="8ee8a-116">Payment schedule</span></span>

2. <span data-ttu-id="8ee8a-117">Platební metoda dodavatele</span><span class="sxs-lookup"><span data-stu-id="8ee8a-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="8ee8a-118">Odběratel (organizace)</span><span class="sxs-lookup"><span data-stu-id="8ee8a-118">Customer (Organization)</span></span>

<span data-ttu-id="8ee8a-119">Zde je pořadí provádění entity **Odběratel**:</span><span class="sxs-lookup"><span data-stu-id="8ee8a-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="8ee8a-120">Skupina odběratelů</span><span class="sxs-lookup"><span data-stu-id="8ee8a-120">Customer group</span></span>

    1. <span data-ttu-id="8ee8a-121">Platební podmínky</span><span class="sxs-lookup"><span data-stu-id="8ee8a-121">Terms of payment</span></span>

        1. <span data-ttu-id="8ee8a-122">Den a řádky platby</span><span class="sxs-lookup"><span data-stu-id="8ee8a-122">Payment day and lines</span></span>
        2. <span data-ttu-id="8ee8a-123">Platba</span><span class="sxs-lookup"><span data-stu-id="8ee8a-123">Payment</span></span> 

2. <span data-ttu-id="8ee8a-124">Způsob platby odběratele</span><span class="sxs-lookup"><span data-stu-id="8ee8a-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="8ee8a-125">Kontakt (osoba)</span><span class="sxs-lookup"><span data-stu-id="8ee8a-125">Contact (Person)</span></span>

<span data-ttu-id="8ee8a-126">Zde je pořadí provádění entity **Kontakt**:</span><span class="sxs-lookup"><span data-stu-id="8ee8a-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="8ee8a-127">Zákazník</span><span class="sxs-lookup"><span data-stu-id="8ee8a-127">Customer</span></span>
2. <span data-ttu-id="8ee8a-128">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="8ee8a-128">Vendor</span></span>
