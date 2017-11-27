--- 
title: "Nastavení typů dokumentů I-9"
description: "Tento postup popisuje, jak zobrazit a nastavit typy dokumentů, které se používají pro ověření I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 950237499441e7f1d5b9e3355c4bd9513ad3783e
ms.openlocfilehash: b47998eccd7509154ee8863e2e19594cc59ac945
ms.contentlocale: cs-cz
ms.lasthandoff: 11/01/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="b785e-103">Nastavení typů dokumentů I-9</span><span class="sxs-lookup"><span data-stu-id="b785e-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="b785e-104">Tento postup popisuje, jak zobrazit a nastavit typy dokumentů, které se používají pro ověření I-9.</span><span class="sxs-lookup"><span data-stu-id="b785e-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="b785e-105">Předtím, než nastavíte typů dokumentů I-9, musíte také nastavit vydávající úřady a typy identifikace.</span><span class="sxs-lookup"><span data-stu-id="b785e-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="b785e-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF, která zahrnuje příklady agentur výdeje a typy identifikace, které jsou nutné k dokončení kroků.</span><span class="sxs-lookup"><span data-stu-id="b785e-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="b785e-107">Přejděte do nabídky Lidské zdroje > Pracovníci > I-9 > Typy dokumentů I-9.</span><span class="sxs-lookup"><span data-stu-id="b785e-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="b785e-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b785e-108">Click New.</span></span>
3. <span data-ttu-id="b785e-109">Zadejte hodnotu do pole Typ dokumentu I-9.</span><span class="sxs-lookup"><span data-stu-id="b785e-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="b785e-110">Příklad: ID školy.</span><span class="sxs-lookup"><span data-stu-id="b785e-110">Example: School ID.</span></span>  
4. <span data-ttu-id="b785e-111">Vyberte typ identifikace.</span><span class="sxs-lookup"><span data-stu-id="b785e-111">Select the identification type.</span></span>  <span data-ttu-id="b785e-112">Příklad: ID školy</span><span class="sxs-lookup"><span data-stu-id="b785e-112">Example:  School ID</span></span>
    * <span data-ttu-id="b785e-113">Příklady typů identifikace zahrnují číslo sociálního pojištění (ČSP), číslo víza, ID pasu nebo řidičského průkazu.</span><span class="sxs-lookup"><span data-stu-id="b785e-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's license.</span></span>  
5. <span data-ttu-id="b785e-114">Vyberte seznam dokumentů I-9 použitý pro daný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b785e-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="b785e-115">Jako součást procesu I-9 musí zaměstnanci poskytnout zaměstnavateli dokumentaci uvádějící jejich totožnost a pracovní povolení.</span><span class="sxs-lookup"><span data-stu-id="b785e-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="b785e-116">Web US Citizenship and Immigration Services obsahuje informace o tom, které dokumenty mohou být použity, a do jakého seznamu patří.</span><span class="sxs-lookup"><span data-stu-id="b785e-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="b785e-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="b785e-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="b785e-118">Do pole Formulář zadejte pro typ dokumentu číslo oficiálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b785e-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="b785e-119">Příklad: ID školy.</span><span class="sxs-lookup"><span data-stu-id="b785e-119">Example: School ID.</span></span>
    * <span data-ttu-id="b785e-120">Na webu US Citizenship and Immigration Services lze najít čísla oficiálního formuláře.</span><span class="sxs-lookup"><span data-stu-id="b785e-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="b785e-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="b785e-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="b785e-122">Zaškrtněte nebo zrušte zaškrtnutí políčka Aktivní.</span><span class="sxs-lookup"><span data-stu-id="b785e-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="b785e-123">V poli Ukončit platnost nastavte datum na „27-10-2019“.</span><span class="sxs-lookup"><span data-stu-id="b785e-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="b785e-124">Datum konce platnosti je volitelné.</span><span class="sxs-lookup"><span data-stu-id="b785e-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="b785e-125">Vyberte agenturu vydávající daný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b785e-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="b785e-126">Příklad: Provincie/území</span><span class="sxs-lookup"><span data-stu-id="b785e-126">Example: Province/territory</span></span>
10. <span data-ttu-id="b785e-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b785e-127">Click Save.</span></span>


