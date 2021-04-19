---
title: Nastavení mobilního pracovního prostoru správy majetku
description: Toto téma popisuje, jak nastavit mobilní aplikace Microsoft Dynamics 365 Supply Chain Management a Finance and Operations (Dynamics 365) pro spuštění mobilního pracovního prostoru Asset management, který mohou pracovníci použít k provádění úkolů správy majetku.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837770"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="cf03e-103">Nastavení mobilního pracovního prostoru správy majetku</span><span class="sxs-lookup"><span data-stu-id="cf03e-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf03e-104">Toto téma popisuje, jak nastavit mobilní aplikace Microsoft Dynamics 365 Supply Chain Management a Finance and Operations (Dynamics 365) ke správě mobilního pracovního prostoru **Správa majetku**, který mohou pracovníci používat k provádění úkolů správy majetku.</span><span class="sxs-lookup"><span data-stu-id="cf03e-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="cf03e-105">Nastavení uživatelů pracovníků údržby v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cf03e-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="cf03e-106">Pro každého uživatele, který vyžaduje přístup do mobilního pracovního prostoru **Správa majetku**, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="cf03e-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="cf03e-107">V části Supply Chain Management přejděte na **Lidské zdroje \> Pracovníci** a ujistěte se, že existuje pracovní záznam pro uživatele, kterého chcete nastavit.</span><span class="sxs-lookup"><span data-stu-id="cf03e-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="cf03e-108">Podle potřeby vytvořte nový záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="cf03e-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="cf03e-109">Jděte na **Správa majetku \> Nastavení \> Pracovníci \> Pracovníci** a ujistěte se, že je záznam pracovníka, který jste identifikovali (nebo vytvořili) v předchozím kroku, je namapován na záznam pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="cf03e-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="cf03e-110">Podle potřeby vytvořte nový záznam pracovníka údržby a nastavte pole **Pracovník** na záznam pracovníka z předchozího kroku.</span><span class="sxs-lookup"><span data-stu-id="cf03e-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="cf03e-111">Jděte na **Správa majetku \> Nastavení \> Pracovníci \> Skupina pracovníků údržby** a ujistěte se, že záznam pracovníka údržby, který jste identifikovali (nebo vytvořili) v předchozím kroku, patří do skupiny pracovníků údržby.</span><span class="sxs-lookup"><span data-stu-id="cf03e-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="cf03e-112">Přejděte do nabídky **Správa systému \> Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="cf03e-113">Vyberte relevantního uživatele v mřížce.</span><span class="sxs-lookup"><span data-stu-id="cf03e-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="cf03e-114">Na kartě s náhledem **Detaily uživatele** nastavte pole **Osoba** na pracovní účet, který chcete přidružit k aktuálnímu uživatelskému účtu.</span><span class="sxs-lookup"><span data-stu-id="cf03e-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="cf03e-115">Tento pracovní účet by měl být pracovním záznamem, který jste identifikovali (nebo vytvořili) v kroku 1 a namapovali na záznam pracovníka údržby v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="cf03e-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="cf03e-116">Na funkce systému Windows se vztahují uživatelská oprávnění a role zabezpečení mobilního pracovního prostoru **Správa majetku**, stejně jako se vztahují na funkce uživatelského rozhraní Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf03e-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="cf03e-117">Proto musí každý uživatel, kterého jste nastavili pro přístup do mobilního pracovního prostoru **Správa majetku**, mít role zabezpečení, které jsou vyžadovány k provádění podobných operací přímo ve správě dodavatelského řetězce.</span><span class="sxs-lookup"><span data-stu-id="cf03e-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="cf03e-118">Publikování mobilního pracovního prostoru správy majetku</span><span class="sxs-lookup"><span data-stu-id="cf03e-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="cf03e-119">Pro zpřístupnění funkcí správy aktiv v mobilní aplikaci Finance and Operations (Dynamics 365) musíte publikovat mobilní pracovní prostor **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="cf03e-120">V části Supply Chain Management vyberte tlačítko **Nastavení** (symbol ozubeného kola v pravém horním rohu) a poté v nabídce vyberte **Mobilní aplikace**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="cf03e-121">V dialogovém okně **Spravovat mobilní aplikaci** najděte dlaždici **Správa majetku**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="cf03e-122">Pokud obsahuje text „V metadatech - nepublikováno,“ pracovní prostor ještě nebyl publikován.</span><span class="sxs-lookup"><span data-stu-id="cf03e-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="cf03e-123">Pokud obsahuje text „V metadatech - publikováno,“ pracovní prostor již byl publikován a zbytek tohoto postupu můžete přeskočit.</span><span class="sxs-lookup"><span data-stu-id="cf03e-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="cf03e-124">![Dialogové okno Správa mobilní aplikace](media/mobile-workspaces.png "Dialogové okno Správa mobilní aplikace")</span><span class="sxs-lookup"><span data-stu-id="cf03e-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="cf03e-125">Vyberte dlaždici **Správa majetku** a poté vyberte **Publikovat** na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="cf03e-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="cf03e-126">Po několika sekundách byste měli obdržet oznámení, které uvádí, že pracovní prostor byl úspěšně publikován.</span><span class="sxs-lookup"><span data-stu-id="cf03e-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="cf03e-127">Text na dlaždici by se měl navíc změnit na „V metadatech - publikováno“.</span><span class="sxs-lookup"><span data-stu-id="cf03e-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="cf03e-128">Nainstalujte a nastavte mobilní aplikaci Finance and Operations (Dynamics 365)</span><span class="sxs-lookup"><span data-stu-id="cf03e-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="cf03e-129">Chcete-li nainstalovat **Microsoft Finance and Operations (Dynamics 365)**, přejděte do jednoho z následujících obchodů s aplikacemi na vašem mobilním zařízení:</span><span class="sxs-lookup"><span data-stu-id="cf03e-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="cf03e-130">Pro zařízení Google Android</span><span class="sxs-lookup"><span data-stu-id="cf03e-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="cf03e-131">Pro zařízení Apple iOS</span><span class="sxs-lookup"><span data-stu-id="cf03e-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="cf03e-132">Otevřete aplikaci Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="cf03e-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="cf03e-133">Měla by se zobrazit přihlašovací stránka.</span><span class="sxs-lookup"><span data-stu-id="cf03e-133">The sign-in page should appear.</span></span> <span data-ttu-id="cf03e-134">Do pole **Přihlásit se** zadejte adresu URL pro správu dodavatelského řetězce nebo vyberte poslední adresu URL v seznamu **Nedávná prostředí** a potom klepněte na **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="cf03e-135">![Přihlašovací stránka](media/mobile-app-sign-in.png "Přihlašovací stránka")</span><span class="sxs-lookup"><span data-stu-id="cf03e-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="cf03e-136">Pokud se zobrazí výzva k potvrzení připojení, zaškrtněte políčko **Rozumím** a potom klepněte na **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="cf03e-137">Na stránce **Vyberte účet** použijte svůj účet Microsoft k přihlášení do mobilní aplikace.</span><span class="sxs-lookup"><span data-stu-id="cf03e-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="cf03e-138">Zobrazí se stránka **Pracovní prostory**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="cf03e-139">Uvádí seznam všech mobilních pracovních prostorů, které byly publikovány vaší instancí Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf03e-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="cf03e-140">![Seznam pracovních prostorů](media/mobile-app-workspaces.png "Seznam pracovních prostorů")</span><span class="sxs-lookup"><span data-stu-id="cf03e-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="cf03e-141">Pokud musíte změnit právnickou osobu (společnost), klepněte na tlačítko Nabídka (někdy označované jako hamburger nebo hamburgerové tlačítko) v levém horním rohu a poté klepněte na **Změnit společnost**.</span><span class="sxs-lookup"><span data-stu-id="cf03e-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="cf03e-142">![Změna právnické osoby.](media/mobile-app-change-comp.png "Změna právnické osoby.")</span><span class="sxs-lookup"><span data-stu-id="cf03e-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="cf03e-143">Na stránce **Pracovní prostory** vyberte pracovní prostor, se kterým chcete pracovat, a otevřete jej.</span><span class="sxs-lookup"><span data-stu-id="cf03e-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="cf03e-144">![Mobilní pracovní prostor správy majetku](media/mobile-app-asset-workspace.png "Mobilní pracovní prostor správy majetku")</span><span class="sxs-lookup"><span data-stu-id="cf03e-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="cf03e-145">Práce s mobilním pracovním prostorem správy majetku</span><span class="sxs-lookup"><span data-stu-id="cf03e-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="cf03e-146">Další informace o tom, jak pracovat s mobilním pracovním prostorem **Správa majetku**, získáte v tématu [Použití mobilního pracovního prostoru Správa majetku](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="cf03e-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="cf03e-147">Více informací o mobilní aplikaci Finance and Operations (Dynamics 365) získáte v tématu [Domovská stránka mobilní aplikace](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="cf03e-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]