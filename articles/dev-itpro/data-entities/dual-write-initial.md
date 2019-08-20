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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797291"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="02809-103">Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="02809-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="02809-104">Před použitím integrace dat je nutné vytvořit počáteční data potřebná pro zákazníky, dodavatele a kontakty.</span><span class="sxs-lookup"><span data-stu-id="02809-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="02809-105">Chcete-li například vytvořit novou položku **Skupina dodavatelů** a nastavit její **platební podmínky** jako **Net30**, pak před pokusem o vytvoření položky **skupiny dodavatelů** je nutné zajistit, aby **Net30** existovala jak v aplikaci Finance and Operations, tak v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="02809-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="02809-106">(V budoucnu bude vydána funkce platformy pro duální zápis nazvaná **Počáteční synchronizace**. Bude provádět jednočasovou synchronizaci dat mezi Finance and Operations a Common Data Service jako součást nastavení pro duální zápis.)</span><span class="sxs-lookup"><span data-stu-id="02809-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="02809-107">Tipy: Vydáváme mapu dvojího zápisu pro všechna referenční data včetně **platebních podmínek**.</span><span class="sxs-lookup"><span data-stu-id="02809-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="02809-108">Pokud již máte počáteční data v jednom systému, může malá operace aktualizace na záznamu spustit pro tento záznam dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="02809-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="02809-109">Je nutné postupovat podle následujícího pořadí priorit a zajistit, aby počáteční data byla k dispozici jak pro Finance and Operations, tak pro Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="02809-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="02809-110">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="02809-110">Vendor</span></span>

<span data-ttu-id="02809-111">Pořadí provedení pro dodavatele je následující:</span><span class="sxs-lookup"><span data-stu-id="02809-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="02809-112">Odběratel (organizace)</span><span class="sxs-lookup"><span data-stu-id="02809-112">Customer (Organization)</span></span>

<span data-ttu-id="02809-113">Pořadí provedení pro odběratele je následující:</span><span class="sxs-lookup"><span data-stu-id="02809-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="02809-114">Kontakt (osoba)</span><span class="sxs-lookup"><span data-stu-id="02809-114">Contact (Person)</span></span>

<span data-ttu-id="02809-115">Pořadí provedení pro kontakt je následující:</span><span class="sxs-lookup"><span data-stu-id="02809-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
