---
title: Proces aktualizace
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031083"
---
# <a name="update-process"></a><span data-ttu-id="34a26-102">Proces aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-102">Update process</span></span>

<span data-ttu-id="34a26-103">Microsoft Dynamics 365 Human Resources je skutečný software poskytovaný jako služba (SaaS), který poskytuje průběžné a automatické aktualizace.</span><span class="sxs-lookup"><span data-stu-id="34a26-103">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="34a26-104">Tyto aktualizace zahrnují změny aplikace i platformy, které často poskytují klíčová vylepšení služby, včetně pravidelných aktualizací.</span><span class="sxs-lookup"><span data-stu-id="34a26-104">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="34a26-105">Zásady aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-105">Update policy</span></span>

<span data-ttu-id="34a26-106">Aktualizace jsou vydávány v pravidelných intervalech pro všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="34a26-106">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="34a26-107">Aplikace Human Resources je podporována podle [Zásad životního cyklu společnosti Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), které poskytují konzistentní a předpověditelné pokyny pro dostupnost podpory.</span><span class="sxs-lookup"><span data-stu-id="34a26-107">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="34a26-108">Interval vydávání</span><span class="sxs-lookup"><span data-stu-id="34a26-108">Release cadence</span></span>

<span data-ttu-id="34a26-109">Aktualizace aplikace Human Resources se automaticky použijí na všechna prostředí.</span><span class="sxs-lookup"><span data-stu-id="34a26-109">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="34a26-110">Aplikace Human Resources poskytuje dva typy vydání:</span><span class="sxs-lookup"><span data-stu-id="34a26-110">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="34a26-111">**Aktualizace služeb**: Týdenní aktualizace, které zahrnují opravy chyb a nové funkce.</span><span class="sxs-lookup"><span data-stu-id="34a26-111">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="34a26-112">Aktualizace služeb také zahrnují platné aktualizace platformy při jejich vydání.</span><span class="sxs-lookup"><span data-stu-id="34a26-112">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="34a26-113">Chcete-li získat představu o tom, kdy jsou aktualizace platformy vydávány, viz [Tabulku 3: Vydání platformy](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="34a26-113">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="34a26-114">Týdenní aktualizace jsou obvykle vydávány ve středu.</span><span class="sxs-lookup"><span data-stu-id="34a26-114">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="34a26-115">Další informace o týdenních aktualizacích viz [Co je nového a co se změnilo v produktu Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="34a26-115">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="34a26-116">Všechna podporovaná datacentra se aktualizují týdně, není-li uvedeno jinak.</span><span class="sxs-lookup"><span data-stu-id="34a26-116">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="34a26-117">Týdenní aktualizace obvykle začínají ve středu a jsou dokončeny do neděle.</span><span class="sxs-lookup"><span data-stu-id="34a26-117">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="34a26-118">Do týdenních aktualizací jsou zahrnuty USA, Austrálie, Evropa, Spojené království, Asie a Kanada.</span><span class="sxs-lookup"><span data-stu-id="34a26-118">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="34a26-119">**Aktualizace řešení Common Data Service**: Tyto aktualizace se uskutečňují podle potřeby, přibližně jednou za šest týdnů.</span><span class="sxs-lookup"><span data-stu-id="34a26-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="34a26-120">Zahrnují nové entity a změny existujících entit ve službě Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="34a26-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="34a26-121">Tyto aktualizace jsou vydávány pro stejné regiony jako týdenní aktualizace a jejich replikace do všech datacenter trvá přibližně šest týdnů.</span><span class="sxs-lookup"><span data-stu-id="34a26-121">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="34a26-122">Aktualizace řešení mohou nebo nemusí být vydávány současně s týdenními aktualizacemi služeb.</span><span class="sxs-lookup"><span data-stu-id="34a26-122">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="34a26-123">V následující tabulce je uvedena ukázka plánu:</span><span class="sxs-lookup"><span data-stu-id="34a26-123">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="34a26-124">Týden</span><span class="sxs-lookup"><span data-stu-id="34a26-124">Week</span></span> | <span data-ttu-id="34a26-125">Typ aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-125">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="34a26-126">1</span><span class="sxs-lookup"><span data-stu-id="34a26-126">1</span></span> | <span data-ttu-id="34a26-127">Aktualizace služby (všechny regiony)</span><span class="sxs-lookup"><span data-stu-id="34a26-127">Service update (all regions)</span></span> |
| <span data-ttu-id="34a26-128">2</span><span class="sxs-lookup"><span data-stu-id="34a26-128">2</span></span> | <span data-ttu-id="34a26-129">Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 1)</span><span class="sxs-lookup"><span data-stu-id="34a26-129">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="34a26-130">3</span><span class="sxs-lookup"><span data-stu-id="34a26-130">3</span></span> | <span data-ttu-id="34a26-131">Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 2)</span><span class="sxs-lookup"><span data-stu-id="34a26-131">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="34a26-132">4</span><span class="sxs-lookup"><span data-stu-id="34a26-132">4</span></span> | <span data-ttu-id="34a26-133">Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 3)</span><span class="sxs-lookup"><span data-stu-id="34a26-133">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="34a26-134">5</span><span class="sxs-lookup"><span data-stu-id="34a26-134">5</span></span> | <span data-ttu-id="34a26-135">Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 4)</span><span class="sxs-lookup"><span data-stu-id="34a26-135">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="34a26-136">6</span><span class="sxs-lookup"><span data-stu-id="34a26-136">6</span></span> | <span data-ttu-id="34a26-137">Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 5)</span><span class="sxs-lookup"><span data-stu-id="34a26-137">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="34a26-138">7</span><span class="sxs-lookup"><span data-stu-id="34a26-138">7</span></span> | <span data-ttu-id="34a26-139">Aktualizace služby (všechny regiony) + aktualizace řešení (regiony pro týden č. 6)</span><span class="sxs-lookup"><span data-stu-id="34a26-139">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="34a26-140">8</span><span class="sxs-lookup"><span data-stu-id="34a26-140">8</span></span> | <span data-ttu-id="34a26-141">Aktualizace služby (všechny regiony)</span><span class="sxs-lookup"><span data-stu-id="34a26-141">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="34a26-142">Aktualizace řešení jsou po vydání k dispozici ve všech datacentrech.</span><span class="sxs-lookup"><span data-stu-id="34a26-142">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="34a26-143">Pokud nechcete čekat na automatickou replikaci aktualizací, můžete tyto aktualizace provést ručně v jakémkoli prostředí, v libovolném datacentru.</span><span class="sxs-lookup"><span data-stu-id="34a26-143">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="34a26-144">V případě potřeby poskytuje aplikace Human Resources také následující typy oprav:</span><span class="sxs-lookup"><span data-stu-id="34a26-144">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="34a26-145">**Revize (oprava hotfix)**: opravy chyb, které mohou být provedeny buďto současně s vydáním týdenní aktualizace služby, nebo odděleně</span><span class="sxs-lookup"><span data-stu-id="34a26-145">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="34a26-146">**Nouzová oprava**: opravy hotfix prováděné preventivně a v reakci na problém, které jsou svojí povahou samostatné, mohou zahrnovat pouze změny konfigurace nebo změny kódu pro odstranění aktuálních problémů a mohou být prováděny odděleně od vydání týdenní aktualizace služby</span><span class="sxs-lookup"><span data-stu-id="34a26-146">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="34a26-147">Vydání jsou kontrolována, testována a ověřována v interním prostředí.</span><span class="sxs-lookup"><span data-stu-id="34a26-147">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="34a26-148">Po schválení jsou sestavení nasazena do výroby.</span><span class="sxs-lookup"><span data-stu-id="34a26-148">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="34a26-149">Výjimky v roce 2019</span><span class="sxs-lookup"><span data-stu-id="34a26-149">Exceptions in 2019</span></span>

