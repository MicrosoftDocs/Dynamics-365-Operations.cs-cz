---
title: Vytvořte účet úložiště Azure a trezor klíčů
description: Toto téma vysvětluje, jak vytvořit účet úložiště Azure a trezor klíčů.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5c2ddad10f9cbedd77a04fe0f42bdc217fd43344
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963232"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="3568d-103">Vytvořte účet úložiště Azure a trezor klíčů</span><span class="sxs-lookup"><span data-stu-id="3568d-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="3568d-104">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="3568d-104">Prerequisites</span></span>

<span data-ttu-id="3568d-105">Před tím, než budete moci provést kroky v tomto tématu, se musíte ujistit, že jsou dokončeny následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="3568d-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="3568d-106">Vytvoření zdroje úložiště klíčů v Azure.</span><span class="sxs-lookup"><span data-stu-id="3568d-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="3568d-107">Další informace viz [Informace o Trezoru klíčů Azure](/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="3568d-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="3568d-108">Vytvořte účet úložiště Azure (úložiště blob).</span><span class="sxs-lookup"><span data-stu-id="3568d-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="3568d-109">Další informace viz [Údržba účtu Azure Storage](/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="3568d-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="3568d-110">Přehled</span><span class="sxs-lookup"><span data-stu-id="3568d-110">Overview</span></span>

<span data-ttu-id="3568d-111">V tomto tématu provedete dva hlavní kroky:</span><span class="sxs-lookup"><span data-stu-id="3568d-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="3568d-112">Nastavte účet úložiště Azure a získejte identifikátor URI účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="3568d-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="3568d-113">Nastavte trezor klíčů pro uložení URI účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="3568d-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="3568d-114">Nastavte účet úložiště Azure a získejte identifikátor URI účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="3568d-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="3568d-115">Otevřete účet úložiště, který plánujete použít s Elektronickou fakturací.</span><span class="sxs-lookup"><span data-stu-id="3568d-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="3568d-116">Přejděte na **Služba Blob** \> **Kontejnery** a vytvořte nový kontejner.</span><span class="sxs-lookup"><span data-stu-id="3568d-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="3568d-117">Zadejte název kontejneru a nastavte pole **Úroveň veřejného přístupu** na **Soukromé (bez anonymního přístupu)**.</span><span class="sxs-lookup"><span data-stu-id="3568d-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="3568d-118">Otevřete kontejner a přejděte na **Nastavení \> Zásady přístupu**.</span><span class="sxs-lookup"><span data-stu-id="3568d-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="3568d-119">Vyberte **Přidat zásady**, chcete-li přidat uloženou zásadu přístupu.</span><span class="sxs-lookup"><span data-stu-id="3568d-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="3568d-120">Nastavte pole **Identifikátor** a **Oprávnění** dle potřeby.</span><span class="sxs-lookup"><span data-stu-id="3568d-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="3568d-121">V poli **Oprávnění** byste měli vybrat všechna oprávnění.</span><span class="sxs-lookup"><span data-stu-id="3568d-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Udělení oprávnění úložiště blob](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="3568d-123">Zadejte data zahájení a ukončení platnosti.</span><span class="sxs-lookup"><span data-stu-id="3568d-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="3568d-124">Doba použitelnosti by měla být v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="3568d-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="3568d-125">Vyberte **OK** pro uložení zásad a poté uložte změny do kontejneru.</span><span class="sxs-lookup"><span data-stu-id="3568d-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="3568d-126">Vraťte se do účtu úložiště a otevřete **Průzkumník úložiště (náhled)**.</span><span class="sxs-lookup"><span data-stu-id="3568d-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="3568d-127">Klikněte pravým tlačítkem na kontejner a poté vyberte **Získejte sdílený přístupový podpis**.</span><span class="sxs-lookup"><span data-stu-id="3568d-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="3568d-128">V dialogovém okně **Sdílený přístupový podpis** zkopírujte a uložte hodnotu do pole **URI**.</span><span class="sxs-lookup"><span data-stu-id="3568d-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="3568d-129">Tato hodnota bude použita v dalším postupu a bude označována jako *sdílený přístupový podpis URI*.</span><span class="sxs-lookup"><span data-stu-id="3568d-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![Výběr a kopírování hodnoty URI](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="3568d-131">Nastavte trezor klíčů pro uložení URI účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="3568d-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="3568d-132">Otevřete trezor klíčů, který hodláte použít s Elektronickou fakturací.</span><span class="sxs-lookup"><span data-stu-id="3568d-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="3568d-133">Přejděte na **Nastavení** \> **Tajné kódy** a potom vyberte **Generovat / importovat** pro vytvoření nového tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="3568d-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="3568d-134">Na stránce **Vytvořte tajný kód** v poli **Možnosti nahrávání** vyberte **Manuální**.</span><span class="sxs-lookup"><span data-stu-id="3568d-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="3568d-135">Zadat název tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="3568d-135">Enter the name of the secret.</span></span> <span data-ttu-id="3568d-136">Tento název bude použit během instalace služby v Regulatory Configuration Service (RCS) a bude označován jako *tajný název trezoru klíčů*.</span><span class="sxs-lookup"><span data-stu-id="3568d-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="3568d-137">V poli **Hodnota** vyberte **URI sdíleného přístupového podpisu** a potom vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="3568d-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="3568d-138">Nastavte zásady přístupu a udělte Elektronické fakturaci správnou úroveň zabezpečeného přístupu k tajnému kódu, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="3568d-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="3568d-139">Přejděte na **Nastavení \> Zásady přístupu** a vyberte **Přidat zásady přístupu**.</span><span class="sxs-lookup"><span data-stu-id="3568d-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="3568d-140">Nastavte tajná oprávnění pro operace **Získat** a **Seznam**.</span><span class="sxs-lookup"><span data-stu-id="3568d-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Udělení přístupu ke službě](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="3568d-142">Nastavte oprávnění pro operace **Získat** a **Seznam**.</span><span class="sxs-lookup"><span data-stu-id="3568d-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Udělení povolení k certifikátu](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="3568d-144">V poli **Vybrat objekt zabezpečení** vyberte **Není vybrán žádný**.</span><span class="sxs-lookup"><span data-stu-id="3568d-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="3568d-145">V dialogovém okně **Objekt zabezpečení** vyberte objekt zabezpečení přidáním **Služba elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="3568d-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="3568d-146">Vyberte **Přidat** a potom vyberte **Uložit změny Trezoru klíčů**.</span><span class="sxs-lookup"><span data-stu-id="3568d-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="3568d-147">Na stránce **Přehled** zkopírujte hodnotu **Název DNS** pro trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="3568d-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="3568d-148">Tato hodnota bude použita během instalace služby v RCS a bude označována jako *identifikátor URI trezoru klíčů*.</span><span class="sxs-lookup"><span data-stu-id="3568d-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>

> [!NOTE]
> <span data-ttu-id="3568d-149">Pro další zabezpečení účtu úložiště nakonfigurujte Azure Defender pro úložiště.</span><span class="sxs-lookup"><span data-stu-id="3568d-149">For additional security on the storage account, configure the Azure Defender for Storage.</span></span>
> 
> <span data-ttu-id="3568d-150">Další informace viz [Úvod do Azure Defender pro úložiště](/azure/security-center/defender-for-storage-introduction).</span><span class="sxs-lookup"><span data-stu-id="3568d-150">For more information, see [Introduction to Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
