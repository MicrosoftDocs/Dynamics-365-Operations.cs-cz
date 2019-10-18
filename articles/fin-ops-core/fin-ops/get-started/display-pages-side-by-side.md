---
title: Zobrazení stránek vedle sebe pomocí funkce Otevřít v novém okně
description: Tento článek vysvětluje způsob zobrazení stránek vedle sebe.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180684"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a><span data-ttu-id="fff08-103">Zobrazení stránek vedle sebe pomocí funkce Otevřít v novém okně</span><span class="sxs-lookup"><span data-stu-id="fff08-103">Show pages side by side by using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fff08-104">Tento článek vysvětluje způsob zobrazení stránek vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="fff08-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="fff08-105">Můžete zobrazit více stránek souběžně a rychle tak dokončit úlohu.</span><span class="sxs-lookup"><span data-stu-id="fff08-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="fff08-106">Například můžete ověřit nebo zadat řádky do více než jednoho deníku.</span><span class="sxs-lookup"><span data-stu-id="fff08-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="fff08-107">Obvykle je třeba přejít oběma směry mezi stránkou, která zobrazuje seznam deníků, a stránkou, která zobrazuje řádky daného deníku.</span><span class="sxs-lookup"><span data-stu-id="fff08-107">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="fff08-108">Funkce **Otevřít v novém okně** umožňuje zobrazení těchto stránek souběžně, aby bylo možné provést úlohy rychle.</span><span class="sxs-lookup"><span data-stu-id="fff08-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="fff08-109">V souladu s příkladem uvedeným výše lze při prohlížení řádků kliknout na ikonu **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="fff08-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="fff08-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="fff08-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="fff08-111">Kliknutím na ikonu **Otevřít v novém okně** otevře stránku s řádky v novém místním prohlížeči a poté přejde v původním prohlížeči v historii na stránku zobrazující seznam deníků.</span><span class="sxs-lookup"><span data-stu-id="fff08-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="fff08-112">Pak můžete zobrazit obě stránky souběžně.</span><span class="sxs-lookup"><span data-stu-id="fff08-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="fff08-113">Po dokončení zobrazení deníku můžete změnit vybraný deník na stránce seznamu deníků a stránku s řádky v místním okně automaticky zobrazí řádky nově vybraného deníku.</span><span class="sxs-lookup"><span data-stu-id="fff08-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="fff08-114">[![stránky-se-zobrazí-vedle-sebe](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="fff08-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="fff08-115">Dynamické propojení a aktualizace probíhá kvůli vztahům, které existují mezi daty, která podporují tyto stránky.</span><span class="sxs-lookup"><span data-stu-id="fff08-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="fff08-116">Pokud systém není obeznámen se vztahy mezi daty, místní okno se nebude automaticky aktualizovat po změně původního okna.</span><span class="sxs-lookup"><span data-stu-id="fff08-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="fff08-117">Některé stránky obsahují více zobrazení, jako je například zobrazení mřížky, zobrazení záhlaví a zobrazení podrobností.</span><span class="sxs-lookup"><span data-stu-id="fff08-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="fff08-118">Ikona **Otevřít v novém okně** způsobí, že celá stránka bude otevřena v novém okně prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="fff08-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="fff08-119">Proto nelze ponechat dvě zobrazení stejné stránky vedle sebe pomocí funkce **Otevřít v novém okně**.</span><span class="sxs-lookup"><span data-stu-id="fff08-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="fff08-120">Téměř všechny tyto stránky však mají navigační seznam, pomocí kterého můžete přepínat mezi záznamy a dosáhnout tak podobné zkušenosti.</span><span class="sxs-lookup"><span data-stu-id="fff08-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="fff08-121">Před použitím funkce **Otevřít v novém okně** je třeba nakonfigurovat funkci blokování automaticky otevíraných oken prohlížeče tak, aby umožnila otevírání automaticky otevíraných oken z adresy URL serveru.</span><span class="sxs-lookup"><span data-stu-id="fff08-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="fff08-122">Například je možné povolit automatické otevírání oken z adresy "\*.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="fff08-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="fff08-123">Funkce **Otevřít v novém okně** je k dispozici pouze, pokud existuje více než jedna stránka otevřená v okně.</span><span class="sxs-lookup"><span data-stu-id="fff08-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="fff08-124">Dále se místní okno automaticky zavře, pokud nejsou žádné další stránky otevřeny (tj. když je zavřena poslední stránka v tomto okně).</span><span class="sxs-lookup"><span data-stu-id="fff08-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="fff08-125">Systém také zavře otevřené stránky, když přejdete do jiné oblasti aplikace.</span><span class="sxs-lookup"><span data-stu-id="fff08-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="fff08-126">Z toho vyplývá, že pokud máte otevřená místní okna a přejdete do jiné oblasti v aplikaci, místní okna budou automaticky uzavřena, protože stránky v těchto oknech byly zavřeny systémem.</span><span class="sxs-lookup"><span data-stu-id="fff08-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="fff08-127">Horní panel v místních oknech zobrazuje informace o společnosti, ve které byla stránka otevřena a je určena jen ke čtení.</span><span class="sxs-lookup"><span data-stu-id="fff08-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="fff08-128">Místní podokna jsou závislá na hlavním okně prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="fff08-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="fff08-129">Je-li hlavní okno zavřeno nebo aktualizováno, všechna otevřená místní okna se stanou jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="fff08-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="fff08-130">To znamená, že stále můžete prohlížet údaje v těchto oknech, ale nebudete moci s nimi spolupracovat.</span><span class="sxs-lookup"><span data-stu-id="fff08-130">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>
