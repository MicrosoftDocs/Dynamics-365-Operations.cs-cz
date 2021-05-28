---
title: Po kopírování prostředí chybí produkty a kategorie
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když produkty a kategorie chybí po zkopírování webu mezi prostředími nebo ve stejném prostředí.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022391"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="cfe58-103">Po kopírování prostředí chybí produkty a kategorie</span><span class="sxs-lookup"><span data-stu-id="cfe58-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfe58-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když produkty a kategorie chybí po zkopírování webu mezi prostředími nebo ve stejném prostředí.</span><span class="sxs-lookup"><span data-stu-id="cfe58-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="cfe58-105">popis</span><span class="sxs-lookup"><span data-stu-id="cfe58-105">Description</span></span>

<span data-ttu-id="cfe58-106">Po zkopírování webu z jednoho prostředí do jiného nebo ve stejném prostředí produkty a kategorie na webu chybí.</span><span class="sxs-lookup"><span data-stu-id="cfe58-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="cfe58-107">Produkty a kategorie budou v prodejně elektronického obchodování a na kartě **Produkty** v Tvůrci webů Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfe58-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="cfe58-108">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="cfe58-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="cfe58-109">Mapování čísla provozní jednotky kanálu na nově zkopírovaný web v nástroji pro tvorbu webů Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe58-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="cfe58-110">Pro mapování čísla provozní jednotky kanálu na nově zkopírovaný web v nástroji pro tvorbu webů Commerce postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="cfe58-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cfe58-111">Vyberte nově zkopírovaný web.</span><span class="sxs-lookup"><span data-stu-id="cfe58-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="cfe58-112">V části **Nastavení webu** vyberte **Kanály**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="cfe58-113">Vedle názvu kanálu vyberte tři tečky (**...**) a poté vyberte **Změnit kanál online obchodu**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="cfe58-114">V dialogovém okně **Změnit kanál online obchodu** vyberte kanál, který se má namapovat na nově zkopírovaný web, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="cfe58-115">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="cfe58-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfe58-116">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="cfe58-116">Additional resources</span></span>

[<span data-ttu-id="cfe58-117">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="cfe58-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
