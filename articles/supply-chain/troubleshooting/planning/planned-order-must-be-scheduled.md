---
title: Plánovaná výrobní zakázka musí být naplánována, než bude možné ji potvrdit
description: Při pokusu o potvrzení plánované objednávky se zobrazí chybová zpráva s oznámením, že objednávku je třeba naplánovat, než bude možné ji potvrdit.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294033"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="aebf2-103">Plánovaná výrobní zakázka musí být naplánována, než bude možné ji potvrdit</span><span class="sxs-lookup"><span data-stu-id="aebf2-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="aebf2-104">Kód chyby: SYS309802</span><span class="sxs-lookup"><span data-stu-id="aebf2-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="aebf2-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="aebf2-105">Symptoms</span></span>

<span data-ttu-id="aebf2-106">Když se pokusíte potvrdit objednávku, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="aebf2-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="aebf2-107">Plánovaná výrobní zakázka musí být před potvrzením naplánována.</span><span class="sxs-lookup"><span data-stu-id="aebf2-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="aebf2-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="aebf2-108">Cause</span></span>

<span data-ttu-id="aebf2-109">Naplánované datum zahájení a ukončení nesmí být prázdné.</span><span class="sxs-lookup"><span data-stu-id="aebf2-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="aebf2-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="aebf2-110">Resolution</span></span>

<span data-ttu-id="aebf2-111">Chcete-li určit počáteční a konečné datum plánované objednávky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="aebf2-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="aebf2-112">Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="aebf2-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="aebf2-113">Otevřete příslušnou plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="aebf2-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="aebf2-114">Na pevné záložce **Všeobecné** v sekci **Naplánováno** uveďte data v polích **Datum začátku** a **Datum ukončení**.</span><span class="sxs-lookup"><span data-stu-id="aebf2-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
