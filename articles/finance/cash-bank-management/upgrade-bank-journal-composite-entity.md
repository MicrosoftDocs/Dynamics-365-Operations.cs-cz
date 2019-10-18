---
title: Aktualizace složité entity bankovního deníku
description: Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 974d6b3b11df92debdec26860fd9eea00a9f2313
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188020"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="cc7d4-103">Aktualizace složité entity bankovního deníku</span><span class="sxs-lookup"><span data-stu-id="cc7d4-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc7d4-104">Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="cc7d4-105">Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="cc7d4-106">Nakompilujte a synchronizujte následující složité entity, entity a tabulky fázování bankovního deníku:</span><span class="sxs-lookup"><span data-stu-id="cc7d4-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="cc7d4-107">Složitá entita\\EntitaBankovníhoDeníku</span><span class="sxs-lookup"><span data-stu-id="cc7d4-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="cc7d4-108">Entita\\EntitaZáhlavíBankovníhoDeníku</span><span class="sxs-lookup"><span data-stu-id="cc7d4-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="cc7d4-109">Entita\\EntitaŘádkuBankovníhoDeníku</span><span class="sxs-lookup"><span data-stu-id="cc7d4-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="cc7d4-110">Tabulka\\FázeZáhlavíBankovníhoDeníku</span><span class="sxs-lookup"><span data-stu-id="cc7d4-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="cc7d4-111">Tabulka\\FázeŘádkuBankovníhoDeníku</span><span class="sxs-lookup"><span data-stu-id="cc7d4-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="cc7d4-112">Správa dat\\datové projekty</span><span class="sxs-lookup"><span data-stu-id="cc7d4-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="cc7d4-113">Vystavte typ **Bankovní transakce**v rozložení **Zdrojová data**.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="cc7d4-114">Formát zdrojových dat = XML-Element</span><span class="sxs-lookup"><span data-stu-id="cc7d4-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="cc7d4-115">Název entity = Bankovní deník</span><span class="sxs-lookup"><span data-stu-id="cc7d4-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="cc7d4-116">Odeslaný datový soubor = SampleBankJournalCompositeEntity.xml nové verze</span><span class="sxs-lookup"><span data-stu-id="cc7d4-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="cc7d4-117">Kliknutím na možnost **Ano** přepíšete existující soubor.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="cc7d4-118">Klikněte na **Ano**, pokud chcete mapování generovat od začátku.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="cc7d4-119">Ověřte, že je namapován typ bankovní transakce.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="cc7d4-120">V entitě Řádek klepněte na **Zobrazit mapu**.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="cc7d4-121">Ověřte, že typ bankovní transakce je namapován ze zdroje do fázování.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="cc7d4-122">Importujte nový výkaz.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-122">Import the new statement.</span></span>




