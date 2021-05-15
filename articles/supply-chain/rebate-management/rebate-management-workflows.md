---
title: Pracovní postupy nabídky správy rabatu
description: Toto téma vysvětluje, jak nastavit pracovní postup nabídky správy rabatu, aby bylo možné nabídky schvalovat a aktivovat.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 16f1c56ecd69f4dc7bfd80e74d3f35147cc173d6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919812"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="218d3-103">Pracovní postupy nabídky správy rabatu</span><span class="sxs-lookup"><span data-stu-id="218d3-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="218d3-104">Ke schválení nabídek rabatů používá správa rabatů stejnou platformu pracovního postupu jako ostatní aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="218d3-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="218d3-105">Ke každému pracovnímu postupu jsou přidruženy dva procesy úloh:</span><span class="sxs-lookup"><span data-stu-id="218d3-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="218d3-106">Jeden prvek pracovního postupu aktivuje nabídku, aby mohl uživatel nebo proces pracovního postupu schválit transakce.</span><span class="sxs-lookup"><span data-stu-id="218d3-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="218d3-107">Jeden prvek pracovního postupu nabídku schvaluje.</span><span class="sxs-lookup"><span data-stu-id="218d3-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="218d3-108">Abyste mohli použít nabídku rabatu, musí být aktivní v modulu **Správa rabatu**.</span><span class="sxs-lookup"><span data-stu-id="218d3-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="218d3-109">Chcete-li aktivovat nabídku, musíte nejprve vytvořit a nakonfigurovat *Pracovní postup nabídek správy rabatů*.</span><span class="sxs-lookup"><span data-stu-id="218d3-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="218d3-110">Po aktivaci pracovního postupu pro správu rabatů nemohou uživatelé ručně schvalovat nabídky.</span><span class="sxs-lookup"><span data-stu-id="218d3-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="218d3-111">Musí být vždy použit pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="218d3-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="218d3-112">Vytvoření a správa pracovních postupů nabídky správy rabatu</span><span class="sxs-lookup"><span data-stu-id="218d3-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="218d3-113">Chcete-li pracovat s pracovními postupy nabídek správy rabatů, přejděte na **Správa rabatů \> Nastavit \> Pracovní postupy správy rabatu**.</span><span class="sxs-lookup"><span data-stu-id="218d3-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="218d3-114">Tam můžete podle potřeby zobrazovat, vytvářet a aktualizovat pracovní postupy.</span><span class="sxs-lookup"><span data-stu-id="218d3-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="218d3-115">Najednou může být aktivní pouze jeden pracovní postup tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="218d3-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="218d3-116">Další informace o pracovních postupech, jak pracovat se stránkou **Pracovní postupy správy rabatu** a jak vytvářet pracovní postupy, naleznete v části [Přehled systému pracovních postupů](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) a souvisejících tématech.</span><span class="sxs-lookup"><span data-stu-id="218d3-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="218d3-117">Použití pracovního postupu k aktivaci nabídky</span><span class="sxs-lookup"><span data-stu-id="218d3-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="218d3-118">Chcete-li aktivovat nabídku prostřednictvím pracovního postupu, otevřete nabídku (například na stránce **Všechny nabídky správy rabatů**).</span><span class="sxs-lookup"><span data-stu-id="218d3-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="218d3-119">Poté v podokně akcí vyberte **Pracovní postup \> Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="218d3-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="218d3-120">Jakmile bude nová nabídka zpracována a schválena prostřednictvím pracovního postupu, bude aktivní a připravená k použití.</span><span class="sxs-lookup"><span data-stu-id="218d3-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="218d3-121">Po aktivaci nabídky nemůžete změnit její nastavení.</span><span class="sxs-lookup"><span data-stu-id="218d3-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="218d3-122">Pokud musíte změnit aktivní nabídku, deaktivujte ji a poté vytvořte novou nabídku.</span><span class="sxs-lookup"><span data-stu-id="218d3-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="218d3-123">Pokud se nová nabídka bude podobat staré nabídce, můžete ji vytvořit zkopírováním staré nabídky.</span><span class="sxs-lookup"><span data-stu-id="218d3-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