<span data-ttu-id="34a26-150">Následující data představují výjimky z plánu pravidelných vydání:</span><span class="sxs-lookup"><span data-stu-id="34a26-150">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="34a26-151">Datum</span><span class="sxs-lookup"><span data-stu-id="34a26-151">Date</span></span> | <span data-ttu-id="34a26-152">Popis</span><span class="sxs-lookup"><span data-stu-id="34a26-152">Description</span></span> |
| --- | --- |
| <span data-ttu-id="34a26-153">Týden zahrnující 25. listopad</span><span class="sxs-lookup"><span data-stu-id="34a26-153">Week of November 25</span></span> | <span data-ttu-id="34a26-154">Žádné aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-154">No updates</span></span> |
| <span data-ttu-id="34a26-155">Týden zahrnující 16. prosinec</span><span class="sxs-lookup"><span data-stu-id="34a26-155">Week of December 16</span></span> | <span data-ttu-id="34a26-156">Pouze menší aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-156">Minor updates only</span></span> |
| <span data-ttu-id="34a26-157">Týden zahrnující 23. prosinec</span><span class="sxs-lookup"><span data-stu-id="34a26-157">Week of December 23</span></span> | <span data-ttu-id="34a26-158">Žádné aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-158">No updates</span></span> |
| <span data-ttu-id="34a26-159">Týden zahrnující 30. prosinec</span><span class="sxs-lookup"><span data-stu-id="34a26-159">Week of December 30</span></span> | <span data-ttu-id="34a26-160">Žádné aktualizace</span><span class="sxs-lookup"><span data-stu-id="34a26-160">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="34a26-161">Sdělení</span><span class="sxs-lookup"><span data-stu-id="34a26-161">Communications</span></span>

