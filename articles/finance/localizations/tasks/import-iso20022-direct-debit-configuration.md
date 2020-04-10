---
title: Import konfigurace přímého debetu ve formátu ISO20022
description: Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby odběratelů.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d4256b155d3e06d63e425fab63b4025ef2577f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140011"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="152cb-103">Import konfigurace přímého debetu ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="152cb-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="152cb-104">Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby odběratelů.</span><span class="sxs-lookup"><span data-stu-id="152cb-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="152cb-105">Tento postup používá jako příklad formát přímého debetu ISO 20022.</span><span class="sxs-lookup"><span data-stu-id="152cb-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="152cb-106">Tento postup byl vytvořen pomocí ukázkových dat společnosti DEMF, ale můžete pro tento účel použít ukázková data libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="152cb-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="152cb-107">Toto je první z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="152cb-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="152cb-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="152cb-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="152cb-109">V seznamu dostupných poskytovatelů konfigurace vyberte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="152cb-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="152cb-110">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="152cb-110">Click Set active.</span></span>
4. <span data-ttu-id="152cb-111">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="152cb-111">Click Repositories.</span></span>
5. <span data-ttu-id="152cb-112">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="152cb-112">Click Open.</span></span>
6. <span data-ttu-id="152cb-113">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="152cb-113">Click Show filters.</span></span>
7. <span data-ttu-id="152cb-114">Použijte následující filtry: Do pole Název konfigurace zadejte hodnotu filtru ISO20022 Direct debit (DE) a použijte operátor filtru začíná na</span><span class="sxs-lookup"><span data-stu-id="152cb-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="152cb-115">Volitelně můžete vyhledat konfiguraci v seznamu, vybrat ji a tento krok přeskočit.</span><span class="sxs-lookup"><span data-stu-id="152cb-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="152cb-116">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="152cb-116">Click Import.</span></span>
    * <span data-ttu-id="152cb-117">Pokud tlačítko Importovat není k dispozici, znamená to, že tato konfigurace je již po importu.</span><span class="sxs-lookup"><span data-stu-id="152cb-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="152cb-118">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="152cb-118">Click Yes.</span></span>

