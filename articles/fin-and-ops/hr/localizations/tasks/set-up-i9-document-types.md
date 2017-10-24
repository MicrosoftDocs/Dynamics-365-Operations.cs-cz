--- 
title: "Nastavení typů dokumentů I-9"
description: "Tento postup popisuje, jak zobrazit a nastavit typy dokumentů, které se používají pro ověření I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="8a936-103">Nastavení typů dokumentů I-9</span><span class="sxs-lookup"><span data-stu-id="8a936-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="8a936-104">Tento postup popisuje, jak zobrazit a nastavit typy dokumentů, které se používají pro ověření I-9.</span><span class="sxs-lookup"><span data-stu-id="8a936-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="8a936-105">Předtím, než nastavíte typů dokumentů I-9, musíte také nastavit vydávající úřady a typy identifikace.</span><span class="sxs-lookup"><span data-stu-id="8a936-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="8a936-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF, která zahrnuje příklady agentur výdeje a typy identifikace, které jsou nutné k dokončení kroků.</span><span class="sxs-lookup"><span data-stu-id="8a936-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="8a936-107">Přejděte do nabídky Lidské zdroje > Pracovníci > I-9 > Typy dokumentů I-9.</span><span class="sxs-lookup"><span data-stu-id="8a936-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="8a936-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8a936-108">Click New.</span></span>
3. <span data-ttu-id="8a936-109">Zadejte hodnotu do pole Typ dokumentu I-9.</span><span class="sxs-lookup"><span data-stu-id="8a936-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="8a936-110">Příklad: ID školy.</span><span class="sxs-lookup"><span data-stu-id="8a936-110">Example: School ID.</span></span>  
4. <span data-ttu-id="8a936-111">Vyberte typ identifikace.</span><span class="sxs-lookup"><span data-stu-id="8a936-111">Select the identification type.</span></span>  <span data-ttu-id="8a936-112">Příklad: ID školy</span><span class="sxs-lookup"><span data-stu-id="8a936-112">Example:  School ID</span></span>
    * <span data-ttu-id="8a936-113">Příklady typů identifikace zahrnují číslo sociálního pojištění (ČSP), číslo víza, ID pasu nebo řidičského průkazu.</span><span class="sxs-lookup"><span data-stu-id="8a936-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="8a936-114">Vyberte seznam dokumentů I-9 použitý pro daný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="8a936-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="8a936-115">Jako součást procesu I-9 musí zaměstnanci poskytnout zaměstnavateli dokumentaci uvádějící jejich totožnost a pracovní povolení.</span><span class="sxs-lookup"><span data-stu-id="8a936-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="8a936-116">Web US Citizenship and Immigration Services obsahuje informace o tom, které dokumenty mohou být použity, a do jakého seznamu patří.</span><span class="sxs-lookup"><span data-stu-id="8a936-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="8a936-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="8a936-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="8a936-118">Do pole Formulář zadejte pro typ dokumentu číslo oficiálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="8a936-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="8a936-119">Příklad: ID školy.</span><span class="sxs-lookup"><span data-stu-id="8a936-119">Example: School ID.</span></span>
    * <span data-ttu-id="8a936-120">Na webu US Citizenship and Immigration Services lze najít čísla oficiálního formuláře.</span><span class="sxs-lookup"><span data-stu-id="8a936-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="8a936-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="8a936-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="8a936-122">Zaškrtněte nebo zrušte zaškrtnutí políčka Aktivní.</span><span class="sxs-lookup"><span data-stu-id="8a936-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="8a936-123">V poli Ukončit platnost nastavte datum na „27-10-2019“.</span><span class="sxs-lookup"><span data-stu-id="8a936-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="8a936-124">Datum konce platnosti je volitelné.</span><span class="sxs-lookup"><span data-stu-id="8a936-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="8a936-125">Vyberte agenturu vydávající daný typ dokumentu.</span><span class="sxs-lookup"><span data-stu-id="8a936-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="8a936-126">Příklad: Provincie/území</span><span class="sxs-lookup"><span data-stu-id="8a936-126">Example: Province/territory</span></span>
10. <span data-ttu-id="8a936-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8a936-127">Click Save.</span></span>


