---
title: "Průzkumník zdroje účetnictví"
description: "Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: d21f214ef8a29c19f0af1d4a2bdfc3264987f0b8
ms.contentlocale: cs-cz
ms.lasthandoff: 12/14/2017

---

# <a name="accounting-source-explorer"></a><span data-ttu-id="50e5a-103">Průzkumník zdroje účetnictví</span><span class="sxs-lookup"><span data-stu-id="50e5a-103">Accounting source explorer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="50e5a-104">Tento článek obsahuje informace o nástroji Průzkumník zdroje účetnictví, který slouží pro podrobnou analýzu informace zdroje za účetními položkami hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="50e5a-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="50e5a-105">Průzkumník zdroje účetnictví je nová stránka, která zobrazuje informace o zdroji.</span><span class="sxs-lookup"><span data-stu-id="50e5a-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="50e5a-106">Můžete použít Průzkumníka zdroje účetnictví buď jako samostatný nástroj nebo k analýze podrobností za účetními položkami hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="50e5a-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="50e5a-107">Průzkumníka zdroje účetnictví můžete například použít k získání podrobných informací o zdroji u zůstatku v předvaze nebo u transakce dokladu.</span><span class="sxs-lookup"><span data-stu-id="50e5a-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="50e5a-108">Poté můžete použít funkci Exportovat do aplikace Microsoft Excel a informace dále rozebírat v Microsoft Excelu (například v kontingenční tabulce nebo sestavě kontingenční tabulky).</span><span class="sxs-lookup"><span data-stu-id="50e5a-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="50e5a-109">Průzkumník zdroje účetnictví vždy zobrazuje stejnou celkovou částku pro účet hlavní knihy, jakou zobrazuje hlavní kniha (například v Předvaze).</span><span class="sxs-lookup"><span data-stu-id="50e5a-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="50e5a-110">Stejně jako v předvaze můžete zobrazit segmenty v samostatných sloupcích.</span><span class="sxs-lookup"><span data-stu-id="50e5a-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="50e5a-111">Stačí vybrat odpovídající sadu finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="50e5a-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="50e5a-112">Parametry slouží k definování časového intervalu pro analýzu.</span><span class="sxs-lookup"><span data-stu-id="50e5a-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="50e5a-113">Tato funkce se také podobá fungování předvahy.</span><span class="sxs-lookup"><span data-stu-id="50e5a-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="50e5a-114">Pro všechny dokumenty používající architekturu zdrojového dokumentu, zobrazí průzkumník zdroje účetnictví další informace, které jsou založené na rozúčtování a v odpovídajících případech rozúčtování projektu.</span><span class="sxs-lookup"><span data-stu-id="50e5a-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="50e5a-115">Tyto informace zahrnují typ peněžní částky, projekt, aktivitu, kategorii a vlastnost řádku.</span><span class="sxs-lookup"><span data-stu-id="50e5a-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="50e5a-116">Zde je několik příkladů analýzy, kterou lze provést:</span><span class="sxs-lookup"><span data-stu-id="50e5a-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="50e5a-117">Odchylky mezi nákupními objednávkami a fakturami dodavatele, protože každou odchylku zastupuje typ peněžní částky, například odchylka ceny</span><span class="sxs-lookup"><span data-stu-id="50e5a-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="50e5a-118">Fakturovatelné a nefakturovatelné hodiny a výdaje na projekt, obchodní jednotku a hlavní účet</span><span class="sxs-lookup"><span data-stu-id="50e5a-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="50e5a-119">Pro zdrojové dokumenty, které používají koncept identit odkazu na zdrojový dokument, zobrazí Průzkumník zdroje účetnictví další podrobnosti, například odběratele, dodavatele, pracovníka, produkt, množství, text jednotky a popisy.</span><span class="sxs-lookup"><span data-stu-id="50e5a-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="50e5a-120">Zde je několik příkladů analýzy, kterou lze provést:</span><span class="sxs-lookup"><span data-stu-id="50e5a-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="50e5a-121">Výdaje za hotel pro obchodní jednotku a značku hotelu pro fiskální období, založené na sestavách výdajů</span><span class="sxs-lookup"><span data-stu-id="50e5a-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="50e5a-122">Slevy na dodavatele, produkt, oddělení</span><span class="sxs-lookup"><span data-stu-id="50e5a-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="50e5a-123">Pro tyto dokumenty můžete také z Průzkumníka zdroje účetnictví přejít na samotný zdrojový dokument.</span><span class="sxs-lookup"><span data-stu-id="50e5a-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




