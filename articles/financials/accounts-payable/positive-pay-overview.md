---
title: "Přehled kladných plateb"
description: "Tento článek poskytuje informace o kladné platbě, kterou můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5b88b940e7a590ff99b6ab8a99ce45d32dfe0505
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="positive-pay-overview"></a><span data-ttu-id="21801-103">Přehled kladných plateb</span><span class="sxs-lookup"><span data-stu-id="21801-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21801-104">Tento článek poskytuje informace o kladné platbě, kterou můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance.</span><span class="sxs-lookup"><span data-stu-id="21801-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="21801-105">Kladné platby můžete použít pro generování elektronických seznamů šeků, které jsou dodávány bance.</span><span class="sxs-lookup"><span data-stu-id="21801-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="21801-106">Soubory kladných plateb pomáhají bankám zabránit podvodným šekům.</span><span class="sxs-lookup"><span data-stu-id="21801-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="21801-107">Nastavte kladné platby pro generování elektronického seznamu šeků při každém tisku šeků.</span><span class="sxs-lookup"><span data-stu-id="21801-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="21801-108">Potom při předložení šeku bance ho banka srovná se seznamem šeků, který byl předložen dříve.</span><span class="sxs-lookup"><span data-stu-id="21801-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="21801-109">Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje.</span><span class="sxs-lookup"><span data-stu-id="21801-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="21801-110">Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.</span><span class="sxs-lookup"><span data-stu-id="21801-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="21801-111">Kladné platby se také označují jako SafePay.</span><span class="sxs-lookup"><span data-stu-id="21801-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="21801-112">Soubory kladných plateb mohou obsahovat citlivé informace o příjemcích plateb a šekových částkách.</span><span class="sxs-lookup"><span data-stu-id="21801-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="21801-113">Nezapomeňte tedy použít dostatečná opatření od doby vytvoření souborů do jejich přijetí do banky.</span><span class="sxs-lookup"><span data-stu-id="21801-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="21801-114">Soubory kladných plateb budou staženy podle pokynů pro stažení ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="21801-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="21801-115">Soubory kladných plateb jsou vytvořeny pomocí datových entit.</span><span class="sxs-lookup"><span data-stu-id="21801-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="21801-116">Před generováním souboru kladných plateb nastavte formáty transformace pro XML, který převádí data do formátu, který může banka používat.</span><span class="sxs-lookup"><span data-stu-id="21801-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="21801-117">Pro každý bankovní účet, pro který chcete generovat informace o souborech kladných plateb, musíte přiřadit formát kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="21801-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="21801-118">Po vygenerování plateb lze vygenerovat soubor kladných plateb pro jednu právnickou osobu a jeden bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="21801-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="21801-119">Případně můžete vygenerovat soubory kladných plateb pro více právnických osob a bankovních účtů současně.</span><span class="sxs-lookup"><span data-stu-id="21801-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="21801-120">Po zaplacení šeků, které jsou uvedeny v souboru kladných plateb, obdržíte číslo potvrzení od banky.</span><span class="sxs-lookup"><span data-stu-id="21801-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="21801-121">Poté můžete potvrdit soubor kladných plateb v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="21801-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="21801-122">Pokud je nutné změnit soubor kladných plateb, můžete jej odvolat.</span><span class="sxs-lookup"><span data-stu-id="21801-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="21801-123">Pro každý šek v souboru kladných plateb se resetuje pole, které označuje, zda byl šek zahrnut do souboru kladných plateb.</span><span class="sxs-lookup"><span data-stu-id="21801-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="21801-124">Další informace naleznete v tématu [Nastavení a generování souborů kladných plateb](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="21801-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>




