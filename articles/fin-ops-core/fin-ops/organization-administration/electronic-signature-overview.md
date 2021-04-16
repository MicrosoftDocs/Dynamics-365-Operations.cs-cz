---
title: Přehled elektronických podpisů
description: Tento článek obsahuje přehled informací o elektronických podpisech a o možnostech jejich použití.
author: maertenm
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 547ab10dabb6bb3f8ea41d0f80db227fc24411a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747704"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="b0512-103">Přehled elektronických podpisů</span><span class="sxs-lookup"><span data-stu-id="b0512-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0512-104">Tento článek obsahuje přehled informací o elektronických podpisech a o možnostech jejich použití.</span><span class="sxs-lookup"><span data-stu-id="b0512-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="b0512-105">Co je elektronický podpis?</span><span class="sxs-lookup"><span data-stu-id="b0512-105">What is an electronic signature?</span></span>

<span data-ttu-id="b0512-106">Elektronický podpis potvrzuje identitu osoby, která spouští nebo schvaluje určitý proces využívající výpočetní techniku.</span><span class="sxs-lookup"><span data-stu-id="b0512-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="b0512-107">V některých průmyslových odvětvích má elektronický podpis stejnou právní hodnotu jako ruční podpis.</span><span class="sxs-lookup"><span data-stu-id="b0512-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="b0512-108">Elektronické podpisy jsou vyžadovány předpisy v několika průmyslových odvětvích, například ve farmaceutickém, potravinářském, leteckém a zbrojním průmyslu.</span><span class="sxs-lookup"><span data-stu-id="b0512-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="b0512-109">Jsou rovněž nezbytnou podmínkou souladu s předpisy směrnice CFR 21, část 11, kterou vydal Úřad pro kontrolu potravin a léků (FDA) ve Spojených státech amerických.</span><span class="sxs-lookup"><span data-stu-id="b0512-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="b0512-110">Elektronický podpis sám o sobě není totéž jako podpis digitální.</span><span class="sxs-lookup"><span data-stu-id="b0512-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="b0512-111">Elektronický podpis je prostou náhražkou podpisu psaného rukou, zatímco digitální podpis je doplněn o další bezpečnostní opatření.</span><span class="sxs-lookup"><span data-stu-id="b0512-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="b0512-112">Digitální podpis vám může pomoci zjistit, zda s daty neoprávněně nemanipuloval jiný uživatel nebo proces.</span><span class="sxs-lookup"><span data-stu-id="b0512-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="b0512-113">Digitální podpis lze rovněž ověřit, přičemž vlastník certifikátu použitého k podepsání dat nemůže platnost ověření popřít.</span><span class="sxs-lookup"><span data-stu-id="b0512-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="b0512-114">Jak je popsáno dále, v aplikaci jsou součástí elektronických podpisů i vestavěné funkce digitálních podpisů.</span><span class="sxs-lookup"><span data-stu-id="b0512-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="b0512-115">Elektronické podpisy</span><span class="sxs-lookup"><span data-stu-id="b0512-115">Electronic signatures</span></span>

<span data-ttu-id="b0512-116">Můžete používat elektronické podpisy pro důležité obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="b0512-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="b0512-117">Některé procesy obsahují vestavěné prvky pro práci s elektronickými podpisy.</span><span class="sxs-lookup"><span data-stu-id="b0512-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="b0512-118">Kromě toho můžete vytvářet vlastní požadavky na podpisy, připojené k libovolné databázové tabulce a poli.</span><span class="sxs-lookup"><span data-stu-id="b0512-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="b0512-119">Součástí digitálního podpisu jsou i elektronické podpisy.</span><span class="sxs-lookup"><span data-stu-id="b0512-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="b0512-120">Každý uživatel, který podepisuje dokumenty, musí získat platný šifrovací certifikát.</span><span class="sxs-lookup"><span data-stu-id="b0512-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="b0512-121">Při podepsání dokumentu proběhne ověření soukromého klíče přidruženého k použitému certifikátu.</span><span class="sxs-lookup"><span data-stu-id="b0512-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="b0512-122">Údaje o elektronických podpisech se zaznamenávají do protokolu, který může sloužit jako záznam auditu.</span><span class="sxs-lookup"><span data-stu-id="b0512-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="b0512-123">Popis nastavení elektronických podpisů viz [Nastavení elektronických podpisů](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="b0512-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="b0512-124">Uživatelé, kteří potřebují přístup k elektronickým podpisům</span><span class="sxs-lookup"><span data-stu-id="b0512-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="b0512-125">Tři druhy uživatelů obvykle vyžadují zabezpečení přístupu k elektronickým podpisům: správci elektronického podpisu, podepisující osoby a auditoři elektronických podpisů.</span><span class="sxs-lookup"><span data-stu-id="b0512-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="b0512-126">Administrátoři elektronických podpisů</span><span class="sxs-lookup"><span data-stu-id="b0512-126">Electronic signature administrator</span></span>

