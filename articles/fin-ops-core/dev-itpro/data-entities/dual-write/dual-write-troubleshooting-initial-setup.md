---
title: Poradce při potížích s počáteční instalací
description: Toto téma obsahuje informace, které vám mohou pomoci vyřešit problémy, které mohou nastat při počátečním nastavení integrace dvojího zápisu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9ffb1378eccf175fbb9bd84228f91ba606125a63
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753983"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="8ec07-103">Poradce při potížích s počáteční instalací</span><span class="sxs-lookup"><span data-stu-id="8ec07-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="8ec07-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8ec07-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="8ec07-105">Konkrétně obsahuje informace, které vám mohou pomoci vyřešit problémy, které mohou nastat při počátečním nastavení integrace dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ec07-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8ec07-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="8ec07-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="8ec07-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="8ec07-108">Nemůžete propojit aplikaci Finance and Operations s Dataverse</span><span class="sxs-lookup"><span data-stu-id="8ec07-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="8ec07-109">**Požadovaná role pro nastavení dvojitého zápisu:** Správce systému v aplikacích Finance and Operations a prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8ec07-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="8ec07-110">Chyby na stránce **Nastavení odkazu na Dataverse** jsou obvykle způsobeny neúplnými problémy s nastavením nebo oprávněními.</span><span class="sxs-lookup"><span data-stu-id="8ec07-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="8ec07-111">Zajistěte, aby celá kontrola stavu prošla na stránce **Nastavení odkazu na Dataverse**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="8ec07-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="8ec07-112">Nemůžete propojit dvojí zapisování, pokud celý stav nepřechází na kontrolu stavu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-112">You can't link dual-write unless the whole health check passes.</span></span>

![Úspěšná kontrola stavu](media/health_check.png)

<span data-ttu-id="8ec07-114">Musíte mít pověření správce klienta Azure AD, chcete-li propojit prostředí Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8ec07-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="8ec07-115">Po propojení prostředí se uživatelé mohou přihlásit pomocí svých pověření účtu a aktualizovat existující mapu tabulek.</span><span class="sxs-lookup"><span data-stu-id="8ec07-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="8ec07-116">Chyba při otevření odkazu na stránku Dataverse</span><span class="sxs-lookup"><span data-stu-id="8ec07-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="8ec07-117">**Požadovaná pověření pro opravu problému:** Správce klienta Azure AD</span><span class="sxs-lookup"><span data-stu-id="8ec07-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="8ec07-118">Může se zobrazit následující chybová zpráva při otevření stránky **Odkaz na Dataverse** v aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8ec07-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="8ec07-119">*Stavový kód odpovědi neoznačuje úspěch: 404 (Nenalezeno).*</span><span class="sxs-lookup"><span data-stu-id="8ec07-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="8ec07-120">K této chybě dojde v případě, že nedojde k dokončení kroku souhlasu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="8ec07-121">Chcete-li ověřit, zda byl krok souhlasu vyplněn, přihlaste se k portal.Azure.com pomocí účtu správce klienta Azure AD a zjistěte, zda se aplikace třetí strany s ID **33976c19-1db5-4c02-810e-c243db79efde** zobrazí v seznamu Azure AD **Podnikové aplikace**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="8ec07-122">Pokud tomu tak není, musíte zadat souhlas s aplikací.</span><span class="sxs-lookup"><span data-stu-id="8ec07-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="8ec07-123">Chcete-li poskytnout souhlas s aplikací, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8ec07-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="8ec07-124">Otevřete následující adresu URL pomocí vašich pověření správce.</span><span class="sxs-lookup"><span data-stu-id="8ec07-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="8ec07-125">Měli byste být vyzváni k zadání souhlasu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="8ec07-126">Výběrem **Přijmout** označíte, že udělujete souhlas s instalací aplikace, která má ID **33976c19-1db5-4c02-810e-c243db79efde** ve vašem klientovi.</span><span class="sxs-lookup"><span data-stu-id="8ec07-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="8ec07-127">Tato aplikace je požadována pro propojení aplikací Dataverse a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8ec07-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="8ec07-128">Pokud máte s tímto krokem potíže, otevřete prohlížeč v anonymním režimu (v aplikaci Google Chrome) nebo v režimu InPrivate (v Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="8ec07-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="8ec07-129">Ověřte, zda jsou při propojování správně nastaveny data společnosti a týmy s duálním zápisem</span><span class="sxs-lookup"><span data-stu-id="8ec07-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="8ec07-130">Chcete-li zajistit správnou funkci dvojího zapisování, budou v prostředí Dataverse vytvořeny společnosti, které vyberete během konfigurace.</span><span class="sxs-lookup"><span data-stu-id="8ec07-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="8ec07-131">Ve výchozím nastavení jsou tyto společnosti určeny jen pro čtení a vlastnost **IsDualWriteEnable** je nastavena na **True**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="8ec07-132">Kromě toho se vytvoří výchozí vlastník organizační jednotky a tým, který obsahuje název společnosti.</span><span class="sxs-lookup"><span data-stu-id="8ec07-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="8ec07-133">Před povolením map se ujistěte, zda je zadán výchozí vlastník týmu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="8ec07-134">Chcete-li najít tabulku **Společnosti (CDM\_Společnost)**, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="8ec07-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="8ec07-135">V aplikaci řízené modelem v produktu Dynamics 365 vyberte filtr v pravém horním rohu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="8ec07-136">V rozevíracím seznamu vyberte **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="8ec07-137">Výsledky zobrazíte výběrem možnosti **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="8ec07-138">Vyberte společnost, která byla propojena při konfiguraci dvojího přepisu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="8ec07-139">Ověřte, zda má sloupec **Výchozí vlastnící tým** hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8ec07-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="8ec07-140">Na následujícím obrázku je sloupec **Výchozí vlastnící tým** nastaveno na **USMF dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Ověřování výchozího vlastnícího týmu](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="8ec07-142">Najít limit počtu právnických osob nebo společností, které lze propojit s dvojím zapisováním</span><span class="sxs-lookup"><span data-stu-id="8ec07-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="8ec07-143">Při pokusu o povolení map se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="8ec07-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="8ec07-144">*Chyba dvojího zápisu – registrace modulu plug-in se nezdařila: \[(nelze získat mapu oddílu pro projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Chyba překračuje maximální počet povolených oddílů pro mapování DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\]. došlo k jedné nebo více chybám.*</span><span class="sxs-lookup"><span data-stu-id="8ec07-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="8ec07-145">Aktuální limit při propojení prostředí je přibližně 40 právnických osob.</span><span class="sxs-lookup"><span data-stu-id="8ec07-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="8ec07-146">K této chybě dojde, pokud se pokusíte povolit mapy a mezi prostředími je propojeno více než 40 právnických osob.</span><span class="sxs-lookup"><span data-stu-id="8ec07-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]