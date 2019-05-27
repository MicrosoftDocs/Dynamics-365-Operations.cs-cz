---
title: Publikování pracovních míst z aplikace Attract na externí weby
description: Toto téma vysvětluje postup použití aplikace Dynamics 365 for Talent - Attract pro publikování pracovních míst na externí náborové weby.
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517529"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="9b122-103">Publikování pracovních míst z aplikace Attract na externí weby</span><span class="sxs-lookup"><span data-stu-id="9b122-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b122-104">Chcete dostat své otevřené pozice před co největší množství kvalifikovaných kandidátů.</span><span class="sxs-lookup"><span data-stu-id="9b122-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="9b122-105">Náborové weby, například Broadbean, vám pomohou dosáhnout tohoto cíle.</span><span class="sxs-lookup"><span data-stu-id="9b122-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="9b122-106">Microsoft Dynamics 365 Talent: Attract vám nyní umožní publikovat pracovní místa na Broadbean a Microsoft neustále v této oblasti poskytuje nové nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b122-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="9b122-107">Publikování pracovních míst na Broadbean</span><span class="sxs-lookup"><span data-stu-id="9b122-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="9b122-108">Před publikováním pracovních míst na Broadbean musíte nakonfigurovat integraci Broadbean.</span><span class="sxs-lookup"><span data-stu-id="9b122-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="9b122-109">Chcete-li publikovat pracovní místa na externí weby, musíte mít [doplněk komplexního náboru](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="9b122-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="9b122-110">Tato funkce je aktuálně v náhledu</span><span class="sxs-lookup"><span data-stu-id="9b122-110">This feature is currently in preview.</span></span> <span data-ttu-id="9b122-111">Pokud chcete provést akci, musíte [ji zapnout v nastavení pro správu Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="9b122-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="9b122-112">Konfigurace integrace s Broadbean</span><span class="sxs-lookup"><span data-stu-id="9b122-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="9b122-113">Přihlaste se do aplikace Attract jako správce.</span><span class="sxs-lookup"><span data-stu-id="9b122-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="9b122-114">Zvolte tlačítko **Nastavení** tlačítko (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="9b122-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="9b122-115">Na kartě **Nastavení pracovní vývěsky** v části **Povolit integraci s Broadbean** zapněte integraci.</span><span class="sxs-lookup"><span data-stu-id="9b122-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="9b122-116">Kontaktujte Broadbean a zadejte informace do **uživatelského jména, ID klienta a tokenu šifrování**.</span><span class="sxs-lookup"><span data-stu-id="9b122-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="9b122-117">Vaše přihlašovací údaje do Broadbean jsou citlivé a důvěrné.</span><span class="sxs-lookup"><span data-stu-id="9b122-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="9b122-118">Proto je uchovávejte a sdílejte zodpovědně.</span><span class="sxs-lookup"><span data-stu-id="9b122-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="9b122-119">Tyto údaje může zobrazit kdokoli, kdo má roli správce v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="9b122-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="9b122-120">Společnost Microsoft a Attract nejsou zahrnuty při vytváření a údržbě těchto hodnot.</span><span class="sxs-lookup"><span data-stu-id="9b122-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="9b122-121">Je to vaše zodpovědnost udržovat je v aktuálním stavu v aplikaci Attract a pracovat s Broadbeanem na řešení problémů, které se týkají vašich přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="9b122-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="9b122-122">Publikování pracovního místa na Broadbean</span><span class="sxs-lookup"><span data-stu-id="9b122-122">Post a job to Broadbean</span></span>

<span data-ttu-id="9b122-123">Po zapnutí Broadbean mohou náboroví pracovníci a správci na tomto webu publikovat pracovní místo.</span><span class="sxs-lookup"><span data-stu-id="9b122-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="9b122-124">Pro úlohu musíte mít adresu URL žádosti.</span><span class="sxs-lookup"><span data-stu-id="9b122-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="9b122-125">V aplikaci Attract otevřete práci, kterou chcete publikovat na Broadbean.</span><span class="sxs-lookup"><span data-stu-id="9b122-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="9b122-126">V části **Publikování** zvolte tlačítko **Publikovat nyní**, které odpovídá Broadbeanu.</span><span class="sxs-lookup"><span data-stu-id="9b122-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="9b122-127">Postupujte podle pokynů v okně Broadbean.</span><span class="sxs-lookup"><span data-stu-id="9b122-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="9b122-128">Attract předává Broadbeanu následující informace:</span><span class="sxs-lookup"><span data-stu-id="9b122-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="9b122-129">ID požadavku</span><span class="sxs-lookup"><span data-stu-id="9b122-129">Request ID</span></span>
- <span data-ttu-id="9b122-130">Pracovní titul</span><span class="sxs-lookup"><span data-stu-id="9b122-130">Job title</span></span>
- <span data-ttu-id="9b122-131">Popis úlohy</span><span class="sxs-lookup"><span data-stu-id="9b122-131">Job description</span></span>
- <span data-ttu-id="9b122-132">Místo výkonu práce</span><span class="sxs-lookup"><span data-stu-id="9b122-132">Job location</span></span>
- <span data-ttu-id="9b122-133">URL adresu žádosti</span><span class="sxs-lookup"><span data-stu-id="9b122-133">Apply URL</span></span>
- <span data-ttu-id="9b122-134">Informace náborového pracovníka</span><span class="sxs-lookup"><span data-stu-id="9b122-134">Recruiter information</span></span>

<span data-ttu-id="9b122-135">Po úspěšném dokončení publikace na Broadbeanu zobrazí část práce **Publikování** v aplikaci Attract stav Broadbean jako **Publikováno**.</span><span class="sxs-lookup"><span data-stu-id="9b122-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="9b122-136">Broadbean vyžaduje pole **Obor**.</span><span class="sxs-lookup"><span data-stu-id="9b122-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="9b122-137">Momentálně je toto pole ve výchozím nastavení nastaveno na **IT**.</span><span class="sxs-lookup"><span data-stu-id="9b122-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="9b122-138">Hodnotu však můžete změnit na správné obor v okně pro publikování práce Broadbean.</span><span class="sxs-lookup"><span data-stu-id="9b122-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="9b122-139">Trvá nějakou dobu, než Broadbean dokončí publikování vaší práce na všechny vývěsky, které jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="9b122-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="9b122-140">Proto může dojít k mírnému zpoždění, než Attract poskytne aktualizaci stavu pro práci.</span><span class="sxs-lookup"><span data-stu-id="9b122-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="9b122-141">Zobrazení publikovaného pracovního místa na Broadbeanu</span><span class="sxs-lookup"><span data-stu-id="9b122-141">View a Broadbean job posting</span></span>

<span data-ttu-id="9b122-142">Po publikování pracovního místa ho můžete zobrazit z aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="9b122-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="9b122-143">V aplikaci Attract otevřete práci, kterou chcete zobrazit na Broadbeanu.</span><span class="sxs-lookup"><span data-stu-id="9b122-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="9b122-144">V části **Publikování** zvolte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="9b122-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="9b122-145">Publikování pracovního místa na Broadbeanu se zobrazí v novém okně.</span><span class="sxs-lookup"><span data-stu-id="9b122-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="9b122-146">Aktualizace publikovaného pracovního místa na Broadbeanu</span><span class="sxs-lookup"><span data-stu-id="9b122-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="9b122-147">Je možné aktualizovat publikované pracovní místo na Broadbeanu dvěma způsoby.</span><span class="sxs-lookup"><span data-stu-id="9b122-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="9b122-148">V aplikaci Attract otevřete práci, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="9b122-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="9b122-149">V části **Publikování** zvolte tlačítko **Aktualizovat publikovanou práci**, které odpovídá Broadbeanu.</span><span class="sxs-lookup"><span data-stu-id="9b122-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="9b122-150">Upravte publikované pracovní místo v okně Broadbean.</span><span class="sxs-lookup"><span data-stu-id="9b122-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="9b122-151">- nebo -</span><span class="sxs-lookup"><span data-stu-id="9b122-151">–or–</span></span>

1. <span data-ttu-id="9b122-152">V aplikaci Attract otevřete práci, kterou chcete zobrazit na Broadbeanu.</span><span class="sxs-lookup"><span data-stu-id="9b122-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="9b122-153">V části **Publikování** zvolte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="9b122-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="9b122-154">V okně Broadbean upravte podrobnosti práce a pak ji znovu publikujte.</span><span class="sxs-lookup"><span data-stu-id="9b122-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="9b122-155">Podrobnosti práce v aplikaci Attract se nezmění.</span><span class="sxs-lookup"><span data-stu-id="9b122-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="9b122-156">Odstranění publikovaného pracovního místa na Broadbeanu</span><span class="sxs-lookup"><span data-stu-id="9b122-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="9b122-157">Můžete odstranit publikované pracovní místo z Broadbeanu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="9b122-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="9b122-158">V aplikaci Attract otevřete práci, kterou chcete odstranit.</span><span class="sxs-lookup"><span data-stu-id="9b122-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="9b122-159">V části **Publikování** zvolte tlačítko s třemi tečkami (**...**), které odpovídá Broadbeanu, a poté vyberte **Odstranit publikovanou práci**.</span><span class="sxs-lookup"><span data-stu-id="9b122-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="9b122-160">Poté, co Broadbean odebere práci, bude mít položka Broadbean v aplikaci Attract tlačítko **Publikovat nyní**.</span><span class="sxs-lookup"><span data-stu-id="9b122-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="9b122-161">Přítomnost tohoto tlačítka označuje, že práce byla odstraněna a lze ji znovu publikovat.</span><span class="sxs-lookup"><span data-stu-id="9b122-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="9b122-162">Řešení problémů s integrací s Broadbean</span><span class="sxs-lookup"><span data-stu-id="9b122-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="9b122-163">Pokud máte problémy s publikováním pracovního místa na Broadbean, vyzkoušejte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="9b122-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="9b122-164">Ověřte, zda jsou přihlašovací údaje Broadbean, které jste zadali v aplikaci Attract, platné a správné.</span><span class="sxs-lookup"><span data-stu-id="9b122-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="9b122-165">Pokud jsou přihlašovací údaje platné a správné, kontaktujte [Broadbean podporu](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="9b122-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="9b122-166">Pokud problém přetrvává, obraťte se na [podporu společnosti Microsoft](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="9b122-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
