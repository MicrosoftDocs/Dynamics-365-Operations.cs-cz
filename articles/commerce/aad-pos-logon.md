---
title: Konfigurace ověření Azure Active Directory pro přihlášení do POS
description: Toto téma vysvětluje, jak konfigurovat Azure Active Directory jako metodu ověřování v místě prodeje Microsoft Dynamics 365 Commerce.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
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
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937451"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="289ed-103">Konfigurace ověření Azure Active Directory pro přihlášení do POS</span><span class="sxs-lookup"><span data-stu-id="289ed-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="289ed-104">Toto téma vysvětluje, jak konfigurovat Azure Active Directory (Azure AD) jako metodu ověřování v místě prodeje (POS) Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="289ed-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="289ed-105">Maloobchodníci, kteří používají Dynamics 365 Commerce spolu s dalšími cloudovými službami společnosti Microsoft, jako je Microsoft Azure, Microsoft 365 a Microsoft Teams, obvykle chtějí použít Azure AD pro centralizovanou správu pověření uživatele pro bezpečné a bezproblémové přihlašování mezi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="289ed-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="289ed-106">Chcete-li použít ověřování Azure AD pro Commerce POS, musíte nejprve nakonfigurovat Azure AD jako metodu ověřování v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="289ed-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="289ed-107">Konfigurace metody ověřování POS</span><span class="sxs-lookup"><span data-stu-id="289ed-107">Configure POS authentication method</span></span>

