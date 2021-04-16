---
title: Uložení průvodců záznamem úloh do LCS a jejich opětovné přehrání
description: Tento článek vysvětluje, jak uložit průvodce záznamem úloh do Microsoft Dynamics Lifecycle Services (LCS) a poté je opětovně přehrát.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51ffdb508f09ceaaefb458cd614b9c64604eb639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797904"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="0e017-103">Uložení průvodců záznamem úloh do LCS a jejich opětovné přehrání</span><span class="sxs-lookup"><span data-stu-id="0e017-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0e017-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="0e017-104">**Environment details**</span></span> 

<span data-ttu-id="0e017-105">Microsoft Dynamics 365 Human Resources, která byla nasazena pomocí služby Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="0e017-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="0e017-106">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="0e017-106">**Issue**</span></span>

<span data-ttu-id="0e017-107">Zákazník chce uložit nové záznamy úlohy do projektu LCS a poté uložené průvodce záznamem úloh přehrát.</span><span class="sxs-lookup"><span data-stu-id="0e017-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="0e017-108">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="0e017-108">**Resolution**</span></span>

<span data-ttu-id="0e017-109">Chcete-li uložit záznam úloh do LCS, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0e017-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="0e017-110">Přihlaste se do LCS a vyberte projekt.</span><span class="sxs-lookup"><span data-stu-id="0e017-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="0e017-111">Zvolte dlaždici **Modelování podnikových procesů**.</span><span class="sxs-lookup"><span data-stu-id="0e017-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="0e017-112">Zobrazte tuto stránku v aktualizované zkušenosti BPM.</span><span class="sxs-lookup"><span data-stu-id="0e017-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="0e017-113">Vyberte knihovnu a pak vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="0e017-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="0e017-114">Zadejte název modelu Modelování podnikových procesů.</span><span class="sxs-lookup"><span data-stu-id="0e017-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="0e017-115">Přihlaste se k modulu Lidské zdroje z LCS.</span><span class="sxs-lookup"><span data-stu-id="0e017-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="0e017-116">Do pole **Vyhledat** zadejte **Nápověda**.</span><span class="sxs-lookup"><span data-stu-id="0e017-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="0e017-117">Otevře se nápověda služeb Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0e017-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="0e017-118">Zvolte tlačítko **Aktualizovat** pro konfiguraci nápovědy ke službě Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="0e017-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="0e017-119">Měla by se zobrazit nová knihovna BPM a měla by být aktivní.</span><span class="sxs-lookup"><span data-stu-id="0e017-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="0e017-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e017-120">Close the page.</span></span>
10. <span data-ttu-id="0e017-121">Vytvořit záznam úkolů.</span><span class="sxs-lookup"><span data-stu-id="0e017-121">Create a task recording.</span></span>
11. <span data-ttu-id="0e017-122">Po dokončení zvolte **Uložit ve službách Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="0e017-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Uložit ve službách Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="0e017-124">Vyberte BPM knihovnu a uzel, do kterého chcete uložit záznam úloh.</span><span class="sxs-lookup"><span data-stu-id="0e017-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="0e017-125">Postupujte podle těchto kroků k opětovnému přehrání průvodce záznamem úloh z LCS.</span><span class="sxs-lookup"><span data-stu-id="0e017-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="0e017-126">Spusťte záznamník úloh.</span><span class="sxs-lookup"><span data-stu-id="0e017-126">Start Task recorder.</span></span>
2. <span data-ttu-id="0e017-127">Zvolte **Otevřít z LCS**.</span><span class="sxs-lookup"><span data-stu-id="0e017-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="0e017-128">Vyberte knihovnu a BPM uzel, který má uloženého průvodce záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="0e017-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="0e017-129">Otevřete průvodce záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="0e017-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]