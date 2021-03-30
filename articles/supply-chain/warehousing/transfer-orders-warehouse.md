---
title: Nastavení skladů pro převodní příkazy
description: Toto téma popisuje způsob nastavení skladů pro převodní příkazy.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e01629982bb383078e90ff3dad0592371f44bd1b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206840"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="19e0a-103">Nastavení skladů pro převodní příkazy</span><span class="sxs-lookup"><span data-stu-id="19e0a-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19e0a-104">Pomocí úrovní skladů můžete vytvořit hierarchii podporující převodní příkazy mezi sklady.</span><span class="sxs-lookup"><span data-stu-id="19e0a-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="19e0a-105">Na základě tohoto nastavení vypočte hlavní plánování požadavky na položky na jedné úrovni skladu a vygeneruje plánované převodní příkazy z přiřazeného zdrojového skladu, aby byly splněny.</span><span class="sxs-lookup"><span data-stu-id="19e0a-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="19e0a-106">Klikněte na možnosti **Řízení zásob > Nastavení > Rozdělení zásob > Sklady**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="19e0a-107">Vyberte sklad, který chcete doplnit.</span><span class="sxs-lookup"><span data-stu-id="19e0a-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="19e0a-108">Na pevné záložce **Hlavní plánování** zaškrtněte políčko **Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="19e0a-109">V poli **Hlavní sklad** vyberte sklad, který chcete přiřadit jako sklad pro doplňování.</span><span class="sxs-lookup"><span data-stu-id="19e0a-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="19e0a-110">Hlavní plánování vypočte pro zvolený sklad požadavek na převod a vygeneruje plánovaný převodní příkaz z přiřazeného střediska **Hlavní sklad**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="19e0a-111">Pokud zrušíte zaškrtnutí políčka <STRONG>Doplňování</STRONG>, bude k vybranému skladu přiřazena úroveň skladu podle hodnoty pole <STRONG>Hlavní sklad</STRONG>, avšak <STRONG>Hlavní sklad</STRONG> nebude nastaven jako doplňovací sklad.</span><span class="sxs-lookup"><span data-stu-id="19e0a-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="19e0a-112">Zavřete stránku k použití nového nastavení.</span><span class="sxs-lookup"><span data-stu-id="19e0a-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="19e0a-113">Chcete-li provést přiřazení určitého skladu pro doplňování, je nutné nejprve daný sklad nastavit jako dimenzi úložiště na stránce <STRONG>Skupiny dimenze úložiště</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="19e0a-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="19e0a-114">Na této stránce vyberte pole <STRONG>Aktivní</STRONG> a <STRONG>plán disponibility podle dimenzí</STRONG> pro sklad.</span><span class="sxs-lookup"><span data-stu-id="19e0a-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="19e0a-115">Nastavení doby realizace přepravy</span><span class="sxs-lookup"><span data-stu-id="19e0a-115">Set up transport lead time</span></span>

<span data-ttu-id="19e0a-116">Je také nutné nastavit dobu realizace přepravy mezi sklady na stránce **Dny přepravy**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="19e0a-117">Přejděte na **Řízení zásob > Nastavení > Distribuce > Dny přepravy**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="19e0a-118">V poli **Místo příjmu** vyberte **sklad**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="19e0a-119">Vyberte **odesílající sklad**, **přijímající sklad** a **Počet dnů přepravy**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="19e0a-120">(Volitelné) Můžete také nastavit dobu přepravy v závislosti na režimu doručení na kartě **Dny dopravy podle způsobu doručení**.</span><span class="sxs-lookup"><span data-stu-id="19e0a-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]