---
title: Vytváření skupin oprávnění POS
description: Toto téma vysvětluje, jak vytvořit skupinu oprávnění POS.
author: scott-tucker
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d4634ec275d3d1c2a131c4c1d61cc983e485b14
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798482"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="f533c-103">Vytváření skupin oprávnění POS</span><span class="sxs-lookup"><span data-stu-id="f533c-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f533c-104">Toto téma vysvětluje, jak vytvořit skupinu oprávnění POS.</span><span class="sxs-lookup"><span data-stu-id="f533c-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="f533c-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="f533c-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f533c-106">Tento úkol je určen pro roli Manažer operací Commerce.</span><span class="sxs-lookup"><span data-stu-id="f533c-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="f533c-107">V navigačním podokně přejděte na **Moduly > Retail and Commerce > Zaměstnanci > Skupiny oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="f533c-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="f533c-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f533c-108">Select **New**.</span></span>
3. <span data-ttu-id="f533c-109">Zadejte hodnotu do pole **ID skupiny oprávnění POS**.</span><span class="sxs-lookup"><span data-stu-id="f533c-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="f533c-110">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f533c-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f533c-111">Vyberte možnost **Ano** v poli **Zobrazit časové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="f533c-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="f533c-112">Nyní můžete povolit nebo zakázat různá oprávnění pro skupinu oprávnění POS.</span><span class="sxs-lookup"><span data-stu-id="f533c-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="f533c-113">U některých oprávnění můžete nastavit hodnotu, která se použije k vyhodnocení, zda může uživatel POS provést akci.</span><span class="sxs-lookup"><span data-stu-id="f533c-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="f533c-114">Tento průvodce úkolem povolí několik oprávnění, která můžete udělit pokladníkovi.</span><span class="sxs-lookup"><span data-stu-id="f533c-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="f533c-115">Vyberte možnost **Ano** v poli **Povolit vytvoření objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f533c-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="f533c-116">Vyberte možnost **Ano** v poli **Povolit úpravu objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f533c-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="f533c-117">Vyberte možnost **Ano** v poli **Povolit načtení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f533c-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="f533c-118">Vyberte možnost **Ano** v poli **Povolit změnu hesla**.</span><span class="sxs-lookup"><span data-stu-id="f533c-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="f533c-119">Vyberte možnost **Ano** v poli **Povolit uzavření bez zadání částky**.</span><span class="sxs-lookup"><span data-stu-id="f533c-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="f533c-120">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f533c-120">Select **Save**.</span></span> <span data-ttu-id="f533c-121">Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v kanálech commerce.</span><span class="sxs-lookup"><span data-stu-id="f533c-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="f533c-122">V navigačním podokně přejděte na **Moduly > Lidské zdroje > Práce > Práce**.</span><span class="sxs-lookup"><span data-stu-id="f533c-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="f533c-123">Dále přiřadíme skupinu oprávnění POS úloze.</span><span class="sxs-lookup"><span data-stu-id="f533c-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="f533c-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f533c-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f533c-125">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="f533c-125">Select **Edit**.</span></span>
15. <span data-ttu-id="f533c-126">Rozbalte část **Klasifikace úlohy**.</span><span class="sxs-lookup"><span data-stu-id="f533c-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="f533c-127">V poli Skupina oprávnění POS zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f533c-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="f533c-128">Pozice všech pracovníků pro tuto úlohu budou používat toto nastavení skupiny oprávnění POS, pokud oprávnění POS pracovníků nebylo přepsáno na úrovni jejich pozice.</span><span class="sxs-lookup"><span data-stu-id="f533c-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="f533c-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f533c-129">Select **Save**.</span></span> <span data-ttu-id="f533c-130">Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v kanálech.</span><span class="sxs-lookup"><span data-stu-id="f533c-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]