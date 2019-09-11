---
title: Přehled předmětů servisu
description: Servisní předměty jsou majetek a produkty zákazníka, u kterých je lze provádět servisní úkony.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a25c4d71d617a0b7cacd31f708421fd9dd960ea
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865866"
---
# <a name="service-objects-overview"></a><span data-ttu-id="272c8-103">Přehled předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="272c8-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="272c8-104">Servisní předměty jsou majetek a produkty zákazníka, u kterých je lze provádět servisní úkony.</span><span class="sxs-lookup"><span data-stu-id="272c8-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="272c8-105">V závislosti na typu poskytované služby se může jednat o hmotné či nehmotné předměty:</span><span class="sxs-lookup"><span data-stu-id="272c8-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="272c8-106">Hmotnými předměty se rozumí věci jako například stroje, zařízení nebo budovy, pro které lze provádět fyzické servisní úkony.</span><span class="sxs-lookup"><span data-stu-id="272c8-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="272c8-107">Hmotným předmětem servisu může být také skladová položka vytvořená ve formuláři Podrobnosti o uvolněném produktu.</span><span class="sxs-lookup"><span data-stu-id="272c8-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="272c8-108">V závislosti na skupině dimenzí zásob připojené k dané položce můžete vytvořit předmět servisu až na úroveň podrobností zahrnující sériové číslo položky.</span><span class="sxs-lookup"><span data-stu-id="272c8-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="272c8-109">To je užitečné v případech, kdy je třeba sledovat přesnou položku, kterou předmět servisu reprezentuje.</span><span class="sxs-lookup"><span data-stu-id="272c8-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="272c8-110">Hmotným předmětem servisu však může být také položka, která přímo nesouvisí s produkty dané společnosti ani s řetězcem dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="272c8-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="272c8-111">Například sada nástrojů používaná pro opravy v rámci servisní zakázky může být předmětem servisu, který není zahrnut v zásobách.</span><span class="sxs-lookup"><span data-stu-id="272c8-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="272c8-112">V takovém případě ji není nutné zaregistrovat jako skladovou položku.</span><span class="sxs-lookup"><span data-stu-id="272c8-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="272c8-113">Nehmotnými předměty se rozumí nefyzické objekty, jako je například soubor účtů nebo právní dokument, u kterého lze provádět servisní úkony.</span><span class="sxs-lookup"><span data-stu-id="272c8-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="272c8-114">Příklady nehmotných předmětů služby</span><span class="sxs-lookup"><span data-stu-id="272c8-114">Example of an intangible service object</span></span>

<span data-ttu-id="272c8-115">Společnost A spravuje finanční záznamy několika malých společností.</span><span class="sxs-lookup"><span data-stu-id="272c8-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="272c8-116">Jedním z klientů společnosti A je místní fotbalový klub, pro který tato společnost A provádí týdenní úkony účetnictví a také výroční audit klubových účtů.</span><span class="sxs-lookup"><span data-stu-id="272c8-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="272c8-117">Účty klubu jsou konfigurovány ve formuláři Předměty servisu a v servisní smlouvě jsou uvedeny jako předmět servisu.</span><span class="sxs-lookup"><span data-stu-id="272c8-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="272c8-118">U objektu existují dva řádky servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="272c8-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="272c8-119">Řádek 1 obsahuje úkony účetnictví v týdenním intervalu, které jsou přiřazeny k řádku, a řádek 2 obsahuje výroční audit, ke kterému je přidělen roční rozsah.</span><span class="sxs-lookup"><span data-stu-id="272c8-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="272c8-120">Související témata</span><span class="sxs-lookup"><span data-stu-id="272c8-120">Related topics</span></span>

[<span data-ttu-id="272c8-121">Tvorba předmětů servisu</span><span class="sxs-lookup"><span data-stu-id="272c8-121">Create service objects</span></span>](create-service-objects.md)

