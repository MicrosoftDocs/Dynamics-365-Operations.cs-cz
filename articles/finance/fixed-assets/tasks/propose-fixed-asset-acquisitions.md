---
title: Nabídka pořízení dlouhodobého majetku
description: Toto téma popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817151"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="3d639-103">Nabídka pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="3d639-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d639-104">Toto téma popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3d639-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="3d639-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="3d639-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="3d639-106">Chcete-li získat dlouhodobý majetek prostřednictvím deníku návrhu dlouhodobého majetku, musíte nejprve vytvořit záznam dlouhodobého majetku a poté definovat pořizovací cenu v majetkové knize.</span><span class="sxs-lookup"><span data-stu-id="3d639-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="3d639-107">Vytvoření návrhu na pořízení majetku</span><span class="sxs-lookup"><span data-stu-id="3d639-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="3d639-108">Chcete-li vytvořit návrh na pořízení majetku, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="3d639-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="3d639-109">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="3d639-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="3d639-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="3d639-110">Select **New**.</span></span>
3. <span data-ttu-id="3d639-111">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3d639-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="3d639-112">V podokně akcí zvolte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="3d639-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="3d639-113">Vyberte **Návrhy**.</span><span class="sxs-lookup"><span data-stu-id="3d639-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="3d639-114">Vyberte **Návrh pořízení**.</span><span class="sxs-lookup"><span data-stu-id="3d639-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="3d639-115">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="3d639-115">Select **Filter**.</span></span> <span data-ttu-id="3d639-116">Kliknutím na tlačítko **Vynulovat** vymažete předchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="3d639-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="3d639-117">Vyberte řádek **Číslo dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="3d639-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="3d639-118">V poli **Kritéria** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3d639-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="3d639-119">Nastavte zbývající kritéria pro dlouhodobý majetek, který chcete získat s tímto návrhem.</span><span class="sxs-lookup"><span data-stu-id="3d639-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="3d639-120">Chcete-li ukončit podokno, klepněte dvakrát na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d639-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="3d639-121">Ověřte, že byly vytvořeny řádky transakce.</span><span class="sxs-lookup"><span data-stu-id="3d639-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="3d639-122">V návrhu pořízení bude zahrnut pouze dlouhodobý majetek s datem pořízení a pořizovací cenou nastavenou v knize.</span><span class="sxs-lookup"><span data-stu-id="3d639-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="3d639-123">Na stránce vyberte kartu **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="3d639-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="3d639-124">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="3d639-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="3d639-125">Zahrnutí výchozích finančních dimenzí do návrhu pořízení majetku</span><span class="sxs-lookup"><span data-stu-id="3d639-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="3d639-126">Transakci pořízení majetku lze vytvořit pomocí doplňků aplikace Excel v části **Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="3d639-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="3d639-127">Vytvořte nový deník a přejděte do sekce **Řádky** na stránce. Vyberte ikonu Excelu a poté vyberte řádek deníku dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3d639-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="3d639-128">Systém vytvoří a otevře šablonu aplikace Excel představující řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="3d639-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="3d639-129">Můžete přidat data pro řádky deníku, které přidáváte do šablony, a poté tyto informace publikovat zpět do systému.</span><span class="sxs-lookup"><span data-stu-id="3d639-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="3d639-130">Pokud byly nastaveny výchozí dimenze pro vybranou knihu majetku a odpovídající dlouhodobý majetek, který byl zadán v šabloně aplikace Excel, budou výchozí finanční dimenze volány z hlavních dat knihy majetku, když je deník publikován z aplikace Excel do systému.</span><span class="sxs-lookup"><span data-stu-id="3d639-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="3d639-131">Chcete-li finanční dimenze do knihy majetku zahrnout automaticky při publikování deníku dlouhodobého majetku z doplňku Excelu, je třeba předem nastavit výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="3d639-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
