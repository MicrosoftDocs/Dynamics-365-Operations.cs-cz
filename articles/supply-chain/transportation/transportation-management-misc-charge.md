---
title: Vedlejší náklady správu dopravy
description: Toto téma vysvětluje, jak musí být poplatky generované přepravou přidruženy ke kódu poplatku.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424283"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="a23da-103">Vedlejší náklady správu dopravy</span><span class="sxs-lookup"><span data-stu-id="a23da-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a23da-104">Stejně jako u vedlejších nákladů musí být poplatky generované přepravou přidruženy ke kódu poplatku.</span><span class="sxs-lookup"><span data-stu-id="a23da-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="a23da-105">V opačném případě nebudou přidány zpět k objednávce jako různé poplatky.</span><span class="sxs-lookup"><span data-stu-id="a23da-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="a23da-106">**Kód poplatku** určuje, jak se účtuje poplatek ve vztahu k objednávce a řádku objednávky, kde je přidána.</span><span class="sxs-lookup"><span data-stu-id="a23da-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="a23da-107">Přejděte na **Správa přepravy > Nastavení > Sazby > Vedlejší poplatky** a definujte kvalifikační kritéria, která určují, kdy se konkrétní **Kód poplatku** vztahuje na poplatek.</span><span class="sxs-lookup"><span data-stu-id="a23da-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="a23da-108">Měli byste mít alespoň jedno nastavení pro každé relevantní nastavení **Modulu poplatků** (*Zákazník* a *Dodavatel*), kde **Typ vedlejších poplatků** je nastaven na *Žádný*.</span><span class="sxs-lookup"><span data-stu-id="a23da-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="a23da-109">Pokud toto chybí, vedlejší poplatek *nebude* přidán k objednávce.</span><span class="sxs-lookup"><span data-stu-id="a23da-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>