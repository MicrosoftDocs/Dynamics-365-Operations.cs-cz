---
title: Potvrzení výdeje kusů
description: Výdej kusů umožňuje ověřit jednotlivé kusy zásob prostřednictvím výdeje nebo inventury u mobilního zařízení.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f9da533998341de60d210e196baae64d285d372
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818841"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="e8e3b-103">Potvrzení výdeje kusů</span><span class="sxs-lookup"><span data-stu-id="e8e3b-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8e3b-104">Výdej kusů umožňuje ověřit jednotlivé kusy zásob prostřednictvím výdeje nebo inventury u mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="e8e3b-105">Pro kusy můžete potvrdit množství práce, které má být zpracováno až do množství, které je specifikováno v práci, která má být dodána.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="e8e3b-106">Pro výpočet práce můžete naskenovat zásoby, které započítáváte, a sledovat celkové množství.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-106">For counting work, you can scan the inventory you are counting and track the total amount.</span></span>

<span data-ttu-id="e8e3b-107">Pokud povolíte úkolové práce, potvrzení produktu je vybráno automaticky.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="e8e3b-108">Pro výdeje typu práce můžete nastavit maximální počet kusů.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-108">For work-type picks, you can set a maximum number of pieces.</span></span> <span data-ttu-id="e8e3b-109">To umožňuje nastavit maximální počet kusů, které musí být potvrzeny v pracovním procesu.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="e8e3b-110">Maximální množství je založeno na aktuální jednotce zpracovávané práce.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="e8e3b-111">Typ práce Inventura nepovoluje maximum.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="e8e3b-112">Můžete také použít množství a měrnou jednotku (MJ) přidružené k naskenovanému čárovému kódu.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="e8e3b-113">To bude fungovat u příchozích toků včetně příjmu smíšených registračních značek, položek nákupní objednávky, převodních položek objednávky a položky nákladu.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="e8e3b-114">Také funguje u výdeje po kusech, kde skenování čárového kódu přidá množství k celkovému počtu potvrzených kusů při převodu mezi měrnou jednotkou na čárovém kódu a jednotkou práce.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="e8e3b-115">Pokud se při započítávání MJ na čárovém kódu potvrdí, že je množství přípustné pro započítání do skupiny klasifikace, bude množství připočteno k celkovému součtu.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-115">When counting the UOM on the bar code, if it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e8e3b-116">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="e8e3b-116">Where it applies</span></span>

<span data-ttu-id="e8e3b-117">Výdej kusů funguje pro všechnu práci při inventuře a pro počáteční výběr u jakéhokoli typu práce.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="e8e3b-118">Výdej kusů se nepoužije, pokud je položka řízena sériovými čísly nebo pokud je výrobní zakázka nebo kanban vyskladněn z registrační značky skladového místa a položka je nastavena na Fázování.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="e8e3b-119">Nastavení výdeje kusů</span><span class="sxs-lookup"><span data-stu-id="e8e3b-119">Set up piece picking</span></span>

1.  <span data-ttu-id="e8e3b-120">V položce nabídky mobilního zařízení otevřete formulář nastavení pro potvrzení práce: Řízení skladu > **Řízení skladu** > **Nastavení** > **Mobilní zařízení** > **Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="e8e3b-121">Z položky nabídky mobilního zařízení otevřete Nastavení potvrzení práce.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="e8e3b-122">Následující možnosti budou k dispozici pro výběr, jestliže je typ práce výdej nebo inventura.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="e8e3b-123">Parametr</span><span class="sxs-lookup"><span data-stu-id="e8e3b-123">Option</span></span>           |                                                                            <span data-ttu-id="e8e3b-124">popis</span><span class="sxs-lookup"><span data-stu-id="e8e3b-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e3b-125">Potvrzení výdeje kusů</span><span class="sxs-lookup"><span data-stu-id="e8e3b-125">Piece picking confirmation</span></span> | <span data-ttu-id="e8e3b-126">K dispozici pro typy prací Výdej a inventura.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-126">Available for pick and counting work types.</span></span> <span data-ttu-id="e8e3b-127">Potvrzení produktu je vybráno automaticky.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="e8e3b-128">Umožňuje vám potvrdit jednotlivé skladové položky z mobilního zařízení při naskenování.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="e8e3b-129">Maximální počet kusů</span><span class="sxs-lookup"><span data-stu-id="e8e3b-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="e8e3b-130">K dispozici pro vyskladnění práce, pokud je povoleno potvrzení výdeje kusů.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="e8e3b-131">Nastaví limit na počet kusů, které je třeba potvrdit.</span><span class="sxs-lookup"><span data-stu-id="e8e3b-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]