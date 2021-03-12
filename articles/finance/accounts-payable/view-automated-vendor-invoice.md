---
title: Zobrazení výsledků automatizace faktur dodavatelů (náhled)
description: Toto téma vysvětluje, jak zobrazit stav dodavatelských faktur, které jsou v automatizovaném procesu odesílání do pracovního postupu.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: baa2f1f55dfb9bb93b4f27c45db563e39850dd37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969719"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="9c565-103">Zobrazení výsledků automatizace faktur dodavatele</span><span class="sxs-lookup"><span data-stu-id="9c565-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c565-104">Toto téma vysvětluje, jak zobrazit stav dodavatelských faktur, které jsou v automatizovaném procesu odesílání do pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="9c565-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="9c565-105">Podrobnosti o historii automatizace se uchovávají pro každou importovanou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="9c565-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="9c565-106">V závislosti na obchodních procesech, které jste u vás automatizovali, zobrazuje stránka **Čekající faktury dodavatele** hodnoty **Stav shody automatického potvrzení** a **Stav automatizovaného odeslání do pracovního postupu**.</span><span class="sxs-lookup"><span data-stu-id="9c565-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="9c565-107">Můžete si zobrazit podrobnosti a vytvořit plán zaměřující se na faktury, u nichž automatický krok selhal.</span><span class="sxs-lookup"><span data-stu-id="9c565-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="9c565-108">Až pak problém opravíte, můžete pokračovat v automatizovaném procesu pro importovanou fakturu.</span><span class="sxs-lookup"><span data-stu-id="9c565-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="9c565-109">Před úpravou odeslané faktury musíte pozastavit automatické zpracování.</span><span class="sxs-lookup"><span data-stu-id="9c565-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="9c565-110">Pokud musí být faktura v automatizovaném procesu odesílání do pracovního postupu pozastavena, nastavte pole **Zahrnout do automatizovaného zpracování** na **Ne** na stránce **Faktury dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9c565-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="9c565-111">Automatizace pak nepoběží, dokud **Zahrnout do automatizovaného zpracování** nenastavíte na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9c565-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="9c565-112">U faktury lze pozastavit další automatizaci, pokud ještě není v systému pracovního postupu a není používána automatizovaným procesem.</span><span class="sxs-lookup"><span data-stu-id="9c565-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="9c565-113">Pokud importovaná faktura podléhá procesu odeslání do pracovního postupu, můžete si zobrazit její hodnotu **Stav automatizace** na stránce **Faktury dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="9c565-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="9c565-114">Sledují se následující stavy:</span><span class="sxs-lookup"><span data-stu-id="9c565-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="9c565-115">**Zahrnuto** – Automatizované procesy definované na stránce **Parametry závazků** běží správně, ale ještě nebyly dokončeny.</span><span class="sxs-lookup"><span data-stu-id="9c565-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="9c565-116">**Pozastaveno** – Automatizované procesy definované na stránce **Parametry závazků** proběhly, ale nejméně jeden krok procesu selhal.</span><span class="sxs-lookup"><span data-stu-id="9c565-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="9c565-117">Stav **Pozastaveno** se použije také v případě, že je pole **Zahrnout do automatizovaného zpracování** nastaveno na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="9c565-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="9c565-118">Selhání si můžete prohlédnout výběrem volby **Zobrazit poslední výsledky**.</span><span class="sxs-lookup"><span data-stu-id="9c565-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="9c565-119">**V pracovním postupu** – Importovaná faktura byla odeslána do systému pracovního postupu, a to buď automatizovaným procesem odeslání do pracovního postupu, nebo ručně.</span><span class="sxs-lookup"><span data-stu-id="9c565-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="9c565-120">**Pracovní postup dokončen** – Proces u importované faktury byl dokončen.</span><span class="sxs-lookup"><span data-stu-id="9c565-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
