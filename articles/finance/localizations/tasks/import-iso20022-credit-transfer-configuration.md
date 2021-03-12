---
title: Import konfigurace převodu kreditu ve formátu ISO20022
description: Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů.
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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38e3c5b3b85eb9ad17270cf7002046896d305548
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988256"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="4271a-103">Import konfigurace převodu kreditu ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="4271a-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4271a-104">Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="4271a-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="4271a-105">Formát pro peněžní převod podle německé normy ISO 20022 slouží jako příklad.</span><span class="sxs-lookup"><span data-stu-id="4271a-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="4271a-106">Tento postup lze použít pro jiný dostupný formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4271a-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="4271a-107">Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF, ale k jeho dokončení můžete použít ukázková data libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="4271a-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="4271a-108">Toto je první z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4271a-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="4271a-109">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="4271a-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="4271a-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4271a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4271a-111">V seznamu dostupných poskytovatelů konfigurace vyberte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4271a-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="4271a-112">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="4271a-112">Click Set active.</span></span>
4. <span data-ttu-id="4271a-113">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="4271a-113">Click Repositories.</span></span>
5. <span data-ttu-id="4271a-114">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="4271a-114">Click Open.</span></span>
6. <span data-ttu-id="4271a-115">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="4271a-115">Click Show filters.</span></span>
7. <span data-ttu-id="4271a-116">Použijte následující filtry: Do pole Název konfigurace zadejte hodnotu filtru ISO20022 Credit transfer (DE) a použijte operátor filtru začíná na</span><span class="sxs-lookup"><span data-stu-id="4271a-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="4271a-117">Případně vyhledejte konfiguraci v seznamu, vyberte ji a převeďte na úlohu importu.</span><span class="sxs-lookup"><span data-stu-id="4271a-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="4271a-118">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="4271a-118">Click Import.</span></span>
    * <span data-ttu-id="4271a-119">Pokud tlačítko Importovat není k dispozici, znamená to, že tato konfigurace je již po importu.</span><span class="sxs-lookup"><span data-stu-id="4271a-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="4271a-120">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="4271a-120">Click Yes.</span></span>

