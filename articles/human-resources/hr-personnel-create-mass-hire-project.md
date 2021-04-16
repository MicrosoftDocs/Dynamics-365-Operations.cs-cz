---
title: Vytvoření projektu masového pronájmu
description: Tento postup vás provede nastavením procesu hromadného zařazování zaměstnanců.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 353bfe6c9a79db91a86e612737ea7705c8cdaeb8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800206"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="268f4-103">Vytvoření projektu masového pronájmu</span><span class="sxs-lookup"><span data-stu-id="268f4-103">Create a mass hire project</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="268f4-104">Tento postup vás provede nastavením procesu hromadného zařazování zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="268f4-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="268f4-105">Náborový zaměstnanec může využívat projekty hromadného zařazení pro snadné vytváření více pozic a zařazení většího počtu pracovníků na tyto pozice.</span><span class="sxs-lookup"><span data-stu-id="268f4-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="268f4-106">Tento postup zahájíte tak, že přejděte na Lidské zdroje > Nábor > Projekty hromadného zařazení.</span><span class="sxs-lookup"><span data-stu-id="268f4-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="268f4-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="268f4-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="268f4-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="268f4-108">Click New.</span></span>
2. <span data-ttu-id="268f4-109">Zadejte hodnotu do pole Projekt hromadného zařazení.</span><span class="sxs-lookup"><span data-stu-id="268f4-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="268f4-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="268f4-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="268f4-111">Zadejte datum do pole Počátek projektu.</span><span class="sxs-lookup"><span data-stu-id="268f4-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="268f4-112">Zadejte datum do pole Konec projektu.</span><span class="sxs-lookup"><span data-stu-id="268f4-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="268f4-113">Klikněte na Otevřít projekt.</span><span class="sxs-lookup"><span data-stu-id="268f4-113">Click Open project.</span></span>
7. <span data-ttu-id="268f4-114">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="268f4-114">Click Yes.</span></span>
8. <span data-ttu-id="268f4-115">Klikněte na Vytvořit pozice.</span><span class="sxs-lookup"><span data-stu-id="268f4-115">Click Create positions.</span></span>
9. <span data-ttu-id="268f4-116">Do pole Množství zadejte počet pozic, které chcete vytvořit</span><span class="sxs-lookup"><span data-stu-id="268f4-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="268f4-117">Počáteční datum se změní na datum náboru nových zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="268f4-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="268f4-118">Konečné datum se změní na datum výpovědi nových zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="268f4-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="268f4-119">Určete, zda noví zaměstnanci budou na pozici zaměstnanců nebo dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="268f4-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="268f4-120">V poli Úloha klikněte na tlačítko rozevíracího seznamu a vyberte úlohu, pro kterou chcete vytvořit pozice.</span><span class="sxs-lookup"><span data-stu-id="268f4-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="268f4-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="268f4-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="268f4-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="268f4-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="268f4-123">Výchozí hodnota ekvivalentu plného úvazku bude vycházet z vybrané práce.</span><span class="sxs-lookup"><span data-stu-id="268f4-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="268f4-124">Tento údaj lze v případě potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="268f4-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="268f4-125">Volitelně vyberte Oddělení pro nové pozice.</span><span class="sxs-lookup"><span data-stu-id="268f4-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="268f4-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="268f4-126">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]