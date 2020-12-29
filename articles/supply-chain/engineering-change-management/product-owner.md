---
title: Vlastníci produktů
description: Toto téma poskytuje informace o vlastnících produktu. Vlastník produktu je skupina uživatelů, kteří odpovídají za konkrétní produkty. Tyto produkty mohou uvolňovat pouze členové skupiny. Vlastníka produktu lze také použít v pracovním postupu schválení.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424262"
---
# <a name="product-owners"></a><span data-ttu-id="de001-106">Vlastníci produktů</span><span class="sxs-lookup"><span data-stu-id="de001-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de001-107">Vlastník produktu je skupina uživatelů, kteří odpovídají za konkrétní produkty.</span><span class="sxs-lookup"><span data-stu-id="de001-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="de001-108">Pokud je produktu přiřazena skupina vlastníků produktů, mohou produkt uvolnit pouze členové této skupiny.</span><span class="sxs-lookup"><span data-stu-id="de001-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="de001-109">Vlastníka produktu lze také použít v pracovním postupu schválení ve správě technických změn.</span><span class="sxs-lookup"><span data-stu-id="de001-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="de001-110">Vlastníci produktů jsou globální nastavení.</span><span class="sxs-lookup"><span data-stu-id="de001-110">Product owners are global settings.</span></span> <span data-ttu-id="de001-111">Proto jsou k dispozici všem právnickým osobám.</span><span class="sxs-lookup"><span data-stu-id="de001-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="de001-112">Vytvoření skupiny vlastníků produktů</span><span class="sxs-lookup"><span data-stu-id="de001-112">Create a product owner group</span></span>

<span data-ttu-id="de001-113">Chcete-li vytvořit skupinu vlastníků produktů a přidat do ní členy, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="de001-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="de001-114">Jděte na **Správa technických změn \> Nastavení \> Vlastníci produktu**.</span><span class="sxs-lookup"><span data-stu-id="de001-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="de001-115">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="de001-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="de001-116">V poli **Vlastník produktu** zadejte název skupiny.</span><span class="sxs-lookup"><span data-stu-id="de001-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="de001-117">Do pole **Název** zadejte popis skupiny.</span><span class="sxs-lookup"><span data-stu-id="de001-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="de001-118">Na záložce s náhledem **Členové** přidejte pracovníky, kteří by měli být členy skupiny.</span><span class="sxs-lookup"><span data-stu-id="de001-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="de001-119">Přiřazení vlastníka produktu k produktu</span><span class="sxs-lookup"><span data-stu-id="de001-119">Assign a product owner to a product</span></span>

<span data-ttu-id="de001-120">Pokud chcete k produktu přiřadit vlastníka produktu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="de001-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="de001-121">Otevřete stránku **Podrobnosti produktu** pro příslušný produkt nebo základní produkt.</span><span class="sxs-lookup"><span data-stu-id="de001-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="de001-122">Na záložce s náhledem **Obecné** nastavte pole **Vlastník produktu** na název příslušné skupiny vlastníků produktů.</span><span class="sxs-lookup"><span data-stu-id="de001-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="de001-123">Zatímco je vlastník produktu přiřazen k produktu, mohou nastavení **Vlastník produktu** upravovat pouze členové skupiny vlastníků produktu.</span><span class="sxs-lookup"><span data-stu-id="de001-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="de001-124">Vlastník produktu je také viditelný na stránce **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="de001-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="de001-125">Vlastníci produktů a uvolnění produktů</span><span class="sxs-lookup"><span data-stu-id="de001-125">Product owners and product releases</span></span>

<span data-ttu-id="de001-126">Tento produkt mohou uvolnit pouze uživatelé ze skupiny vlastníků produktů.</span><span class="sxs-lookup"><span data-stu-id="de001-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="de001-127">Existuje však výjimka, když je produkt podřízenou položkou a jeho nadřazená položka je uvolněna vlastníkem nadřazené položky.</span><span class="sxs-lookup"><span data-stu-id="de001-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="de001-128">Jinými slovy, pokud je produkt součástí kusovníku jiného produktu, systém nekontroluje vlastníka produktu každé položky v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="de001-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="de001-129">Kontroluje pouze vlastníka produktu nadřazené položky.</span><span class="sxs-lookup"><span data-stu-id="de001-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="de001-130">Například produkt X je přiřazen ke skupině vlastníků produktu *Designové skříňky*.</span><span class="sxs-lookup"><span data-stu-id="de001-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="de001-131">Produkt X je také součástí kusovníku produktu Y, který je přiřazen ke skupině vlastníků produktů *Designové reproduktory*.</span><span class="sxs-lookup"><span data-stu-id="de001-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="de001-132">Pokud uživatel ze skupiny vlastníků produktů *Designové reproduktory* uvolňuje produkt Y a jeho kusovník, produkt X bude uvolněn společně s produktem Y.</span><span class="sxs-lookup"><span data-stu-id="de001-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="de001-133">Vlastníci produktů a schválení</span><span class="sxs-lookup"><span data-stu-id="de001-133">Product owners and approvals</span></span>

<span data-ttu-id="de001-134">Protože vlastníci produktů vědí, zda konkrétní technické změny budou pro jejich produkty přínosem, má často smysl je zahrnout jako součást schvalovacího procesu do správy technických změn.</span><span class="sxs-lookup"><span data-stu-id="de001-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="de001-135">Tento přístup můžete implementovat nastavením vlastníků produktů jako poskytovatelů účastníků v pracovních postupech, které se používají pro správu technických změn.</span><span class="sxs-lookup"><span data-stu-id="de001-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="de001-136">Systém poté přiřadí úkoly schválení v pracovních postupech na základě produktů, které jsou v požadavcích na technické změny a příkazech k technickým změnám.</span><span class="sxs-lookup"><span data-stu-id="de001-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="de001-137">Další informace naleznete v tématu [Správa změn technických produktů](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="de001-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
