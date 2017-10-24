---
title: "Vykazování daně z prodeje pro Českou republiku"
description: "Toto téma uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku."
author: LizaGolub
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxGroup, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 1696023
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7289d83146765b6c8fda8f2c9b286d4b540d5ae8
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-reporting-for-the-czech-republic"></a><span data-ttu-id="822e7-103">Vykazování daně z prodeje pro Českou republiku</span><span class="sxs-lookup"><span data-stu-id="822e7-103">Sales tax reporting for the Czech Republic</span></span>

<span data-ttu-id="822e7-104">Toto téma uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku.</span><span class="sxs-lookup"><span data-stu-id="822e7-104">This topic provides information about how intra-community value-added tax (VAT) is calculated and posted for the Czech Republic.</span></span> 

<span data-ttu-id="822e7-105">Když právnické osoby, které mají svou primární adresu v České republice, nakupují od členských států Evropské unie (EU), měly by provést vlastní vyměření daně z přidané hodnoty (DPH), aby se zajistilo, že jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="822e7-105">When legal entities that have their primary address in the Czech Republic purchase from European Union (EU) member states, they should do a self-assessment of value-added tax (VAT) to make sure that the following conditions are met:</span></span>

-   <span data-ttu-id="822e7-106">DPH na výstupu se platí v období DPH, kdy byla vystavena faktura (datum dokumentu).</span><span class="sxs-lookup"><span data-stu-id="822e7-106">The output VAT is paid in the VAT period when the invoice was issued (document date).</span></span>
-   <span data-ttu-id="822e7-107">DPH na vstupu nebyla odečtena před přijetím dokumentu (datum rejstříku DPH).</span><span class="sxs-lookup"><span data-stu-id="822e7-107">The input VAT wasn't deducted before the document receipt (VAT register date).</span></span>

<span data-ttu-id="822e7-108">Informace o intrakomunitární DPH mohou být vypočteny a zaúčtovány automaticky.</span><span class="sxs-lookup"><span data-stu-id="822e7-108">Information about intra-community VAT can be calculated and posted automatically.</span></span> <span data-ttu-id="822e7-109">Při zaúčtování faktury dodavatele v Evropské unii (EU) jsou vytvořeny dvě transakce DPH ve stejné výši.</span><span class="sxs-lookup"><span data-stu-id="822e7-109">When you post an EU vendor invoice, two VAT transactions for the same amount are created.</span></span> <span data-ttu-id="822e7-110">Jedna transakce DPH je vytvořena pro závazek prodejní daně a druhá pro pohledávku prodejní daně.</span><span class="sxs-lookup"><span data-stu-id="822e7-110">One VAT transaction is created for payable sales tax, and the other transaction is created for receivable sales tax.</span></span> <span data-ttu-id="822e7-111">Aby se tento požadavek projevil v aplikaci Microsoft Dynamics 365 for Finance and Operations, je třeba nastavit následující položky:</span><span class="sxs-lookup"><span data-stu-id="822e7-111">To reflect this requirement in Microsoft Dynamics 365 for Finance and Operations, you should complete the following setup:</span></span>

-   <span data-ttu-id="822e7-112">Zaškrtněte políčko **DPH intrakomunitárního plnění** na stránce **Parametry závazků** (**Závazky** &gt; **Nastavení** &gt; **Parametry závazků**).</span><span class="sxs-lookup"><span data-stu-id="822e7-112">Select the **Intra-community VAT** check box on the **Accounts payables parameters** page (**Accounts payable** &gt; **Setup** &gt; **Accounts payables parameters**).</span></span>
-   <span data-ttu-id="822e7-113">Zaškrtněte políčko **Datum dokumentu pro intrakomunitární DPH** na stránce **Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="822e7-113">Select the **Document date for intra-community VAT** check box on the **Accounts payables parameters** page.</span></span>
-   <span data-ttu-id="822e7-114">Vytvořte dva kódy daně z prodeje: jeden, který má kladné procento daně z prodeje a druhý, který má záporné procento daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="822e7-114">Create two sales tax codes: one that has a positive sales tax percentage and another that has a negative sales tax percentage.</span></span>
-   <span data-ttu-id="822e7-115">Vytvořte skupinu daně z prodeje obsahující kladné i záporné kódy daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="822e7-115">Create a sales tax group that contains both the positive and negative sales tax codes.</span></span> <span data-ttu-id="822e7-116">Pro záporný kód daně z prodeje vyberte parametr **DPH intrakomunitárního plnění**.</span><span class="sxs-lookup"><span data-stu-id="822e7-116">Select the **Intra-community VAT** parameter for the negative sales tax code.</span></span>
-   <span data-ttu-id="822e7-117">V denících vyberte parametr **Datum dokumentu pro intrakomunitární DPH**.</span><span class="sxs-lookup"><span data-stu-id="822e7-117">In journals, select the **Document date for intra-community VAT** parameter.</span></span>

<span data-ttu-id="822e7-118">Při zaúčtování nákupní faktury, pohledávka DPH a závazek DPH jsou účtovány ve stejnou dobu.</span><span class="sxs-lookup"><span data-stu-id="822e7-118">When a purchase invoice is posted, the receivable VAT and payable VAT are posted at the same time.</span></span> <span data-ttu-id="822e7-119">V případě kladných transakcí daně z prodeje je datum registru DPH nastaveno na datum registru DPH ze stránky zaúčtování faktury a směrování daně z prodeje je **DPH na vstupu**.</span><span class="sxs-lookup"><span data-stu-id="822e7-119">For the positive sales tax transaction, the VAT register date is set to the VAT register date from the invoice posting page, and the sales tax direction is **Sales tax receivable**.</span></span> <span data-ttu-id="822e7-120">V případě záporných transakcí daně z prodeje je datum registru DPH nastaveno na datum dokumentu a směrování daně z prodeje je **DPH na výstupu**.</span><span class="sxs-lookup"><span data-stu-id="822e7-120">For the negative sales tax transaction, the VAT register date is set to the document date, and the sales tax direction is **Sales tax payable**.</span></span>


