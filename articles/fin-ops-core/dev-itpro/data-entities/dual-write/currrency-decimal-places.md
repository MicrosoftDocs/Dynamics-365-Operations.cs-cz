---
title: Migrace datového typu měny pro dvojitý zápis
description: Toto téma popisuje, jak změnit počet desetinných míst, která pro měnu podporuje duální zápis.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456807"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="cf25a-103">Migrace datového typu měny pro dvojitý zápis</span><span class="sxs-lookup"><span data-stu-id="cf25a-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf25a-104">Můžete zvýšit počet desetinných míst, která jsou podporována pro hodnoty měny, maximálně na 10.</span><span class="sxs-lookup"><span data-stu-id="cf25a-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="cf25a-105">Výchozí limit jsou čtyři desetinná místa.</span><span class="sxs-lookup"><span data-stu-id="cf25a-105">The default limit is four decimal places.</span></span> <span data-ttu-id="cf25a-106">Zvýšením počtu desetinných míst pomáháte zabránit ztrátě dat při synchronizaci dat pomocí duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="cf25a-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="cf25a-107">Zvýšení počtu desetinných míst je změna typu opt-in.</span><span class="sxs-lookup"><span data-stu-id="cf25a-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="cf25a-108">Chcete-li jej implementovat, musíte požádat o pomoc společnost Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf25a-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="cf25a-109">Proces změny počtu desetinných míst má dva kroky:</span><span class="sxs-lookup"><span data-stu-id="cf25a-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="cf25a-110">Žádost o migraci od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf25a-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="cf25a-111">Změna počtu desetinných míst v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf25a-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="cf25a-112">Aplikace Finance and Operations a Common Data Service musí podporovat stejný počet desetinných míst v hodnotách měny.</span><span class="sxs-lookup"><span data-stu-id="cf25a-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="cf25a-113">Jinak může dojít ke ztrátě dat, když jsou tyto informace synchronizovány mezi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="cf25a-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="cf25a-114">Proces migrace překonfiguruje způsob uložení hodnot měny a směnného kurzu, ale nezmění žádná data.</span><span class="sxs-lookup"><span data-stu-id="cf25a-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="cf25a-115">Po dokončení migrace lze zvýšit počet desetinných míst pro měnové kódy a ceny a data, která uživatelé zadávají a zobrazují, mohou mít větší desetinnou přesnost.</span><span class="sxs-lookup"><span data-stu-id="cf25a-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="cf25a-116">Migrace je volitelná.</span><span class="sxs-lookup"><span data-stu-id="cf25a-116">Migration is optional.</span></span> <span data-ttu-id="cf25a-117">Pokud byste mohli mít podporu pro více desetinných míst, doporučujeme zvážit migraci.</span><span class="sxs-lookup"><span data-stu-id="cf25a-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="cf25a-118">Organizace, které nevyžadují hodnoty, které mají více než čtyři desetinná místa, nemusí migrovat.</span><span class="sxs-lookup"><span data-stu-id="cf25a-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="cf25a-119">Žádost o migraci od společnosti Microsoft</span><span class="sxs-lookup"><span data-stu-id="cf25a-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="cf25a-120">Úložiště pro existující měnová pole v Common Data Service nemůže podporovat více než čtyři desetinná místa.</span><span class="sxs-lookup"><span data-stu-id="cf25a-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="cf25a-121">Proto během procesu migrace jsou hodnoty měny zkopírovány do nových interních polí v databázi.</span><span class="sxs-lookup"><span data-stu-id="cf25a-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="cf25a-122">Tento proces probíhá nepřetržitě, dokud nebudou migrována všechna data.</span><span class="sxs-lookup"><span data-stu-id="cf25a-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="cf25a-123">Interně na konci migrace nové typy úložišť nahrazují staré typy úložišť, ale hodnoty dat se nezmění.</span><span class="sxs-lookup"><span data-stu-id="cf25a-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="cf25a-124">Pole měny pak mohou podporovat až 10 desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="cf25a-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="cf25a-125">Během procesu migrace lze Common Data Service nadále používat bez přerušení.</span><span class="sxs-lookup"><span data-stu-id="cf25a-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="cf25a-126">Současně jsou měnové kurzy upravovány tak, aby podporovaly až 12 desetinných míst místo současného limitu 10.</span><span class="sxs-lookup"><span data-stu-id="cf25a-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="cf25a-127">Tato změna je nutná, aby počet desetinných míst byl stejný v aplikaci Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf25a-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="cf25a-128">Migrace nezmění žádná data.</span><span class="sxs-lookup"><span data-stu-id="cf25a-128">Migration doesn't change any data.</span></span> <span data-ttu-id="cf25a-129">Po převodu polí měny a směnného kurzu mohou správci nakonfigurovat systém tak, aby používal až 10 desetinných míst pro měnová pole zadáním počtu desetinných míst pro každou měnu transakce a pro stanovení ceny.</span><span class="sxs-lookup"><span data-stu-id="cf25a-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="cf25a-130">Požádejte o migraci</span><span class="sxs-lookup"><span data-stu-id="cf25a-130">Request a migration</span></span>

