---
title: EUR-00015 Nastavení DIČ
description: Tato procedura vás provede předpoklady registrace DIČ, jako je nastavení typu registrace a jeho přiřazení kategorii registrace.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5488bb020209d6bf6fb39ae0b4f897f5513bdf93
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821796"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="5d728-103">EUR-00015 Nastavení DIČ</span><span class="sxs-lookup"><span data-stu-id="5d728-103">EUR-00015 Set up VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d728-104">Tato procedura vás provede předpoklady registrace DIČ, jako je nastavení typu registrace a jeho přiřazení kategorii registrace.</span><span class="sxs-lookup"><span data-stu-id="5d728-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="5d728-105">Další informace o ID registrace a zpracování ID registrace, včetně povinných požadavků, najdete v tématu nápovědy věnovaném ID registrace a zpracování ID registrace.</span><span class="sxs-lookup"><span data-stu-id="5d728-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="5d728-106">Informace zde uvedené se vztahují na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="5d728-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="5d728-107">Tento úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="5d728-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="5d728-108">Tento úkol je určen pro správce systému.</span><span class="sxs-lookup"><span data-stu-id="5d728-108">This task is intended for system administrators.</span></span> <span data-ttu-id="5d728-109">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="5d728-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="5d728-110">Přejděte na položky Správa organizace > Globální adresář > Typy registrace > Typy registrace.</span><span class="sxs-lookup"><span data-stu-id="5d728-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="5d728-111">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5d728-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="5d728-112">Do pole Název zadejte DIČ.</span><span class="sxs-lookup"><span data-stu-id="5d728-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="5d728-113">Do pole Popis zadejte Číslo DPH.</span><span class="sxs-lookup"><span data-stu-id="5d728-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="5d728-114">V poli Země/oblast zadejte nebo vyberte hodnotu DEU.</span><span class="sxs-lookup"><span data-stu-id="5d728-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="5d728-115">Vyberte Ano v poli Jedinečný.</span><span class="sxs-lookup"><span data-stu-id="5d728-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="5d728-116">Zaškrtněte toto políčko, chcete-li ověřit, zda je DPH jedinečná.</span><span class="sxs-lookup"><span data-stu-id="5d728-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="5d728-117">Vyberte možnost Primární v poli Země.</span><span class="sxs-lookup"><span data-stu-id="5d728-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="5d728-118">Toto políčko zaškrtněte, pokud bude DIČ platit pro všechny adresy patřící do určené země nebo regionu.</span><span class="sxs-lookup"><span data-stu-id="5d728-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="5d728-119">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="5d728-119">Click Create.</span></span>
9. <span data-ttu-id="5d728-120">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="5d728-120">Click Add.</span></span>
10. <span data-ttu-id="5d728-121">V poli Země/oblast zadejte nebo vyberte hodnotu ITA.</span><span class="sxs-lookup"><span data-stu-id="5d728-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="5d728-122">Do pole formát napište '###########'.</span><span class="sxs-lookup"><span data-stu-id="5d728-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="5d728-123">Při zadání ID registrace tohoto typu pro vybranou zemi nebo oblast bude ID registrace ověřeno na základě tohoto formátu.</span><span class="sxs-lookup"><span data-stu-id="5d728-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="5d728-124">Zaškrtněte políčko Jedinečné.</span><span class="sxs-lookup"><span data-stu-id="5d728-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="5d728-125">Zaškrtněte toto políčko, chcete-li ověřit, zda je DPH jedinečná.</span><span class="sxs-lookup"><span data-stu-id="5d728-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="5d728-126">Zaškrtněte políčko Primární pro zemi.</span><span class="sxs-lookup"><span data-stu-id="5d728-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="5d728-127">Toto políčko zaškrtněte, pokud bude DIČ platit pro všechny adresy patřící do určené země nebo regionu.</span><span class="sxs-lookup"><span data-stu-id="5d728-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="5d728-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5d728-128">Click Save.</span></span>
15. <span data-ttu-id="5d728-129">Přejděte na položky Správa organizace > Globální adresář > Typy registrace > Kategorie registrace.</span><span class="sxs-lookup"><span data-stu-id="5d728-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="5d728-130">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5d728-130">Click New.</span></span>
17. <span data-ttu-id="5d728-131">V poli Země/oblast zadejte nebo vyberte hodnotu DIČ, DEU.</span><span class="sxs-lookup"><span data-stu-id="5d728-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="5d728-132">V poli kategorie registrace vyberte DIČ.</span><span class="sxs-lookup"><span data-stu-id="5d728-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="5d728-133">Přiřaďte typ registrace, který jste vytvořili dříve, k předdefinované kategorii registrace.</span><span class="sxs-lookup"><span data-stu-id="5d728-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="5d728-134">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5d728-134">Click New.</span></span>
20. <span data-ttu-id="5d728-135">V poli Země/oblast zadejte nebo vyberte hodnotu DIČ, ITA.</span><span class="sxs-lookup"><span data-stu-id="5d728-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="5d728-136">V poli kategorie registrace vyberte DIČ.</span><span class="sxs-lookup"><span data-stu-id="5d728-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="5d728-137">Přiřaďte typ registrace, který jste vytvořili, k předdefinované kategorii registrace.</span><span class="sxs-lookup"><span data-stu-id="5d728-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="5d728-138">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5d728-138">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]