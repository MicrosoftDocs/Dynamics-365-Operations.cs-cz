---
title: Nastavení způsobu platby pro převody kreditu ve formátu ISO20022
description: Tento postup ukazuje, jak nastavit metodu platby dodavatele pro převedení kreditu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92bc314e69628f2a287ba7c9a7c2d3d73a0bfd33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988095"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="d94f7-103">Nastavení způsobu platby pro převody kreditu ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="d94f7-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d94f7-104">Tento postup ukazuje, jak nastavit metodu platby dodavatele pro převedení kreditu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru.</span><span class="sxs-lookup"><span data-stu-id="d94f7-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="d94f7-105">Před provedením tohoto úkolu musíte exportovat konfigurace formátu a nastavit platební účty.</span><span class="sxs-lookup"><span data-stu-id="d94f7-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="d94f7-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="d94f7-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="d94f7-107">Toto je třetí z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="d94f7-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d94f7-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="d94f7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d94f7-109">Přejděte do nabídky Závazky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="d94f7-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="d94f7-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="d94f7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d94f7-111">Můžete například filtrovat v poli Metody platby pomocí hodnoty „SEPA CT“.</span><span class="sxs-lookup"><span data-stu-id="d94f7-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="d94f7-112">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="d94f7-112">Click Edit.</span></span>
4. <span data-ttu-id="d94f7-113">Vyberte položku Celkem v poli Období.</span><span class="sxs-lookup"><span data-stu-id="d94f7-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="d94f7-114">V poli Typ platby vyberte „Elektronická platba“.</span><span class="sxs-lookup"><span data-stu-id="d94f7-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="d94f7-115">Rozbalte oddíl Formáty souborů.</span><span class="sxs-lookup"><span data-stu-id="d94f7-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="d94f7-116">Vyberte možnost Ano v poli Obecné elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="d94f7-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="d94f7-117">V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d94f7-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="d94f7-118">V seznamu vyberte hodnotu ISO20022 – Převedení kreditu (DE).</span><span class="sxs-lookup"><span data-stu-id="d94f7-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="d94f7-119">Pokud je seznam prázdný, nejsou žádné importované a aktivní konfigurace formátu exportu platby dodavatele.</span><span class="sxs-lookup"><span data-stu-id="d94f7-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="d94f7-120">V poli Typ účtu vyberte „Banka“.</span><span class="sxs-lookup"><span data-stu-id="d94f7-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="d94f7-121">Zadejte hodnoty DEMF OPER do pole Platební účet.</span><span class="sxs-lookup"><span data-stu-id="d94f7-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="d94f7-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d94f7-122">Click Save.</span></span>

