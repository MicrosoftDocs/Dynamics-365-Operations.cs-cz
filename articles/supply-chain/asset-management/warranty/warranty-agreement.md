---
title: Záruční smlouvy
description: Toto téma popisuje záruční smlouvy v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: da60d098aff96780ca1e40832db34e3c9cc835e7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569678"
---
# <a name="warranty-agreements"></a><span data-ttu-id="02082-103">Záruční smlouvy</span><span class="sxs-lookup"><span data-stu-id="02082-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="02082-104">V modulu Správa majetku můžete nastavit záruční podmínky, které mohou být spojeny s majetkem nebo typem majetku.</span><span class="sxs-lookup"><span data-stu-id="02082-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="02082-105">Jsou vytvořeny záruční podmínky pro určité období.</span><span class="sxs-lookup"><span data-stu-id="02082-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="02082-106">Záruku lze nastavit tak, aby poskytovala úplné pokrytí nebo částečné pokrytí, a můžete nastavit podmínky, které souvisejí s hodinami, výdaji a položkami.</span><span class="sxs-lookup"><span data-stu-id="02082-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="02082-107">Prvním krokem je vytvoření libovolných záručních smluv dodavatele, které máte pro své vybavení.</span><span class="sxs-lookup"><span data-stu-id="02082-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="02082-108">Poté připojíte záruční smlouvy k majetku nebo typům majetku.</span><span class="sxs-lookup"><span data-stu-id="02082-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="02082-109">Záruční smlouvy dodavatele se používají pouze pro informativní účely.</span><span class="sxs-lookup"><span data-stu-id="02082-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="02082-110">Pokud je u majetku nastavena záruka dodavatele, můžete zobrazit období krytí záruky majetku.</span><span class="sxs-lookup"><span data-stu-id="02082-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="02082-111">Vytvoření záruční smlouvy</span><span class="sxs-lookup"><span data-stu-id="02082-111">Create a warranty agreement</span></span>

<span data-ttu-id="02082-112">Záruční smlouva může zahrnovat několik řádků smlouvy, které pokryjí záruku za pracovní dobu, výdaje a položky.</span><span class="sxs-lookup"><span data-stu-id="02082-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="02082-113">Vyberte **Správa majetku** \> **Nastavení** \> **Majetek** \> **Záruka**.</span><span class="sxs-lookup"><span data-stu-id="02082-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="02082-114">Zvolte **Nový** pro vytvoření produktu.</span><span class="sxs-lookup"><span data-stu-id="02082-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="02082-115">V poli **Záruka** zadejte ID záruky.</span><span class="sxs-lookup"><span data-stu-id="02082-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="02082-116">Do pole **Název** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="02082-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="02082-117">Na pevné záložce **Podrobnosti** pole **Majetek** zobrazuje množství aktivního majetku, který používá záruční smlouvu.</span><span class="sxs-lookup"><span data-stu-id="02082-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="02082-118">Na pevných záložkách **Hodinová záruka** a **Položková záruka** přidejte řádky, které mají být zahrnuty do záruční smlouvy týkající se hodin nebo položek, pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="02082-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="02082-119">Zvolte **Přidat řádek** a přidejte k záruce novou podmínku.</span><span class="sxs-lookup"><span data-stu-id="02082-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="02082-120">Do pole **Řádek** se automaticky zadá pořadové číslo řádku.</span><span class="sxs-lookup"><span data-stu-id="02082-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="02082-121">V poli **Období** vyberte typ období záruky.</span><span class="sxs-lookup"><span data-stu-id="02082-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="02082-122">V poli **Interval** zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="02082-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="02082-123">Toto pole definuje počet období, pro která má být záruka platná.</span><span class="sxs-lookup"><span data-stu-id="02082-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="02082-124">V poli **Procento** zadejte procento disponibility pro řádek záruky.</span><span class="sxs-lookup"><span data-stu-id="02082-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="02082-125">Procentuální hodnota označuje, kolik je kryto vaší společností.</span><span class="sxs-lookup"><span data-stu-id="02082-125">The percentage indicates how much is covered by your company.</span></span>

![Stránka Záruka](media/01-warranty.png)
