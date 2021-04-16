---
title: Konfigurace podmíněných rozhodnutí ve workflow
description: Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.
author: ChrisGarty
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
ms.openlocfilehash: ed53eeb26e1b4b1df1647739ce1d115c7dd169f8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747924"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="be827-103">Konfigurace podmíněných rozhodnutí ve workflow</span><span class="sxs-lookup"><span data-stu-id="be827-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be827-104">Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="be827-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="be827-105">Podmíněné rozhodnutí je bod, ve kterém se workflow dělí na dvě větve.</span><span class="sxs-lookup"><span data-stu-id="be827-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="be827-106">Pokud budete chtít nakonfigurovat podmíněné rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na podmíněné rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="be827-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="be827-107">Pojmenování rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="be827-107">Name a decision</span></span>

<span data-ttu-id="be827-108">Pomocí následujících kroků zadejte název podmíněného rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="be827-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="be827-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="be827-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="be827-110">V poli **Název** zadejte jedinečný podmíněného rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="be827-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="be827-111"> Stanovení podmínek</span><span class="sxs-lookup"><span data-stu-id="be827-111">Set conditions</span></span>

<span data-ttu-id="be827-112">V tomto okamžiku systém určí, která větev se použije, vyhodnocením odeslaného dokumentu k určení, zda vyhovuje konkrétním podmínkám.</span><span class="sxs-lookup"><span data-stu-id="be827-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="be827-113">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="be827-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="be827-114">Klikněte na možnost **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="be827-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="be827-115">Zadání podmínky</span><span class="sxs-lookup"><span data-stu-id="be827-115">Enter a condition.</span></span>
4. <span data-ttu-id="be827-116">Zadejte všechny další podmínky, pokud jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="be827-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="be827-117">Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="be827-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="be827-118">Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.</span><span class="sxs-lookup"><span data-stu-id="be827-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="be827-119">Vyberte v oblasti **Ověřit podmínku** formuláře záznam.</span><span class="sxs-lookup"><span data-stu-id="be827-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="be827-120">Klepněte na možnost **Test**.</span><span class="sxs-lookup"><span data-stu-id="be827-120">Click **Test**.</span></span> <span data-ttu-id="be827-121">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="be827-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="be827-122">Kliknutím na tlačítko **OK** nebo **Zrušit** se vraťte do formuláře **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="be827-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]