<span data-ttu-id="cf25a-131">Tuto funkci zpřístupníte odesláním e-mailu na **CDSExpandDecimal@microsoft.com** a obsahují následující informace:</span><span class="sxs-lookup"><span data-stu-id="cf25a-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="cf25a-132">**Předmět:** Žádost o povolení rozšířené desetinné podpory pro \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="cf25a-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="cf25a-133">**Text:** Chtěl bych povolit rozšířenou desetinnou podporu pro moji organizaci \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="cf25a-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="cf25a-134">Zástupce společnosti Microsoft vás bude kontaktovat do dvou až tří pracovních dnů pro další kroky.</span><span class="sxs-lookup"><span data-stu-id="cf25a-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="cf25a-135">Když požádáte o migraci, měli byste znát následující podrobnosti a podle toho je naplánovat:</span><span class="sxs-lookup"><span data-stu-id="cf25a-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="cf25a-136">Čas potřebný k migraci dat závisí na množství dat v systému.</span><span class="sxs-lookup"><span data-stu-id="cf25a-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="cf25a-137">Migrace velkých databází může trvat několik dní.</span><span class="sxs-lookup"><span data-stu-id="cf25a-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="cf25a-138">Velikost databáze se během migrace dočasně zvyšuje, protože pro indexy je potřeba další místo.</span><span class="sxs-lookup"><span data-stu-id="cf25a-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="cf25a-139">Po dokončení migrace je většina volného místa uvolněna.</span><span class="sxs-lookup"><span data-stu-id="cf25a-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="cf25a-140">Pokud během procesu migrace dojde k chybám, které brání dokončení migrace, systém upozorní podporu společnosti Microsoft, aby mohli pracovníci podpory zasáhnout.</span><span class="sxs-lookup"><span data-stu-id="cf25a-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="cf25a-141">I když se však během migrace vyskytnou chyby, Common Data Service zůstává plně k dispozici pro pravidelné používání.</span><span class="sxs-lookup"><span data-stu-id="cf25a-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="cf25a-142">Proces migrace není reverzibilní.</span><span class="sxs-lookup"><span data-stu-id="cf25a-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="cf25a-143">Změna počtu desetinných míst</span><span class="sxs-lookup"><span data-stu-id="cf25a-143">Changing the number of decimal places</span></span>

<span data-ttu-id="cf25a-144">Po dokončení migrace Common Data Service může ukládat čísla, která mají více desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="cf25a-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="cf25a-145">Správci si mohou vybrat, kolik desetinných míst se použije pro konkrétní kódy měn a pro stanovení ceny.</span><span class="sxs-lookup"><span data-stu-id="cf25a-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="cf25a-146">Uživatelé Microsoft Power Apps, Power BI, a Power Automate pak mohou zobrazit a používat čísla, která mají více desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="cf25a-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="cf25a-147">Chcete-li provést tuto změnu, musíte aktualizovat následující nastavení v aplikaci Power Apps:</span><span class="sxs-lookup"><span data-stu-id="cf25a-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="cf25a-148">**Systémová nastavení: Přesnost měny pro stanovení ceny** - pole **Nastavit přesnost měny, která se používá pro stanovení cen v celém systému** definuje, jak se bude měna chovat pro organizaci, když je vybrána **Přesnost stanovení cen**.</span><span class="sxs-lookup"><span data-stu-id="cf25a-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="cf25a-149">**Řízení podniku: měny** - Pole **Přesnost měny** umožňuje určit vlastní počet desetinných míst pro konkrétní měnu.</span><span class="sxs-lookup"><span data-stu-id="cf25a-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="cf25a-150">Existuje nastavení pro celou organizaci.</span><span class="sxs-lookup"><span data-stu-id="cf25a-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="cf25a-151">Existují některá omezení:</span><span class="sxs-lookup"><span data-stu-id="cf25a-151">There are some limitations:</span></span>

+ <span data-ttu-id="cf25a-152">Nelze konfigurovat pole měny na entitě.</span><span class="sxs-lookup"><span data-stu-id="cf25a-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="cf25a-153">Více než čtyři desetinná místa můžete zadat pouze na úrovni **Stanovení ceny** a **Měna transakce**.</span><span class="sxs-lookup"><span data-stu-id="cf25a-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="cf25a-154">Systémová nastavení: Přesnost měny pro stanovení ceny</span><span class="sxs-lookup"><span data-stu-id="cf25a-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="cf25a-155">Po dokončení migrace mohou správci nastavit přesnost měny.</span><span class="sxs-lookup"><span data-stu-id="cf25a-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="cf25a-156">Přejděte na **Nastavení \> Správa** a vyberte **Nastavení systému**.</span><span class="sxs-lookup"><span data-stu-id="cf25a-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="cf25a-157">Pak na kartě **Obecné** změňte hodnotu pole **Nastavit přesnost měny, která se používá pro stanovení cen v celém systému**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="cf25a-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![Systémová nastavení měny](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="cf25a-159">Řízení podniku: měny</span><span class="sxs-lookup"><span data-stu-id="cf25a-159">Business Management: Currencies</span></span>

<span data-ttu-id="cf25a-160">Pokud požadujete, aby se přesnost měny pro konkrétní měnu lišila od přesnosti měny použité pro stanovení ceny, můžete ji změnit.</span><span class="sxs-lookup"><span data-stu-id="cf25a-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="cf25a-161">Přejděte na **Nastavení \> Řízení podniku**, vyberte **Měny** a vyberte měnu, kterou chcete změnit.</span><span class="sxs-lookup"><span data-stu-id="cf25a-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="cf25a-162">Pak nastavte pole **Přesnost měny** a zadejte požadovaný počet desetinných míst, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="cf25a-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Nastavení měny pro konkrétní národní prostředí](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="cf25a-164">Entity: Pole měny</span><span class="sxs-lookup"><span data-stu-id="cf25a-164">Entities: Currency field</span></span>

<span data-ttu-id="cf25a-165">Počet desetinných míst, která lze konfigurovat pro konkrétní pole měny, je omezen na čtyři.</span><span class="sxs-lookup"><span data-stu-id="cf25a-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>
