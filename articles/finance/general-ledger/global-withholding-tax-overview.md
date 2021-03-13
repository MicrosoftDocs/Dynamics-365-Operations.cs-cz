---
title: Globální srážková daň
description: Toto téma poskytuje informace o globální funkci srážkové daně a o tom, jak ji nastavit. Globální funkce srážkové daně je vylepšena u transakcí dodavatelů a zákazníků, takže srážková daň se počítá na úrovni položky.
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
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075731"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="db8de-104">Globální srážková daň</span><span class="sxs-lookup"><span data-stu-id="db8de-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db8de-105">Toto téma poskytuje informace o globální funkci srážkové daně a vysvětluje, jak ji nastavit.</span><span class="sxs-lookup"><span data-stu-id="db8de-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="db8de-106">Tato nová funkce je k dispozici ve verzi 10.0.17 a novější.</span><span class="sxs-lookup"><span data-stu-id="db8de-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="db8de-107">Globální funkce srážkové daně je vylepšena u transakcí dodavatelů a zákazníků, takže srážková daň se počítá na úrovni položky.</span><span class="sxs-lookup"><span data-stu-id="db8de-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="db8de-108">Zůstatek na účtu srážkové daně z nákupních transakcí lze vyrovnat spuštěním úlohy platby srážkové daně proti účtu vyrovnání srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="db8de-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="db8de-109">Globální srážková daň nepodporuje funkci **Spravovat náklady** na stránkách nákupní objednávky, faktury dodavatele a prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="db8de-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="db8de-110">Zapnutí globální srážkové daně</span><span class="sxs-lookup"><span data-stu-id="db8de-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="db8de-111">V pracovním prostoru **Správa funkcí** vyberte **Globální srážková daň** a poté vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="db8de-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="db8de-112">Přejděte na **Daň \> Nastavení \> Parametry \> Parametry hlavní knihy** a poté na kartě **Srážková daň** nastavte možnost **Povolit globální srážkovou daň** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="db8de-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="db8de-113">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="db8de-113">Select **Save**.</span></span>
4. <span data-ttu-id="db8de-114">Aktualizujte stránku ve webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="db8de-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="db8de-115">Globální funkce srážkové daně nelze zapnout pro země/oblasti, kde již existují lokalizovaná řešení srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="db8de-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="db8de-116">Mezi tyto oblasti patří mimo jiné Indie, Brazílie, Thajsko, Saúdská Arábie, Irsko, Velká Británie a Spojené státy.</span><span class="sxs-lookup"><span data-stu-id="db8de-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
