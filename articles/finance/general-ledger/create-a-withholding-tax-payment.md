---
title: Vytvoření platby srážkové daně
description: Procedura úlohy platby srážkové daně slouží k vyrovnání zůstatků srážkové daně ze závazků na účet srážkové daně a jejich vyrovnání na účtu pro vyrovnání srážkové daně za dané období. Toto téma uvádí kroky pro nastavení platby srážkové daně.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212270"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="48f04-104">Vytvoření platby srážkové daně</span><span class="sxs-lookup"><span data-stu-id="48f04-104">Create a withholding tax payment</span></span>

<span data-ttu-id="48f04-105">Procedura úlohy platby srážkové daně slouží k vyrovnání zůstatků srážkové daně ze závazků na účet srážkové daně a jejich vyrovnání na účtu pro vyrovnání srážkové daně za dané období.</span><span class="sxs-lookup"><span data-stu-id="48f04-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="48f04-106">Toto téma uvádí kroky pro nastavení platby srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="48f04-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="48f04-107">Při výpočtu platby srážkové daně se nebere v úvahu kompenzace srážkové daně (z pohledávek).</span><span class="sxs-lookup"><span data-stu-id="48f04-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="48f04-108">Přejděte na **Navigační podokno > Moduly > Daň > Přiznání > Srážková daň > Platba srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="48f04-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="48f04-109">V poli **Období vyrovnání** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="48f04-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="48f04-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="48f04-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="48f04-111">Do pole **Od data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="48f04-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="48f04-112">Zadejte datum do pole **Datum transakce**.</span><span class="sxs-lookup"><span data-stu-id="48f04-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="48f04-113">Vyberte **Aktualizace** k zaúčtování dokladu platby srážkové daně na účet vyrovnání srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="48f04-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="48f04-114">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="48f04-114">Click **OK**.</span></span>

![Parametry platby srážkové daně](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]