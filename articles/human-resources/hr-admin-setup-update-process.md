---
title: Aktualizace procesu
description: Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace při změnách aplikací a platforem.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d841a026f589d774ec5ada3ac9adcc84dde9aee1
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527793"
---
# <a name="update-process"></a><span data-ttu-id="2122b-103">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="2122b-103">Update process</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2122b-104">Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace.</span><span class="sxs-lookup"><span data-stu-id="2122b-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="2122b-105">Tyto aktualizace zahrnují změny aplikace i platformy, které často poskytují klíčová vylepšení služby, včetně pravidelných aktualizací.</span><span class="sxs-lookup"><span data-stu-id="2122b-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="2122b-106">Zásady aktualizace</span><span class="sxs-lookup"><span data-stu-id="2122b-106">Update policy</span></span>

<span data-ttu-id="2122b-107">Aktualizace jsou vydávány v pravidelných intervalech pro všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="2122b-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="2122b-108">Aplikace Human Resources je podporována podle [Zásad životního cyklu společnosti Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), které poskytují konzistentní a předpověditelné pokyny pro dostupnost podpory.</span><span class="sxs-lookup"><span data-stu-id="2122b-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="2122b-109">Interval vydávání</span><span class="sxs-lookup"><span data-stu-id="2122b-109">Release cadence</span></span> 

