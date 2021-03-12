---
title: Vytvoření skupiny leasingu
description: Toto téma vysvětluje, jak nastavit skupiny leasingu. Skupiny leasingu jsou nutné k vytvoření nových leasingů.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c06f6f943c8a47fbe650a67017b95d799914a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971346"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="22cb1-104">Vytvoření skupiny leasingu</span><span class="sxs-lookup"><span data-stu-id="22cb1-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22cb1-105">Toto téma vysvětluje, jak nastavit skupiny leasingu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="22cb1-106">Skupiny leasingu jsou nutné k vytvoření nových leasingů.</span><span class="sxs-lookup"><span data-stu-id="22cb1-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="22cb1-107">Leasingové knihy jsou přidruženy ke každé skupině leasingu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="22cb1-108">Leasingové knihy určují výchozí knihy, které musí být vytvořeny pro každý leasing.</span><span class="sxs-lookup"><span data-stu-id="22cb1-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="22cb1-109">Konkrétní účty můžete přiřadit skupině leasingu na stránce **Parametry zaúčtování leasingu**.</span><span class="sxs-lookup"><span data-stu-id="22cb1-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="22cb1-110">Vytvořte leasingovou knihu a přidejte skupinu leasingu</span><span class="sxs-lookup"><span data-stu-id="22cb1-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="22cb1-111">Přejděte na **Leasing majetku \> Nastavení \> Skupiny leasingu**.</span><span class="sxs-lookup"><span data-stu-id="22cb1-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="22cb1-112">V podokně Akce volbou **Nový** přidejte skupinu leasingu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="22cb1-113">Do mřížky je přidán řádek.</span><span class="sxs-lookup"><span data-stu-id="22cb1-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="22cb1-114">Na novém řádku v poli **Skupina leasingu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="22cb1-115">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="22cb1-116">Informace, které jste právě zadali, se přidají do pole **Skupina leasingu** na stránce **Přidat leasing**.</span><span class="sxs-lookup"><span data-stu-id="22cb1-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="22cb1-117">Přidružení knihy ke skupině leasingu</span><span class="sxs-lookup"><span data-stu-id="22cb1-117">Associate a book with a lease group</span></span>

<span data-ttu-id="22cb1-118">Po vytvoření skupin leasingu můžete ke každé skupině přiřadit knihy.</span><span class="sxs-lookup"><span data-stu-id="22cb1-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="22cb1-119">Když vytvoříte leasing a přiřadíte jej ke skupině leasingu, systém vytvoří sadu plánů pro každou knihu, která je přidružena k dané skupině leasingu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="22cb1-120">Knihy je třeba vytvořit, než je lze přiřadit ke skupině leasingu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="22cb1-121">Přejděte na **Leasing majetku \> Nastavení \> Skupina leasingu**.</span><span class="sxs-lookup"><span data-stu-id="22cb1-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="22cb1-122">Vyberte skupinu leasingu a poté vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="22cb1-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="22cb1-123">Vyberte **Nový** a poté v poli **Typ knihy** vyberte knihu, kterou chcete přiřadit do skupiny leasingu.</span><span class="sxs-lookup"><span data-stu-id="22cb1-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="22cb1-124">Skupině leasingu můžete přiřadit více knih, pokud musí být leasing účtován různými způsoby.</span><span class="sxs-lookup"><span data-stu-id="22cb1-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>