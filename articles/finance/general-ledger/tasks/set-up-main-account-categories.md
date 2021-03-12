---
title: Nastavení kategorií hlavního účtu
description: Toto téma vysvětluje, jak nastavit kategorie hlavního účtu v aplikaci Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d53181d63f7b362662d993e21671e9b685b5dfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968418"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="005ec-103">Nastavení kategorií hlavního účtu</span><span class="sxs-lookup"><span data-stu-id="005ec-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="005ec-104">Toto téma vysvětluje, jak nastavit kategorie hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="005ec-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="005ec-105">Kategorie hlavního účtu se používají pro výchozí sestavy ve finančních výkazech a Power BI.</span><span class="sxs-lookup"><span data-stu-id="005ec-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="005ec-106">Kategorie hlavního účtu, které jsou vytvořeny ve výchozím nastavení, lze přejmenovat, ale nelze je odstranit.</span><span class="sxs-lookup"><span data-stu-id="005ec-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="005ec-107">Kategorie dalších účtů lze vytvořit a používat pro účely vytváření sestav a analýzy.</span><span class="sxs-lookup"><span data-stu-id="005ec-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="005ec-108">Toto téma využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="005ec-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="005ec-109">Vytvoření kategorie hlavního účtu</span><span class="sxs-lookup"><span data-stu-id="005ec-109">Create a main account category</span></span>
1. <span data-ttu-id="005ec-110">V navigačním podokně přejděte do části **Moduly >Hlavní kniha > Účtová osnova > Účty > Kategorie hlavního účtu**.</span><span class="sxs-lookup"><span data-stu-id="005ec-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="005ec-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="005ec-111">Select **New**.</span></span>
3. <span data-ttu-id="005ec-112">Do pole **Kategorie hlavního účtu** zadejte jedinečný název.</span><span class="sxs-lookup"><span data-stu-id="005ec-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="005ec-113">Do pole **Popis** zadejte popis nové kategorie hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="005ec-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="005ec-114">V poli **Typ hlavního účtu** vyberte typ hlavního účtu, který bude propojen do kategorie.</span><span class="sxs-lookup"><span data-stu-id="005ec-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="005ec-115">Propojení kategorie účtu s hlavními účty</span><span class="sxs-lookup"><span data-stu-id="005ec-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="005ec-116">Klikněte na **Připojit hlavní účty**.</span><span class="sxs-lookup"><span data-stu-id="005ec-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="005ec-117">V seznamu vyberte hlavní účty, které chcete přiřadit do kategorie hlavního účtu zaškrtnutím políček ve sloupci **Propojeno**.</span><span class="sxs-lookup"><span data-stu-id="005ec-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="005ec-118">Přiřazením hlavních účtů do kategorie hlavních účtů budou nahromaděny zůstatky účtů, když tato kategorie se používá k vytváření finančních sestav a analýzy.</span><span class="sxs-lookup"><span data-stu-id="005ec-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="005ec-119">Hlavní účty vyberete zvolením nebo zrušením výběru **Propojeno**.</span><span class="sxs-lookup"><span data-stu-id="005ec-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="005ec-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="005ec-120">Select **OK**.</span></span>
5. <span data-ttu-id="005ec-121">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="005ec-121">Select **Yes**.</span></span>
