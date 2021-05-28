---
title: Povolení integrace Dynamics 365 Commerce a Microsoft Teams
description: Toto téma popisuje, jak povolit integraci Microsoft Dynamics 365 Commerce a Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019828"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="05dba-103">Povolení integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="05dba-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05dba-104">Toto téma popisuje, jak povolit integraci Microsoft Dynamics 365 Commerce a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="05dba-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="05dba-105">Chcete-li zřídit Teams s informacemi z Dynamics 365 Commerce a synchronizovat funkce správy úkolů mezi Teams a aplikací POS (point of sale), musíte povolit integrační funkce v Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="05dba-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="05dba-106">Když povolíte integraci Teams, souhlasíte se sdílením svých dat s Teams.</span><span class="sxs-lookup"><span data-stu-id="05dba-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="05dba-107">Data sdílená s Teams se mohou nacházet v jiné zemi než vaše data aplikace Commerce a mohou podléhat různým standardům dodržování předpisů.</span><span class="sxs-lookup"><span data-stu-id="05dba-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="05dba-108">Další informace naleznete v tématu [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="05dba-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="05dba-109">Informace o zásadách ochrany osobních údajů společnosti Microsoft najdete v [Prohlášení společnosti Microsoft o ochraně osobních údajů](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="05dba-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="05dba-110">Povolení integrace Teams</span><span class="sxs-lookup"><span data-stu-id="05dba-110">Enable Teams integration</span></span>

<span data-ttu-id="05dba-111">Než budete moci povolit integraci Microsoft Teams s aplikací Commerce, musíte zaregistrovat aplikaci Teams se svým klientem na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="05dba-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="05dba-112">Pokud chcete zaregistrovat aplikaci Teams se svým klientem na portálu Azure, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="05dba-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="05dba-113">Postupujte podle pokynů v části [Rychlý start: registrace aplikace pomocí platformy identity Microsoft](/azure/active-directory/develop/quickstart-register-app) k registraci aplikace Teams se svým klientem na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="05dba-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="05dba-114">Zkopírujte hodnotu **ID aplikace (klienta)** ze stránky **Přehled** pro registrovanou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="05dba-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="05dba-115">Tuto hodnotu použijete k povolení integrace Teams v Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="05dba-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="05dba-116">Zkopírujte hodnotu certifikátu, která byla zadána, když jste [přidali certifikát](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) v kroku 1.</span><span class="sxs-lookup"><span data-stu-id="05dba-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="05dba-117">Certifikát je také známý jako veřejný klíč nebo klíč aplikace.</span><span class="sxs-lookup"><span data-stu-id="05dba-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="05dba-118">Tuto hodnotu použijete k povolení integrace Teams v Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="05dba-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="05dba-119">Chcete-li povolit integraci Teams v Commerce Headquarters, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="05dba-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="05dba-120">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="05dba-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="05dba-121">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="05dba-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="05dba-122">Nastavte možnost **Povolit integraci Microsoft Teams** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="05dba-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="05dba-123">V polích **ID aplikace** a **Klíč aplikace** zadejte hodnoty, které jste získali při registraci aplikace Teams na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="05dba-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="05dba-124">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="05dba-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="05dba-125">Následující obrázek ukazuje příklad konfigurace integrace Teams v Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="05dba-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Konfigurace integrace Teams v Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="05dba-127">Zákaz integrace Teams</span><span class="sxs-lookup"><span data-stu-id="05dba-127">Disable Teams integration</span></span>

<span data-ttu-id="05dba-128">Chcete-li zakázat integraci Microsoft Teams v Commerce Headquarters, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="05dba-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="05dba-129">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="05dba-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="05dba-130">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="05dba-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="05dba-131">Nastavte možnost **Povolit integraci Microsoft Teams** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="05dba-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="05dba-132">Vymažte hodnoty z polí **ID aplikace** a **Klíč aplikace**.</span><span class="sxs-lookup"><span data-stu-id="05dba-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="05dba-133">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="05dba-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="05dba-134">Po zákazu integrace Teams s Commerce již POS terminály nebudou zobrazovat úkoly, které jsou publikovány z aplikace Teams.</span><span class="sxs-lookup"><span data-stu-id="05dba-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05dba-135">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="05dba-135">Additional resources</span></span>

[<span data-ttu-id="05dba-136">Přehled integrace Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="05dba-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="05dba-137">Zřízení Microsoft Teams z Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="05dba-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="05dba-138">Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="05dba-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="05dba-139">Správa uživatelských rolí v Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="05dba-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="05dba-140">Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy</span><span class="sxs-lookup"><span data-stu-id="05dba-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="05dba-141">Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="05dba-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)