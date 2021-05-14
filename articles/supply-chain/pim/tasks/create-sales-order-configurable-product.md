---
title: Vytvoření prodejní objednávky pro konfigurovatelný produkt
description: Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921282"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="a424a-103">Vytvoření prodejní objednávky pro konfigurovatelný produkt</span><span class="sxs-lookup"><span data-stu-id="a424a-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a424a-104">Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="a424a-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="a424a-105">Tento příklad využívá model reproduktoru D0006 v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a424a-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="a424a-106">Zpracovatel prodejních objednávek obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="a424a-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="a424a-107">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="a424a-107">Create a sales order</span></span>

1. <span data-ttu-id="a424a-108">Přejděte do **Prodej a marketing \> Pracovní prostory \> Zpracování a poptávka prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="a424a-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="a424a-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a424a-109">Select **New**.</span></span>
1. <span data-ttu-id="a424a-110">Vyberte **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="a424a-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="a424a-111">V poli **Účet odběratele** vyberte *US-001*.</span><span class="sxs-lookup"><span data-stu-id="a424a-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="a424a-112">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a424a-112">Select **OK**.</span></span>
1. <span data-ttu-id="a424a-113">V poli **Číslo položky** zvolte *D0006*.</span><span class="sxs-lookup"><span data-stu-id="a424a-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="a424a-114">Pro tento úkol je nutné vybrat konfigurovatelný produkt.</span><span class="sxs-lookup"><span data-stu-id="a424a-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="a424a-115">Vyberte **Produkt a dodávka**.</span><span class="sxs-lookup"><span data-stu-id="a424a-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="a424a-116">Vyberte **Nakonfigurovat řádek**.</span><span class="sxs-lookup"><span data-stu-id="a424a-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="a424a-117">Všimněte si, že se změnila cena, na základě konfigurace, která byla vybrána, a že pole **Zahrnout kabel** je nyní nastaveno na hodnotu *True*.</span><span class="sxs-lookup"><span data-stu-id="a424a-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="a424a-118">Všimněte si výchozí ceny a nastavení, která jsou vybrána pro kabel.</span><span class="sxs-lookup"><span data-stu-id="a424a-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="a424a-119">Vyberte **Načíst šablonu**.</span><span class="sxs-lookup"><span data-stu-id="a424a-119">Select **Load template**.</span></span>
    * <span data-ttu-id="a424a-120">Tento příklad ukazuje, jak lze použít šablonu pro výběr předdefinované konfigurace.</span><span class="sxs-lookup"><span data-stu-id="a424a-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="a424a-121">Pokud používáte tuto proceduru jako průvodce záznamem úloh a chcete zjistit další dostupné hodnoty atributů, musíte vybrat tlačítko **Odemknout**.</span><span class="sxs-lookup"><span data-stu-id="a424a-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="a424a-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a424a-122">Select **OK**.</span></span>
1. <span data-ttu-id="a424a-123">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a424a-123">Select **OK**.</span></span>
1. <span data-ttu-id="a424a-124">Rozbalte sekci **Podrobnosti řádku**.</span><span class="sxs-lookup"><span data-stu-id="a424a-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="a424a-125">Vyberte kartu **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="a424a-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="a424a-126">Konfigurace položky je nyní uvedena pod dimenzemi produktu.</span><span class="sxs-lookup"><span data-stu-id="a424a-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="a424a-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a424a-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]