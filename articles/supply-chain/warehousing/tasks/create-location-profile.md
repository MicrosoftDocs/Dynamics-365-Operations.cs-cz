---
title: Vytvoření profilu skladového místa
description: Každé umístění ve skladu musí mít přidružený profil umístění, který popisuje vlastnosti umístění, například zda umístění povoluje smíšené zboží.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bc7705b7db46af8fbe8bf9e78a878a53249b452
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "361376"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="a0458-103">Vytvoření profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="a0458-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0458-104">Každé umístění ve skladu musí mít přidružený profil umístění, který popisuje vlastnosti umístění, například zda umístění povoluje smíšené zboží.</span><span class="sxs-lookup"><span data-stu-id="a0458-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="a0458-105">V této proceduře vytvoříte profil pro umístění, které nevyžaduje kontrolu registrační značky.</span><span class="sxs-lookup"><span data-stu-id="a0458-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="a0458-106">Povolíme stav Smíšené zboží a Smíšené zásoby a také periodickou inventuru.</span><span class="sxs-lookup"><span data-stu-id="a0458-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="a0458-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a0458-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="a0458-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a0458-108">Click New.</span></span>
2. <span data-ttu-id="a0458-109">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="a0458-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="a0458-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="a0458-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a0458-111">V poli Formát skladového místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a0458-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="a0458-112">V poli Typ místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a0458-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="a0458-113">V poli ID profilu správy dokování zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a0458-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="a0458-114">Vyberte možnost Ano v poli Povolit smíšené položky.</span><span class="sxs-lookup"><span data-stu-id="a0458-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="a0458-115">Vyberte možnost Ano v poli Povolit smíšené stavy zásob.</span><span class="sxs-lookup"><span data-stu-id="a0458-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="a0458-116">Vyberte možnost Ano v poli Povolit cyklickou inventuru.</span><span class="sxs-lookup"><span data-stu-id="a0458-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="a0458-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a0458-117">Click Save.</span></span>
11. <span data-ttu-id="a0458-118">Přejděte do nabídky Řízení skladu > Nastavení > Sklad > Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="a0458-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

