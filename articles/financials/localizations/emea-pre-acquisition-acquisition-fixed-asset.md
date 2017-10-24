---
title: "Účtování předpořízení dlouhodobého majetku"
description: "Toto téma vysvětluje, jak vytvořit a zaúčtovat předpořízení dlouhodobého majetku."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264704
ms.search.region: Czech Republic, Hungary
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f5b5f442daa64d5ae3b414b88efe1fd6f546523
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="post-the-pre-acquisition-of-a-fixed-asset"></a><span data-ttu-id="bb106-103">Účtování předpořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="bb106-103">Post the pre-acquisition of a fixed asset</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bb106-104">Toto téma vysvětluje, jak vytvořit a zaúčtovat předpořízení dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="bb106-104">This topic explains how to set up and post fixed asset pre-acquisitions.</span></span>

<span data-ttu-id="bb106-105">**Poznámka:** Funkce pro účtování předpořízení dlouhodobého majetku je k dispozici pouze pro právnické osoby, které mají své primární adresy v Maďarsku a České republice.</span><span class="sxs-lookup"><span data-stu-id="bb106-105">**Note:** The functionality for posting fixed asset pre-acquisitions is available only for legal entities that have their primary address in Hungary or the Czech Republic.</span></span> <span data-ttu-id="bb106-106">Předpořízení dlouhodobého majetku se neodpisuje a nemá vliv na náklady na pořízení nebo zůstatkové účetní hodnoty dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="bb106-106">A pre-acquisition of a fixed asset isn't depreciable, and it doesn't affect the acquisition costs or the net book value of the fixed asset.</span></span> <span data-ttu-id="bb106-107">Při účtování předpořízení, stav dlouhodobého majetku se změní na **Získáno**.</span><span class="sxs-lookup"><span data-stu-id="bb106-107">When you post a pre-acquisition, the status of the fixed asset is changed to **Acquired**.</span></span> <span data-ttu-id="bb106-108">Dlouhodobý majetek, který má stav **Získáno**, není odpisovatelný.</span><span class="sxs-lookup"><span data-stu-id="bb106-108">A fixed asset that has the **Acquired** status isn't depreciable.</span></span> <span data-ttu-id="bb106-109">Naproti tomu, při účtování pořízení se stav změní na **Otevřeno** a dlouhodobý majetek je odpisovatelný.</span><span class="sxs-lookup"><span data-stu-id="bb106-109">By contrast, when you post an acquisition, the status is changed to **Open**, and the fixed asset is depreciable.</span></span>

## <a name="set-up-preacquisitions"></a><span data-ttu-id="bb106-110">Nastavení předpořízení</span><span class="sxs-lookup"><span data-stu-id="bb106-110">Set up preacquisitions</span></span>
<span data-ttu-id="bb106-111">Předtím, než budete moci zaúčtovat předpořízení, je třeba dokončit toto nastavení.</span><span class="sxs-lookup"><span data-stu-id="bb106-111">Before you can post a pre-acquisition, you must complete the following setup:</span></span>

-   <span data-ttu-id="bb106-112">Na stránce **Parametry dlouhodobého majetku** nastavte možnost **Povolit předpořízení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="bb106-112">On the **Fixed assets parameters** page, set the **Allow pre-acquisitions** option to **Yes**.</span></span>
-   <span data-ttu-id="bb106-113">Na stránce **Účetní profily dlouhodobého majetku** nastavte účetní profil dlouhodobého majetku na typ zaúčtování předpořízení dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="bb106-113">On the **Fixed asset posting profiles** page, set up a fixed asset posting profile for the pre-acquisition posting type.</span></span>

## <a name="post-a-preacquisition-of-a-fixed-asset"></a><span data-ttu-id="bb106-114">Účtování předpořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="bb106-114">Post a preacquisition of a fixed asset</span></span>
1.  <span data-ttu-id="bb106-115">Na stránce **Dlouhodobý majetek** vytvořte nový deník a zadejte všechny příslušné údaje podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="bb106-115">On the **Fixed assets** page, create a new journal, and enter all applicable information, as required.</span></span>
2.  <span data-ttu-id="bb106-116">U deníku, který jste právě vytvořili, klikněte na **Řádky** k otevření stránky **Doklad deníku**.</span><span class="sxs-lookup"><span data-stu-id="bb106-116">For the journal that you just created, click **Lines** to open the **Journal voucher** page.</span></span>
3.  <span data-ttu-id="bb106-117">Kliknutím na možnost **Nový** vytvořte řádek.</span><span class="sxs-lookup"><span data-stu-id="bb106-117">Click **New** to create a line.</span></span>
4.  <span data-ttu-id="bb106-118">V poli **Typ transakce** vyberte transakci typu **Předpořízení**.</span><span class="sxs-lookup"><span data-stu-id="bb106-118">In the **Transaction type** field, select a transaction that has the **Pre-Acquisition** transaction type.</span></span>
5.  <span data-ttu-id="bb106-119">Podle potřeby zadejte hodnoty pro zbývající pole.</span><span class="sxs-lookup"><span data-stu-id="bb106-119">Enter values for the remaining fields as required.</span></span>
6.  <span data-ttu-id="bb106-120">Kliknutím na možnost **Ověřit** ověřte řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="bb106-120">Click **Validate** to validate the journal lines.</span></span>
7.  <span data-ttu-id="bb106-121">Klikněte na **Návrhy** &gt; **Návrh předpořízení**.</span><span class="sxs-lookup"><span data-stu-id="bb106-121">Click **Proposals** &gt; **Pre-acquisition proposal**.</span></span>
8.  <span data-ttu-id="bb106-122">Kliknutím na **Vybrat** nastavte kritéria výběru a klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb106-122">Click **Select** to set up the selection criteria, and then click **OK**.</span></span>
9.  <span data-ttu-id="bb106-123">Kliknutím na tlačítko **OK** zavřete stránku **Návrh předpořízení**.</span><span class="sxs-lookup"><span data-stu-id="bb106-123">Click **OK** to close the **Pre-acquisition proposal** page.</span></span>
10. <span data-ttu-id="bb106-124">Kliknutím na **Zaúčtovat** &gt; **Zaúčtovat** zaúčtujte transakci předpořízení.</span><span class="sxs-lookup"><span data-stu-id="bb106-124">Click **Post** &gt; **Post** to post the pre-acquisition transaction.</span></span> <span data-ttu-id="bb106-125">Stav dlouhodobého majetku na stránce **Knihy** by teď měl být **Pořízené**.</span><span class="sxs-lookup"><span data-stu-id="bb106-125">On the **Books** page, the status of the fixed asset should now be **Acquired**.</span></span>