<span data-ttu-id="b0512-127">Administrátor elektronických podpisů určuje požadavky na podpisy, nastavuje obecné parametry a schvalovatele a přijímá výstrahy v případě, že podpisy nelze ověřit.</span><span class="sxs-lookup"><span data-stu-id="b0512-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="b0512-128">Ve výchozím nastavení uživatel, který patří do role zabezpečení **Manažer informačních technologií**, má oprávnění ke správě elektronických podpisů.</span><span class="sxs-lookup"><span data-stu-id="b0512-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="b0512-129">Podepisující uživatel</span><span class="sxs-lookup"><span data-stu-id="b0512-129">Signer</span></span>

<span data-ttu-id="b0512-130">Podepisující uživatel připojuje elektronické podpisy k dokumentům a procesům, které vyžadují podepsání.</span><span class="sxs-lookup"><span data-stu-id="b0512-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="b0512-131">Ve výchozím nastavení uživatel, který patří do role zabezpečení **Uživatel systému**, má oprávnění k elektronickému podepisování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="b0512-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="b0512-132">Podepisující uživatel může vyžadovat další oprávnění pro přístup k datům souvisejícím s podepisovaným dokumentem nebo procesem.</span><span class="sxs-lookup"><span data-stu-id="b0512-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="b0512-133">Uživatel, který mění data a musí provedené změny pak podepsat, musí mít oprávnění ke změnám těchto dat.</span><span class="sxs-lookup"><span data-stu-id="b0512-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="b0512-134">Uživatel, který podepisuje jménem jiného uživatele nevyžaduje přístup k datům.</span><span class="sxs-lookup"><span data-stu-id="b0512-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="b0512-135">Příkladem tohoto typu uživatele je nadřízený, který podepisuje změny zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="b0512-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="b0512-136">Auditor elektronických podpisů</span><span class="sxs-lookup"><span data-stu-id="b0512-136">Electronic signature auditor</span></span>

<span data-ttu-id="b0512-137">Auditor elektronických podpisů kontroluje databázový protokol a kontrolní protokol podpisů, který je k dispozici prostřednictvím databázového protokolu.</span><span class="sxs-lookup"><span data-stu-id="b0512-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="b0512-138">Ve výchozím nastavení uživatel, který patří do role zabezpečení **Manažer informačních technologií**, má oprávnění k auditu elektronických podpisů.</span><span class="sxs-lookup"><span data-stu-id="b0512-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="b0512-139">Pokud má uživatel jinou roli, než **Manažer informačních technologií**, ujistěte se, že jsou roli přiřazena následující oprávnění:</span><span class="sxs-lookup"><span data-stu-id="b0512-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="b0512-140">Zobrazit chyby elektronických podpisů</span><span class="sxs-lookup"><span data-stu-id="b0512-140">View electronic signature failures</span></span>
- <span data-ttu-id="b0512-141">Zobrazit protokol databáze</span><span class="sxs-lookup"><span data-stu-id="b0512-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="b0512-142">Elektronické podepsání dokumentů</span><span class="sxs-lookup"><span data-stu-id="b0512-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="b0512-143">Získání certifikátu</span><span class="sxs-lookup"><span data-stu-id="b0512-143">Get a certificate</span></span>

