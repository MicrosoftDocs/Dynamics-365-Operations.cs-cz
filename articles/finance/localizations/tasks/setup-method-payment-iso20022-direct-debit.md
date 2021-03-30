---
title: Nastavení způsobu platby pro přímý debet ISO20022
description: Tento postup ukazuje, jak nastavit metodu platby odběratele pro převedení přímého debetu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2ce4e1e960e04c0033990f99eb71897c7ea730f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208400"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="2cbb9-103">Nastavení způsobu platby pro přímý debet ISO20022</span><span class="sxs-lookup"><span data-stu-id="2cbb9-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2cbb9-104">Tento postup ukazuje, jak nastavit metodu platby odběratele pro převedení přímého debetu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="2cbb9-105">Před provedením tohoto úkolu musíte exportovat konfigurace formátu a nastavit platební účty.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="2cbb9-106">Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="2cbb9-107">Toto je třetí z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="2cbb9-108">Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="2cbb9-109">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2cbb9-110">Můžete například filtrovat v poli Metody platby pomocí hodnoty „ELECTRONIC“.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="2cbb9-111">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-111">Click Edit.</span></span>
4. <span data-ttu-id="2cbb9-112">Zadejte hodnoty DEMF OPER do pole Platební účet.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="2cbb9-113">Rozbalte oddíl Formáty souborů.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="2cbb9-114">Vyberte možnost Ano v poli Obecné elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="2cbb9-115">V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="2cbb9-116">V seznamu vyberte ISO20022 – přímý debet (DE).</span><span class="sxs-lookup"><span data-stu-id="2cbb9-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="2cbb9-117">Pokud je seznam prázdný, nejsou žádné importované a aktivní konfigurace formátu exportu platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="2cbb9-118">Vyberte možnost Ano v poli Požadovat zmocnění.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="2cbb9-119">Pro vlastní formáty platby vyberte parametr Požadovat zmocnění, který vyžaduje zahrnutí informací o zmocnění do zprávy o platbě, jako je přímý debet SEPA.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="2cbb9-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2cbb9-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]