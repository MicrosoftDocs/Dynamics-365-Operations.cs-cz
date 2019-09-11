---
title: Expedice pracovního příkazu
description: Toto téma vysvětluje, jak expedovat pracovní příkaz v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887198"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="c0e22-103">Expedice pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="c0e22-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c0e22-104">Pomocí funkce **Expedovat** můžete naplánovat jeden pracovní příkaz nebo úlohy pracovního příkaz pro jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="c0e22-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="c0e22-105">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c0e22-106">V seznamu vyberte pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="c0e22-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="c0e22-107">Na kartě **Obecné** klikněte na volbu **Expedovat**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="c0e22-108">V dialogovém okně **Naplánovat pracovní příkaz** vyberte pracovníka v poli **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-108">n the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="c0e22-109">V poli **Naplánovat hodiny** můžete vložit očekávanou pracovní dobu v případě, že se očekávaná pracovní doba liší od hodin prognózy.</span><span class="sxs-lookup"><span data-stu-id="c0e22-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="c0e22-110">V poli **Plánované zahájení** můžete upravit počáteční datum a čas v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="c0e22-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="c0e22-111">Pokud by proces plánování měl zohledňovat omezení kapacity týkající se již naplánovaných zdrojů na jiné úlohy, zkontrolujte, zda jsou přepínací tlačítka **Majetek**, **Nástroj** a **Pracovník** nastavena na hodnotu „Ano“.</span><span class="sxs-lookup"><span data-stu-id="c0e22-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to "Yes".</span></span> <span data-ttu-id="c0e22-112">Chcete-li zobrazit podrobné informace o procesu plánování, vyberte v přepínacím tlačítku **Podrobný** možnost „Ano“.</span><span class="sxs-lookup"><span data-stu-id="c0e22-112">If you want to see detailed information about the scheduling process, select "Yes" on the **Verbose** toggle button.</span></span> <span data-ttu-id="c0e22-113">To znamená, že v informačním protokolu budou zobrazeny podrobné informace o vypočteném skóre na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="c0e22-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="c0e22-114">Chcete-li ignorovat uzavřené dny v kalendáři (platí pro majetek, pracovníka a nástroje), vyberte možnost Ano na přepínacím tlačítku **Ignorvat plán**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-114">Select "Yes" on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="c0e22-115">Výběrem možnosti Ano na přepínacím tlačítku **Ignorovat plánované provádění** můžete ignorovat omezení, která byla vybrána v pracovním příkazu týkajícím se plánování.</span><span class="sxs-lookup"><span data-stu-id="c0e22-115">Select "Yes" on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> <span data-ttu-id="c0e22-116">Informace o nastavení plánovaného provádění naleznete v části [Plánované provádění](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="c0e22-116">Refer to the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section for information on the setup of scheduled execution.</span></span>

9. <span data-ttu-id="c0e22-117">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-117">Click **OK**.</span></span> <span data-ttu-id="c0e22-118">Stav životního cyklu pracovního příkazu je automaticky aktualizován do stavu životního Naplánováno, který je určen v **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Modely životního cyklu**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-118">The work order lifecycle state is automatically updated to the "Scheduled" lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="c0e22-119">Na následujícím obrázku je uveden příklad výběru expedice v dialogovém okně **Naplánovat pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="c0e22-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Obrázek č. 1](media/04-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="c0e22-121">Pokud chcete odstranit plán na pracovním příkazu, proveďte to výběrem pracovního příkazu v možnosti **Všechny pracovní příkazy** a kliknutím možnost **Odstranit plán** na kartě **Obecné** . Nezapomeňte ručně aktualizovat stav životního cyklu pracovního příkazu, pokud jste plán odstranili.</span><span class="sxs-lookup"><span data-stu-id="c0e22-121">If you want to delete the schedule on a work order, this is done by selecting the work order in **All work orders** and clicking **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

