---
title: Snadný offline přepínač pro operace dárkového poukazu a dobropisu
description: V tomto tématu je uveden přehled vylepšení, která poskytují jednoduchý offline přepínač pro určité typy plateb.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230661"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="8c90b-103">Snadný offline přepínač pro operace dárkového poukazu a dobropisu</span><span class="sxs-lookup"><span data-stu-id="8c90b-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c90b-104">Pokud zařízení pokladního místa (POS) ztratí spojení s databází kanálu, většina operací a transakcí POS, které probíhaly, mohou pokračovat poté, co pokladník obdrží varovnou zprávu o ztrátě připojení.</span><span class="sxs-lookup"><span data-stu-id="8c90b-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="8c90b-105">V některých případech však transakce obsahují prvky, které vyžadují službu v reálném čase, a tyto prvky nejsou podporovány v případě, že je POS offline.</span><span class="sxs-lookup"><span data-stu-id="8c90b-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="8c90b-106">V tomto tématu jsou popsány některé funkce, které v takových případech pomáhají snižovat dopad ztraceného připojení.</span><span class="sxs-lookup"><span data-stu-id="8c90b-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="8c90b-107">Provedení transakcí dárkového poukazu v offline režimu</span><span class="sxs-lookup"><span data-stu-id="8c90b-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="8c90b-108">Interní dárkové poukazy vyžadují službu v reálném čase, protože zůstatek pro dárkové poukazy musí být centrálně udržován v Microsoft Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8c90b-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="8c90b-109">Aby se zabránilo podvodům nebo jiným problémům se synchronizací, dárkové poukazy jsou uzamčeny okamžitě po přidání do transakce.</span><span class="sxs-lookup"><span data-stu-id="8c90b-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="8c90b-110">Funkce uzamknutí zajišťuje, že dárkový poukaz nelze použít na více terminálech současně.</span><span class="sxs-lookup"><span data-stu-id="8c90b-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="8c90b-111">Po dokončení transakce je dárkový poukaz automaticky aktualizován a odemknut.</span><span class="sxs-lookup"><span data-stu-id="8c90b-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="8c90b-112">Pokud však POS ztratí spojení po přidání dárkového poukazu do transakce, může být dárkový poukaz nepoužitelný.</span><span class="sxs-lookup"><span data-stu-id="8c90b-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="8c90b-113">Chcete-li předejít této situaci, Dynamics 365 Commerce obsahuje parametr, který umožňuje dokončit transakce zahrnující řádek dárkového poukazu v době, kdy je POS v režimu offline.</span><span class="sxs-lookup"><span data-stu-id="8c90b-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="8c90b-114">Je-li tento parametr zapnut, budou transakce dárkových poukazů, které jsou vynuceny offline, uloženy společně s offline transakcemi a budou synchronizovány s Commerce Headquarters při synchronizaci offline transakcí.</span><span class="sxs-lookup"><span data-stu-id="8c90b-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="8c90b-115">Synchronizace také odemkne dárkový poukaz, takže jej bude možné použít na jiném terminálu.</span><span class="sxs-lookup"><span data-stu-id="8c90b-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="8c90b-116">Chcete-li povolit funkci uzavření transakcí dárkového poukazu po přepnutí do režimu offline, přejděte na kartu **Zaúčtování** na stránce **Parametry Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8c90b-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="8c90b-117">Na dané kartě vyhledejte pevnou záložku **Dárkový poukaz** a nastavte možnost **Povolit uzavření transakcí dárkového poukazu v offline režimu** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8c90b-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Nastavení dárkového poukazu offline](../media/gift.png)

<span data-ttu-id="8c90b-119">Parametry Commerce jsou obvykle uloženy v mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="8c90b-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="8c90b-120">Z toho vyplývá, že po aktualizaci nastavení tohoto parametru a při zahájení plánu distribuce dojde k synchronizaci změny v kanálu, takže se tato změna může uskutečnit až 24 hodin.</span><span class="sxs-lookup"><span data-stu-id="8c90b-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="8c90b-121">Chcete-li provést okamžitou efektivní změnu, obnovte službu IIS (Microsoft Internet Information Services).</span><span class="sxs-lookup"><span data-stu-id="8c90b-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="8c90b-122">Provedení transakcí dobropisu v offline režimu</span><span class="sxs-lookup"><span data-stu-id="8c90b-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="8c90b-123">Stejně jako u interních dárkových poukazů jsou dobropisy centrálně udržovány v Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8c90b-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="8c90b-124">Comerce má parametr, který umožňuje dokončení transakcí dobropisu v době, kdy je POS v režimu offline.</span><span class="sxs-lookup"><span data-stu-id="8c90b-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="8c90b-125">Tento parametr funguje podobně jako parametr dárkového poukazu uvedený v předchozí sekci.</span><span class="sxs-lookup"><span data-stu-id="8c90b-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="8c90b-126">Je-li parametr zapnutý, budou transakce dobropisu, které jsou vynuceny offline, synchronizovány zpět s databází kanálů spolu s ostatními transakcemi, které byly provedeny v době, kdy byl POS v režimu offline.</span><span class="sxs-lookup"><span data-stu-id="8c90b-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="8c90b-127">Chcete-li povolit funkci uzavření transakcí dobropisu po přepnutí do režimu offline, přejděte na kartu **Zaúčtování** na stránce **Parametry Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8c90b-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="8c90b-128">Na dané kartě vyhledejte pevnou záložku **Dobropis** a nastavte možnost **Povolit uzavření transakcí dobropisu v offline režimu** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8c90b-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Nastavení dobropisu offline](../media/creditmemo.png)

<span data-ttu-id="8c90b-130">Parametry Commerce jsou obvykle uloženy v mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="8c90b-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="8c90b-131">Z toho vyplývá, že po aktualizaci nastavení tohoto parametru a při zahájení plánu distribuce dojde k synchronizaci změny v kanálu, takže se tato změna může uskutečnit až 24 hodin.</span><span class="sxs-lookup"><span data-stu-id="8c90b-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="8c90b-132">Chcete-li provést změny okamžitě, obnovte službu IIS.</span><span class="sxs-lookup"><span data-stu-id="8c90b-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c90b-133">Související témata</span><span class="sxs-lookup"><span data-stu-id="8c90b-133">Related topics</span></span>

- [<span data-ttu-id="8c90b-134">Offline funkce pokladního místa (POS)</span><span class="sxs-lookup"><span data-stu-id="8c90b-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="8c90b-135">Online a offline operace pokladního místa (POS)</span><span class="sxs-lookup"><span data-stu-id="8c90b-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]