<span data-ttu-id="2122b-110">Aktualizace aplikace Human Resources se automaticky použijí na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="2122b-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="2122b-111">Aplikace Human Resources poskytuje dva typy vydání:</span><span class="sxs-lookup"><span data-stu-id="2122b-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="2122b-112">**Aktualizace služeb**: Dvoutýdenní aktualizace, které zahrnují opravy chyb a nové funkce.</span><span class="sxs-lookup"><span data-stu-id="2122b-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="2122b-113">Aktualizace služeb také zahrnují platné aktualizace platformy při jejich vydání.</span><span class="sxs-lookup"><span data-stu-id="2122b-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="2122b-114">Chcete-li získat představu o tom, kdy jsou aktualizace platformy vydávány, viz [Tabulku 3: Vydání platformy](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="2122b-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="2122b-115">Čtrnáctidenní intervaly aktualizace mají průběžné globální zavedení mezi oblastmi.</span><span class="sxs-lookup"><span data-stu-id="2122b-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="2122b-116">Další informace o čtrnáctidenních aktualizacích viz [Co je nového a co se změnilo v produktu Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="2122b-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="2122b-117">Všechna podporovaná datacentra se aktualizují každé dva týdny, není-li uvedeno jinak.</span><span class="sxs-lookup"><span data-stu-id="2122b-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="2122b-118">Do čtrnáctidenních aktualizací jsou zahrnuty USA, Austrálie, Evropa, Spojené království, Asie a Kanada.</span><span class="sxs-lookup"><span data-stu-id="2122b-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="2122b-119">**Aktualizace řešení Common Data Service**: Tyto aktualizace se uskutečňují podle potřeby, přibližně jednou za šest týdnů.</span><span class="sxs-lookup"><span data-stu-id="2122b-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="2122b-120">Zahrnují nové entity a změny existujících entit ve službě Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2122b-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="2122b-121">Tyto aktualizace jsou vydávány pro stejné regiony jako čtrnáctidenní aktualizace a jejich replikace do všech datacenter trvá přibližně šest týdnů.</span><span class="sxs-lookup"><span data-stu-id="2122b-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="2122b-122">Aktualizace řešení mohou nebo nemusí být vydávány současně s čtrnáctidenními aktualizacemi služeb.</span><span class="sxs-lookup"><span data-stu-id="2122b-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="2122b-123">Aktualizace řešení jsou po vydání k dispozici ve všech datacentrech.</span><span class="sxs-lookup"><span data-stu-id="2122b-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="2122b-124">Pokud nechcete čekat na automatickou replikaci aktualizací, můžete tyto aktualizace provést ručně v jakémkoli prostředí, v libovolném datacentru.</span><span class="sxs-lookup"><span data-stu-id="2122b-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="2122b-125">V případě potřeby poskytuje aplikace Human Resources také následující typy oprav:</span><span class="sxs-lookup"><span data-stu-id="2122b-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="2122b-126">**Revize (oprava hotfix)**: opravy chyb, které mohou být provedeny buďto současně s vydáním čtrnáctidenní aktualizace služby, nebo odděleně</span><span class="sxs-lookup"><span data-stu-id="2122b-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="2122b-127">**Nouzová oprava**: opravy hotfix prováděné preventivně a v reakci na problém, které jsou svojí povahou samostatné, mohou zahrnovat pouze změny konfigurace nebo změny kódu pro odstranění aktuálních problémů a mohou být prováděny odděleně od vydání čtrnáctidenní aktualizace služby</span><span class="sxs-lookup"><span data-stu-id="2122b-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="2122b-128">Vydání jsou kontrolována, testována a ověřována v interním prostředí.</span><span class="sxs-lookup"><span data-stu-id="2122b-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="2122b-129">Po schválení jsou sestavení nasazena do výroby.</span><span class="sxs-lookup"><span data-stu-id="2122b-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="2122b-130">Uvolnit výjimky frekvence v 2020</span><span class="sxs-lookup"><span data-stu-id="2122b-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="2122b-131">Kvůli svátkům je plán vydání pro listopad a prosinec 2020 následující:</span><span class="sxs-lookup"><span data-stu-id="2122b-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="2122b-132">Vydání v listopadu: 2. listopadu – 13. listopadu</span><span class="sxs-lookup"><span data-stu-id="2122b-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="2122b-133">Vydání v prosinci: 30. listopadu – 11. prosince</span><span class="sxs-lookup"><span data-stu-id="2122b-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="2122b-134">Kadence dvoutýdenního vydání bude obnovena jako obvykle 11. ledna 2021.</span><span class="sxs-lookup"><span data-stu-id="2122b-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="2122b-135">Sdělení</span><span class="sxs-lookup"><span data-stu-id="2122b-135">Communications</span></span>

<span data-ttu-id="2122b-136">Zde uvádíme, co bylo provedeno v případě aplikace Human Resources a co jsme vydali v následujících místech:</span><span class="sxs-lookup"><span data-stu-id="2122b-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="2122b-137">Dynamics 365 Human Resources plán</span><span class="sxs-lookup"><span data-stu-id="2122b-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="2122b-138">Plány vydání Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2122b-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="2122b-139">Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="2122b-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="2122b-140">[Hledání problémů ve službě Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (pouze chyby týkající se platformy)</span><span class="sxs-lookup"><span data-stu-id="2122b-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="2122b-141">Blog aplikace Human Resources</span><span class="sxs-lookup"><span data-stu-id="2122b-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="2122b-142">Komunita aplikace Human Resources v síti Yammer</span><span class="sxs-lookup"><span data-stu-id="2122b-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="2122b-143">Ověření předběžných verzí funkcí v izolovaném testovacím prostředí (sandbox)</span><span class="sxs-lookup"><span data-stu-id="2122b-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="2122b-144">Předběžnou verzi funkcí můžete ověřit v izolovaném testovacím prostředí předtím, než ji povolíte ve svém produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="2122b-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="2122b-145">Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="2122b-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="2122b-146">Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní.</span><span class="sxs-lookup"><span data-stu-id="2122b-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="2122b-147">Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu.</span><span class="sxs-lookup"><span data-stu-id="2122b-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="2122b-148">Jakmile se v pracovním prostoru Správa funkcí zobrazí nové funkce, můžete je zapnout.</span><span class="sxs-lookup"><span data-stu-id="2122b-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="2122b-149">Některé funkce mohou být ve výchozím nastavení zapnuty.</span><span class="sxs-lookup"><span data-stu-id="2122b-149">Some features may be on by default.</span></span>

<span data-ttu-id="2122b-150">V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor Správa funkcí).</span><span class="sxs-lookup"><span data-stu-id="2122b-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="2122b-151">Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích.</span><span class="sxs-lookup"><span data-stu-id="2122b-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="2122b-152">Pracovní prostor Správa funkcí označuje, kdy bude funkce náhledu povinná.</span><span class="sxs-lookup"><span data-stu-id="2122b-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="2122b-153">Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání.</span><span class="sxs-lookup"><span data-stu-id="2122b-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="2122b-154">Nemůžete zapínat a vypínat povinné funkce.</span><span class="sxs-lookup"><span data-stu-id="2122b-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="2122b-155">Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.</span><span class="sxs-lookup"><span data-stu-id="2122b-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="2122b-156">Důrazně doporučujeme ověřovat funkce v izolovaném testovacím prostředí nebo ve zkušebním prostředí.</span><span class="sxs-lookup"><span data-stu-id="2122b-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="2122b-157">Nejlepším řešením je vytvořit kopii vašeho aktuálního produkčního prostředí nebo databáze v izolovaném testovacím prostředí (sandbox), tak abyste mohli kompletně vyzkoušet nové funkce na svých datech.</span><span class="sxs-lookup"><span data-stu-id="2122b-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="2122b-158">Další informace o zřizování izolovaného testovacího prostředí naleznete v tématu [Zřízení projektu aplikace Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="2122b-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="2122b-159">Informace o odebrání testovacího prostředí naleznete v tématu [Odebrání instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="2122b-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="2122b-160">Hlášení chyb</span><span class="sxs-lookup"><span data-stu-id="2122b-160">Report bugs</span></span>

<span data-ttu-id="2122b-161">Při testování předběžných verzí funkcí nebo při zkoušení nových funkcí můžete zjistit, že některé položky nefungují dle očekávání.</span><span class="sxs-lookup"><span data-stu-id="2122b-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="2122b-162">Veškeré chyby nahlaste prostřednictvím [podpory služby Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="2122b-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="2122b-163">Viz také</span><span class="sxs-lookup"><span data-stu-id="2122b-163">See also</span></span>

[<span data-ttu-id="2122b-164">Služba Dynamics 365 a plány vydání Power Platform</span><span class="sxs-lookup"><span data-stu-id="2122b-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="2122b-165">Co je nového nebo co se změnilo v aplikaci Human Resource služby Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2122b-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2122b-166">Zásady životního cyklu softwaru</span><span class="sxs-lookup"><span data-stu-id="2122b-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

