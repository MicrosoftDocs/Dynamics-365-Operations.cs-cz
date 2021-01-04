---
title: Nastavení srážkové daně
description: Toto téma vysvětluje, jak nastavit srážkovou daň.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441066"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="cb9df-103">Nastavení srážkové daně</span><span class="sxs-lookup"><span data-stu-id="cb9df-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb9df-104">Toto téma vysvětluje, jak nastavit srážkovou daň.</span><span class="sxs-lookup"><span data-stu-id="cb9df-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="cb9df-105">*Srážková daň* je daň uvalená na dodavatele, která nevytváří transakce prodejní daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="cb9df-106">Srážková daň vypočtená pro platby dodavatelů je povinná.</span><span class="sxs-lookup"><span data-stu-id="cb9df-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="cb9df-107">Pro zaúčtování srážkové daně jsou proto platnými účty pouze účty rozvahy nebo závazků.</span><span class="sxs-lookup"><span data-stu-id="cb9df-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="cb9df-108">Tento průvodce úkolem popisuje, jak nastavit srážkovou daň.</span><span class="sxs-lookup"><span data-stu-id="cb9df-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="cb9df-109">Přejděte na **Navigační podokno > Moduly > Daň > Nepřímé daně > Srážková daň > Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="cb9df-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-110">Select **New**.</span></span>
3. <span data-ttu-id="cb9df-111">V poli **Kód srážkové daně** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cb9df-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="cb9df-112">Do pole **Název srážkové daně** zadejte název kódu srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="cb9df-113">V poli **Hlavní účet** vyberte hlavní účet pro zaúčtování povinnosti srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="cb9df-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-114">Select **Save**.</span></span>
7. <span data-ttu-id="cb9df-115">V seznamu vyberte **Hodnoty** a označte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="cb9df-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="cb9df-116">V poli **Hodnota** zadejte procento používané pro výpočet srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="cb9df-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-117">Select **Save**.</span></span>
10. <span data-ttu-id="cb9df-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cb9df-118">Close the page.</span></span>
11. <span data-ttu-id="cb9df-119">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-119">Select **Save**.</span></span>
12. <span data-ttu-id="cb9df-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cb9df-120">Close the page.</span></span>
13. <span data-ttu-id="cb9df-121">Přejděte na **Navigační podokno > Moduly > Daň > Nepřímé daně > Srážková daň > Skupiny srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="cb9df-122">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-122">Select **New**.</span></span>
15. <span data-ttu-id="cb9df-123">Do pole **Skupina srážkové daně** zadejte identifikátor skupiny srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="cb9df-124">Do pole **Popis** zadejte název skupiny srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="cb9df-125">V poli **Kód srážkové daně** vyberte kód srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="cb9df-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="cb9df-126">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cb9df-126">Select **Save**.</span></span>
19. <span data-ttu-id="cb9df-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cb9df-127">Close the page.</span></span>

