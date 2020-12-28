---
title: Konfigurace několika klientů typu B2C v prostředí obchodu
description: Toto téma popisuje, kdy a jak nastavit vícen klientů typu business-to-consumer (B2C) Microsoft Azure Active Directory (Azure AD) na kanál pro ověření uživatele ve vyhrazeném prostředí Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: da27e3ed0a0e50126590609d09575befe17a7aa2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517109"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="a6fc8-103">Konfigurace několika klientů typu B2C v prostředí obchodu</span><span class="sxs-lookup"><span data-stu-id="a6fc8-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6fc8-104">Toto téma popisuje, kdy a jak nastavit vícen klientů typu business-to-consumer (B2C) Microsoft Azure Active Directory (Azure AD) na kanál pro ověření uživatele ve vyhrazeném prostředí Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="a6fc8-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="a6fc8-105">Overview</span></span>

<span data-ttu-id="a6fc8-106">Dynamics 365 Commerce používá službu cloudové identity typu B2C Azure AD k podpoře uživatelských pověření a toků ověřování.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="a6fc8-107">Uživatelé mohou použít ověřovací toky k přihlášení, přihlášení a resetování hesla.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="a6fc8-108">B2C Azure AD ukládá citlivé informace o ověřování uživatele (například jeho uživatelské jméno a heslo).</span><span class="sxs-lookup"><span data-stu-id="a6fc8-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="a6fc8-109">Uživatelský záznam je jedinečný pro každého klienta B2C a používá buď pověření uživatelského jména (e-mailová adresa) nebo pověření poskytovatele sociálních identit.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="a6fc8-110">Ve většině případů se v prostředí Commerce používá jediný klient B2C Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="a6fc8-111">Zákazníci v Commerce mohou poté vytvářet a publikovat více pracovišť ve stejném prostředí Commerce a na těchto webech budou používat stejná pověření zákazníka.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="a6fc8-112">Pokud je však pracoviště v prostředí považováno za různé značky a zobrazují se uživatelům jako samostatné podniky, může být pro kanál, který se používá pro oddělení pracoviště/značky, nakonfigurován klient B2C.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="a6fc8-113">Důležité informace o nastavení více B2C klientů na kanál</span><span class="sxs-lookup"><span data-stu-id="a6fc8-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="a6fc8-114">Pokud je každý kanál nebo pracoviště považováno za samostatnou firmu, nejlepším způsobem, s ohledem na ověřovací toky uživatelů v obchodu, je použití oddělených právnických osob.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="a6fc8-115">Chcete-li však ponechat každý kanál nebo web ve stejném prostředí a právnické osobě, ale chcete mít pro každé pracoviště samostatné ověřování uživatelů, je důležité zvážit následující body, než budete pokračovat:</span><span class="sxs-lookup"><span data-stu-id="a6fc8-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="a6fc8-116">Uživatelé budou mít pro každý kanál nebo pracoviště vlastní odlišná pověření.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="a6fc8-117">Stejná osoba může mít dva oddělené účty na kanál nebo web, protože každý účet bude jedinečným vstupem do samostatného klienta B2C.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="a6fc8-118">V prostředí Microsoft Dynamics budou pro hledání v globálních záznamech vráceny samostatné záznamy odběratelů.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="a6fc8-119">Pokud uživatel používá stejnou e-mailovou adresu v rámci kanálů nebo pracovišť, vrátí globální vyhledávání zákazníků výsledky pro každý kanál nebo Web.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="a6fc8-120">(Zobrazí se indikátor kanálu.)</span><span class="sxs-lookup"><span data-stu-id="a6fc8-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="a6fc8-121">Adresář lze použít k usnadnění seskupení uživatelů, aby bylo možné je sledovat podle jednotlivých kanálů.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="a6fc8-122">Počet záznamů odběratelů na kanál se může zvýšit a tento nárůst může ovlivnit výkon globálních hledání zákazníků.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="a6fc8-123">Klienti B2C musí být pečlivě mapováni na kanál, aby se předešlo situacím, kdy se odběratelé zaregistrují pro nesprávného klienta.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="a6fc8-124">V opačném případě může dojít k nejasnostem nebo sledování problémů.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="a6fc8-125">Následující ilustrace znázorňuje několik B2C klientů v prostředí obchodu.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Několik klientů typu B2C v prostředí Commerce](media/MultiB2C_In_Environment.png)

