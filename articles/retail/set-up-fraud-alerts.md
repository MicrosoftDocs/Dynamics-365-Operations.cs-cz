---
title: "Nastavit upozornění na podvod"
description: "Toto téma vysvětluje, jak nastavit pravidla výstrahy pro zástupce z oddělení služeb zákazníkům zaměřené na potenciálně podvodné informace při zpracování objednávek. Můžete definovat zvláštní kódy, které jsou automaticky nebo ručně použity k blokování podezřelých objednávek."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="ebeb8-104">Nastavit upozornění na podvod</span><span class="sxs-lookup"><span data-stu-id="ebeb8-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ebeb8-105">Toto téma vysvětluje, jak nastavit pravidla výstrahy pro zástupce z oddělení služeb zákazníkům zaměřené na potenciálně podvodné informace při zpracování objednávek.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="ebeb8-106">Můžete definovat zvláštní kódy, které jsou automaticky nebo ručně použity k blokování podezřelých objednávek.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="ebeb8-107">Před nastavením a použitím pravidel pro zjišťování podvodů musíte povolit zjišťování podvodů a definovat základní hodnoty zjišťování podvodů v parametrech kontaktních středisek.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="ebeb8-108">Existují dva typy pravidel podvodů:</span><span class="sxs-lookup"><span data-stu-id="ebeb8-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="ebeb8-109">**Statická pravidla** používají určitou hodnotu, jako je například telefonní číslo, které má být zakázáno.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="ebeb8-110">**Dynamická pravidla** mohou být složena z proměnných a podmínek.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="ebeb8-111">Než vytvoříte dynamické pravidlo, je nutné vytvořit proměnné a podmínky, které definují, koho se pravidla týkají, a kdy se pravidla mají použít.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="ebeb8-112">Chcete například vytvořit pravidlo, které vyžaduje, aby jakákoli prodejní objednávka, kterou odběratel 1202 vystaví v ceně 1 000,00 nebo více jednotek, byla blokována, dokud se neověří platba odběratele.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="ebeb8-113">V tomto případu je proměnná odběratel 1202 a celková objednávka 1 000,00 jednotek.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="ebeb8-114">Podmínka určuje, že pokud odběratel 1202 vystaví objednávku a celková částka na objednávce je rovna nebo více než 1 000,00, prodejní objednávku je nutné blokovat, dokud lze ověřit platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="ebeb8-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




