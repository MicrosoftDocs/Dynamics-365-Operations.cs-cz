---
title: Z důvodu odsouhlasení můžete jako kreditní účet přidat pouze hlavní účet
description: Když ve správě dopravy nastavíte důvod odsouhlasení, můžete jako úvěrový účet přidat pouze hlavní účet.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026323"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="77c69-103">Z důvodu odsouhlasení můžete jako kreditní účet přidat pouze hlavní účet</span><span class="sxs-lookup"><span data-stu-id="77c69-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="77c69-104">Číslo článku znalostní báze: 4603538</span><span class="sxs-lookup"><span data-stu-id="77c69-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="77c69-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="77c69-105">Symptoms</span></span>

<span data-ttu-id="77c69-106">Když ve správě dopravy nastavíte důvod odsouhlasení, můžete jako úvěrový účet přidat pouze hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="77c69-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="77c69-107">Jako kreditní účet nemůžete přidat nákladové středisko ani jinou dimenzi.</span><span class="sxs-lookup"><span data-stu-id="77c69-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="77c69-108">Debetní účet vám však umožňuje vybrat jiné dimenze.</span><span class="sxs-lookup"><span data-stu-id="77c69-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="77c69-109">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="77c69-109">Resolution</span></span>

<span data-ttu-id="77c69-110">Pokud se odsouhlasení neprovede za účelem platby prodejci, ale za účelem připsání částky na konkrétní hlavní účet, systém vám při nastavení důvodu odsouhlasení neumožní vybrat finanční dimenzi pro úvěrový účet.</span><span class="sxs-lookup"><span data-stu-id="77c69-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="77c69-111">Pokud struktura účtu vyžaduje specifickou hodnotu finanční dimenze pro hlavní úvěrový účet, výsledný deník dodavatele nelze zaúčtovat automaticky, protože chybí hodnota finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="77c69-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="77c69-112">Proto musíte nejprve ručně zadat kreditní účet pomocí stránky **Deník faktur**.</span><span class="sxs-lookup"><span data-stu-id="77c69-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="77c69-113">Protože u úvěrového účtu je vyžadována hodnota dimenze, nelze deník faktur dodavatele automaticky zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="77c69-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="77c69-114">Poté, co ručně přidáte hodnotu dimenze do hlavního účtu pro kreditní hranici, musíte ji zaúčtovat ručně.</span><span class="sxs-lookup"><span data-stu-id="77c69-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
