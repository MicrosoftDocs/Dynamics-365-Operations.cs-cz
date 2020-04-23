---
title: Nastavení omezení přepravy pro položku
description: Tento postup nastaví omezení přepravy a zabrání přepravě vybrané položky pomocí vybraného centra.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8eb9873f0ad6f404dc88d27ed5feedfc71fd62b5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201403"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="81e4f-103">Nastavení omezení přepravy pro položku</span><span class="sxs-lookup"><span data-stu-id="81e4f-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81e4f-104">Tento postup nastaví omezení přepravy a zabrání přepravě vybrané položky pomocí vybraného centra.</span><span class="sxs-lookup"><span data-stu-id="81e4f-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="81e4f-105">Tento úkol obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="81e4f-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="81e4f-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="81e4f-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="81e4f-107">Vytvoření omezení položky</span><span class="sxs-lookup"><span data-stu-id="81e4f-107">Create an item constaint</span></span>
1. <span data-ttu-id="81e4f-108">Přejděte na Omezení.</span><span class="sxs-lookup"><span data-stu-id="81e4f-108">Go to Constraints.</span></span>
2. <span data-ttu-id="81e4f-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="81e4f-109">Click New.</span></span>
3. <span data-ttu-id="81e4f-110">Zadejte hodnotu do pole Omezení položky.</span><span class="sxs-lookup"><span data-stu-id="81e4f-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="81e4f-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="81e4f-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="81e4f-112">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="81e4f-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="81e4f-113">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="81e4f-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="81e4f-114">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="81e4f-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="81e4f-115">V poli Centrum zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="81e4f-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="81e4f-116">Vyberte volbu v poli Akce omezení.</span><span class="sxs-lookup"><span data-stu-id="81e4f-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="81e4f-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="81e4f-117">Click Save.</span></span>
11. <span data-ttu-id="81e4f-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="81e4f-118">Close the page.</span></span>

