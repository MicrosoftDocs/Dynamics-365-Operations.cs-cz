---
title: Vložení aplikací Power Apps do Dynamics 365 Human Resources
description: Toto téma vysvětluje, jak vyřešit problém, kdy položka nabídky Microsoft Power Apps zmizela z modulu správy systému.
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460526"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="d9a3a-103">Vložení aplikací Power Apps do Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d9a3a-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="d9a3a-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="d9a3a-104">**Issue**</span></span>

<span data-ttu-id="d9a3a-105">Položka nabídky **Power Apps** zmizela z modulu **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="d9a3a-106">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="d9a3a-106">**Cause**</span></span>

<span data-ttu-id="d9a3a-107">Došlo ke změně návrhu uživatelského rozhraní a Microsoft Power Apps je nyní zahrnuta v standardním modelu přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="d9a3a-108">**Rozlišení**</span><span class="sxs-lookup"><span data-stu-id="d9a3a-108">**Resolution**</span></span>

<span data-ttu-id="d9a3a-109">Způsob integrace aplikací Power Apps se změnil.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="d9a3a-110">Aplikace Power Apps jsou nyní přidávány prostřednictvím modelu přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="d9a3a-111">Aplikace Power Apps můžete přidat téměř na všechny stránky aplikace Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="d9a3a-112">Podrobné informace o tom, jak integrovat aplikace Power Apps do aplikace Talent, najdete v tématu [Integrace Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="d9a3a-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="d9a3a-113">Všichni zákazníci Power Apps, kteří integrovali aplikace před změnou, by měli být upgradováni na nový model.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="d9a3a-114">Tlačítko **Power Apps** je v pravém horním rohu téměř každé stránky v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="d9a3a-115">Toto tlačítko můžete použít pro vložení aplikací.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="d9a3a-116">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-116">Here is an example.</span></span>

1. <span data-ttu-id="d9a3a-117">Přejděte na **Správa zaměstnanců \> Odkazy \> Pracovníci \> Zaměstnanci**.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="d9a3a-118">Vyberte tlačítko **Power Apps** a poté vyberte možnost **Přidat aplikaci z Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Tlačítko Power Apps](media/png.png)

3. <span data-ttu-id="d9a3a-120">Vyplňte pole v dialogovém okně **Přidat aplikaci z Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Přidání aplikace z dialogového okna Power Apps](media/insert-powerapp.png)

<span data-ttu-id="d9a3a-122">Popřípadě postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="d9a3a-123">V podokně akcí stránky na kartě **Možnosti** ve skupině **Přizpůsobit** zvolte **Přizpůsobit tuto stránku**.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Přizpůsobení skupiny na kartě Možnosti](media/options.png)

    <span data-ttu-id="d9a3a-125">Zobrazí se panel nástrojů individuálních nastavení.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="d9a3a-126">Na panelu nástrojů vyberte možnost **Přidat aplikaci z Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="d9a3a-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Přidání aplikace z Power Apps pomocí panelu nástrojů individuálního nastavení](media/powerapp-bar.png)
