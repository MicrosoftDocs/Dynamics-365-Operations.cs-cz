---
title: Rozšířené odsouhlasení bankovního výpisu MT940 Import – Aktualizace kombinované datové entity
description: Pořadové číslo musí být přidáno k importu bankovního výpisu entity pro podporu MT940 formátu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "343781"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="8512a-103">Rozšířené odsouhlasení bankovního výpisu MT940 Import – Aktualizace kombinované datové entity</span><span class="sxs-lookup"><span data-stu-id="8512a-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8512a-104">Pořadové číslo musí být přidáno k importu bankovního výpisu entity pro podporu MT940 formátu.</span><span class="sxs-lookup"><span data-stu-id="8512a-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="8512a-105">Následující postup slouží k přidání importu bankovního výpisu entity pro podporu formátu MT940.</span><span class="sxs-lookup"><span data-stu-id="8512a-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="8512a-106">Kompilovat a synchronizovat následující:</span><span class="sxs-lookup"><span data-stu-id="8512a-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="8512a-107">Kombinovaná entita\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="8512a-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="8512a-108">Entita\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="8512a-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="8512a-109">Entita\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="8512a-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="8512a-110">Entita\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="8512a-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="8512a-111">Entita\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="8512a-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="8512a-112">Tabulky\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="8512a-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="8512a-113">Správa dat\\datové projekty.</span><span class="sxs-lookup"><span data-stu-id="8512a-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="8512a-114">Načíst projekt(y) importu MT940.</span><span class="sxs-lookup"><span data-stu-id="8512a-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="8512a-115">Změna požadavku XSLT.</span><span class="sxs-lookup"><span data-stu-id="8512a-115">Change XSLT.</span></span>
            -   <span data-ttu-id="8512a-116">Klikněte na možnost **Zobrazit mapu**.</span><span class="sxs-lookup"><span data-stu-id="8512a-116">Click **View map**.</span></span>
            -   <span data-ttu-id="8512a-117">Klepněte na tlačítko **Zobrazit mapu** na dokumentu bankovního výpisu.</span><span class="sxs-lookup"><span data-stu-id="8512a-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="8512a-118">Klikněte na tlačítko **Transformace**</span><span class="sxs-lookup"><span data-stu-id="8512a-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="8512a-119">Odstraňte soubor BankReconiliation-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="8512a-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="8512a-120">Přidejte novou verzi BankReconiliation-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="8512a-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="8512a-121">Vystavte **Pořadové číslo** do rozvržení **Zdrojová data**.</span><span class="sxs-lookup"><span data-stu-id="8512a-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="8512a-122">Formát zdrojových dat = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="8512a-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="8512a-123">Název entity = Výpisy banky.</span><span class="sxs-lookup"><span data-stu-id="8512a-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="8512a-124">Odeslaný datový soubor = Nová verze SampleBankJournalCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="8512a-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="8512a-125">Kliknutím na možnost **Ano** přepíšete existující soubor.</span><span class="sxs-lookup"><span data-stu-id="8512a-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="8512a-126">Klikněte na **Ano**, pokud chcete generovat nové mapování.</span><span class="sxs-lookup"><span data-stu-id="8512a-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="8512a-127">Ověřte, že je S**equenceNumber** mapováno.</span><span class="sxs-lookup"><span data-stu-id="8512a-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="8512a-128">Klepněte na tlačítko **Zobrazit mapu** na dokumentu výpisu entity.</span><span class="sxs-lookup"><span data-stu-id="8512a-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="8512a-129">Ověřte, že **SequenceNumber** je namapováno ze zdroje do fázování.</span><span class="sxs-lookup"><span data-stu-id="8512a-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="8512a-130">Importujte nový výkaz.</span><span class="sxs-lookup"><span data-stu-id="8512a-130">Import the new statement.</span></span>




