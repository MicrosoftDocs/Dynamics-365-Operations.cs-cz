---
title: Zákaz pravidel v kontrole konzistence maloobchodních transakcí
description: Toto téma popisuje funkci pro zákaz pravidel kontroly konzistence maloobchodních transakcí v aplikaci Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586290"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="e75db-103">Zákaz pravidel v kontrole konzistence maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="e75db-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e75db-104">Maloobchodní prodejci mohou mít obchodní scénáře a procesy, které jsou pro ně jedinečné.</span><span class="sxs-lookup"><span data-stu-id="e75db-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="e75db-105">Proto ne všechna pravidla, která jsou zahrnuta ve výchozím nastavení v kontrole konzistence transakcí maloobchodu, platí pro všechny maloobchodní prodejce.</span><span class="sxs-lookup"><span data-stu-id="e75db-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="e75db-106">Pro přizpůsobení rozdílů poskytuje aplikace Microsoft Dynamics 365 Retail funkci, kterou lze použít k zakázání pravidel, která nelze použít.</span><span class="sxs-lookup"><span data-stu-id="e75db-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="e75db-107">Chcete-li zobrazit seznam pravidel, která jsou k dispozici v kontrole konzistence transakcí maloobchodu ve vašem prostředí, a zobrazit stav jednotlivých pravidel, přejděte na **Maloobchod \> Nastavení centrály \> Parametry \> Parametry maloobchodu** a pak zvolte kartu **Ověření transakce**</span><span class="sxs-lookup"><span data-stu-id="e75db-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="e75db-108">Ve výchozím nastavení je stav každého pravidla nastaven na **Povoleno**.</span><span class="sxs-lookup"><span data-stu-id="e75db-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="e75db-109">Proto se všechna pravidla používají k ověření maloobchodních transakcí předtím, než jsou načtena do maloobchodních výkazů.</span><span class="sxs-lookup"><span data-stu-id="e75db-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="e75db-110">Chcete-li pravidlo zakázat, změňte jeho stav na **Zakázáno**.</span><span class="sxs-lookup"><span data-stu-id="e75db-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="e75db-111">Zakázaná pravidla nejsou zvažována při ověřování maloobchodních transakcí během procesu výpočtu výkazu.</span><span class="sxs-lookup"><span data-stu-id="e75db-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="e75db-112">Chcete-li obejít celý proces ověření bez ohledu na povolená pravidla, přejděte na **Maloobchod \> Nastavení centrály \> Parametry \> Parametry maloobchodu** a pak na kartě **Ověření transakcí** nastavte možnost **Zakázat kontrolu konzistence pro maloobchodní transakce** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e75db-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="e75db-113">Po nastavení této možnosti na **Ne** ji nelze z uživatelského rozhraní nastavit zpět na možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="e75db-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
