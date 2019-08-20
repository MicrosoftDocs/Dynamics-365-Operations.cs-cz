---
title: Import a udržování transakce platební karty
description: Toto téma vysvětluje postup, jak importovat a udržovat transakce platební karty týkající se výdajů. Tyto transakce lze nastavit tak, aby byly automaticky importovány v opakovaném plánování, nebo ručně importovány podle potřeby.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4484ea6fa446c73b8854e7822237bb3c6b9f9023
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840930"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="0f30d-104">Import a udržování transakce platební karty</span><span class="sxs-lookup"><span data-stu-id="0f30d-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f30d-105">Transakce platební karty související s výdaji lze nastavit tak, aby byly automaticky importovány v opakujícím se plánu.</span><span class="sxs-lookup"><span data-stu-id="0f30d-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="0f30d-106">Popřípadě lze transakce ručně importovat podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="0f30d-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="0f30d-107">Transakce platebních karet jsou importovány prostřednictvím datové entity Transakce platebních karet.</span><span class="sxs-lookup"><span data-stu-id="0f30d-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="0f30d-108">Další informace o datových entitách naleznete v tématu [Datové entity](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="0f30d-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="0f30d-109">Importovat transakce platebních karet</span><span class="sxs-lookup"><span data-stu-id="0f30d-109">Import credit card transactions</span></span>

1. <span data-ttu-id="0f30d-110">Na stránce **Transakce platebních karet** vyberte **Importovat transakce**.</span><span class="sxs-lookup"><span data-stu-id="0f30d-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="0f30d-111">Pokud otevíráte správu dat poprvé, systém musí aktualizovat seznam datových entit předtím, než můžete pokračovat.</span><span class="sxs-lookup"><span data-stu-id="0f30d-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="0f30d-112">V poli **Název** zadejte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="0f30d-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="0f30d-113">V poli **Formát dat zdroje** vyberte formát souboru, který obsahuje transakce platebních karet k importu.</span><span class="sxs-lookup"><span data-stu-id="0f30d-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="0f30d-114">Vyberte **Odeslat**a poté vyhledejte a vyberte soubor, který chcete importovat.</span><span class="sxs-lookup"><span data-stu-id="0f30d-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="0f30d-115">Po odeslání souboru ověřte mapování souboru transakcí platebních karet a sloupce datové entity Transakce platebních karet pomocí výběru odkazu **Zobrazit mapu** na dlaždici.</span><span class="sxs-lookup"><span data-stu-id="0f30d-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="0f30d-116">Pokud došlo k chybám mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo z karty **Podrobnosti mapování**.</span><span class="sxs-lookup"><span data-stu-id="0f30d-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="0f30d-117">Chcete-li automatizovat transakce platebních karet, vyberte možnost **Vytvořit opakovanou datovou úlohu**.</span><span class="sxs-lookup"><span data-stu-id="0f30d-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="0f30d-118">Pak lze nastavit opakování, které definuje, jak často mají být importovány transakce platebních karet.</span><span class="sxs-lookup"><span data-stu-id="0f30d-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="0f30d-119">Po dokončení zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f30d-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="0f30d-120">Chcete-li nyní importovat vybraný soubor, zvolte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="0f30d-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="0f30d-121">Při výskytu chyb během importu můžete zobrazit protokol provádění nebo fázování dat chyby, abyste zjistili chyby, které je nutné opravit k zajištění úspěšného importu.</span><span class="sxs-lookup"><span data-stu-id="0f30d-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="0f30d-122">Pokud je nutné importovat více než jeden formát souborů, je nutné vytvořit úlohy importu pro každý typ formátu.</span><span class="sxs-lookup"><span data-stu-id="0f30d-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="0f30d-123">Opětovně přiřazení transakcí platebních karet pro zrušené zaměstnance</span><span class="sxs-lookup"><span data-stu-id="0f30d-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="0f30d-124">Po ukončení záznamu zaměstnance je zakázán zaměstnancův účet služby Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="0f30d-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="0f30d-125">Mohou však existovat aktivní transakce platební karty, které musí být ještě zaneseny do výdajů a uhrazeny.</span><span class="sxs-lookup"><span data-stu-id="0f30d-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="0f30d-126">Ze stránky **Transakce platebních karet** můžete opět přiřadit zaměstnance k libovolné transakci platební karty, pokud byl související zaměstnanec propuštěn.</span><span class="sxs-lookup"><span data-stu-id="0f30d-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="0f30d-127">Vyberte jednu nebo více transakcí platebních karet a poté vyberte **Opětovně přiřadit transakce**.</span><span class="sxs-lookup"><span data-stu-id="0f30d-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="0f30d-128">Poté můžete vybrat jiného zaměstnance, ke kterému přiřadíte transakce platebních karet.</span><span class="sxs-lookup"><span data-stu-id="0f30d-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="0f30d-129">Poté, co opět přiřadíte transakce platební karty, můžete je vybrat pro sestavu výdajů a zaplatit běžným procesem pro uhrazení vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="0f30d-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
