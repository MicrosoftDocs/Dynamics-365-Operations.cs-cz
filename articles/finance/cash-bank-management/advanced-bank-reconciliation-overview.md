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
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09128f33d4208bc5c987683bb881aa1129b0dc8e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985429"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="938f7-104">Přehled rozšířeného odsouhlasení banky</span><span class="sxs-lookup"><span data-stu-id="938f7-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="938f7-105">Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="938f7-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="938f7-106">Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.</span><span class="sxs-lookup"><span data-stu-id="938f7-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="938f7-107">Funkce rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy.</span><span class="sxs-lookup"><span data-stu-id="938f7-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="938f7-108">Importované bankovní výpisy lze poté automaticky odsouhlasit v rámci bankovních transakcí.</span><span class="sxs-lookup"><span data-stu-id="938f7-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="938f7-109">Zde je postup pro tok rozšířeného odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="938f7-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="938f7-110">Nastavte import bankovních výpisů.</span><span class="sxs-lookup"><span data-stu-id="938f7-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="938f7-111">Importujte bankovní výpisy prostřednictvím rozhraní datové entity.</span><span class="sxs-lookup"><span data-stu-id="938f7-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="938f7-112">Součástí aplikace jsou tři obvyklé formáty bankovních výpisů: ISO20022, BAI2 a MT940.</span><span class="sxs-lookup"><span data-stu-id="938f7-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="938f7-113">Tuto funkci lze rozšířit o jakýkoli formát.</span><span class="sxs-lookup"><span data-stu-id="938f7-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="938f7-114">Nastavte číselnou řadu pro použití rozšířeného odsouhlasení banky a definujte pravidla párování pro odsouhlasení banky.</span><span class="sxs-lookup"><span data-stu-id="938f7-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="938f7-115">Odpovídající pravidlo odsouhlasení představují sadu kritérií, která se používají k filtrování řádků bankovních výpisů a řádků bankovních transakcí aplikace Microsoft Dynamics 365 Finance během procesu sesouhlasení.</span><span class="sxs-lookup"><span data-stu-id="938f7-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="938f7-116">V závislosti na vašich obchodních praktikách můžete nastavit více než jedno pravidlo párování k automatizaci a optimalizaci vašeho procesu odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="938f7-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="938f7-117">Odsouhlaste bankovní výpisy s bankovními transakcemi aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="938f7-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="938f7-118">Proveďte automatické párování a vytvoření deníků odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="938f7-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="938f7-119">Zobrazte bankovní výpisy a bankovní transakce aplikace Finance vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="938f7-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="938f7-120">Automaticky zaúčtujte bankovní transakce aplikace Finance, pokud se zobrazí na bankovním výpisu, ale nezobrazí v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="938f7-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="938f7-121">Generujte výkaz odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="938f7-121">Generate a reconciliation statement.</span></span>





