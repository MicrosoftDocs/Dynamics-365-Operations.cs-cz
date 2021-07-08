---
title: Kód dodavatele není autorizován pro konkrétní produkt a datum
description: Při pokusu o potvrzení plánované objednávky nebo přidání řádku k nákupní objednávce se zobrazí chybová zpráva s oznámením, že kód dodavatele není pro produkt a datum autorizován.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294032"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="cadcb-103">Kód dodavatele není autorizován pro konkrétní produkt a datum</span><span class="sxs-lookup"><span data-stu-id="cadcb-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="cadcb-104">Kód chyby: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="cadcb-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="cadcb-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="cadcb-105">Symptoms</span></span>

<span data-ttu-id="cadcb-106">Když se pokusíte potvrdit plánovanou objednávku nebo přidat řádek k nákupní objednávce, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="cadcb-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="cadcb-107">Kód dodavatele %1 není autorizován pro %2 v %3.</span><span class="sxs-lookup"><span data-stu-id="cadcb-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="cadcb-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="cadcb-108">Cause</span></span>

<span data-ttu-id="cadcb-109">Došlo k chybě, protože je pole **Metoda kontroly schváleného dodavatele** je nastaveno na *Pouze varování* nebo *Nepovoleno* pro zadaný produkt a dodavatel není aktuálně oprávněn dodat tento produkt.</span><span class="sxs-lookup"><span data-stu-id="cadcb-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="cadcb-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="cadcb-110">Resolution</span></span>

<span data-ttu-id="cadcb-111">Chcete-li tento problém vyřešit, deaktivujte kontrolu dodavatele u příslušného produktu nebo schvalte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="cadcb-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="cadcb-112">Chcete-li zakázat kontrolu dodavatele produktu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="cadcb-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="cadcb-113">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="cadcb-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="cadcb-114">Otevřete relevantní produkt.</span><span class="sxs-lookup"><span data-stu-id="cadcb-114">Open the relevant product.</span></span>
1. <span data-ttu-id="cadcb-115">Na pevné záložce **Nákup** nastavte pole **Metoda kontroly schváleného dodavatele** na jinou hodnotu než *Pouze varování* nebo *Nepovoleno*.</span><span class="sxs-lookup"><span data-stu-id="cadcb-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="cadcb-116">Chcete-li schválit dodavatele produktu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="cadcb-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="cadcb-117">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="cadcb-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="cadcb-118">Otevřete relevantní položku.</span><span class="sxs-lookup"><span data-stu-id="cadcb-118">Open the relevant item.</span></span>
1. <span data-ttu-id="cadcb-119">V podokně Akce na kartě **Nákup** ve skupině **Schválený dodavatel** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="cadcb-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="cadcb-120">Na stránce seznamu **Schválený dodavatel** přidejte řádek do mřížky a pak pro ni nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="cadcb-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="cadcb-121">**Dodavatel** - Vyberte dodavatele ke schválení pro aktuální produkt.</span><span class="sxs-lookup"><span data-stu-id="cadcb-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="cadcb-122">**Datum účinnosti** - Vyberte první datum, pro které je dodavatel schválen.</span><span class="sxs-lookup"><span data-stu-id="cadcb-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="cadcb-123">**Datum vypršení platnosti** - Vyberte poslední datum, pro které je dodavatel schválen.</span><span class="sxs-lookup"><span data-stu-id="cadcb-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="cadcb-124">Pro další informace viz [Schválení dodavatelů pro konkrétní produkty](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="cadcb-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
