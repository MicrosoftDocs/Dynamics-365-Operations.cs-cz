---
title: Nastavení parametrů TDS
description: Toto téma vysvětluje, jak nastavit parametry pro aktivaci funkce TDS (daň odečtená u zdroje) v zadaných transakcích. Toto je nezbytný krok k použití funkce Daň odečtená u zdroje TDS.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023086"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="17d57-104">Nastavení parametrů TDS</span><span class="sxs-lookup"><span data-stu-id="17d57-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17d57-105">Toto téma vysvětluje, jak nastavit parametry pro aktivaci funkce TDS (daň odečtená u zdroje) v zadaných transakcích.</span><span class="sxs-lookup"><span data-stu-id="17d57-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="17d57-106">Toto je nezbytný krok k použití funkce Daň odečtená u zdroje TDS.</span><span class="sxs-lookup"><span data-stu-id="17d57-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="17d57-107">Přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="17d57-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="17d57-108">Na kartě **Přímé daně** v části **Daň odečtená u zdroje** nastavte možnost **Aktivovat TDS** na **Ano** k aktivaci funkčnosti TDS a stránek a polí, která se pro ni používají.</span><span class="sxs-lookup"><span data-stu-id="17d57-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="17d57-109">Nastavte možnost **Faktura** na **Ano** k aktivaci pole, která se používají k výpočtu a odpočtu TDS na úrovni faktury.</span><span class="sxs-lookup"><span data-stu-id="17d57-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="17d57-110">Nastavte možnost **Platba** na **Ano** k aktivaci pole, která se používají k výpočtu a odpočtu TDS na úrovni platby.</span><span class="sxs-lookup"><span data-stu-id="17d57-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="17d57-111">[![Karta Přímé daně](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="17d57-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="17d57-112">Na kartě **Číselné řady** najděte řádek, kde je pole **Odkaz** nastaveno na **Platba srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="17d57-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="17d57-113">V poli **Kód číselné řady** pro daný řádek vyberte kód číselné řady.</span><span class="sxs-lookup"><span data-stu-id="17d57-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="17d57-114">Kód číselné řady se používá ke generování čísel dokladů pro periodický proces vypořádání TDS.</span><span class="sxs-lookup"><span data-stu-id="17d57-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="17d57-115">Chcete-li spustit periodický proces vypořádání TDS, přejděte na **Daň \> Přiznání \> Srážková daň \> Platba srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="17d57-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="17d57-116">[![Karta Číselné řady](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="17d57-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="17d57-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="17d57-117">Close the page.</span></span>
