---
title: Poslední uzavřený řádek práce musí mít hodnotu Vložit
description: Poslední uzavřený řádek práce musí mít hodnotu Vložit
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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924368"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="94bc9-103">Poslední uzavřený řádek práce musí mít hodnotu Vložit</span><span class="sxs-lookup"><span data-stu-id="94bc9-103">The last closed work line must be a put</span></span>

<span data-ttu-id="94bc9-104">Kód chyby: WAX1285</span><span class="sxs-lookup"><span data-stu-id="94bc9-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="94bc9-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="94bc9-105">Symptoms</span></span>

<span data-ttu-id="94bc9-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="94bc9-106">The system shows the following error message:</span></span>

> <span data-ttu-id="94bc9-107">Poslední uzavřený řádek práce musí mít hodnotu Vložit.</span><span class="sxs-lookup"><span data-stu-id="94bc9-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="94bc9-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="94bc9-108">Cause</span></span>

<span data-ttu-id="94bc9-109">Práce nemůže být zrušena v aktuálním stavu.</span><span class="sxs-lookup"><span data-stu-id="94bc9-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="94bc9-110">Na posledním pracovním řádku je pole **Stav práce** nastaveno na hodnotu *Uzavřeno*, ale pole **Typ práce** není nastaveno na hodnotu *Vložit*.</span><span class="sxs-lookup"><span data-stu-id="94bc9-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="94bc9-111">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="94bc9-111">Resolution</span></span>

<span data-ttu-id="94bc9-112">Chcete-li zrušit práci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="94bc9-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="94bc9-113">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="94bc9-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="94bc9-114">Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="94bc9-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="94bc9-115">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="94bc9-115">Select **OK**.</span></span>
1. <span data-ttu-id="94bc9-116">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="94bc9-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="94bc9-117">Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="94bc9-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
