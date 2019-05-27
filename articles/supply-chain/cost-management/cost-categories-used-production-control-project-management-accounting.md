---
title: Nákladové kategorie, které se používají v modulu Řízení výroby a Řízení a účetnictví projektů
description: Některé typy výrobní práce se mohou vztahovat na odhadovaný čas projektu a zprávy. Tento článek obsahuje informace o nákladových kategoriích, které je nutné definovat pro tyto typy výrobních prací pro účely výroby a projektů.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cab4629740e92f9075b7afc7a5d228b2e01c4664
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557864"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="d8f97-104">Nákladové kategorie, které se používají v modulu Řízení výroby a Řízení a účetnictví projektů</span><span class="sxs-lookup"><span data-stu-id="d8f97-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8f97-105">Některé typy výrobní práce se mohou vztahovat na odhadovaný čas projektu a zprávy.</span><span class="sxs-lookup"><span data-stu-id="d8f97-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="d8f97-106">Tento článek obsahuje informace o nákladových kategoriích, které je nutné definovat pro tyto typy výrobních prací pro účely výroby a projektů.</span><span class="sxs-lookup"><span data-stu-id="d8f97-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="d8f97-107">Některé typy výrobní práce se mohou vztahovat na odhadovaný čas projektu a zprávy.</span><span class="sxs-lookup"><span data-stu-id="d8f97-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="d8f97-108">Nákladová kategorie v tomto případě je nutná pro účely výroby a projektu.</span><span class="sxs-lookup"><span data-stu-id="d8f97-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="d8f97-109">Další informace související s projektem je nutné definovat při použití kategorie nákladů v produkci a projektech.</span><span class="sxs-lookup"><span data-stu-id="d8f97-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="d8f97-110">Například hodinové náklady přidružené k projektům se mohou lišit od hodinových nákladů přidružených k výrobě.</span><span class="sxs-lookup"><span data-stu-id="d8f97-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="d8f97-111">Stránku **Nákladové kategorie** lze použít a definovat s ní nákladové kategorie, které se používají v modulu Řízení výroby a Řízení a účetnictví projektů.</span><span class="sxs-lookup"><span data-stu-id="d8f97-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="d8f97-112">**Poznámka:** Nákladové účetnictví obsahuje stránku **Kategorie projektu**, ale nemá žádný vztah k funkcím popsaným v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="d8f97-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="d8f97-113">Používáte-li nákladovou kategorii na projektech, stránka **Nákladové kategorie** obsahuje další karty, které obsahují další údaje související s projektem.</span><span class="sxs-lookup"><span data-stu-id="d8f97-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="d8f97-114">Tyto informace zahrnují skupinu kategorií, vlastnost řádku a účty hlavní knihy, které jsou přiřazeny k nákladové kategorii.</span><span class="sxs-lookup"><span data-stu-id="d8f97-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="d8f97-115">Kategorii nákladů je nutné přiřadit skupině kategorií, která podporuje typ transakce **Hodiny**.</span><span class="sxs-lookup"><span data-stu-id="d8f97-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="d8f97-116">Vlastnost řádku určuje výchozí informace o způsobu fakturování hlášeného času v projektu.</span><span class="sxs-lookup"><span data-stu-id="d8f97-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="d8f97-117">Účty hlavní knihy, které souvisí s náklady a prodeji, jsou obvykle definovány pro skupinu kategorií přiřazenou kategorii nákladů.</span><span class="sxs-lookup"><span data-stu-id="d8f97-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="d8f97-118">Konkrétní účty ale lze definovat pro samostatnou kategorii nákladů.</span><span class="sxs-lookup"><span data-stu-id="d8f97-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="d8f97-119">Další tlačítka na stránce **Nákladové kategorie** poskytují přístup k informacím souvisejícím s projektem o vybrané kategorii nákladů.</span><span class="sxs-lookup"><span data-stu-id="d8f97-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="d8f97-120">Můžete například zobrazit transakce související s projektem, definovat zaměstnance nebo projekty, definovat hodinové náklady a prodejní ceny, nebo zobrazit sestavy.</span><span class="sxs-lookup"><span data-stu-id="d8f97-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>



