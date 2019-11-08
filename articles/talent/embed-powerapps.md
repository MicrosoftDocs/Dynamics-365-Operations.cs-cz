---
title: Integrace aplikací PowerApps v Dynamics 365 - Core HR
description: Toto téma vysvětluje, jak vyřešit problém, kdy položka nabídky PowerApps zmizela z modulu správy systému.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550996"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="e5c08-103">Integrace aplikací PowerApps v Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="e5c08-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5c08-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="e5c08-104">**Issue**</span></span>

<span data-ttu-id="e5c08-105">Položka nabídky **PowerApps** zmizela z modulu **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="e5c08-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="e5c08-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="e5c08-106">**Cause**</span></span>

<span data-ttu-id="e5c08-107">Došlo ke změně návrhu uživatelského rozhraní a Microsoft PowerApps je nyní zahrnuta v standardním modelu přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="e5c08-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="e5c08-108">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="e5c08-108">**Resolution**</span></span>

<span data-ttu-id="e5c08-109">Způsob integrace PowerApps se změnil.</span><span class="sxs-lookup"><span data-stu-id="e5c08-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="e5c08-110">Aplikace PowerApps jsou nyní přidávány prostřednictvím modelu přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="e5c08-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="e5c08-111">Aplikace PowerApps můžete přidat téměř na všechny stránky aplikace Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="e5c08-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="e5c08-112">Podrobné informace o tom, jak integrovat aplikace PowerApps do aplikace Talent, najdete v tématu [Integrace aplikací PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="e5c08-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="e5c08-113">Všichni zákazníci PowerApps, kteří integrovali aplikace před změnou, by měli být upgradováni na nový model.</span><span class="sxs-lookup"><span data-stu-id="e5c08-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="e5c08-114">Tlačítko **PowerApps** je v pravém horním rohu téměř každé stránky v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="e5c08-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="e5c08-115">Toto tlačítko můžete použít pro vložení aplikace PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e5c08-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="e5c08-116">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="e5c08-116">Here is an example.</span></span>

1. <span data-ttu-id="e5c08-117">Přejděte na **Správa zaměstnanců \> Odkazy \> Pracovníci \> Zaměstnanci**.</span><span class="sxs-lookup"><span data-stu-id="e5c08-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="e5c08-118">Vyberte tlačítko **PowerApps** a pak vyberte **Vložit PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5c08-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![Tlačítko PowerApps](media/png.png)

3. <span data-ttu-id="e5c08-120">Vyplňte pole v dialogovém okně **Vložit PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5c08-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Vložení dialogového okna PowerApp](media/insert-powerapp.png)

<span data-ttu-id="e5c08-122">Popřípadě postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="e5c08-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="e5c08-123">V podokně akcí stránky na kartě **Možnosti** ve skupině **Přizpůsobit** zvolte **Přizpůsobit tento formulář**.</span><span class="sxs-lookup"><span data-stu-id="e5c08-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Přizpůsobení skupiny na kartě Možnosti](media/options.png)

    <span data-ttu-id="e5c08-125">Zobrazí se panel nástrojů individuálních nastavení.</span><span class="sxs-lookup"><span data-stu-id="e5c08-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="e5c08-126">Na panelu nástrojů zvolte **Vložit \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5c08-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Vložení aplikace PowerApps pomocí panelu nástrojů individuálního nastavení](media/powerapp-bar.png)
