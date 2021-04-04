---
title: Nastavení stavu cesty
description: Toto téma popisuje, jak nastavit stavové hodnoty, které mohou uživatelé přiřadit cestám.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500879"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="6a0eb-103">Nastavení stavu cesty</span><span class="sxs-lookup"><span data-stu-id="6a0eb-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6a0eb-104">Na stránce **Stav plavby** nastavíte stavové hodnoty, které mohou uživatelé přiřadit plavbám.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="6a0eb-105">Uživatelé mohou přiřadit hodnoty stavu cesty všem úrovním cesty: cestě, přepravnímu kontejneru, foliu, nákupní objednávce a položce (řádky nákupu a řádky převodní objednávky).</span><span class="sxs-lookup"><span data-stu-id="6a0eb-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="6a0eb-106">Používají se pouze pro dva účely:</span><span class="sxs-lookup"><span data-stu-id="6a0eb-106">They are used for two purposes:</span></span>

- <span data-ttu-id="6a0eb-107">Informujte uživatele o stavu plavby, přepravního kontejneru, folia, nákupní objednávky nebo položky (řádky nákupu a řádky převodní objednávky).</span><span class="sxs-lookup"><span data-stu-id="6a0eb-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="6a0eb-108">Omezte použití oblasti nákladů zabráněním úpravám nebo odstranění.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="6a0eb-109">Chcete-li nastavit stavy cesty, přejděte na **Náklady za doručení \> Nastavení \> Stavy cesty**.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="6a0eb-110">Můžete zde přidávat, odebírat a upravovat stavy pomocí tlačítek v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="6a0eb-111">Každá oblast nákladů má vlastní sadu a hierarchii stavů cesty.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="6a0eb-112">Proto na stránce **Stav plavby** v poli **Oblast nákladů** musíte nejprve vybrat oblast nákladů, pro kterou chcete zobrazit nebo vytvořit stav cesty.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="6a0eb-113">Potom pro každý stav cesty podle potřeby nastavte pole, která jsou popsána v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="6a0eb-114">Všimněte si, že stav cesty lze také automaticky změnit podle systémových událostí, jako jsou pravidla, která byla vytvořena pomocí řídicího centra sledování.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="6a0eb-115">Pole</span><span class="sxs-lookup"><span data-stu-id="6a0eb-115">Field</span></span> | <span data-ttu-id="6a0eb-116">popis</span><span class="sxs-lookup"><span data-stu-id="6a0eb-116">Description</span></span> |
|---|---|
| <span data-ttu-id="6a0eb-117">Stav cesty</span><span class="sxs-lookup"><span data-stu-id="6a0eb-117">Voyage status</span></span> | <span data-ttu-id="6a0eb-118">Zadejte jméno stavu cesty.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="6a0eb-119">popis</span><span class="sxs-lookup"><span data-stu-id="6a0eb-119">Description</span></span> | <span data-ttu-id="6a0eb-120">Zadejte popis vybraného stavu cesty.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="6a0eb-121">Změnit</span><span class="sxs-lookup"><span data-stu-id="6a0eb-121">Modify</span></span> | <span data-ttu-id="6a0eb-122">Toto políčko zaškrtněte, pokud mají uživatelé povoleno upravovat cesty, které mají tento stav.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="6a0eb-123">Odstranit</span><span class="sxs-lookup"><span data-stu-id="6a0eb-123">Delete</span></span> | <span data-ttu-id="6a0eb-124">Toto políčko zaškrtněte, pokud mají uživatelé povoleno odstraňovat cesty, které mají tento stav.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="6a0eb-125">Povinné</span><span class="sxs-lookup"><span data-stu-id="6a0eb-125">Mandatory</span></span> | <span data-ttu-id="6a0eb-126">Zaškrtnutím tohoto políčka nastavíte stav cesty jako povinný, aby jej nebylo možné přeskočit.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="6a0eb-127">Nadřazená položka</span><span class="sxs-lookup"><span data-stu-id="6a0eb-127">Parent</span></span> | <span data-ttu-id="6a0eb-128">Toto pole slouží k vytvoření hierarchie mezi hodnotami stavu.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="6a0eb-129">Stav cesty lze změnit (ručně nebo automaticky) pouze dolů v hierarchii, z nadřazeného stavu na jeden z jejích podřízených stavů.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="6a0eb-130">Musíte nastavit pouze konkrétní stavy plavby, které vaše organizace používá.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="6a0eb-131">Mezi typické stavy plavby patří *Potvrzeno*, *Zboží v přepravě*, *Přijato*, *Připraveno k výpočtu nákladů* a *Vypočítané náklady*.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="6a0eb-132">Mohou však existovat i jiné stavy.</span><span class="sxs-lookup"><span data-stu-id="6a0eb-132">However, other statuses might be present.</span></span>
