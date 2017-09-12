---
title: "Řešení nesrovnalostí během párování součtů faktur"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="86d8a-102">Řešení nesrovnalostí během párování součtů faktur</span><span class="sxs-lookup"><span data-stu-id="86d8a-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="86d8a-103">Párování součtu faktur je jeden typ ověřování párování faktur.</span><span class="sxs-lookup"><span data-stu-id="86d8a-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="86d8a-104">Chcete-li určit, že má systém provést součty spárovaných faktur, na stránce **Parametry závazků** na kartě **Ověření faktury**, nastavte možnost **Párování součtu faktur** na možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="86d8a-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="86d8a-105">Párování součtu faktur můžete použít k ověření toho, zda se celkové částky na faktuře neodlišují od očekávaných částek o větší než přijatelnou odchylku.</span><span class="sxs-lookup"><span data-stu-id="86d8a-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="86d8a-106">Šest součtů je porovnáváno na stránce **Shodné podrobnosti o celkových součtech faktur**.</span><span class="sxs-lookup"><span data-stu-id="86d8a-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="86d8a-107">Pokud některý z celkové částky se liší od očekávané odpovídající celkové nákupní objednávky, je označena odchylka párování.</span><span class="sxs-lookup"><span data-stu-id="86d8a-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="86d8a-108">Ke kontrole faktury, která obsahuje odlišnosti v celkové spárované částce, v pracovním prostoru **Záznam faktury dodavatele** klepněte na dlaždici **Čekající faktury**.</span><span class="sxs-lookup"><span data-stu-id="86d8a-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="86d8a-109">Poté v podokně akcí na kartě **Kontroly** klepněte na možnost **Párování – podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="86d8a-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="86d8a-110">Pokud byly zjištěny odlišnosti v párování, zobrazí se varovné ikony vedle fakturované částky.</span><span class="sxs-lookup"><span data-stu-id="86d8a-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="86d8a-111">Zobrazením podrobností o shodách součtů faktur lze o součtech zobrazit další podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="86d8a-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="86d8a-112">Poté, co jste identifikovali nesrovnalost, budete pravděpodobně muset kontaktovat dodavatele, jestliže se domníváte, že informace na faktuře není správná.</span><span class="sxs-lookup"><span data-stu-id="86d8a-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="86d8a-113">V závislosti na výsledku dohody s dodavatelem můžete provést některou z následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="86d8a-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="86d8a-114">Akceptovat cenovou odchylku a zaúčtovat fakturu s odlišností v párování.</span><span class="sxs-lookup"><span data-stu-id="86d8a-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="86d8a-115">Pokud existují odlišnosti v párování, můžete systém nastavit požadovat schválení předtím, než ho lze zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="86d8a-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="86d8a-116">V takovém případě musíte schválit odchylku párování a volitelně můžete zadat schvalovací komentář.</span><span class="sxs-lookup"><span data-stu-id="86d8a-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="86d8a-117">Poté můžete vybrat zaúčtovat fakturu.</span><span class="sxs-lookup"><span data-stu-id="86d8a-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="86d8a-118">Opravte částku faktury na očekávanou částku a doklad zaúčtujte.</span><span class="sxs-lookup"><span data-stu-id="86d8a-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="86d8a-119">Požádat dodavatele o dobropis a o novou opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="86d8a-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="86d8a-120">Další informace naleznete v tématu [Prozkoumání nebo vyřešení výjimek](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="86d8a-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



