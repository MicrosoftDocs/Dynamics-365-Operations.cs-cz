---
title: Vytvoření schémat časového rozlišení
description: Toto téma vysvětluje, jak vytvořit schéma časového rozlišení.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41ea75b5c54f43efd4d5b9ef194e6394fc50bccc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815133"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="713d4-103">Vytvoření schémat časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="713d4-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="713d4-104">Toto téma vysvětluje, jak vytvořit schéma časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="713d4-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="713d4-105">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="713d4-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="713d4-106">Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Nastavení deníku > Schémata časového rozlišení**.</span><span class="sxs-lookup"><span data-stu-id="713d4-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="713d4-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="713d4-107">Select **New**.</span></span>
3. <span data-ttu-id="713d4-108">Zadejte hodnotu do pole **Identifikace časového rozlišení**.</span><span class="sxs-lookup"><span data-stu-id="713d4-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="713d4-109">Do pole **Popis schématu časového rozlišení** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="713d4-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="713d4-110">Zadejte požadované hodnoty do pole **Má dáti**.</span><span class="sxs-lookup"><span data-stu-id="713d4-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="713d4-111">Definovaný hlavní účet nahradí hlavní účet Má dáti v řádku dokladu deníku také bude použit pro stornování časově rozlišených položek na základě transakcí časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="713d4-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="713d4-112">Zadejte požadované hodnoty do pole **Dal**.</span><span class="sxs-lookup"><span data-stu-id="713d4-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="713d4-113">Definovaný hlavní účet nahradí kreditní hlavní účet řádku dokladu deníku a také bude použit pro stornování časově rozlišených položek podle transakcí časového rozlišení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="713d4-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="713d4-114">V poli **Doklad** vyberte způsob určení dokladu, když jsou transakce zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="713d4-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="713d4-115">V poli **Popis** zadejte hodnotu k popisu transakcí, které mají být zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="713d4-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="713d4-116">V poli **Frekvence období** vyberte, jak často by transakce měla být zaznamenána.</span><span class="sxs-lookup"><span data-stu-id="713d4-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="713d4-117">Do pole **Počet výskytů podle období** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="713d4-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="713d4-118">V poli **Zaúčtovat transakce** vyberte, kdy transakce mají být zaúčtovány – například **měsíčně**.</span><span class="sxs-lookup"><span data-stu-id="713d4-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]