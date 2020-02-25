---
title: Správa funkcí
description: Toto téma popisuje, jak může správce povolit funkce náhledu, a uvádí seznam funkcí v aplikaci Microsoft Dynamics 365 Talent, které jsou nyní povoleny pro náhled.
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006419"
---
# <a name="manage-features"></a><span data-ttu-id="9f817-103">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="9f817-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f817-104">V rámci našeho průběžného přidávání schopností cyklu správy lidského kapitálu v aplikaci Microsoft Dynamics 365 Human Resources chceme, aby zákazníci co nejdříve měli k dispozici nové funkce.</span><span class="sxs-lookup"><span data-stu-id="9f817-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="9f817-105">Správci mohou zobrazit a používat funkce náhledu v rámci prostředí.</span><span class="sxs-lookup"><span data-stu-id="9f817-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="9f817-106">Tyto funkce jsou téměř připraveny k obecné dostupnosti a prošly rozsáhlým testováním.</span><span class="sxs-lookup"><span data-stu-id="9f817-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="9f817-107">Právě hledáme další z zpětnou vazbu od zákazníků a ověření před tím, než budou dostupné široké veřejnosti.</span><span class="sxs-lookup"><span data-stu-id="9f817-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="9f817-108">Toto téma popisuje, jak lze povolit funkce náhledu, a uvádí seznam funkcí, které jsou nyní k dispozici pro náhled.</span><span class="sxs-lookup"><span data-stu-id="9f817-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="9f817-109">Tento seznam bude aktualizován s tím, jak budou vydávány nové funkce pro všeobecnou dostupnost a nové funkce, které budou uvolněny k zobrazení náhledu.</span><span class="sxs-lookup"><span data-stu-id="9f817-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="9f817-110">Při uvolnění funkcí k náhledu není vydáno žádné upozornění.</span><span class="sxs-lookup"><span data-stu-id="9f817-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="9f817-111">Uživatelé jen uvidí funkce.</span><span class="sxs-lookup"><span data-stu-id="9f817-111">Users will just start to see the features.</span></span> <span data-ttu-id="9f817-112">Další informace o nových funkcích v aplikaci Talent získáte v části [Co je nového nebo změněného v aplikaci Dynamics 365 Talent](./whats-new.md) a [Poznámky k verzi Dynamics 365 a Power Platform](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="9f817-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="9f817-113">Povolit nebo zakázat funkce náhledu</span><span class="sxs-lookup"><span data-stu-id="9f817-113">Enable or disable preview features</span></span>

<span data-ttu-id="9f817-114">Chcete-li získat přístup k funkcím náhledu, je nutné je nejprve povolit ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="9f817-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="9f817-115">Povolení nebo zakázání funkcí náhledu se vztahuje ke konkrétnímu prostředí.</span><span class="sxs-lookup"><span data-stu-id="9f817-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f817-116">Když zapnete nastavení **Funkce náhledu**, povolíte tím funkce Náhledu pro všechny uživatele ve vaší organizaci, kteří jsou v prostředí.</span><span class="sxs-lookup"><span data-stu-id="9f817-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="9f817-117">Vypnutím nastavení zakážete funkce náhledu a způsobíte, že budou uživatelům nepřístupné.</span><span class="sxs-lookup"><span data-stu-id="9f817-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="9f817-118">Funkce náhledu mají v aplikaci Talent omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="9f817-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="9f817-119">Mohou používat méně opatření pro soukromí a bezpečnostních opatření a nejsou zahrnuty do smlouvy o úrovni služeb (SLA) aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="9f817-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="9f817-120">Neměli byste je používat ke zpracování osobních údajů (to znamená všech informací, které vás mohou identifikovat), nebo ke zpracování jiných dat, které podléhají požadavkům na vyhovění zákonům nebo předpisům.</span><span class="sxs-lookup"><span data-stu-id="9f817-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="9f817-121">Attract</span><span class="sxs-lookup"><span data-stu-id="9f817-121">Attract</span></span>

