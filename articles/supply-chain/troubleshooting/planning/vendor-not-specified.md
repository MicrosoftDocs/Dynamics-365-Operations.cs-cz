---
title: Prodejce není potvrzen, když jsou plánované objednávky aktivovány
description: Při pokusu o potvrzení plánovaných objednávek se zobrazí chybová zpráva s oznámením, že není vybrán žádný dodavatel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cf41295045211f8a714194494028922d573c9e9e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294026"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a><span data-ttu-id="323da-103">Prodejce není potvrzen, když jsou plánované objednávky aktivovány</span><span class="sxs-lookup"><span data-stu-id="323da-103">Vendor isn't specified when planned orders are firmed</span></span>

<span data-ttu-id="323da-104">Kód chyby: SYS23532</span><span class="sxs-lookup"><span data-stu-id="323da-104">Error code: SYS23532</span></span>

## <a name="symptoms"></a><span data-ttu-id="323da-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="323da-105">Symptoms</span></span>

<span data-ttu-id="323da-106">Když se pokusíte potvrdit plánované objednávky, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="323da-106">When you try to firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="323da-107">Dodavatel není zadán</span><span class="sxs-lookup"><span data-stu-id="323da-107">Vendor is not specified</span></span>

## <a name="resolution"></a><span data-ttu-id="323da-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="323da-108">Resolution</span></span>

<span data-ttu-id="323da-109">Chcete-li zadat dodavatele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="323da-109">To specify a vendor, follow these steps.</span></span>

1. <span data-ttu-id="323da-110">Otevřete plánovanou objednávku, u které chybí dodavatel.</span><span class="sxs-lookup"><span data-stu-id="323da-110">Open the planned order that is missing a vendor.</span></span>
1. <span data-ttu-id="323da-111">Na pevné záložce **Plánovaná dodávka** v poli **Dodavatel** vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="323da-111">On the **Planned supply** FastTab, in the **Vendor** field, select a vendor.</span></span>
