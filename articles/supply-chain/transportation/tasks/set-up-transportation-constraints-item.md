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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2ff8458a9821e1aa2ae8d2dc93cc89cfc318d70
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233552"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="5f247-103">Nastavení omezení přepravy pro položku</span><span class="sxs-lookup"><span data-stu-id="5f247-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f247-104">Tento postup nastaví omezení přepravy a zabrání přepravě vybrané položky pomocí vybraného centra.</span><span class="sxs-lookup"><span data-stu-id="5f247-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="5f247-105">Tento úkol obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="5f247-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="5f247-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="5f247-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="5f247-107">Vytvoření omezení položky</span><span class="sxs-lookup"><span data-stu-id="5f247-107">Create an item constaint</span></span>
1. <span data-ttu-id="5f247-108">Přejděte na Omezení.</span><span class="sxs-lookup"><span data-stu-id="5f247-108">Go to Constraints.</span></span>
2. <span data-ttu-id="5f247-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5f247-109">Click New.</span></span>
3. <span data-ttu-id="5f247-110">Zadejte hodnotu do pole Omezení položky.</span><span class="sxs-lookup"><span data-stu-id="5f247-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="5f247-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="5f247-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5f247-112">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5f247-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="5f247-113">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5f247-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="5f247-114">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5f247-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="5f247-115">V poli Centrum zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5f247-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="5f247-116">Vyberte volbu v poli Akce omezení.</span><span class="sxs-lookup"><span data-stu-id="5f247-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="5f247-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5f247-117">Click Save.</span></span>
11. <span data-ttu-id="5f247-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f247-118">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]