1. <span data-ttu-id="9f817-122">Přihlaste se do aplikace Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="9f817-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="9f817-123">V nabídce **Nastavení** (symbol ozubeného kola) v pravém horním rohu vyberte **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="9f817-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="9f817-124">Na kartě **Správa funkcí** vyberte možnost vedle položky **náhled funkce**, aby se zbarvila modře a uváděla informaci **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="9f817-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Povolení nebo zákaz ukázkových funkcí v systému Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="9f817-126">Vyberte nebo zrušte výběr jednotlivých funkcí náhledu.</span><span class="sxs-lookup"><span data-stu-id="9f817-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="9f817-127">Pokud neprovedete žádnou akci, budou povoleny všechny funkce náhledu, které jsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="9f817-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="9f817-128">Aktualizujte prohlížeč tak, abyste viděli nové funkce.</span><span class="sxs-lookup"><span data-stu-id="9f817-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="9f817-129">Všichni uživatelé, kteří jsou již přihlášeni, uvidí funkce při příštím přihlášení, nebo mohou aktualizovat svůj prohlížeč, aby funkce viděli okamžitě.</span><span class="sxs-lookup"><span data-stu-id="9f817-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="9f817-130">Některé funkce náhledu mohou vyžadovat další konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="9f817-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="9f817-131">Pomocí odkazů vedle funkce náhledu dokončete její instalaci.</span><span class="sxs-lookup"><span data-stu-id="9f817-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="9f817-132">Zpětná vazba</span><span class="sxs-lookup"><span data-stu-id="9f817-132">Feedback</span></span>

<span data-ttu-id="9f817-133">Rádi bychom se o vás dozvěděli něco o zkušenostech s těmito funkcemi náhledu.</span><span class="sxs-lookup"><span data-stu-id="9f817-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="9f817-134">Doporučujeme vám pravidelně zveřejňovat zpětnou vazbu na následujících webech během používání těchto a dalších funkcí:</span><span class="sxs-lookup"><span data-stu-id="9f817-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="9f817-135">[Komunita](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – tento web je skvělým zdrojem, kde mohou uživatelé diskutovat o případech použití, ptát se a získat nápovědu komunity.</span><span class="sxs-lookup"><span data-stu-id="9f817-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="9f817-136">Dejte nám vědět, jaké funkce chcete zobrazit v produktu nebo o jakýchkoli změnách, které by měly podle vašeho názoru být provedeny u existujících funkcí.</span><span class="sxs-lookup"><span data-stu-id="9f817-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="9f817-137">Pomocí následujících webů navrhujte nápady k produktům:</span><span class="sxs-lookup"><span data-stu-id="9f817-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="9f817-138">Nápady Attract</span><span class="sxs-lookup"><span data-stu-id="9f817-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="9f817-139">Nápady Onboard</span><span class="sxs-lookup"><span data-stu-id="9f817-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="9f817-140">Neuvádějte ve zpětné vazbě nebo recenzích na produkty své osobní údaje (některé informace, které by vás mohly identifikovat).</span><span class="sxs-lookup"><span data-stu-id="9f817-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="9f817-141">Shromážděné informace mohou být dále analyzovány a nebudou použity k odpovídání na žádosti v rámci platných zákonů o ochraně osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="9f817-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="9f817-142">Osobní údaje, které jsou získány samostatně v rámci těchto programů, se řídí [Prohlášením společnosti Microsoft o ochraně osobních údajů](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="9f817-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="9f817-143">Toto téma si uložte do záložek a často se vracejte, abyste měli informace o nových funkcích náhledu, když je vydáme.</span><span class="sxs-lookup"><span data-stu-id="9f817-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f817-144">Viz také</span><span class="sxs-lookup"><span data-stu-id="9f817-144">See also</span></span>

- [<span data-ttu-id="9f817-145">Vyzkoušení nebo nákup aplikací Talent</span><span class="sxs-lookup"><span data-stu-id="9f817-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="9f817-146">Co je nového a co se změnilo v aplikaci Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="9f817-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="9f817-147">Plány vydání</span><span class="sxs-lookup"><span data-stu-id="9f817-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="9f817-148">Získání podpory pro Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="9f817-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
