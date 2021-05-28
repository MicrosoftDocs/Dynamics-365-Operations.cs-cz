---
title: Obrácení hlášení po dokončení vytvoří neočekávanou otevřenou transakci
description: Převrácení hlášení jako dokončeného, které má označení, vytvoří otevřenou transakci, kde má převrácené množství stejné rozměry zásob jako převrácené transakce.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026349"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="82625-103">Obrácení hlášení po dokončení vytvoří neočekávanou otevřenou transakci</span><span class="sxs-lookup"><span data-stu-id="82625-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="82625-104">Číslo článku znalostní báze: 4612469</span><span class="sxs-lookup"><span data-stu-id="82625-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="82625-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="82625-105">Symptoms</span></span>

<span data-ttu-id="82625-106">Pokud převrátíte hlášení jako dokončené, které má označení, systém vytvoří otevřenou transakci, kde má převrácené množství stejné rozměry zásob jako převrácená transakce, která byla stornována.</span><span class="sxs-lookup"><span data-stu-id="82625-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="82625-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="82625-107">Resolution</span></span>

<span data-ttu-id="82625-108">Když obrátíte operaci sestavy jako hotovou, dimenze zásob se inicializuje z výrobního deníku.</span><span class="sxs-lookup"><span data-stu-id="82625-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="82625-109">Proto je číslo dávky získáno.</span><span class="sxs-lookup"><span data-stu-id="82625-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="82625-110">Kvůli označení zdědí transakce prodejní objednávky číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="82625-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="82625-111">Dimenzi lze resetovat, když se zaúčtuje hlášení po dokončení.</span><span class="sxs-lookup"><span data-stu-id="82625-111">The dimension can be reset when the reporting as finished is posted.</span></span>
