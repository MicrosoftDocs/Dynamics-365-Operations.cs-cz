---
title: Číselná řada správa přepravy
description: Toto téma popisuje, jak nastavit číselné řady pro správu přepravy.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807673"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="5951b-103">Číselná řada správa přepravy</span><span class="sxs-lookup"><span data-stu-id="5951b-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5951b-104">Použijte stránku **Číselné řady** v modulu správy přepravy a nastavte různá PRO čísla.</span><span class="sxs-lookup"><span data-stu-id="5951b-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="5951b-105">PRO čísla používají dopravci k organizaci a sledování průběhu každé zásilky.</span><span class="sxs-lookup"><span data-stu-id="5951b-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="5951b-106">Vytvořte číselnou řadu pro PRO čísla.</span><span class="sxs-lookup"><span data-stu-id="5951b-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="5951b-107">Chcete-li vytvořit číselnou řadu pro PRO čísla, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="5951b-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="5951b-108">Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="5951b-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="5951b-109">Zvolte **Nový** pro vytvoření nové číselné řady.</span><span class="sxs-lookup"><span data-stu-id="5951b-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="5951b-110">Zadejte jedinečné ID a popisný název číselné řady.</span><span class="sxs-lookup"><span data-stu-id="5951b-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="5951b-111">V poli **Typ číselné řady** je *PRO číslo* jediná možnost.</span><span class="sxs-lookup"><span data-stu-id="5951b-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="5951b-112">V poli **Kontrolní číslice** je *Kontrolní číslice* jedinou možností a je nastavena jako obecný výpočet.</span><span class="sxs-lookup"><span data-stu-id="5951b-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="5951b-113">Na záložce s náhledem **Řada** uveďte informace o řadě.</span><span class="sxs-lookup"><span data-stu-id="5951b-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="5951b-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5951b-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="5951b-115">Propojte číselnou řadu s přepravcem</span><span class="sxs-lookup"><span data-stu-id="5951b-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="5951b-116">Chcete-li spojit číselnou řadu s dopravcem, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="5951b-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="5951b-117">Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Dopravci dodávky**.</span><span class="sxs-lookup"><span data-stu-id="5951b-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="5951b-118">Vyberte dopravce.</span><span class="sxs-lookup"><span data-stu-id="5951b-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="5951b-119">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5951b-119">Select **Edit**.</span></span>
1. <span data-ttu-id="5951b-120">Na záložce s náhledem **Přehled** vyberte možnost v poli **Řada PRO čísel**.</span><span class="sxs-lookup"><span data-stu-id="5951b-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="5951b-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5951b-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]