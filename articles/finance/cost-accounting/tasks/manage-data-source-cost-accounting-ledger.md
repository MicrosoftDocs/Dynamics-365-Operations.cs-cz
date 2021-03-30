---
title: Správa datového zdroje pro hlavní knihu nákladového účetnictví
description: Tento postup slouží k řízení zdroje dat hlavní knihy pro hlavní knihu nákladového účetnictví.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fef42f1866b0995182ac6fd022045f7dd31906
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218904"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="30adc-103">Správa datového zdroje pro hlavní knihu nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="30adc-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30adc-104">Tento postup slouží k řízení zdroje dat hlavní knihy pro hlavní knihu nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="30adc-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="30adc-105">Před dokončením tohoto úkolu se nezapomeňte podívat na průvodce Tvorba hlavní knihy nákladového účetnictví a Definování jednotek řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="30adc-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="30adc-106">Tento záznam používá v ukázkových datech společnost USP2.</span><span class="sxs-lookup"><span data-stu-id="30adc-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="30adc-107">Přejděte na Nákladové účetnictví > Nastavení hlavní knihy > Hlavní knihy nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="30adc-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="30adc-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="30adc-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="30adc-109">Klikněte na Skutečné verze.</span><span class="sxs-lookup"><span data-stu-id="30adc-109">Click Actual versions.</span></span>
4. <span data-ttu-id="30adc-110">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="30adc-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="30adc-111">Klikněte na Nastavení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="30adc-111">Click General ledger.</span></span>
6. <span data-ttu-id="30adc-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="30adc-112">Click New.</span></span>
7. <span data-ttu-id="30adc-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="30adc-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="30adc-114">V poli Poskytovatel dat zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="30adc-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="30adc-115">V tomto příkladu vyberte Dynamics 365 Finance – Položky hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="30adc-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="30adc-116">V poli Dimenze prvku nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="30adc-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="30adc-117">V tomto příkladu vyberte Nákladové elementy.</span><span class="sxs-lookup"><span data-stu-id="30adc-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="30adc-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="30adc-118">Click Save.</span></span>
11. <span data-ttu-id="30adc-119">Klikněte na Konfigurovat poskytovatele dat.</span><span class="sxs-lookup"><span data-stu-id="30adc-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="30adc-120">V poli Právnická osoba zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="30adc-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="30adc-121">V tomto příkladu vyberte USP2.</span><span class="sxs-lookup"><span data-stu-id="30adc-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="30adc-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="30adc-122">Click New.</span></span>
14. <span data-ttu-id="30adc-123">V poli Účtovací vrstvy vyberte Aktuální.</span><span class="sxs-lookup"><span data-stu-id="30adc-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="30adc-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="30adc-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]