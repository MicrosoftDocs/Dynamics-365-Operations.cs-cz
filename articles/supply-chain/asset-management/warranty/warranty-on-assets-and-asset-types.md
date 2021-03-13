---
title: Záruky na majetek a typy majetku
description: Toto téma vysvětluje, jak nastavit záruky na majetek a typy majetku v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c0359bfe31b3d01f28028bb17d5d30af39a1db9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021596"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="c2fe3-103">Záruky na majetek a typy majetku</span><span class="sxs-lookup"><span data-stu-id="c2fe3-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="c2fe3-104">Toto téma vysvětluje, jak nastavit záruky na majetek a typy majetku v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="c2fe3-105">Nastavení záruky na typ majetku</span><span class="sxs-lookup"><span data-stu-id="c2fe3-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="c2fe3-106">Vyberte **Správa majetku**\>**Nastavení**\> **Typy majetku** \>**Typy majetku**.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="c2fe3-107">V levém podokně vyberte typ majetku, ke kterému chcete připojit záruční smlouvu dodavatele, a poté vyberte **Výchozí hodnoty typu majetku**.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="c2fe3-108">Na pevné záložce **Obecné** v poli **Záruka dodavatele** vyberte smlouvu.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="c2fe3-109">Nastavení záruky na majetek</span><span class="sxs-lookup"><span data-stu-id="c2fe3-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="c2fe3-110">Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="c2fe3-111">Vyberte majetek a poté zvolte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="c2fe3-112">Na pevné záložce **Dodavatel**, v oddílu **Záruka dodavatele**, v poli **Záruka** vyberte záruční smlouvu.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="c2fe3-113">V polích **Začátek záruky** a **Konec záruky** vyberte počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c2fe3-114">Pokud je v poli **Začátek záruky** na pracovním příkazu vybráno datum, záruka bude platit pro tento pracovní příkaz k tomuto datu.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="c2fe3-115">Při vytvoření pracovního příkazu je pole **Začátek záruky** automaticky nastaveno na datum vytvoření.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="c2fe3-116">Datum však můžete změnit tak, aby odpovídalo například počátečnímu datu záruční smlouvy.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Stránka Pracovní příkaz](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="c2fe3-118">Když vytvoříte pracovní příkaz pro majetek, který je pokryt záruční smlouvou dodavatele, a pokud má pracovní příkaz očekávané počáteční datum během záruční doby, obdržíte oznámení o záruční smlouvě.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="c2fe3-119">Poté můžete požadovaný pracovní příkaz zrušit podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="c2fe3-119">You can then cancel the work order, as you require.</span></span>
