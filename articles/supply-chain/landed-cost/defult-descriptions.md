---
title: Výchozí popisy pro hlavní knihu
description: Výchozí popisy lze použít k aktualizaci pole Popis v zaúčtování dokladů do hlavní knihy.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021605"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="be697-103">Výchozí popisy pro hlavní knihu</span><span class="sxs-lookup"><span data-stu-id="be697-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be697-104">Výchozí popisy lze použít k aktualizaci pole **Popis** v zaúčtování dokladů do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="be697-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="be697-105">Tato funkce byla vylepšena pro práci s náklady za doručení.</span><span class="sxs-lookup"><span data-stu-id="be697-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="be697-106">Chcete-li nastavit výchozí popisy zaúčtování do hlavní knihy, přejděte na uzel **Organizační správa \> Nastavení \> Výchozí popisy**.</span><span class="sxs-lookup"><span data-stu-id="be697-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="be697-107">V následující tabulce jsou uvedeny nové hodnoty, které byly přidány pro pole **Popis** na stránce **Výchozí popisy**, aby podporovaly náklady za doručení.</span><span class="sxs-lookup"><span data-stu-id="be697-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="be697-108">Typ popisu</span><span class="sxs-lookup"><span data-stu-id="be697-108">Description type</span></span> | <span data-ttu-id="be697-109">Poznámky</span><span class="sxs-lookup"><span data-stu-id="be697-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="be697-110">Importovat výpočet nákladů - časové rozlišení nákladů</span><span class="sxs-lookup"><span data-stu-id="be697-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="be697-111">Když je zaúčtována faktura za nákupní objednávku, je zpracováno časové rozlišení nákladů pro odhad nákladů na cestu.</span><span class="sxs-lookup"><span data-stu-id="be697-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="be697-112">Lze zadat výchozí popisy, které do popisu přidají číslo cesty.</span><span class="sxs-lookup"><span data-stu-id="be697-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="be697-113">Pro číslo dodávky použijte zápis *%4*.</span><span class="sxs-lookup"><span data-stu-id="be697-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="be697-114">Importovat výpočet nákladů – objednávka přepravovaného zboží</span><span class="sxs-lookup"><span data-stu-id="be697-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="be697-115">Pokud používáte zpracování během přepravy, zaúčtuje se faktura za nákupní objednávku a zboží se zaúčtuje na účet zboží v přepravě.</span><span class="sxs-lookup"><span data-stu-id="be697-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="be697-116">Lze zadat výchozí popisy, které do popisu přidají číslo objednávky v přepravě.</span><span class="sxs-lookup"><span data-stu-id="be697-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="be697-117">Pro číslo objednávky v přepravě použijte zápis *%4*.</span><span class="sxs-lookup"><span data-stu-id="be697-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="be697-118">Sklad – uzávěrka – úpravy</span><span class="sxs-lookup"><span data-stu-id="be697-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="be697-119">Když je faktura za závazky (AP) zpracována z hlediska nákladů na cestu, je zpracována úprava zásob pro odhad nákladů na cestu.</span><span class="sxs-lookup"><span data-stu-id="be697-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="be697-120">Lze zadat výchozí popisy, které do popisu přidají číslo cesty.</span><span class="sxs-lookup"><span data-stu-id="be697-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="be697-121">Pro číslo dodávky použijte zápis *%4*.</span><span class="sxs-lookup"><span data-stu-id="be697-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="be697-122">Další informace o tom, jak pracovat se stránkou **Výchozí popisy** najdete v tématu [Nastavení výchozích popisů pro automatické zaúčtování](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="be697-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
