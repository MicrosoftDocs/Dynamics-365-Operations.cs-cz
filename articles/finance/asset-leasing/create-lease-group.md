---
title: Vytvoření skupiny leasingu
description: Toto téma vysvětluje, jak nastavit skupiny leasingu. Skupiny leasingu jsou nutné k vytvoření nových leasingů.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88a49e4db868078fd05875df33ca5727363aaa18
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881221"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="74167-104">Vytvoření skupiny leasingu</span><span class="sxs-lookup"><span data-stu-id="74167-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74167-105">Toto téma vysvětluje, jak nastavit skupiny leasingu.</span><span class="sxs-lookup"><span data-stu-id="74167-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="74167-106">Skupiny leasingu jsou nutné k vytvoření nových leasingů.</span><span class="sxs-lookup"><span data-stu-id="74167-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="74167-107">Leasingové knihy jsou přidruženy ke každé skupině leasingu.</span><span class="sxs-lookup"><span data-stu-id="74167-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="74167-108">Leasingové knihy určují výchozí knihy, které musí být vytvořeny pro každý leasing.</span><span class="sxs-lookup"><span data-stu-id="74167-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="74167-109">Konkrétní účty můžete přiřadit skupině leasingu na stránce **Parametry zaúčtování leasingu**.</span><span class="sxs-lookup"><span data-stu-id="74167-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="74167-110">Vytvořte leasingovou knihu a přidejte skupinu leasingu</span><span class="sxs-lookup"><span data-stu-id="74167-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="74167-111">Přejděte na **Leasing majetku \> Nastavení \> Skupiny leasingu**.</span><span class="sxs-lookup"><span data-stu-id="74167-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="74167-112">V podokně Akce volbou **Nový** přidejte skupinu leasingu.</span><span class="sxs-lookup"><span data-stu-id="74167-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="74167-113">Do mřížky je přidán řádek.</span><span class="sxs-lookup"><span data-stu-id="74167-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="74167-114">Na novém řádku v poli **Skupina leasingu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74167-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="74167-115">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74167-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="74167-116">Informace, které jste právě zadali, se přidají do pole **Skupina leasingu** na stránce **Přidat leasing**.</span><span class="sxs-lookup"><span data-stu-id="74167-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="74167-117">Přidružení knihy ke skupině leasingu</span><span class="sxs-lookup"><span data-stu-id="74167-117">Associate a book with a lease group</span></span>

<span data-ttu-id="74167-118">Po vytvoření skupin leasingu můžete ke každé skupině přiřadit knihy.</span><span class="sxs-lookup"><span data-stu-id="74167-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="74167-119">Když vytvoříte leasing a přiřadíte jej ke skupině leasingu, systém vytvoří sadu plánů pro každou knihu, která je přidružena k dané skupině leasingu.</span><span class="sxs-lookup"><span data-stu-id="74167-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="74167-120">Knihy je třeba vytvořit, než je lze přiřadit ke skupině leasingu.</span><span class="sxs-lookup"><span data-stu-id="74167-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="74167-121">Přejděte na **Leasing majetku \> Nastavení \> Skupina leasingu**.</span><span class="sxs-lookup"><span data-stu-id="74167-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="74167-122">Vyberte skupinu leasingu a poté vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="74167-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="74167-123">Vyberte **Nový** a poté v poli **Typ knihy** vyberte knihu, kterou chcete přiřadit do skupiny leasingu.</span><span class="sxs-lookup"><span data-stu-id="74167-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="74167-124">Skupině leasingu můžete přiřadit více knih, pokud musí být leasing účtován různými způsoby.</span><span class="sxs-lookup"><span data-stu-id="74167-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
