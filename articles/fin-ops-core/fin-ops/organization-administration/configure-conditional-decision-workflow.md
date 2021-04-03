---
title: Konfigurace podmíněných rozhodnutí ve workflow
description: Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a593d4e188f47b73967f0c5468f7d7c3e9f64dc8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567453"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="f26dc-103">Konfigurace podmíněných rozhodnutí ve workflow</span><span class="sxs-lookup"><span data-stu-id="f26dc-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f26dc-104">Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="f26dc-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="f26dc-105">Podmíněné rozhodnutí je bod, ve kterém se workflow dělí na dvě větve.</span><span class="sxs-lookup"><span data-stu-id="f26dc-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="f26dc-106">Pokud budete chtít nakonfigurovat podmíněné rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na podmíněné rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="f26dc-107">Pojmenování rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="f26dc-107">Name a decision</span></span>

<span data-ttu-id="f26dc-108">Pomocí následujících kroků zadejte název podmíněného rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="f26dc-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="f26dc-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f26dc-110">V poli **Název** zadejte jedinečný podmíněného rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="f26dc-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="f26dc-111"> Stanovení podmínek</span><span class="sxs-lookup"><span data-stu-id="f26dc-111">Set conditions</span></span>

<span data-ttu-id="f26dc-112">V tomto okamžiku systém určí, která větev se použije, vyhodnocením odeslaného dokumentu k určení, zda vyhovuje konkrétním podmínkám.</span><span class="sxs-lookup"><span data-stu-id="f26dc-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="f26dc-113">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f26dc-114">Klikněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="f26dc-115">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="f26dc-115">Enter a condition.</span></span>
4. <span data-ttu-id="f26dc-116">Zadejte všechny další podmínky, pokud jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="f26dc-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="f26dc-117">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="f26dc-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="f26dc-118">Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="f26dc-119">Vyberte v oblasti **Ověřit podmínku** formuláře záznam.</span><span class="sxs-lookup"><span data-stu-id="f26dc-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="f26dc-120">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-120">Click **Test**.</span></span> <span data-ttu-id="f26dc-121">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="f26dc-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="f26dc-122">Kliknutím na tlačítko **OK** nebo **Zrušit** se vraťte do formuláře **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="f26dc-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]