<span data-ttu-id="289ed-108">Konfiguraci metody ověřování POS v centrále Commerce provedete následovně.</span><span class="sxs-lookup"><span data-stu-id="289ed-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="289ed-109">Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily** a zvolte profil funkcí, který chcete změnit.</span><span class="sxs-lookup"><span data-stu-id="289ed-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="289ed-110">V části **Přihlášení zaměstnanců POS** rychlé karty **Funkce** vyberte požadovanou možnost metody ověřování z rozbalovacího seznamu **Metoda ověřování přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="289ed-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="289ed-111">**Metoda ověřování přihlášení** má tři možnosti:</span><span class="sxs-lookup"><span data-stu-id="289ed-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="289ed-112">**ID pracovníka a heslo** – Tato výchozí možnost vyžaduje, aby uživatelé POS zadali osobní ID a heslo pro přihlášení k POS a pro přístup k funkcím přepsání správce.</span><span class="sxs-lookup"><span data-stu-id="289ed-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="289ed-113">**Azure AD bez jednotného přihlášení** – Tato možnost vyžaduje, aby uživatelé POS používali přihlašovací údaje Azure AD pro přihlášení do POS a přístupu k funkci přepsání správce.</span><span class="sxs-lookup"><span data-stu-id="289ed-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="289ed-114">Když je POS klient obnoven nebo znovu otevřen, musí uživatel POS znovu zadat přihlašovací údaje Azure AD pro opětovné přihlášení.</span><span class="sxs-lookup"><span data-stu-id="289ed-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="289ed-115">**Azure AD s jednotným přihlášením** – Když je vybrána tato možnost, uživatelé POS se mohou přihlásit do cloudového POS (CPOS) pomocí aktivních přihlašovacích údajů Azure AD, které používají jiné webové aplikace ve stejném webovém prohlížeči, nebo se přihlásí pomocí Modern POS (MPOS) pomocí přihlašovacích údajů Azure AD přihlášených k systému Windows.</span><span class="sxs-lookup"><span data-stu-id="289ed-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="289ed-116">Obě metody umožňují přihlášení bez nutnosti zadávat přihlašovací údaje Azure AD na přihlašovací obrazovce POS.</span><span class="sxs-lookup"><span data-stu-id="289ed-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="289ed-117">Přístup k funkci přepsání správce POS však bude i nadále vyžadovat přihlášení pomocí přihlašovacích údajů Azure AD.</span><span class="sxs-lookup"><span data-stu-id="289ed-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="289ed-118">Přejděte na **Retail a Commerce > IT Retail a Commerce IT > Distribuční plán** a spusťte úlohu **1070 (konfigurace kanálu)** k synchronizaci nejnovějšího nastavení profilu funkce s klienty POS.</span><span class="sxs-lookup"><span data-stu-id="289ed-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="289ed-119">Možnost metody ověřování **Azure AD bez jednotného přihlášení** nahrazuje možnost **Azure Active Directory** v Commerce verzi 10.0.18 a starší.</span><span class="sxs-lookup"><span data-stu-id="289ed-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="289ed-120">ověřování Azure AD vyžaduje aktivní připojení k internetu a nebude fungovat, když je POS offline.</span><span class="sxs-lookup"><span data-stu-id="289ed-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="289ed-121">Přidružení účtů Azure AD s uživateli POS</span><span class="sxs-lookup"><span data-stu-id="289ed-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="289ed-122">Chcete-li použít Azure AD jako metodu ověřování POS, musíte přidružit účty Azure AD s uživateli POS v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="289ed-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="289ed-123">Chcete-li přidružit účty Azure AD s uživateli POS v ústředí Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="289ed-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="289ed-124">Přejděte na **Retail a Commerce > Zaměstnanci> Pracovníci** a otevřete záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="289ed-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="289ed-125">V podokně akcí vyberte kartu **Commerce** poté ve skupině **Externí identita** zvolte **Přidružit existující identitu**.</span><span class="sxs-lookup"><span data-stu-id="289ed-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="289ed-126">V dialogovém okně **Použít existující externí identitu** vyberte možnost **Hledat pomocí e-mailu**, zadejte e-mailovou adresu Azure AD a pak vyberte možnost **Hledat**.</span><span class="sxs-lookup"><span data-stu-id="289ed-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="289ed-127">Vyberte požadovaný účet Azure AD a poté vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="289ed-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="289ed-128">Po provedení výše uvedeného postupu konfigurace Pole **Alias**, **UPN** a **Externí dílčí identifikátor** na kartě **Commerce** na stránce Podrobnosti pracovníka budou vyplněna.</span><span class="sxs-lookup"><span data-stu-id="289ed-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="289ed-129">Musíte spustit úlohu **1060 (zaměstnanci)** v **Retail a Commerce > IT Retail a Commerce > Distribuční plán** k synchronizaci nejnovějšího uživatele POS a dat účtu Azure AD do kanálu.</span><span class="sxs-lookup"><span data-stu-id="289ed-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="289ed-130">Jako osvědčený postup je po aktualizací údajů o pracovníkovi, jako je heslo, oprávnění POS, přidružený účet Azure AD nebo adresář zaměstnance, v centrále Commerce, je velmi doporučeno spustit úlohu **1060 (zaměstnanci)** pro synchronizaci nejnovějších informací o pracovníkovi s kanálem.</span><span class="sxs-lookup"><span data-stu-id="289ed-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="289ed-131">Klient POS pak může načíst správná data pro ověření uživatele a kontrolu autorizace.</span><span class="sxs-lookup"><span data-stu-id="289ed-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="289ed-132">Odhlášení od pokladny POS a odhlášení pomocí ověřování Azure AD</span><span class="sxs-lookup"><span data-stu-id="289ed-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="289ed-133">Když je POS nakonfigurován pro použití metody ověřování Azure AD, dojde k následujícímu:</span><span class="sxs-lookup"><span data-stu-id="289ed-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="289ed-134">Funkce **Uzamknout pokladnu** nebude v aplikaci POS k dispozici.</span><span class="sxs-lookup"><span data-stu-id="289ed-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="289ed-135">Funkce **Automaticky uzamknout** se bude chovat stejně jako funkce **Automatické odhlášení**.</span><span class="sxs-lookup"><span data-stu-id="289ed-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="289ed-136">Pokud uživatel POS zvolí **Odhlásit se**, bude uživatel vyzván k přihlášení pomocí přihlašovacích údajů Azure AD při příštím spuštění POS, bez ohledu na to, zda je povoleno jednotné přihlášení.</span><span class="sxs-lookup"><span data-stu-id="289ed-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="289ed-137">Funkce přepsání správce pomocí ověřování Azure AD</span><span class="sxs-lookup"><span data-stu-id="289ed-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="289ed-138">Když je POS nakonfigurován k použití ověřování Azure AD, funkce přepsání správce otevře dialogové okno s výzvou pro zadání přihlašovacích údajů uživatele správce Azure AD.</span><span class="sxs-lookup"><span data-stu-id="289ed-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="289ed-139">Po schválení přihlášení správce budou přihlašovací údaje Azure AD správce zrušena a přihlašovací údaje předchozího uživatele Azure AD budou použita pro následné operace POS.</span><span class="sxs-lookup"><span data-stu-id="289ed-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="289ed-140">V Commerce verzí 10.0.18 a starších nepodporuje funkce přepsání správce Azure AD.</span><span class="sxs-lookup"><span data-stu-id="289ed-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="289ed-141">ID pracovníka a heslo jsou povinné, i když je POS nakonfigurována na použití metody ověřování Azure AD.</span><span class="sxs-lookup"><span data-stu-id="289ed-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="289ed-142">Pokud používáte CPOS s webovým prohlížečem Safari na zařízení Apple iOS, musíte nejprve vypnout **Blokovat vyskakovací okna** v nastavení Safari, aby přepsání funkcí správce fungovalo s ověřováním Azure AD.</span><span class="sxs-lookup"><span data-stu-id="289ed-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="289ed-143">Osvědčené postupy zabezpečení pro ověřování POS na základě Azure AD na sdílených zařízeních</span><span class="sxs-lookup"><span data-stu-id="289ed-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="289ed-144">Mnoho maloobchodníků nastavuje prostředí maloobchodních prodejen tak, aby více uživatelů potřebovalo přístup k aplikaci POS ze sdíleného fyzického zařízení.</span><span class="sxs-lookup"><span data-stu-id="289ed-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="289ed-145">V tomto kontextu, zatímco jednotné přihlášení poskytuje pohodlné a bezproblémové ověřování, může také vytvořit bezpečnostní mezeru, kde si aktuální uživatel POS nemusí uvědomit, že při provádění transakcí nebo operací v POS se používají přihlašovací údaje jiného uživatele.</span><span class="sxs-lookup"><span data-stu-id="289ed-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="289ed-146">Před konfigurací POS pro použití metody ověřování Azure AD důrazně doporučujeme zkontrolovat zásady zabezpečení a nastavení přihlášení sdíleného zařízení a rozhodnout, která možnost je nejvhodnější.</span><span class="sxs-lookup"><span data-stu-id="289ed-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="289ed-147">Pokud vaše maloobchodní prostředí používá pro přihlášení fyzického zařízení sdílený účet (například místní účet), doporučuje se použít možnost **Azure AD bez jednotného přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="289ed-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="289ed-148">Tím je zajištěno, že každý uživatel POS výslovně zadává přihlašovací údaje Azure AD pro přihlášení k POS.</span><span class="sxs-lookup"><span data-stu-id="289ed-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="289ed-149">Pokud vaše prostředí maloobchodu vyžaduje, aby zaměstnanci používali své vlastní účty Azure AD pro přihlášení k POS a hostuje fyzické zařízení, doporučuje se použít možnost **Azure AD s jednotným přihlášením**.</span><span class="sxs-lookup"><span data-stu-id="289ed-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="289ed-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="289ed-150">Additional resources</span></span>

[<span data-ttu-id="289ed-151"> Konfigurace pracovníka</span><span class="sxs-lookup"><span data-stu-id="289ed-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="289ed-152">Vytvoření funkčního profilu maloobchodu</span><span class="sxs-lookup"><span data-stu-id="289ed-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="289ed-153">Nastavení funkce rozšířeného přihlášení pro MPOS a Cloud POS</span><span class="sxs-lookup"><span data-stu-id="289ed-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="289ed-154">Osvědčené postupy zabezpečení pro Cloud POS ve sdílených prostředích</span><span class="sxs-lookup"><span data-stu-id="289ed-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
