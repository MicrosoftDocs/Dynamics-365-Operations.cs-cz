---
title: Nemůžete zrušit práci, která je na uživateli
description: Nemůžete zrušit práci, která je na uživateli
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924394"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="509fc-103">Nemůžete zrušit práci, která je na uživateli</span><span class="sxs-lookup"><span data-stu-id="509fc-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="509fc-104">Kód chyby: WAX708</span><span class="sxs-lookup"><span data-stu-id="509fc-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="509fc-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="509fc-105">Symptoms</span></span>

<span data-ttu-id="509fc-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="509fc-106">The system shows the following error message:</span></span>

> <span data-ttu-id="509fc-107">Nelze stornovat práci, která je u daného uživatele.</span><span class="sxs-lookup"><span data-stu-id="509fc-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="509fc-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="509fc-108">Cause</span></span>

<span data-ttu-id="509fc-109">Práce je uzamčena uživatelem a nelze ji zrušit.</span><span class="sxs-lookup"><span data-stu-id="509fc-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="509fc-110">Chcete-li to potvrdit, otevřete ID práce a poté otevřete kartu **Obecné**. Pokud je práce uzamčena, pole **Stav práce** bude nastaveno na hodnotu *Probíhá* a pole **Zamknul** bude nastaveno na ID uživatele.</span><span class="sxs-lookup"><span data-stu-id="509fc-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="509fc-111">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="509fc-111">Resolution</span></span>

<span data-ttu-id="509fc-112">Chcete-li zrušit práci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="509fc-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="509fc-113">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="509fc-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="509fc-114">Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="509fc-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="509fc-115">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="509fc-115">Select **OK**.</span></span>
1. <span data-ttu-id="509fc-116">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="509fc-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="509fc-117">Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="509fc-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
