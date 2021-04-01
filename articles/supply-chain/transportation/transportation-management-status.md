---
title: Stavy správy přepravy
description: Toto téma vysvětluje, jak vytvořit stav přepravy a mapovat tento stav na stav přepravce.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: fb0d98729046330037f96ab7e13a1bf897e35a1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233336"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="c7f6f-103">Stavy správy přepravy</span><span class="sxs-lookup"><span data-stu-id="c7f6f-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7f6f-104">Nastavte hlavní kódy pro stavy přepravy k interpretaci kódů poskytovaných vašimi přepravci.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="c7f6f-105">To vám umožní integrovat se s přepravci a poskytnout stav.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="c7f6f-106">Stav přepravy, který uvedete pro hlavní kód stavu přepravy, může pomoci sledovat stav nákladu, dodávky nebo kontejneru.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="c7f6f-107">Konkrétní stav přepravy nákladu, zásilky nebo kontejneru lze aktualizovat pouze prostřednictvím integrace dat, nikoli ručně prostřednictvím uživatelského rozhraní.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="c7f6f-108">Vytvoření stavu přepravy</span><span class="sxs-lookup"><span data-stu-id="c7f6f-108">Create a transportation status</span></span>

<span data-ttu-id="c7f6f-109">Chcete-li vytvořit stav přepravy, postupujte dle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="c7f6f-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="c7f6f-110">Přejděte do nabídky **Správa přepravy \> Nastavení \> Hlavní stavy přepravy**.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="c7f6f-111">Zvolte **Nový** a vytvořte hlavní stav přepravy.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="c7f6f-112">V poli **Hlavní stav přepravy** zadejte jedinečný kód pro stav přepravy.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="c7f6f-113">V poli **Typ přepravy** vyberte buď *Přepravce* nebo *Nadřazený uzel* jako typ dopravy.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="c7f6f-114">Zadejte název a stav přepravy.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="c7f6f-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="c7f6f-116">Mapování stavu přepravy na stav přepravce</span><span class="sxs-lookup"><span data-stu-id="c7f6f-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="c7f6f-117">Pro mapování stavu přepravy na stav přepravce postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="c7f6f-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="c7f6f-118">Přejděte do nabídky **Správa přepravy \> \> Přepravci \> Stav přepravy přepravce**.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="c7f6f-119">Vyberte **Nový** a proveďte mapování kódu od dopravce na hlavní kód stavu přepravy.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="c7f6f-120">Vyberte jedinečný identifikátor pro dopravce a službu dopravce.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="c7f6f-121">Vyberte kód stavu přepravy, který má být mapován na kód vybraného dopravce.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="c7f6f-122">Zadejte externí kód, který používá dopravce.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="c7f6f-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c7f6f-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]