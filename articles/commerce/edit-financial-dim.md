---
title: Úprava finančních dimenzí pro maloobchodní transakce
description: Toto téma popisuje, jak upravit finanční dimenze pro maloobchodní transakce v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: ff16d8e2e75a877e5ca7de604c7915e908473da6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792698"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="3e9fc-103">Úprava finančních dimenzí pro maloobchodní transakce</span><span class="sxs-lookup"><span data-stu-id="3e9fc-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e9fc-104">Toto téma popisuje, jak upravit finanční dimenze pro maloobchodní transakce v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="3e9fc-105">Úprava finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="3e9fc-105">Edit financial dimensions</span></span>

<span data-ttu-id="3e9fc-106">Chcete-li upravit finanční dimenze pro maloobchodní transakce v Commerce Headquarters, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3e9fc-107">Otevřete stránku **Konfigurace finanční dimenze pro integraci aplikací**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="3e9fc-108">Vyberte aktivní záznam **Výchozí integrace dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="3e9fc-109">Na záložce s náhledem **Finanční dimenze** se ujistěte, že všechny dimenze, které chcete upravit v listu aplikace Excel, jsou přítomny v seznamu **Vybrané**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="3e9fc-110">Další informace viz [Datové entity](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="3e9fc-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="3e9fc-111">Stáhněte a otevřete soubor Excel ze stránky **Výkazy**, stránky **Maloobchodní transakce** nebo dlaždice **Selhání ověření transakcí** v pracovním prostoru **Finance obchodu**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="3e9fc-112">Chcete-li změnit finanční dimenzi transakce, vyberte **Návrh** a potom vyberte symbol tužky vedle řádku **Transakce (auditovatelná)**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="3e9fc-113">Najděte a vyberte pole **FinancialDimensionDisplayValue**, vyberte buňku v části záhlaví listu aplikace Excel a poté vyberte **Přidat popisek**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="3e9fc-114">Vyberte buňku pod buňkou, kterou jste vybrali v předchozím kroku, vyberte **Přidat hodnotu** a potom vyberte **Obnovit**.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="3e9fc-115">Finanční dimenze jsou přidány do listu aplikace Excel a poté je lze upravit a publikovat.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="3e9fc-116">Chcete-li změnit dimenze na řádcích transakce, vyberte řádek **Prodejní transakce (auditovatelné)**, vyberte symbol tužky a opakujte kroky 6 a 7.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="3e9fc-117">Chcete-li změnit dimenze na řádcích platby, vyberte řádek **Platební transakce (auditovatelné)**, vyberte symbol tužky a opakujte kroky 6 a 7.</span><span class="sxs-lookup"><span data-stu-id="3e9fc-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e9fc-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3e9fc-118">Additional resources</span></span>

[<span data-ttu-id="3e9fc-119">Úpravy a audit transakcí cash and carry a řízení hotovosti</span><span class="sxs-lookup"><span data-stu-id="3e9fc-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="3e9fc-120">Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="3e9fc-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="3e9fc-121">Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="3e9fc-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="3e9fc-122">Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="3e9fc-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]