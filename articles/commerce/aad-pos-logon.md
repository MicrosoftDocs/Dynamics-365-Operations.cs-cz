---
title: Povolit ověřování Azure Active Directory pro přihlášení POS
description: V tomto tématu je vysvětleno, jak nakonfigurovat přihlašovací prostředí pro Microsoft Dynamics 365 Commerce pokladní místo (POS) tak, aby používalo ověřování Azure Active Directory.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 6946cb5f8bc8aa451f72d1eebcd324f408ad5f7a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975064"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="4b8cc-103">Povolit ověřování Azure Active Directory pro přihlášení POS</span><span class="sxs-lookup"><span data-stu-id="4b8cc-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="4b8cc-104">Mnozí zákazníci, kteří používají Microsoft Dynamics 365 Commerce také používají jiné cloudové služby Microsoft Cloud Service a mohou používat Azure Active Directory (Azure AD) ke správě uživatelských pověření pro tyto služby.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="4b8cc-105">V těchto případech mohou zákazníci chtít použít stejný Azure AD účet napříč aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="4b8cc-106">V tomto tématu je vysvětleno, jak nakonfigurovat přihlašovací prostředí pro pokladní místo (POS) Commerce tak, aby používalo ověřování Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="4b8cc-107">Konfigurace ověřování Azure AD</span><span class="sxs-lookup"><span data-stu-id="4b8cc-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="4b8cc-108">Chcete-li použít Azure AD pro ověřování přihlášení POS pro obchod, je nutné nakonfigurovat nastavení funkčního profilu obchodu a pak tato nastavení aplikovat na klienty POS.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="4b8cc-109">Při konfiguraci nového funkčního profilu postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="4b8cc-110">Přejděte na **Maloobchodní a velkoobchodní prodej** \> **Nastavení kanálu** \> **Nastavení POS** \> **Profily POS** \> **Funkční profily** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles** .</span></span>
1. <span data-ttu-id="4b8cc-111">Vyberte funkční profil, který chcete změnit.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="4b8cc-112">Na pevné záložce **Funkce** v části **přihlášení zaměstnance POS** změňte hodnotu pole **Metoda ověření přihlášení** z **ID a heslo personálu** na **Azure Active Directory** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory** .</span></span>

<span data-ttu-id="4b8cc-113">Všechny funkční profily standardně používají jako metodu ověřování POS **ID a heslo personálu** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="4b8cc-114">Chcete-li tedy použít Azure AD, je nutné změnit hodnotu pole **Metoda ověření přihlášení** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="4b8cc-115">Tato změna ovlivní všechny maloobchodní obchody propojené s vybraným profilem funkčnosti.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="4b8cc-116">Chcete-li použít změny POS, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="4b8cc-117">Přejděte na **Retail a Commerce** \> **IT pro Retail a Commerce** \> **Plán distribuce** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule** .</span></span>
1. <span data-ttu-id="4b8cc-118">Spusťte plán distribuce **1070** ( **Konfigurace kanálu** ).</span><span class="sxs-lookup"><span data-stu-id="4b8cc-118">Run the **1070** ( **Channel configuration** ) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="4b8cc-119">Ověření Azure AD vyžaduje připojení k Internetu.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="4b8cc-120">Pokud je POS v offline režimu, nebude fungovat.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="4b8cc-121">V současné době funkce **Přepsání manažerem** nepodporuje Azure AD jako metodu ověřování.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="4b8cc-122">ID operátora a heslo jsou povinné, i když je řešení Azure AD nakonfigurováno jako metoda ověřování pro přihlášení do POS.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="4b8cc-123">Přiřazení účtu Azure AD k pracovníkovi</span><span class="sxs-lookup"><span data-stu-id="4b8cc-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="4b8cc-124">Dříve, než může pracovník obchodu použít účet Azure AD pro přihlášení k aplikaci POS, musí být tento účet Azure AD přidružen k danému pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="4b8cc-125">Chcete-li účet Azure AD přidružit k pracovníkovi, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="4b8cc-126">Přejděte na **Retail a Commerce** \> **Zaměstnanci** \> **Pracovníci** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-126">Go to **Retail and Commerce** \> **Employees** \> **Workers** .</span></span>
1. <span data-ttu-id="4b8cc-127">Otevře stránku podrobností pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="4b8cc-128">V podokně akcí na kartě **Commerce** ve skupině **Externí identita** zvolte **Přidružit existující identitu** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity** .</span></span>
1. <span data-ttu-id="4b8cc-129">V dialogovém okně **Použít existující externí identitu** vyberte možnost **Hledat pomocí e-mailu** , zadejte e-mailovou adresu Azure AD a pak vyberte možnost **Hledat** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-129">In the **Use existing external identity** dialog box, select **Search using email** , enter an Azure AD email address, and then select **Search** .</span></span>
1. <span data-ttu-id="4b8cc-130">Vyberte požadovaný účet Azure AD a poté vyberte tlačítko **OK** .</span><span class="sxs-lookup"><span data-stu-id="4b8cc-130">Select the Azure AD account that is returned, and then select **OK** .</span></span>

<span data-ttu-id="4b8cc-131">Pole **Alias** , **UPN** a **Externí dílčí identifikátor** na kartě **Commerce** na stránce Podrobnosti pracovníka budou vyplněna.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-131">The **Alias** , **UPN** , and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="4b8cc-132">Po aktualizaci záznamu pracovníka, například pokud je nový Azure AD účet přidružen, změněno heslo nebo aktualizován adresář zaměstnance, doporučujeme spustit rozvrh distribuce **1060** ( **Personál** ) pro synchronizaci nejnovějších informací o personálu s kanálem.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** ( **Staff** ) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="4b8cc-133">Aplikace POS tak může načíst správná data pro ověření uživatele a kontrolu autorizace.</span><span class="sxs-lookup"><span data-stu-id="4b8cc-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b8cc-134">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4b8cc-134">Additional resources</span></span>

[<span data-ttu-id="4b8cc-135">Nastavení funkce rozšířeného přihlášení pro MPOS a Cloud POS</span><span class="sxs-lookup"><span data-stu-id="4b8cc-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="4b8cc-136">Vytvoření funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="4b8cc-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="4b8cc-137"> Konfigurace pracovníka</span><span class="sxs-lookup"><span data-stu-id="4b8cc-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
