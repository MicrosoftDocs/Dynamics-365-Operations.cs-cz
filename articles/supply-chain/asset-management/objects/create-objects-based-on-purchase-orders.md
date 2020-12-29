---
title: Vytvoření majetku na základě nákupních objednávek
description: Toto téma vysvětluje, jak lze vytvořit seznam položek dlouhodobého majetku, který lze použít jako základ pro práce údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423760"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="e3a1a-103">Vytvoření majetku na základě nákupních objednávek</span><span class="sxs-lookup"><span data-stu-id="e3a1a-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e3a1a-104">Toto téma vysvětluje, jak lze vytvořit seznam položek dlouhodobého majetku, který lze použít jako základ pro práce údržby v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="e3a1a-105">Na základě položek majetku můžete zobrazit přehled řádků nákupních objednávek, které byly na těchto položkách vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="e3a1a-106">Účelem této funkce je snadné vytvoření majetku ve správě majetku na základě nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="e3a1a-107">Nejdříve nastavíte zboží, které bude použito pro vytváření majetku z nákupní objednávky v **položkách majetku**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="e3a1a-108">Po vytvoření řádku nákupní objednávky vytvoříte majetek v části **Čekající majetek**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="e3a1a-109">Je možné rozhodnout, v jaké fázi nákupní objednávky má být majetek vytvořen.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="e3a1a-110">Výběr položek majetku</span><span class="sxs-lookup"><span data-stu-id="e3a1a-110">Select asset items</span></span>

1. <span data-ttu-id="e3a1a-111">Klikněte na **Správa majetku** > **Nastavení** > **Majetek** > **Zboží**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="e3a1a-112">Klikněte na možnost **Nové**, abyste vytvořili novou položku majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="e3a1a-113">V poli **Číslo položky** vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="e3a1a-114">Když toto pole opustíte, název položky bude automaticky vložen do pole **Název produktu**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="e3a1a-115">Na pevné záložce **Obecné** vyberte typ majetku pro položku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="e3a1a-116">Vyberte výrobce majetku a model pro položku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="e3a1a-117">Uložte položku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="e3a1a-118">Vytvoření majetku z čekajícího majetku</span><span class="sxs-lookup"><span data-stu-id="e3a1a-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="e3a1a-119">Klikněte na **Správa majetku** > **Společné** > **Majetek** > **Čekající majetek**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="e3a1a-120">Zobrazí se aktualizovaný přehled nákupních objednávek na základě položek vybraných v okně **Položky majetku**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="e3a1a-121">Můžete filtrovat stav nákupních objednávek a vybrat, ve kterém stavu životního cyklu má být majetek vytvořen.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="e3a1a-122">Můžete například chtít vytvořit majetek pouze v případě, že příjemka produktu byla zaúčtována na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="e3a1a-123">Vyberte odkaz **Referenční číslo** odkaz na řádku nákupní objednávky a zobrazte detailní informace o zboží.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="e3a1a-124">Pokud chcete upravit, které dimenze se zobrazí na pevné záložce **dimenze zásob**, klikněte na tlačítko **Zobrazit dimenze** a vyberte požadované možnosti.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="e3a1a-125">Pokud chcete vytvořit majetek na základě řádku nákupní objednávky, zaškrtněte políčko ve sloupci **Značka** pro tento řádek na stránce se seznamem a klikněte na možnost **Vytvořit majetek.**</span><span class="sxs-lookup"><span data-stu-id="e3a1a-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="e3a1a-126">Zobrazí se zpráva s informacemi o ID majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="e3a1a-127">Vyberte majetek v seznamu **Všechen majetek** a kliknutím na tlačítko **Upravit** přidejte k majetku Další informace.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="e3a1a-128">Pokud chcete odstranit řádek, protože nechcete vytvořit majetek, zaškrtněte v části **Čekající majetek** políčko ve sloupci **Značka** pro tento řádek a klikněte na **Zahodit čekající majetek**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="e3a1a-129">Zobrazí se zpráva s informacemi o ID majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="e3a1a-130">Neodstraňujete nákupní objednávku nebo prodejní objednávku, pouze záznam, ze kterého jste mohli vytvořit majetek v modulu **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="e3a1a-131">Všechny dimenze produktu (velikost, barva, konfigurace atd.) jsou automaticky převedeny do atributů majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="e3a1a-132">Sledovací dimenze (sériové číslo) jsou při vytvoření majetku uloženy přímo v majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="e3a1a-133">Vyhledání čekajícího majetku</span><span class="sxs-lookup"><span data-stu-id="e3a1a-133">Find pending assets</span></span>

<span data-ttu-id="e3a1a-134">Můžete spustit **Inventuru čekajícího majetku** ke kontrole čekajícího majetku.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="e3a1a-135">Tuto funkci lze například použít k přijetí oznámení pokaždé, když je čekající majetek připraven k vytvoření jako majetek.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="e3a1a-136">Klikněte na **Správa majetku** > **Periodická** > **Majetek** > **Inventura čekajícího majetku**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="e3a1a-137">Kliknutím na tlačítko **OK** spusťte úlohu a aktualizujte seznam v okně **Čekající majetek**.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="e3a1a-138">Tuto úlohu můžete nastavit tak, aby byla spouštěna jako dávková úloha, například jednou denně.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="e3a1a-139">**Upozornění:** Pokud dojde ke změně dat na nákupní objednávce *poté*, co jste vytvořili majetek na základě příslušející položky, tyto změny se na majetku neprojeví.</span><span class="sxs-lookup"><span data-stu-id="e3a1a-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