<span data-ttu-id="b0512-144">Před elektronickým podepsáním dokumentů si musí každý podepisující uživatel vyžádat certifikát.</span><span class="sxs-lookup"><span data-stu-id="b0512-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="b0512-145">Funkce Microsoft SQL Server se používají k vytváření certifikátů a povolení elektronického podepisování.</span><span class="sxs-lookup"><span data-stu-id="b0512-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="b0512-146">Není vyžadována žádná další infrastruktura certifikátů ani veřejných klíčů (PKI).</span><span class="sxs-lookup"><span data-stu-id="b0512-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="b0512-147">Vyžádáte-li si certifikát, bude pro vás vytvořen veřejný a soukromý klíč.</span><span class="sxs-lookup"><span data-stu-id="b0512-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="b0512-148">Soukromý klíč je zašifrován s použitím hesla, které znáte pouze vy.</span><span class="sxs-lookup"><span data-stu-id="b0512-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="b0512-149">Při elektronickém podepsání dokumentu proběhne ověření vaší totožnosti podle hesla, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="b0512-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="b0512-150">Pro zažádání o certifikát klikněte na stránce **Možnosti** na kartě **Účty** na tlačítko **Získat certifikát**.</span><span class="sxs-lookup"><span data-stu-id="b0512-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="b0512-151">Zadejte a potvrďte heslo, které budete používat pro podepisování.</span><span class="sxs-lookup"><span data-stu-id="b0512-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="b0512-152">Heslo slouží k ochraně soukromého klíče a k autorizaci použití vašeho certifikátu.</span><span class="sxs-lookup"><span data-stu-id="b0512-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="b0512-153">Heslo se neukládá do databáze a nemá k němu přístup nikdo jiný než vy, tj. ani administrátor.</span><span class="sxs-lookup"><span data-stu-id="b0512-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="b0512-154">Jestliže zapomenete heslo připojené k vašemu certifikátu, musíte tento certifikát vynulovat.</span><span class="sxs-lookup"><span data-stu-id="b0512-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="b0512-155">Vynulování certifikátu neovlivní dokumenty, které jste podepsali s použitím původního certifikátu.</span><span class="sxs-lookup"><span data-stu-id="b0512-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="b0512-156">Chcete-li obnovit certifikát, na stránce **Možnosti** klepněte na tlačítko **Obnovit certifikát**.</span><span class="sxs-lookup"><span data-stu-id="b0512-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="b0512-157">Elektronické podepsání dokumentu</span><span class="sxs-lookup"><span data-stu-id="b0512-157">Sign a document electronically</span></span>

<span data-ttu-id="b0512-158">Když provedete změnu, která vyžaduje elektronický podpis, zobrazí se stránka **Podepsat dokument**.</span><span class="sxs-lookup"><span data-stu-id="b0512-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="b0512-159">Na stránce **Podepsat dokument** klepněte na kartu **Dokument** a zkontrolujte provedené změny.</span><span class="sxs-lookup"><span data-stu-id="b0512-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="b0512-160">Na kartě **Podpis** vyberte kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="b0512-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="b0512-161">Zadejte komentář, pokud je vyžadován.</span><span class="sxs-lookup"><span data-stu-id="b0512-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="b0512-162">Není-li v poli **Podepisující uživatel** zobrazeno vaše ID uživatele, vyberte je ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0512-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="b0512-163">Zadejte umístění, pokud jsou tyto informace požadovány.</span><span class="sxs-lookup"><span data-stu-id="b0512-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="b0512-164">Klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0512-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="b0512-165">Podepsat změny jiného uživatele</span><span class="sxs-lookup"><span data-stu-id="b0512-165">Sign for another user's changes</span></span>

<span data-ttu-id="b0512-166">V určitých situacích je třeba, aby změny provedené jedním uživatelem podepsal jiný uživatel.</span><span class="sxs-lookup"><span data-stu-id="b0512-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="b0512-167">Příkladem jsou změny kusovníku provedené zaměstnancem, které musí podpisem potvrdit jeho nadřízený.</span><span class="sxs-lookup"><span data-stu-id="b0512-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="b0512-168">Tento postup použijte, chcete-li určitého uživatele ustanovit podepisujícím uživatelem pro jiného uživatele.</span><span class="sxs-lookup"><span data-stu-id="b0512-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="b0512-169">V případě, že jeden uživatel podepisuje změny provedené jiným uživatelem, musí být podpis zadán na pracovní stanici uživatele, který změny provedl.</span><span class="sxs-lookup"><span data-stu-id="b0512-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="b0512-170">Uživatel nemůže provedené změny uložit, dokud nebudou podepsány.</span><span class="sxs-lookup"><span data-stu-id="b0512-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="b0512-171">Chcete-li určit schvalovatele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b0512-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="b0512-172">Na stránce **Možnosti** na kartě **Účty** klepněte na tlačítko **Určit schvalovatele**.</span><span class="sxs-lookup"><span data-stu-id="b0512-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="b0512-173">V poli **ID schvalujícího uživatele** vyberte ID uživatele, který musí podepsat změny provedené jiným uživatelem.</span><span class="sxs-lookup"><span data-stu-id="b0512-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="b0512-174">V poli **Podepsat pro ID uživatele** vyberte ID uživatele, jehož změny musí být podepsány.</span><span class="sxs-lookup"><span data-stu-id="b0512-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]