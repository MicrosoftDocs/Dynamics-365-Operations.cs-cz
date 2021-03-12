---
title: Režimy a metody správy přepravy
description: Toto téma ukazuje, jak nastavit režimy a metody správy přepravy.
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
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b9b548212c6f1f3faac56cd7ca182d84cc339bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973903"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="a13fd-103">Režimy a metody správy přepravy</span><span class="sxs-lookup"><span data-stu-id="a13fd-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a13fd-104">Režim správy přepravy představuje typ přepravy, který dopravce používá pro dopravení dodávky, jako je méně než nákladní vůz (LTL) nebo nákladní vůz (TL) nebo zásilka.</span><span class="sxs-lookup"><span data-stu-id="a13fd-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="a13fd-105">Metoda přepravy představuje způsob přepravy, který dopravce používá pro dopravení dodávky, jako je vzduch, země, oceán nebo železnice.</span><span class="sxs-lookup"><span data-stu-id="a13fd-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="a13fd-106">Režimy a metody přepravy se používají v několika kontextech.</span><span class="sxs-lookup"><span data-stu-id="a13fd-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="a13fd-107">V plánech tras se používají pouze režimy, zatímco při nastavování přepravců a služeb dopravců se používají jak režimy, tak metody dopravy.</span><span class="sxs-lookup"><span data-stu-id="a13fd-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="a13fd-108">Mezi režimy a metodami přepravy neexistuje explicitní vztah nebo hierarchie.</span><span class="sxs-lookup"><span data-stu-id="a13fd-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="a13fd-109">Vytvoření režimu</span><span class="sxs-lookup"><span data-stu-id="a13fd-109">Create a mode</span></span>

<span data-ttu-id="a13fd-110">Při vytváření režimu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a13fd-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="a13fd-111">Přejděte do **Správa přepravy \> Nastavení \> Dopravci \> Způsob**.</span><span class="sxs-lookup"><span data-stu-id="a13fd-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="a13fd-112">Zvolte **Nový** pro vytvoření nového režimu.</span><span class="sxs-lookup"><span data-stu-id="a13fd-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="a13fd-113">Zadejte jedinečné ID a popisný název režimu.</span><span class="sxs-lookup"><span data-stu-id="a13fd-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="a13fd-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a13fd-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="a13fd-115">Vytvoření metody přepravy</span><span class="sxs-lookup"><span data-stu-id="a13fd-115">Create a transportation method</span></span>

<span data-ttu-id="a13fd-116">Chcete-li vytvořit metodu přepravy, postupujte dle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="a13fd-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="a13fd-117">Přejděte do nabídky **Správa přepravy \> \> Přepravci \> Metody přepravy**.</span><span class="sxs-lookup"><span data-stu-id="a13fd-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="a13fd-118">Zvolte **Nová** a vytvořte novou metodu přepravy.</span><span class="sxs-lookup"><span data-stu-id="a13fd-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="a13fd-119">Zadejte jedinečné ID a popisný název metody přepravy.</span><span class="sxs-lookup"><span data-stu-id="a13fd-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="a13fd-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a13fd-120">Close the page.</span></span>