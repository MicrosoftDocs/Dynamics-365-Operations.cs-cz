---
title: Pohyb zásob s přidruženou prací v řízení skladu
description: Toto téma popisuje, jak nastavit a použít potvrzení výdeje kusů a registrační značky z mobilního zařízení.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 618942ff22b6a81c75bd472955e4add14e6f4d84
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "347645"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="a4af3-103">Pohyb zásob s přidruženou prací v řízení skladu</span><span class="sxs-lookup"><span data-stu-id="a4af3-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4af3-104">Pomocí přesunu zásob, je možné rozhodnout, kteří pracovníci skladu mohou přesunout rezervované zásoby.</span><span class="sxs-lookup"><span data-stu-id="a4af3-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="a4af3-105">Tím je zajištěna flexibilita v regulovaných skladech, kde se můžete rozhodnout nepovolil pracovníkovi zvolit nové místo vyskladnění pro již vytvořenou práci výdeje.</span><span class="sxs-lookup"><span data-stu-id="a4af3-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="a4af3-106">Umožňuje také vedoucímu skladu řídit, které možnosti mají někteří méně zkušení pracovníci.</span><span class="sxs-lookup"><span data-stu-id="a4af3-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="a4af3-107">Flexibilita řízení každodenního provozu pracovníků skladu může být užitečné v situacích, jako jsou tyto:</span><span class="sxs-lookup"><span data-stu-id="a4af3-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="a4af3-108">Scénář 1</span><span class="sxs-lookup"><span data-stu-id="a4af3-108">Scenario 1</span></span>
<span data-ttu-id="a4af3-109">Společnost má poměrně malou oblast příjmu a je přetížena paletami a krabicemi, které čekají na vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="a4af3-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="a4af3-110">Očekává se velká dodávka v aktuální den, takže přijímající pracovník rozhodne uklidit oblast příjmu přesunutím některých palet do sekundární příchozí přípravné oblasti.</span><span class="sxs-lookup"><span data-stu-id="a4af3-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="a4af3-111">Scénář 2</span><span class="sxs-lookup"><span data-stu-id="a4af3-111">Scenario 2</span></span>
<span data-ttu-id="a4af3-112">Zkušený pracovník skladu zaznamená ve skladu příležitost konsolidovat položky v jenom místě, místo aby je bylo nutné rozdělit do tří nedalekých míst po malých množstvích.</span><span class="sxs-lookup"><span data-stu-id="a4af3-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="a4af3-113">Pracovník chce sloučit množství přesunutím položek z každého takového skladového místa na stejné místo a se stejnou registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="a4af3-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="a4af3-114">Scénář 3</span><span class="sxs-lookup"><span data-stu-id="a4af3-114">Scenario 3</span></span>
<span data-ttu-id="a4af3-115">Paleta čeká na dodávku do přechodného skladového místa, například STAGE01, který se nachází v BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="a4af3-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="a4af3-116">Z důvodu změny plánů však je však naplánován příjezd dodávky na BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="a4af3-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="a4af3-117">Úředník to ví a potřebuje mít jistotu, že dodávka nemusí čekat na naložení v místě STAGE01.</span><span class="sxs-lookup"><span data-stu-id="a4af3-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="a4af3-118">Úředník rozhodne, že chcete převést položky v této dodávce z místa STAGE01 do STAGE04, které je blíž novému cíli.</span><span class="sxs-lookup"><span data-stu-id="a4af3-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="a4af3-119">Aktuální omezení</span><span class="sxs-lookup"><span data-stu-id="a4af3-119">Current limitations</span></span>

<span data-ttu-id="a4af3-120">Rezervace práce, které lze přesunout, jsou omezeny na prodejní objednávku, převod objednávky výdeje, příjem objednávky převodu, nákupní objednávky a práci doplnění.</span><span class="sxs-lookup"><span data-stu-id="a4af3-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="a4af3-121">Přesunutí položek je omezeno, aby se zabránilo rozdělení řádků práce.</span><span class="sxs-lookup"><span data-stu-id="a4af3-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="a4af3-122">To znamená, že pokud máte ze skladovacího místa Loc1 řádek práce pro 100 kusů položky A, nebude možné odtud přesunout pouze 30 kusů položky A do jiného umístění.</span><span class="sxs-lookup"><span data-stu-id="a4af3-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="a4af3-123">Vzhledem k tomu, že skladová místa jsou nyní různá, znamenalo by to rozdělení řádku stávající práce na 30 a 70.</span><span class="sxs-lookup"><span data-stu-id="a4af3-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="a4af3-124">U scénářů fázování, kdy registrační značka, ze které přesouváte zboží, nebo registrační značka, na kterou přesouváte zboží, je nastavena jako cílová registrační značka pro výrobní příkaz platí, že je povolen pouze přesun celé registrační značky, aby se nerozdělila cílová registrační značka.</span><span class="sxs-lookup"><span data-stu-id="a4af3-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="a4af3-125">Pouze pohyb ad hoc je aktuálně podporován.</span><span class="sxs-lookup"><span data-stu-id="a4af3-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="a4af3-126">To znamená, že nebudete moci přesunout rezervované zásoby prostřednictvím pohybu podle položek nabídky mobilního zařízení šablony.</span><span class="sxs-lookup"><span data-stu-id="a4af3-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="a4af3-127">Nastavení oprávnění k přesunutí zásob rezervovaných pro jednotlivé pracovníky</span><span class="sxs-lookup"><span data-stu-id="a4af3-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="a4af3-128">U pracovníka, který má dovoleno přesunout rezervované zásoby, zaškrtněte políčko **Povolit pohyb zásob s přidruženou prací** ve skupinovém rámečku **řízení skladu** > **nastavení** > **pracovník**.</span><span class="sxs-lookup"><span data-stu-id="a4af3-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="a4af3-129">Přeneseno zpět</span><span class="sxs-lookup"><span data-stu-id="a4af3-129">Backported</span></span>

<span data-ttu-id="a4af3-130">Tato funkce také byla přenesena zpět do aplikace Microsoft Dynamics AX 2012 R3 a bude dostupná v rámci CU12.</span><span class="sxs-lookup"><span data-stu-id="a4af3-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="a4af3-131">Lze ji stáhnout také samostatně prostřednictvím KB číslo 3192548.</span><span class="sxs-lookup"><span data-stu-id="a4af3-131">It can also be downloaded individually through KB number 3192548.</span></span> 

