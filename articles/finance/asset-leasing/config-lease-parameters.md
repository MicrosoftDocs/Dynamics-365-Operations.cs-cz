---
title: Konfigurace parametrů leasingu (Preview)
description: Toto téma popisuje nastavení konfigurace pro leasing majetku, například informace o zabezpečení a nastavení účetnictví.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441358"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="47101-103">Konfigurace parametrů leasingu</span><span class="sxs-lookup"><span data-stu-id="47101-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47101-104">Chování leasingu majetku ovlivňuje několik nastavení konfigurace.</span><span class="sxs-lookup"><span data-stu-id="47101-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="47101-105">Tato nastavení zahrnují názvy deníků, obecné parametry a nastavení profilu účtování.</span><span class="sxs-lookup"><span data-stu-id="47101-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="47101-106">Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="47101-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="47101-107">Na kartě **Leasingy** vyberte záložku s náhledem **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="47101-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="47101-108">Parametr **Povolit ruční přepsání klasifikace** určuje, zda lze klasifikaci leasingu přepsat před potvrzením platebního kalendáře.</span><span class="sxs-lookup"><span data-stu-id="47101-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="47101-109">Parametr **Dávka mezi entitami** určuje, zda můžete odesílat provádět zaúčtování do jiných právnických osob z aktuální právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="47101-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="47101-110">Pokud je tento parametr zapnutý, můžete vytvořit položky deníku pro právnické osoby, ke kterým máte přístup.</span><span class="sxs-lookup"><span data-stu-id="47101-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="47101-111">Nastavte možnost **Povolit odstranění potvrzených leasingů** na **Ano**, aby bylo možné odstranit leasingy, které mají potvrzené platební kalendáře.</span><span class="sxs-lookup"><span data-stu-id="47101-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="47101-112">Leasingy nelze odstranit, pokud jsou k nim přidruženy zaúčtované nebo nezaúčtované transakce bez ohledu na nastavení této možnosti.</span><span class="sxs-lookup"><span data-stu-id="47101-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="47101-113">Po odstranění záznamu leasingu jej nemůžete obnovit.</span><span class="sxs-lookup"><span data-stu-id="47101-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="47101-114">Pokud odešlete jakékoli záznamy pro odstraněný leasing, ať už ručně nebo prostřednictvím datových entit, bude se s odeslanými informacemi zacházet jako s novými, nikoli jako s aktualizací existujícího leasingu.</span><span class="sxs-lookup"><span data-stu-id="47101-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="47101-115">Pokud nastavíte tuto možnost na **Ano** a typ přechodu knihy je **Možnost kumulativní opravy A nebo B**, systém nastaví pole **Přírůstková výpůjční úroková sazba** na hodnotu **Přírůstková výpůjční úroková sazba při přechodu** na stránce **Nastavení knihy**.</span><span class="sxs-lookup"><span data-stu-id="47101-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="47101-116">Pokud je tato možnost nastavena na **Ne**, sazba předního leasingu je nastavena na hodnotu **Přírůstková výpůjční proková sazba** na stránce **Podrobnosti o knize** bez ohledu na typ přechodu knihy.</span><span class="sxs-lookup"><span data-stu-id="47101-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="47101-117">Nastavte možnost **Povolit stornování odpisů ve verzi uzavřené knihy** možnost **Ano**, aby bylo možné stornovat transakce odpisových výdajů.</span><span class="sxs-lookup"><span data-stu-id="47101-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="47101-118">Transakce výdajů lze stornovat, i když je kniha uzavřena.</span><span class="sxs-lookup"><span data-stu-id="47101-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47101-119">Doporučujeme ponechat tuto možnost nastavenou na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="47101-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="47101-120">Nastavení této možnosti se používá jako ověření a kontrola, aby se zabránilo náhodnému odepsání verze uzavřené knihy.</span><span class="sxs-lookup"><span data-stu-id="47101-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="47101-121">Ponecháním možnosti nastavenou na **Ne** pomůžete udržet přesnou zůstatkovou účetní hodnotu a přesné výpočty budoucích odpisů.</span><span class="sxs-lookup"><span data-stu-id="47101-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
