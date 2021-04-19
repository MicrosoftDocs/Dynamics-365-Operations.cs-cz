---
title: Záruky na majetek a typy majetku
description: Toto téma vysvětluje, jak nastavit záruky na majetek a typy majetku v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f05f5af76aeb037d606d38a368a49d011f0d2bd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825559"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="18b52-103">Záruky na majetek a typy majetku</span><span class="sxs-lookup"><span data-stu-id="18b52-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="18b52-104">Toto téma vysvětluje, jak nastavit záruky na majetek a typy majetku v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="18b52-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="18b52-105">Nastavení záruky na typ majetku</span><span class="sxs-lookup"><span data-stu-id="18b52-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="18b52-106">Vyberte **Správa majetku**\>**Nastavení**\> **Typy majetku** \>**Typy majetku**.</span><span class="sxs-lookup"><span data-stu-id="18b52-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="18b52-107">V levém podokně vyberte typ majetku, ke kterému chcete připojit záruční smlouvu dodavatele, a poté vyberte **Výchozí hodnoty typu majetku**.</span><span class="sxs-lookup"><span data-stu-id="18b52-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="18b52-108">Na pevné záložce **Obecné** v poli **Záruka dodavatele** vyberte smlouvu.</span><span class="sxs-lookup"><span data-stu-id="18b52-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="18b52-109">Nastavení záruky na majetek</span><span class="sxs-lookup"><span data-stu-id="18b52-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="18b52-110">Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="18b52-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="18b52-111">Vyberte majetek a poté zvolte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="18b52-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="18b52-112">Na pevné záložce **Dodavatel**, v oddílu **Záruka dodavatele**, v poli **Záruka** vyberte záruční smlouvu.</span><span class="sxs-lookup"><span data-stu-id="18b52-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="18b52-113">V polích **Začátek záruky** a **Konec záruky** vyberte počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="18b52-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="18b52-114">Pokud je v poli **Začátek záruky** na pracovním příkazu vybráno datum, záruka bude platit pro tento pracovní příkaz k tomuto datu.</span><span class="sxs-lookup"><span data-stu-id="18b52-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="18b52-115">Při vytvoření pracovního příkazu je pole **Začátek záruky** automaticky nastaveno na datum vytvoření.</span><span class="sxs-lookup"><span data-stu-id="18b52-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="18b52-116">Datum však můžete změnit tak, aby odpovídalo například počátečnímu datu záruční smlouvy.</span><span class="sxs-lookup"><span data-stu-id="18b52-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Stránka Pracovní příkaz](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="18b52-118">Když vytvoříte pracovní příkaz pro majetek, který je pokryt záruční smlouvou dodavatele, a pokud má pracovní příkaz očekávané počáteční datum během záruční doby, obdržíte oznámení o záruční smlouvě.</span><span class="sxs-lookup"><span data-stu-id="18b52-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="18b52-119">Poté můžete požadovaný pracovní příkaz zrušit podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="18b52-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]