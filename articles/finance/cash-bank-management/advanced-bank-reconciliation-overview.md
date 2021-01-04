---
title: Přehled rozšířeného odsouhlasení banky
description: Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky. Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441252"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="5ba66-104">Přehled rozšířeného odsouhlasení banky</span><span class="sxs-lookup"><span data-stu-id="5ba66-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ba66-105">Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="5ba66-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="5ba66-106">Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.</span><span class="sxs-lookup"><span data-stu-id="5ba66-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="5ba66-107">Funkce rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy.</span><span class="sxs-lookup"><span data-stu-id="5ba66-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="5ba66-108">Importované bankovní výpisy lze poté automaticky odsouhlasit v rámci bankovních transakcí.</span><span class="sxs-lookup"><span data-stu-id="5ba66-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="5ba66-109">Zde je postup pro tok rozšířeného odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="5ba66-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="5ba66-110">Nastavte import bankovních výpisů.</span><span class="sxs-lookup"><span data-stu-id="5ba66-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="5ba66-111">Importujte bankovní výpisy prostřednictvím rozhraní datové entity.</span><span class="sxs-lookup"><span data-stu-id="5ba66-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="5ba66-112">Součástí aplikace jsou tři obvyklé formáty bankovních výpisů: ISO20022, BAI2 a MT940.</span><span class="sxs-lookup"><span data-stu-id="5ba66-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="5ba66-113">Tuto funkci lze rozšířit o jakýkoli formát.</span><span class="sxs-lookup"><span data-stu-id="5ba66-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="5ba66-114">Nastavte číselnou řadu pro použití rozšířeného odsouhlasení banky a definujte pravidla párování pro odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="5ba66-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="5ba66-115">Odpovídající pravidlo odsouhlasení představují sadu kritérií, která se používají k filtrování řádků bankovních výpisů a řádků bankovních transakcí aplikace Microsoft Dynamics 365 Finance během procesu sesouhlasení.</span><span class="sxs-lookup"><span data-stu-id="5ba66-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="5ba66-116">V závislosti na vašich obchodních praktikách můžete nastavit více než jedno pravidlo párování k automatizaci a optimalizaci vašeho procesu odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="5ba66-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="5ba66-117">Odsouhlaste bankovní výpisy s bankovními transakcemi aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="5ba66-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="5ba66-118">Proveďte automatické párování a vytvoření deníků odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="5ba66-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="5ba66-119">Zobrazte bankovní výpisy a bankovní transakce aplikace Finance vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="5ba66-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="5ba66-120">Automaticky zaúčtujte bankovní transakce aplikace Finance, pokud se zobrazí na bankovním výpisu, ale nezobrazí v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="5ba66-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="5ba66-121">Generujte výkaz odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="5ba66-121">Generate a reconciliation statement.</span></span>





