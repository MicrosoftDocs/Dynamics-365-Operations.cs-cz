---
title: Nastavení parametrů lidských zdrojů mezi právnickými osobami
description: Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 9c205973097c82a4b131a3784392fa8d8cb5ecba
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812803"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="467cd-104">Nastavení parametrů lidských zdrojů mezi právnickými osobami</span><span class="sxs-lookup"><span data-stu-id="467cd-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="467cd-105">Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice.</span><span class="sxs-lookup"><span data-stu-id="467cd-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="467cd-106">Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="467cd-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="467cd-107">Některé typy záznamů jako jsou například Záznamy pozice, jsou sdíleny mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="467cd-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="467cd-108">Pro tyto záznamy musíte nastavit sdílené parametry.</span><span class="sxs-lookup"><span data-stu-id="467cd-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="467cd-109">Můžete například použít stránku **Sdílené parametry lidských zdrojů** k nastavení parametrů lidských zdrojů mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="467cd-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="467cd-110">Na stránce **Sdílené parametry lidských zdrojů** jsou seskupeny parametry do skupin podle jejich funkce.</span><span class="sxs-lookup"><span data-stu-id="467cd-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="467cd-111">Dříve vydané funkce</span><span class="sxs-lookup"><span data-stu-id="467cd-111">Previously released functionality</span></span>
<span data-ttu-id="467cd-112">Na kartě **Identifikace** je nutné vybrat typy identifikace, které představují identifikační čísla, která jsou uvedena na stránce.</span><span class="sxs-lookup"><span data-stu-id="467cd-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="467cd-113">Typy identifikace musíte nastavit před zadáním identifikačních informací o zaměstnancích.</span><span class="sxs-lookup"><span data-stu-id="467cd-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="467cd-114">Informace o čísle sociálního pojištění, národním identifikačním čísle, rodném čísle cizince a identifikační kód osoby jsou uvedeny na stránce **Typ identifikace**.</span><span class="sxs-lookup"><span data-stu-id="467cd-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="467cd-115">Definujte nový typ identifikace nebo zkontrolujte seznam stávajících typů kliknutím na možnost **Správa personálu** &gt; **Karta Odkazy** &gt; **Nastavení** &gt; **Typy identifikace**.</span><span class="sxs-lookup"><span data-stu-id="467cd-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="467cd-116">Můžete zadat jednoduchý kód a popis.</span><span class="sxs-lookup"><span data-stu-id="467cd-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-talent"></a><span data-ttu-id="467cd-117">Pokud používáte Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="467cd-117">If you're using Dynamics 365 Talent</span></span>
<span data-ttu-id="467cd-118">Na kartě **Identifikace** je nutné vybrat typy identifikace, které představují identifikační čísla, která jsou uvedena na stránce.</span><span class="sxs-lookup"><span data-stu-id="467cd-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="467cd-119">Typy identifikace musíte nastavit před zadáním identifikačních informací o zaměstnancích.</span><span class="sxs-lookup"><span data-stu-id="467cd-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="467cd-120">Informace o čísle sociálního pojištění, národním identifikačním čísle, rodném čísle cizince a identifikační kód osoby jsou uvedeny na stránce **Typ identifikace**.</span><span class="sxs-lookup"><span data-stu-id="467cd-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="467cd-121">Definujte nový typ identifikace nebo zkontrolujte seznam stávajících typů kliknutím na možnost **Lidské zdroje** &gt; **Nastavení** &gt; **Typy identifikace**.</span><span class="sxs-lookup"><span data-stu-id="467cd-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="467cd-122">Můžete zadat jednoduchý kód a popis.</span><span class="sxs-lookup"><span data-stu-id="467cd-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="467cd-123">Na kartě **Číselné řady** můžete vybrat číselné řady, které se používají pro následující záznamy: osobní číslo, pozice, ID požadavku uživatele, dokument I-9, uchazeč, diskuse, ID výhody a akce personálu (je-li povolen tento typ záznamu).</span><span class="sxs-lookup"><span data-stu-id="467cd-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="467cd-124">Pro správu číselné řady odkazů a kódů, použijte stránky seznamu **Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="467cd-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="467cd-125">Použijte funkci vyhledávání stránky, chcete-li tuto stránku najít.</span><span class="sxs-lookup"><span data-stu-id="467cd-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="467cd-126">Na kartě **Pozice** určete, zda jsou k dispozici nové pozice pro přiřazení ve výchozím nastavení:</span><span class="sxs-lookup"><span data-stu-id="467cd-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="467cd-127">**Nikdy** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic.</span><span class="sxs-lookup"><span data-stu-id="467cd-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="467cd-128">Při vytváření pozic se čas a datum položky **K dispozici pro přiřazení** na kartě **Obecné** stránky **Pozice** automaticky nastavuje na datum a čas vytvoření.</span><span class="sxs-lookup"><span data-stu-id="467cd-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="467cd-129">**Niky** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic.</span><span class="sxs-lookup"><span data-stu-id="467cd-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="467cd-130">Pokud vyberete tuto možnost, je třeba otevřít stránku **Pozice** pro každou novou pozici, jakmile je k dispozici, a pak na kartě **Obecné** zadat datum položky **K dispozici pro přiřazení**, aby bylo aktivováno přiřazení pracovníka.</span><span class="sxs-lookup"><span data-stu-id="467cd-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="467cd-131">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="467cd-131">Additional resources</span></span>
--------

[<span data-ttu-id="467cd-132">Nastavení parametrů lidských zdrojů pro konkrétní společnost</span><span class="sxs-lookup"><span data-stu-id="467cd-132">Set up company-specific Human resources (HR) parameters</span></span>](set-up-company-specific-hr-parameters.md)



