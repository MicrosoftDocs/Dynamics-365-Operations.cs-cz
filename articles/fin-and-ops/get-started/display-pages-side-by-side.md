---
title: "Zobrazení stránek-souběžně pomocí ikony Otevřít v novém okně"
description: "Tento článek popisuje způsob zobrazení stránek vedle sebe v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b375e87af24a17633d6d1590277ece9e2df189da
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a><span data-ttu-id="534fd-103">Zobrazení stránek vedle sebe pomocí ikony Otevřít v novém okně</span><span class="sxs-lookup"><span data-stu-id="534fd-103">Display pages side-by-side using the Open in New Window icon</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="534fd-104">Tento článek popisuje způsob zobrazení stránek vedle sebe v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="534fd-104">This article explains how to display pages side-by-side in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="534fd-105">Microsoft Dynamics 365 for Finance and Operations slouží k efektivnímu provádění úloh.</span><span class="sxs-lookup"><span data-stu-id="534fd-105">Microsoft Dynamics 365 for Finance and Operations helps you perform tasks efficiently.</span></span> <span data-ttu-id="534fd-106">V některých případech můžete zobrazit více stránek-souběžně a rychle tak dokončit úlohu.</span><span class="sxs-lookup"><span data-stu-id="534fd-106">In some cases, you may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="534fd-107">Například můžete ověřit nebo zadat řádky do více než jednoho deníku.</span><span class="sxs-lookup"><span data-stu-id="534fd-107">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="534fd-108">Obvykle je třeba přejít oběma směry mezi stránkou, která zobrazuje seznam deníků, a stránkou, která zobrazuje řádky daného deníku.</span><span class="sxs-lookup"><span data-stu-id="534fd-108">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="534fd-109">Funkce **Otevřít v novém okně** umožňuje zobrazení těchto stránek souběžně, aby bylo možné provést úlohy rychle.</span><span class="sxs-lookup"><span data-stu-id="534fd-109">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span> 

<span data-ttu-id="534fd-110">V souladu s příkladem uvedeným výše lze při prohlížení řádků kliknout na ikonu **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="534fd-110">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span> 

<span data-ttu-id="534fd-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="534fd-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span> 

<span data-ttu-id="534fd-112">Kliknutím na ikonu **Otevřít v novém okně** otevře stránku s řádky v novém místním prohlížeči a poté přejde v původním prohlížeči v historii na stránku zobrazující seznam deníků.</span><span class="sxs-lookup"><span data-stu-id="534fd-112">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="534fd-113">Pak můžete zobrazit obě stránky souběžně.</span><span class="sxs-lookup"><span data-stu-id="534fd-113">You can then display both pages side-by-side.</span></span> <span data-ttu-id="534fd-114">Po dokončení zobrazení deníku můžete změnit vybraný deník na stránce seznamu deníků a stránku s řádky v místním okně automaticky zobrazí řádky nově vybraného deníku.</span><span class="sxs-lookup"><span data-stu-id="534fd-114">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span> 

<span data-ttu-id="534fd-115">[![stránky-se-zobrazí-vedle-sebe](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="534fd-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span> 

<span data-ttu-id="534fd-116">Dynamické propojení a aktualizace probíhá kvůli vztahům, které existují mezi daty, která podporují tyto stránky.</span><span class="sxs-lookup"><span data-stu-id="534fd-116">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="534fd-117">Pokud systém není obeznámen se vztahy mezi daty, místní okno se nebude automaticky aktualizovat po změně původního okna.</span><span class="sxs-lookup"><span data-stu-id="534fd-117">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span> 

<span data-ttu-id="534fd-118">Některé stránky obsahují více zobrazení, jako je například zobrazení mřížky, zobrazení záhlaví a zobrazení podrobností.</span><span class="sxs-lookup"><span data-stu-id="534fd-118">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="534fd-119">Ikona **Otevřít v novém okně** způsobí, že celá stránka bude otevřena v novém okně prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="534fd-119">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="534fd-120">Proto nelze ponechat dvě zobrazení stejné stránky vedle sebe pomocí funkce **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="534fd-120">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="534fd-121">Téměř všechny tyto stránky však mají navigační seznam, pomocí kterého můžete přepínat mezi záznamy a dosáhnout tak podobné zkušenosti.</span><span class="sxs-lookup"><span data-stu-id="534fd-121">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span> 

<span data-ttu-id="534fd-122">Před použitím funkce **Otevřít v novém okně** je třeba nakonfigurovat funkci blokování automaticky otevíraných oken prohlížeče tak, aby umožnila otevírání automaticky otevíraných oken z adresy URL serveru Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="534fd-122">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the Finance and Operations site.</span></span> <span data-ttu-id="534fd-123">Například je možné povolit automatické otevírání oken z adresy "\*.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="534fd-123">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span> 

<span data-ttu-id="534fd-124">Funkce **Otevřít v novém okně** je k dispozici pouze, pokud existuje více než jedna stránka otevřená v okně.</span><span class="sxs-lookup"><span data-stu-id="534fd-124">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="534fd-125">Dále se místní okno automaticky zavře, pokud nejsou žádné další stránky otevřeny (tj. když je zavřena poslední stránka v tomto okně).</span><span class="sxs-lookup"><span data-stu-id="534fd-125">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="534fd-126">Finance and Operations také zavře otevřené stránky, když přejdete do jiné oblasti aplikace.</span><span class="sxs-lookup"><span data-stu-id="534fd-126">Finance and Operations also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="534fd-127">Z toho vyplývá, že pokud máte otevřená místní okna a přejdete do jiné oblasti v aplikaci, místní okna budou automaticky uzavřena, protože stránky v těchto oknech byly zavřeny systémem.</span><span class="sxs-lookup"><span data-stu-id="534fd-127">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span> 

<span data-ttu-id="534fd-128">Horní panel v místních oknech zobrazuje informace o společnosti, ve které byla stránka otevřena a je určena jen ke čtení.</span><span class="sxs-lookup"><span data-stu-id="534fd-128">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="534fd-129">Místní podokna jsou závislá na hlavním okně prohlížeče Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="534fd-129">The pop-up windows also rely on the main Finance and Operations browser window.</span></span> <span data-ttu-id="534fd-130">Je-li hlavní okno zavřeno nebo aktualizováno, všechna otevřená místní okna se stanou jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="534fd-130">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="534fd-131">To znamená, že stále můžete prohlížet údaje v těchto oknech, ale nebudete moci s nimi spolupracovat.</span><span class="sxs-lookup"><span data-stu-id="534fd-131">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>