<span data-ttu-id="a6fc8-127">Pokud se rozhodnete, že váš podnik vyžaduje jedinečné B2C klienty na kanál ve stejném Commerce prostředí, požádejte o tuto funkci postupy uvedené v následujících oddílech.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="a6fc8-128">Požadavek, aby byl ve vašem prostředí povolen B2C pro kanál</span><span class="sxs-lookup"><span data-stu-id="a6fc8-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="a6fc8-129">V případě, že chcete, aby byl k dispozici samostatný B2C klient na kanál ve stejném Commerce Environment, musíte odeslat žádost Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="a6fc8-130">Další informace naleznete v tématech [Získání podpory pro Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) nebo diskutujte o vašem problému s kontaktem pro Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="a6fc8-131">Konfigurovat klienty B2C ve vašem prostředí</span><span class="sxs-lookup"><span data-stu-id="a6fc8-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="a6fc8-132">Chcete-li konfigurovat klienta typu B2C ve vašem prostředí, proveďte příslušné postupy v této části.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="a6fc8-133">Přidejte klienta B2C Azure AD</span><span class="sxs-lookup"><span data-stu-id="a6fc8-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="a6fc8-134">Chcete-li do prostředí přidat klienta B2C Azure AD, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="a6fc8-135">Přihlaste se ke konfigurátoru webů Commerce pro vaše prostředí jako správce systému. Chcete-li konfigurovat klienta B2C Azure AD, musíte být správcem systému pro prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="a6fc8-136">V levém navigačním podokně vyberte **Nastavení klienta** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="a6fc8-137">Vyberte **Nastavení B2C** a poté vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="a6fc8-138">Vyberte **Přidat aplikaci B2C** a poté zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="a6fc8-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="a6fc8-139">**Název aplikace**: zadejte název, který má být použit pro aplikaci v kontextu jeho správy ve službě Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="a6fc8-140">Doporučujeme, abyste používali název aplikace, který jste zvolili při nastavení aplikace Azure AD B2C na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="a6fc8-141">Tímto způsobem lze omezit záměnu při správě B2C klientů ve službě Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="a6fc8-142">**Název klienta**: zadejte název klienta B2C, jak se objevuje na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="a6fc8-143">**Zapomenout ID zásad hesla**: Zadejte ID zásad (název zásady na portálu Azure).</span><span class="sxs-lookup"><span data-stu-id="a6fc8-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="a6fc8-144">**ID zásady registrace a přihlášení**: Zadejte ID zásad (název zásady na portálu Azure).</span><span class="sxs-lookup"><span data-stu-id="a6fc8-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="a6fc8-145">**GUID klienta**: zadejte ID klienta B2C Azure AD tak, jak se objevuje na portálu Azure (ne v ID aplikace pro klienta B2C).</span><span class="sxs-lookup"><span data-stu-id="a6fc8-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="a6fc8-146">**ID zásad úprav profilu**: Zadejte ID zásad (název zásady na portálu Azure).</span><span class="sxs-lookup"><span data-stu-id="a6fc8-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="a6fc8-147">Až tyto informace dokončíte, výběrem **OK** uložte provedené změny.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="a6fc8-148">Pole **Rozsah**, **ID neinteraktivních zásad**, **ID neinteraktivních klientů**, **Vlastní doména přihlašování** a **ID zásad registrace** ponechte prázdná, pokud vám tým Dynamics 365 Commerce neřekne, abyste je nastavili.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="a6fc8-149">Váš nový klient B2C Azure AD by se nyní měl objevit v seznamu v části **Spravovat aplikace B2C**.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="a6fc8-150">Správa nebo odstranění klienta B2C Azure AD</span><span class="sxs-lookup"><span data-stu-id="a6fc8-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="a6fc8-151">Přihlaste se ke konfigurátoru webů Commerce pro vaše prostředí jako správce systému. Chcete-li konfigurovat klienta B2C Azure AD, musíte být správcem systému pro prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="a6fc8-152">V levém navigačním podokně vyberte **Nastavení klienta** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="a6fc8-153">Vyberte **Nastavení B2C** a poté vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="a6fc8-154">Chcete-li upravit B2C klienta, vyberte symbol tužky vedle něj.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="a6fc8-155">Chcete-li odstranit klienta B2C, vyberte symbol odpadkového koše.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="a6fc8-156">Vyberte **Uložit** a potom **Publikovat** pro aktivaci svých změn.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="a6fc8-157">Pokud je klient B2C nakonfigurován pro aktivní nebo publikovaný web, mohou se uživatelé přihlásili pomocí účtů, které jsou k dispozici v klientovi.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="a6fc8-158">Odstraníte-li nakonfigurovaného klienta v nabídce **Nastavení klienta \> Klient B2C**, odeberte přidružení tohoto klienta B2C z webů, které jsou přidruženy ke všem kanálům klienta.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="a6fc8-159">V takovém případě se může stát, že uživatelé již nebudou schopni přihlásit se ke svým účtům.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="a6fc8-160">Proto při odstraňování nakonfigurovaného klienta buďte velmi opatrní.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="a6fc8-161">Po odstranění nakonfigurovaného klienta budou i nadále udržovat klienta B2C a záznamy, ale konfigurace systému Commerce pro daného klienta bude změněna nebo odebrána.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="a6fc8-162">Uživatelé, kteří se pokusí zaregistrovat nebo se přihlásit k webu, vytvoří nový záznam účtu ve výchozím nebo nově přidruženém klientovi B2C, který je nakonfigurován pro kanál webu.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="a6fc8-163">Nakonfigurujte kanál pomocí klienta B2C</span><span class="sxs-lookup"><span data-stu-id="a6fc8-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="a6fc8-164">Přihlaste se ke konfigurátoru webů Commerce pro vaše prostředí jako správce systému. Chcete-li konfigurovat klienta B2C Azure AD, musíte být správcem systému pro prostředí Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="a6fc8-165">V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="a6fc8-166">Vyberte **Kanály** a poté vyberte kanál, který chcete konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="a6fc8-167">V podokně vlastnosti vpravo v poli **Vybrat aplikaci B2C** vyberte pro tento kanál konfigurovaného klienta B2C Azure AD pro použití v tomto kanálu.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="a6fc8-168">V řádku příkazů výběrem možnosti **Uložit a publikovat** potvrďte novou nebo aktualizovanou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="a6fc8-169">Pokud změníte aplikaci B2C, která je přiřazena kanálu, odstraníte aktuální odkazy, které byly vytvořeny pro všechny uživatele, kteří se již v prostředí registrovali.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="a6fc8-170">V tomto případě nebudou mít uživatelé k dispozici žádná pověření přidružená k aktuálně přiřazené B2C aplikaci.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="a6fc8-171">Konfiguraci B2C kanálů Azure AD proto měňte pouze v případě, že jste kanál poprvé nastavili a žádní uživatelé se nemohou registrovat.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="a6fc8-172">V opačném případě se může stát, že se uživatelé budou muset znovu přihlásit, aby vytvořili záznam v novém klientovi B2C Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a6fc8-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="a6fc8-173">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a6fc8-173">Additional resources</span></span>

[<span data-ttu-id="a6fc8-174">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="a6fc8-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a6fc8-175">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="a6fc8-175">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a6fc8-176">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="a6fc8-176">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a6fc8-177">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="a6fc8-177">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a6fc8-178">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="a6fc8-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a6fc8-179">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="a6fc8-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a6fc8-180">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="a6fc8-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a6fc8-181">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="a6fc8-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a6fc8-182">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="a6fc8-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a6fc8-183">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="a6fc8-183">Enable location-based store detection</span></span>](enable-store-detection.md)