<span data-ttu-id="34a26-162">Zde uvádíme, co bylo provedeno v případě aplikace Human Resources a co jsme vydali v následujících místech:</span><span class="sxs-lookup"><span data-stu-id="34a26-162">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="34a26-163">Dynamics 365 Human Resources plán</span><span class="sxs-lookup"><span data-stu-id="34a26-163">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="34a26-164">Plány vydání Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="34a26-164">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="34a26-165">Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="34a26-165">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="34a26-166">[Hledání problémů ve službě Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (pouze chyby týkající se platformy)</span><span class="sxs-lookup"><span data-stu-id="34a26-166">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="34a26-167">Blog aplikace Human Resources</span><span class="sxs-lookup"><span data-stu-id="34a26-167">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="34a26-168">Komunita aplikace Human Resources v síti Yammer</span><span class="sxs-lookup"><span data-stu-id="34a26-168">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="34a26-169">Ověření předběžných verzí funkcí v izolovaném testovacím prostředí (sandbox)</span><span class="sxs-lookup"><span data-stu-id="34a26-169">Preview features in a sandbox environment</span></span>

<span data-ttu-id="34a26-170">Předběžnou verzi funkcí můžete ověřit v izolovaném testovacím prostředí předtím, než ji povolíte ve svém produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="34a26-170">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="34a26-171">Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="34a26-171">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="34a26-172">Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní.</span><span class="sxs-lookup"><span data-stu-id="34a26-172">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="34a26-173">Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu.</span><span class="sxs-lookup"><span data-stu-id="34a26-173">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="34a26-174">Jakmile se v pracovním prostoru Správa funkcí zobrazí nové funkce, můžete je zapnout.</span><span class="sxs-lookup"><span data-stu-id="34a26-174">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="34a26-175">Některé funkce mohou být ve výchozím nastavení zapnuty.</span><span class="sxs-lookup"><span data-stu-id="34a26-175">Some features may be on by default.</span></span>

<span data-ttu-id="34a26-176">V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor Správa funkcí).</span><span class="sxs-lookup"><span data-stu-id="34a26-176">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="34a26-177">Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích.</span><span class="sxs-lookup"><span data-stu-id="34a26-177">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="34a26-178">Pracovní prostor Správa funkcí označuje, kdy bude funkce náhledu povinná.</span><span class="sxs-lookup"><span data-stu-id="34a26-178">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="34a26-179">Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání.</span><span class="sxs-lookup"><span data-stu-id="34a26-179">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="34a26-180">Nemůžete zapínat a vypínat povinné funkce.</span><span class="sxs-lookup"><span data-stu-id="34a26-180">You can't turn off mandatory features.</span></span> <span data-ttu-id="34a26-181">Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.</span><span class="sxs-lookup"><span data-stu-id="34a26-181">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="34a26-182">Důrazně doporučujeme ověřovat funkce v izolovaném testovacím prostředí nebo ve zkušebním prostředí.</span><span class="sxs-lookup"><span data-stu-id="34a26-182">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="34a26-183">Nejlepším řešením je vytvořit kopii vašeho aktuálního produkčního prostředí nebo databáze v izolovaném testovacím prostředí (sandbox), tak abyste mohli kompletně vyzkoušet nové funkce na svých datech.</span><span class="sxs-lookup"><span data-stu-id="34a26-183">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="34a26-184">Další informace o zřizování izolovaného testovacího prostředí naleznete v tématu [Zřízení projektu aplikace Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="34a26-184">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="34a26-185">Informace o odebrání testovacího prostředí naleznete v tématu [Odebrání instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="34a26-185">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="34a26-186">Hlášení chyb</span><span class="sxs-lookup"><span data-stu-id="34a26-186">Report bugs</span></span>

<span data-ttu-id="34a26-187">Při testování předběžných verzí funkcí nebo při zkoušení nových funkcí můžete zjistit, že některé položky nefungují dle očekávání.</span><span class="sxs-lookup"><span data-stu-id="34a26-187">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="34a26-188">Veškeré chyby nahlaste prostřednictvím [podpory služby Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="34a26-188">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="34a26-189">Viz také</span><span class="sxs-lookup"><span data-stu-id="34a26-189">See also</span></span>

- [<span data-ttu-id="34a26-190">Služba Dynamics 365 a plány vydání Power Platform</span><span class="sxs-lookup"><span data-stu-id="34a26-190">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="34a26-191">Co je nového nebo co se změnilo v aplikaci Human Resource služby Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="34a26-191">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="34a26-192">Zásady životního cyklu softwaru</span><span class="sxs-lookup"><span data-stu-id="34a26-192">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

