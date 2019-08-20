---
title: Zapůjčený majetek
description: Toto téma popisuje, jak registrovat zapůjčený majetek v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8680241b1300aceda3280893982a1eff3d2e09e0
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847475"
---
# <a name="asset-loans"></a><span data-ttu-id="58323-103">Zapůjčený majetek</span><span class="sxs-lookup"><span data-stu-id="58323-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="58323-104">Pokud vaše společnost obdrží aktiva pro práce opravy nebo údržby z interních míst nebo od odběratelů a pokud dočasně půjčíte majetek na tato místa nebo těmto zákazníkům, může modul Správa majetku sledovat zapůjčený majetek.</span><span class="sxs-lookup"><span data-stu-id="58323-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="58323-105">Registrace půjček majetku v požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="58323-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="58323-106">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="58323-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="58323-107">Vyberte požadavek na údržbu, na kterém má být zaregistrován zapůjčený majetek, a pak vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="58323-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="58323-108">Na stránce **Požadavek** vyberte **Odeslat zapůjčený majetek**.</span><span class="sxs-lookup"><span data-stu-id="58323-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="58323-109">Vyberte majetek a zadejte očekávané datum vrácení.</span><span class="sxs-lookup"><span data-stu-id="58323-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="58323-110">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="58323-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="58323-111">Zapůjčený majetek lze odeslat pouze v případě, že je k dispozici majetek se stejným typem majetku.</span><span class="sxs-lookup"><span data-stu-id="58323-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="58323-112">Zapůjčený majetek musí mít stav životního cyklu majetku, který umožňuje použití jako investiční majetek, jako je například **InStorage.**</span><span class="sxs-lookup"><span data-stu-id="58323-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="58323-113">Po registraci zapůjčeného majetku se stav životního cyku majetku automaticky aktualizuje například na **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="58323-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="58323-114">Chcete-li zobrazit seznam všech majetků, které jste zapůjčili na jiná místa nebo jiným zákazníkům, vyberte možnost **Správa majetku** \> **Společné** \> **Zapůjčený majetek** \> **Všechen zapůjčený majetek**.</span><span class="sxs-lookup"><span data-stu-id="58323-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="58323-115">Pokud je u majetku zaškrtnuto políčko **ukončeno**, byl majetek registrován jako vrácený do vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="58323-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Obrázek č. 1](media/06-manage-maintenance-requests.png)

<span data-ttu-id="58323-117">Na stránce **aktivní zapůjčený majetek** můžete zobrazit seznam všeho zapůjčeného majetku, který nebyl ještě vrácen do vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="58323-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="58323-118">Registrace zapůjčeného majetku jako vráceného</span><span class="sxs-lookup"><span data-stu-id="58323-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="58323-119">Vyberte **Správa majetku** \> **Společné** \> **Zapůjčený majetek** \> **Aktivní zapůjčené majetky**.</span><span class="sxs-lookup"><span data-stu-id="58323-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="58323-120">Vyberte zapůjčený majetek, který chcete zaregistrovat jako vrácený, a poté vyberte **Vrátit zapůjčený majetek**.</span><span class="sxs-lookup"><span data-stu-id="58323-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="58323-121">V poli **Vráceno** zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="58323-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="58323-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="58323-122">Select **OK**.</span></span>
5. <span data-ttu-id="58323-123">Aktualizujte stránku seznamu **Aktivních zapůjčený majetek** a všimněte si, že se zapůjčený majetek již v seznamu nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="58323-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
