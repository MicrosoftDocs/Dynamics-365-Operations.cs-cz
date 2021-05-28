---
title: Na vydaný produkt nelze použít šablonu
description: Na vydaný produkt nelze použít šablonu.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026330"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="2ddae-103">Na vytvoření vydaného produktu nelze použít šablonu.</span><span class="sxs-lookup"><span data-stu-id="2ddae-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="2ddae-104">Číslo článku znalostní báze: 4612097</span><span class="sxs-lookup"><span data-stu-id="2ddae-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="2ddae-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="2ddae-105">Symptoms</span></span>

<span data-ttu-id="2ddae-106">Když vytvoříte nový vydaný produkt pomocí dialogového okna **Nově vydaný produkt**, můžete vybrat šablonu.</span><span class="sxs-lookup"><span data-stu-id="2ddae-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="2ddae-107">Šablona by měla poskytovat výchozí nastavení pro mnoho polí nově vydaného produktu.</span><span class="sxs-lookup"><span data-stu-id="2ddae-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="2ddae-108">Některá nebo všechna pole se však po výběru šablony nenastaví.</span><span class="sxs-lookup"><span data-stu-id="2ddae-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="2ddae-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="2ddae-109">Cause</span></span>

<span data-ttu-id="2ddae-110">Mnoho stránek v Microsoft Dynamics 365 Supply Chain Management vám umožní vytvořit šablonu, která stanoví počáteční nastavení pro záznamy, které se zobrazují na těchto stránkách.</span><span class="sxs-lookup"><span data-stu-id="2ddae-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="2ddae-111">Jednu z těchto šablon můžete vytvořit výběrem možnosti **Informace o záznamu** na kartě **Možnosti** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="2ddae-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="2ddae-112">Vydané produkty jsou však mnohem komplexnější než většina ostatních typů záznamů.</span><span class="sxs-lookup"><span data-stu-id="2ddae-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="2ddae-113">I když můžete vybrat **Informace o záznamu** na stránce **Vydané produkty** k vytvoření šablony, a i když tuto šablonu můžete vybrat při vytváření vydaného produktu, šablona neposkytne očekávané hodnoty polí pro nově vydaný produkt.</span><span class="sxs-lookup"><span data-stu-id="2ddae-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="2ddae-114">Proto u vydaných produktů nemůžete použít šablony „informace o záznamu“.</span><span class="sxs-lookup"><span data-stu-id="2ddae-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="2ddae-115">Místo toho musíte vytvořit vyhrazené šablony produktů.</span><span class="sxs-lookup"><span data-stu-id="2ddae-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="2ddae-116">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="2ddae-116">Resolution</span></span>

<span data-ttu-id="2ddae-117">Chcete-li vytvořit šablonu produktu, použijte nabídku **Šablona** na kartě **Produkt** podokna akcí, nikoli tlačítko **Informace o záznamu** na kartě **Možnosti**.</span><span class="sxs-lookup"><span data-stu-id="2ddae-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="2ddae-118">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="2ddae-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2ddae-119">V podokně akcí na kartě **Produkt** ve skupině **Nový** vyberte **Šablona** a pak vyberte **Vytvořit osobní šablonu** nebo **Vytvořit sdílenou šablonu**.</span><span class="sxs-lookup"><span data-stu-id="2ddae-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
