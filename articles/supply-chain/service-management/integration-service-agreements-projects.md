---
title: Integrace pro servisní smlouvy a projekty
description: Při práci se servisními smlouvami a řádky servisních smluv používáte data, která byla nastavená v oblastech řízení a účtování projektu.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd0a7de17e8ff098220fd183b714b77225cc217f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247303"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="e32dd-103">Integrace pro servisní smlouvy a projekty</span><span class="sxs-lookup"><span data-stu-id="e32dd-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e32dd-104">Při práci se servisními smlouvami a řádky servisních smluv používáte data, která byla nastavená v následujících oblastech **řízení a účtování projektu**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="e32dd-105">Projektové ceny</span><span class="sxs-lookup"><span data-stu-id="e32dd-105">Project prices</span></span>

<span data-ttu-id="e32dd-106">Náklady a prodejní cena transakce servisní smlouvy jsou odvozeny z nastavení nákladové ceny použité pro projekt, který je připojený k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="e32dd-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="e32dd-107">Náklady a prodejní ceny lze nastavit podle projektu, zaměstnance a kategorie.</span><span class="sxs-lookup"><span data-stu-id="e32dd-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="e32dd-108">Ověření projektu</span><span class="sxs-lookup"><span data-stu-id="e32dd-108">Project validation</span></span>

<span data-ttu-id="e32dd-109">Projekty, zaměstnanci a kategorie, ze kterých lze vybírat na řádku servisní smlouvy, mohou být omezeny nastavením ověření v části **Řízení a účtování projektu**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="e32dd-110">Pomocí nastavení ověřování zaměstnanců, projektů a kategorií v nastavení ověření můžete řídit přístup.</span><span class="sxs-lookup"><span data-stu-id="e32dd-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="e32dd-111">Vlastnosti řádku projektu</span><span class="sxs-lookup"><span data-stu-id="e32dd-111">Project line properties</span></span>

<span data-ttu-id="e32dd-112">Pro řádek servisní smlouvy se vlastnost řádku zadává automaticky.</span><span class="sxs-lookup"><span data-stu-id="e32dd-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="e32dd-113">Vlastnosti řádku se vytvářejí ve formuláři **vlastnosti řádku** v **řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="e32dd-114">Vlastnost řádku, která je zadána v servisní smlouvě, je připojena k projektu, který je vybrán pro servisní smlouvu a poté dědí řádek servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e32dd-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="e32dd-115">Výchozí protiúčty</span><span class="sxs-lookup"><span data-stu-id="e32dd-115">Default offset accounts</span></span>

<span data-ttu-id="e32dd-116">Zadáte-li transakci nákladů, vybere se pro tuto transakci automaticky výchozí nákladový účet.</span><span class="sxs-lookup"><span data-stu-id="e32dd-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="e32dd-117">Tento výchozí nákladový účet se nastavuje u projektu, který je připojený k aktuální servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="e32dd-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="e32dd-118">Kategorie projektů</span><span class="sxs-lookup"><span data-stu-id="e32dd-118">Project categories</span></span>

<span data-ttu-id="e32dd-119">Kategorie, které jsou dostupné pro řádky servisní smlouvy, se nastavují ve formuláři **Kategorie projektu** v části **Řízení a účtování projektu**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="e32dd-120">Lze vybrat kategorie, které mají zaškrtnuté políčko <STRONG>Aktivní v denících</STRONG> na kartě <STRONG>Projekt</STRONG> ve formuláři <STRONG>Kategorie projektu</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e32dd-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="e32dd-121">Pokud je však zaškrtnuté políčko <STRONG>Neaktivní kategorie</STRONG> na kartě <STRONG>Deníky</STRONG> ve formuláři <STRONG>Parametry řízení projektu a účetnictví</STRONG>, lze vybrat všechny kategorie.</span><span class="sxs-lookup"><span data-stu-id="e32dd-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="e32dd-122">Parametry projektu</span><span class="sxs-lookup"><span data-stu-id="e32dd-122">Project parameters</span></span>

<span data-ttu-id="e32dd-123">Pokud je zaškrtnuté políčko **Propuštění pracovníci** na kartě **Deníky** v okně **Parametry řízení a účetnictví projektu**, můžete vybrat neaktivní zaměstnance a aktivní zaměstnance ve formulářích **servisní smlouvy** a **servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="e32dd-124">Dále můžete zpřístupnit pole **Počáteční čas** a **Koncový čas** na kartě **Projekt** ve formuláři **Servisní zakázky** a umožnit tak zadávání času zahájení a ukončení v řádcích servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e32dd-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="e32dd-125">Povolení zadávání času zahájení a ukončení v servisních zakázkách</span><span class="sxs-lookup"><span data-stu-id="e32dd-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="e32dd-126">Klikněte na **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="e32dd-127">Klepněte na tlačítko **deníky** a zaškrtněte políčko **zobrazit časy zahájení a ukončení**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="e32dd-128">Klikněte na uzel **Řízení a účtování projektů** \> **Nastavení** \> **Deníky** \> **Názvy deníku**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="e32dd-129">Vyberte název deníku připojeného k servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="e32dd-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="e32dd-130">Klepněte na kartu **Obecné** a zaškrtněte políčko **zobrazit časy zahájení a ukončení**.</span><span class="sxs-lookup"><span data-stu-id="e32dd-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e32dd-131">Vyberte název deníku pro servisní zakázku v poli <STRONG>Hodina</STRONG> na kartě <STRONG>Deníky</STRONG> ve formuláři <STRONG>Parametry správy služby</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e32dd-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]