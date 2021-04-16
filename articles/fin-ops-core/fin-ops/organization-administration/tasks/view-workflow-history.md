---
title: Zobrazení historie workflow
description: Toto téma popisuje, jak zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351f9c80eab8e9810fa6a4538f003eaef1a4a4fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747218"
---
# <a name="view-workflow-history"></a><span data-ttu-id="2a02c-103">Zobrazení historie workflow</span><span class="sxs-lookup"><span data-stu-id="2a02c-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a02c-104">Toto téma popisuje, jak zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení.</span><span class="sxs-lookup"><span data-stu-id="2a02c-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="2a02c-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="2a02c-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2a02c-106">Přejde na **Navigační podokno > Moduly > Obecné > Dotazy > Workflow > Historie workflowu**.</span><span class="sxs-lookup"><span data-stu-id="2a02c-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="2a02c-107">Pomocí tohoto formuláře můžete zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení.</span><span class="sxs-lookup"><span data-stu-id="2a02c-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="2a02c-108">**ID instance** je identifikační kód instance workflowu, která zpracovává nebo již zpracovala daný dokument.</span><span class="sxs-lookup"><span data-stu-id="2a02c-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="2a02c-109">**Stav** je stav workflowu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="2a02c-110">**ID workflowu** je identifikační kód workflowu, který zpracovává nebo již zpracoval daný dokument.</span><span class="sxs-lookup"><span data-stu-id="2a02c-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="2a02c-111">**Dokument** je identifikační kód dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="2a02c-112">**Typ dokumentu** je typ dokumentu, který byl odeslán ke zpracování.</span><span class="sxs-lookup"><span data-stu-id="2a02c-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="2a02c-113">**Workflow** je název workflowu, který zpracovává nebo již zpracoval daný dokument.</span><span class="sxs-lookup"><span data-stu-id="2a02c-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="2a02c-114">**Verze** je číslo verze workflowu, který zpracovává nebo již zpracoval daný dokument.</span><span class="sxs-lookup"><span data-stu-id="2a02c-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="2a02c-115">**Datum a čas vytvoření** je datum a čas odeslání dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="2a02c-116">**Uplynulý čas** je doba, která uplynula od odeslání dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="2a02c-117">Tlačítkem **Pokračovat** můžete obnovit proces workflowu pro vybraný dokument.</span><span class="sxs-lookup"><span data-stu-id="2a02c-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="2a02c-118">Tlačítkem **Odvolat** můžete stornovat vybraný dokument tak, aby nebyl zpracován.</span><span class="sxs-lookup"><span data-stu-id="2a02c-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="2a02c-119">Vyberte odkaz na požadovaném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="2a02c-120">Ujistěte se, že je rozbalená část **Pracovní položky**.</span><span class="sxs-lookup"><span data-stu-id="2a02c-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="2a02c-121">V této sekci můžete zobrazit pracovní položky, které jsou přidruženy k vybranému dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="2a02c-122">Může být například nutné dokončit určitou úlohu nebo schválit určitý dokument.</span><span class="sxs-lookup"><span data-stu-id="2a02c-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="2a02c-123">Tlačítko **Opětovné přiřazení** otevře dialogové okno, ve kterém můžete opětovně přiřadit pracovní položku jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="2a02c-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="2a02c-124">Ujistěte se, že je rozbalená část **Sledování podrobností**.</span><span class="sxs-lookup"><span data-stu-id="2a02c-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="2a02c-125">V této sekci můžete zobrazit historii workflowu vybraného dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2a02c-125">In this section you can view the workflow history of the selected document.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]