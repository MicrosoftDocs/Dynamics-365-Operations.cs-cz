---
title: Rozšířené odsouhlasení bankovního výpisu MT940 Import – Aktualizace kombinované datové entity
description: Pořadové číslo musí být přidáno k importu bankovního výpisu entity pro podporu MT940 formátu.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6534cc0835eabe91ab485e1d71412885d12123f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827427"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="cc7ae-103">Rozšířené odsouhlasení bankovního výpisu MT940 Import – Aktualizace kombinované datové entity</span><span class="sxs-lookup"><span data-stu-id="cc7ae-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc7ae-104">Pořadové číslo musí být přidáno k importu bankovního výpisu entity pro podporu MT940 formátu.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="cc7ae-105">Následující postup slouží k přidání importu bankovního výpisu entity pro podporu formátu MT940.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="cc7ae-106">Kompilovat a synchronizovat následující:</span><span class="sxs-lookup"><span data-stu-id="cc7ae-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="cc7ae-107">Kombinovaná entita\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="cc7ae-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="cc7ae-108">Entita\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="cc7ae-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="cc7ae-109">Entita\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="cc7ae-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="cc7ae-110">Entita\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="cc7ae-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="cc7ae-111">Entita\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="cc7ae-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="cc7ae-112">Tabulky\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="cc7ae-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="cc7ae-113">Správa dat\\datové projekty.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="cc7ae-114">Načíst projekt(y) importu MT940.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="cc7ae-115">Změna požadavku XSLT.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-115">Change XSLT.</span></span>
            -   <span data-ttu-id="cc7ae-116">Klikněte na možnost **Zobrazit mapu**.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-116">Click **View map**.</span></span>
            -   <span data-ttu-id="cc7ae-117">Klepněte na tlačítko **Zobrazit mapu** na dokumentu bankovního výpisu.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="cc7ae-118">Klikněte na tlačítko **Transformace**</span><span class="sxs-lookup"><span data-stu-id="cc7ae-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="cc7ae-119">Odstraňte soubor BankReconiliation-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="cc7ae-120">Přidejte novou verzi BankReconiliation-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="cc7ae-121">Vystavte **Pořadové číslo** do rozvržení **Zdrojová data**.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="cc7ae-122">Formát zdrojových dat = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="cc7ae-123">Název entity = Výpisy banky.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="cc7ae-124">Odeslaný datový soubor = Nová verze SampleBankJournalCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="cc7ae-125">Kliknutím na možnost **Ano** přepíšete existující soubor.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="cc7ae-126">Klikněte na **Ano**, pokud chcete generovat nové mapování.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="cc7ae-127">Ověřte, že je S **equenceNumber** mapováno.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="cc7ae-128">Klepněte na tlačítko **Zobrazit mapu** na dokumentu výpisu entity.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="cc7ae-129">Ověřte, že **SequenceNumber** je namapováno ze zdroje do fázování.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="cc7ae-130">Importujte nový výkaz.</span><span class="sxs-lookup"><span data-stu-id="cc7ae-130">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]