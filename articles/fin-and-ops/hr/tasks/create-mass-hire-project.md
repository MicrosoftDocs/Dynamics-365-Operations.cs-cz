---
title: Vytvoření projektu masového pronájmu
description: Tento postup vás provede nastavením procesu hromadného zařazování zaměstnanců.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea0f4638a968d2aecf4e3bb27acbd19e6455a8b3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510652"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="51159-103">Vytvoření projektu masového pronájmu</span><span class="sxs-lookup"><span data-stu-id="51159-103">Create a mass hire project</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51159-104">Tento postup vás provede nastavením procesu hromadného zařazování zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="51159-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="51159-105">Náborový zaměstnanec může využívat projekty hromadného zařazení pro snadné vytváření více pozic a zařazení většího počtu pracovníků na tyto pozice.</span><span class="sxs-lookup"><span data-stu-id="51159-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="51159-106">Tento postup zahájíte tak, že přejděte na Lidské zdroje > Nábor > Projekty hromadného zařazení.</span><span class="sxs-lookup"><span data-stu-id="51159-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="51159-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="51159-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="51159-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="51159-108">Click New.</span></span>
2. <span data-ttu-id="51159-109">Zadejte hodnotu do pole Projekt hromadného zařazení.</span><span class="sxs-lookup"><span data-stu-id="51159-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="51159-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="51159-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="51159-111">Zadejte datum do pole Počátek projektu.</span><span class="sxs-lookup"><span data-stu-id="51159-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="51159-112">Zadejte datum do pole Konec projektu.</span><span class="sxs-lookup"><span data-stu-id="51159-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="51159-113">Klikněte na Otevřít projekt.</span><span class="sxs-lookup"><span data-stu-id="51159-113">Click Open project.</span></span>
7. <span data-ttu-id="51159-114">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="51159-114">Click Yes.</span></span>
8. <span data-ttu-id="51159-115">Klikněte na Vytvořit pozice.</span><span class="sxs-lookup"><span data-stu-id="51159-115">Click Create positions.</span></span>
9. <span data-ttu-id="51159-116">Do pole Množství zadejte počet pozic, které chcete vytvořit</span><span class="sxs-lookup"><span data-stu-id="51159-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="51159-117">Počáteční datum se změní na datum náboru nových zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="51159-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="51159-118">Konečné datum se změní na datum výpovědi nových zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="51159-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="51159-119">Určete, zda noví zaměstnanci budou na pozici zaměstnanců nebo dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="51159-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="51159-120">V poli Úloha klikněte na tlačítko rozevíracího seznamu a vyberte úlohu, pro kterou chcete vytvořit pozice.</span><span class="sxs-lookup"><span data-stu-id="51159-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="51159-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="51159-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="51159-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="51159-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51159-123">Výchozí hodnota ekvivalentu plného úvazku bude vycházet z vybrané práce.</span><span class="sxs-lookup"><span data-stu-id="51159-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="51159-124">Tento údaj lze v případě potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="51159-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="51159-125">Volitelně vyberte Oddělení pro nové pozice.</span><span class="sxs-lookup"><span data-stu-id="51159-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="51159-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51159-126">Click OK.</span></span>

