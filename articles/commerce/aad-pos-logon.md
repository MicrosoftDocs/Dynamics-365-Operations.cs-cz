---
title: Povolit ověřování Azure Active Directory pro přihlášení POS
description: V tomto tématu je vysvětleno, jak nakonfigurovat přihlašovací prostředí pro Microsoft Dynamics 365 Commerce pokladní místo (POS) tak, aby používalo ověřování Azure Active Directory.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248933"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="5f2b5-103">Povolit ověřování Azure Active Directory pro přihlášení POS</span><span class="sxs-lookup"><span data-stu-id="5f2b5-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="5f2b5-104">Mnozí zákazníci, kteří používají Microsoft Dynamics 365 Commerce také používají jiné cloudové služby Microsoft Cloud Service a mohou používat Azure Active Directory (Azure AD) ke správě uživatelských pověření pro tyto služby.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="5f2b5-105">V těchto případech mohou zákazníci chtít použít stejný Azure AD účet napříč aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="5f2b5-106">V tomto tématu je vysvětleno, jak nakonfigurovat přihlašovací prostředí pro pokladní místo (POS) Commerce tak, aby používalo ověřování Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="5f2b5-107">Konfigurace ověřování Azure AD</span><span class="sxs-lookup"><span data-stu-id="5f2b5-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="5f2b5-108">Chcete-li použít Azure AD pro ověřování přihlášení POS pro obchod, je nutné nakonfigurovat nastavení funkčního profilu obchodu a pak tato nastavení aplikovat na klienty POS.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="5f2b5-109">Při konfiguraci nového funkčního profilu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="5f2b5-110">Přejděte na **Maloobchodní a velkoobchodní prodej** \> **Nastavení kanálu** \> **Nastavení POS** \> **Profily POS** \> **Funkční profily**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="5f2b5-111">Vyberte funkční profil, který chcete změnit.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="5f2b5-112">Na pevné záložce **Funkce** v části **přihlášení zaměstnance POS** změňte hodnotu pole **Metoda ověření přihlášení** z **ID a heslo personálu** na **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="5f2b5-113">Všechny funkční profily standardně používají jako metodu ověřování POS **ID a heslo personálu**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="5f2b5-114">Chcete-li tedy použít Azure AD, je nutné změnit hodnotu pole **Metoda ověření přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="5f2b5-115">Tato změna ovlivní všechny maloobchodní obchody propojené s vybraným profilem funkčnosti.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="5f2b5-116">Chcete-li použít změny POS, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="5f2b5-117">Přejděte na **Retail and Commerce** \> **IT pro Retail and Commerce** \> **Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="5f2b5-118">Spusťte plán distribuce **1070** (**Konfigurace kanálu**).</span><span class="sxs-lookup"><span data-stu-id="5f2b5-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="5f2b5-119">Ověření Azure AD vyžaduje připojení k Internetu.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="5f2b5-120">Pokud je POS v offline režimu, nebude fungovat.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-120">It won't work when POS is in offline mode.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="5f2b5-121">Přiřazení účtu Azure AD k pracovníkovi</span><span class="sxs-lookup"><span data-stu-id="5f2b5-121">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="5f2b5-122">Dříve, než může pracovník obchodu použít účet Azure AD pro přihlášení k aplikaci POS, musí být tento účet Azure AD přidružen k danému pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-122">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="5f2b5-123">Chcete-li účet Azure AD přidružit k pracovníkovi, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-123">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="5f2b5-124">Přejděte na **Retail and Commerce** \> **Zaměstnanci** \> **Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-124">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="5f2b5-125">Otevře stránku podrobností pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-125">Open the details page for a worker.</span></span>
1. <span data-ttu-id="5f2b5-126">V podokně akcí na kartě **Commerce** ve skupině **Externí identita** zvolte **Přidružit existující identitu**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-126">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="5f2b5-127">V dialogovém okně **Použít existující externí identitu** vyberte možnost **Hledat pomocí e-mailu**, zadejte e-mailovou adresu Azure AD a pak vyberte možnost **Hledat**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-127">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="5f2b5-128">Vyberte požadovaný účet Azure AD a poté vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-128">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="5f2b5-129">Pole **Alias**, **UPN** a **Externí dílčí identifikátor** na kartě **Commerce** na stránce Podrobnosti pracovníka budou vyplněna.</span><span class="sxs-lookup"><span data-stu-id="5f2b5-129">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f2b5-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="5f2b5-130">Additional resources</span></span>

[<span data-ttu-id="5f2b5-131">Nastavení funkce rozšířeného přihlášení pro MPOS a Cloud POS</span><span class="sxs-lookup"><span data-stu-id="5f2b5-131">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="5f2b5-132">Vytvoření funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="5f2b5-132">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="5f2b5-133"> Konfigurace pracovníka</span><span class="sxs-lookup"><span data-stu-id="5f2b5-133">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
