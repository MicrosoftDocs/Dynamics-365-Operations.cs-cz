---
title: Import konfigurace převodu kreditu ve formátu ISO20022
description: Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a96827bc6e126a7f5de6d67338b5233a65d93c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840906"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="80a41-103">Import konfigurace převodu kreditu ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="80a41-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80a41-104">Tento postup ukazuje, jak importovat konfiguraci elektronického výkaznictví pro platby dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="80a41-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="80a41-105">Formát pro peněžní převod podle německé normy ISO 20022 slouží jako příklad.</span><span class="sxs-lookup"><span data-stu-id="80a41-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="80a41-106">Tento postup lze použít pro jiný dostupný formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="80a41-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="80a41-107">Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF, ale k jeho dokončení můžete použít ukázková data libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="80a41-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="80a41-108">Toto je první z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="80a41-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="80a41-109">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="80a41-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="80a41-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="80a41-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="80a41-111">V seznamu dostupných poskytovatelů konfigurace vyberte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80a41-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="80a41-112">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="80a41-112">Click Set active.</span></span>
4. <span data-ttu-id="80a41-113">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="80a41-113">Click Repositories.</span></span>
5. <span data-ttu-id="80a41-114">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="80a41-114">Click Open.</span></span>
6. <span data-ttu-id="80a41-115">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="80a41-115">Click Show filters.</span></span>
7. <span data-ttu-id="80a41-116">Použijte následující filtry: Do pole Název konfigurace zadejte hodnotu filtru ISO20022 Credit transfer (DE) a použijte operátor filtru začíná na</span><span class="sxs-lookup"><span data-stu-id="80a41-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="80a41-117">Případně vyhledejte konfiguraci v seznamu, vyberte ji a převeďte na úlohu importu.</span><span class="sxs-lookup"><span data-stu-id="80a41-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="80a41-118">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="80a41-118">Click Import.</span></span>
    * <span data-ttu-id="80a41-119">Pokud tlačítko Importovat není k dispozici, znamená to, že tato konfigurace je již po importu.</span><span class="sxs-lookup"><span data-stu-id="80a41-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="80a41-120">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="80a41-120">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]