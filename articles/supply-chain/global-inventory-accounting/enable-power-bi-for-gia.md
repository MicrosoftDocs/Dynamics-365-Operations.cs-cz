---
title: Povolit Power BI pro globální účetnictví zásob
description: Toto téma popisuje, jak povolit Microsoft Power BI pro globální účtování zásob.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273125"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="e7d61-103">Povolit Power BI pro globální účetnictví zásob</span><span class="sxs-lookup"><span data-stu-id="e7d61-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="e7d61-104">Můžete připnout dlaždice, řídicí panely a zprávy ze svého účtu [PowerBI.com](https://powerbi.com/) do pracovního prostoru aplikace Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e7d61-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e7d61-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="e7d61-105">Prerequisites</span></span>

<span data-ttu-id="e7d61-106">Než budete moci povolit výkaznicktví Power BI, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="e7d61-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="e7d61-107">V aplikaci Dynamics 365 musíte být správcem systému.</span><span class="sxs-lookup"><span data-stu-id="e7d61-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="e7d61-108">Musíte mít účet [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="e7d61-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="e7d61-109">Musíte mít alespoň jeden řídicí panel a jednu sestavu ve svém účtu Power BI.</span><span class="sxs-lookup"><span data-stu-id="e7d61-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="e7d61-110">Musíte být správcem svého účtu Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e7d61-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="e7d61-111">Doména Azure AD musí být stejná doména, kterou jste použili pro svůj účet [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="e7d61-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="e7d61-112">Nastavení</span><span class="sxs-lookup"><span data-stu-id="e7d61-112">Setup</span></span>

<span data-ttu-id="e7d61-113">Pro nastavení integrace Power BI postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e7d61-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="e7d61-114">Přihlaste se do [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="e7d61-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="e7d61-115">Přčejděte na **Knihovnu sdíleného majetku**, vyberte **model vykazování Power BI** jako typ majetku a stáhněte balíček **Globální účtování zásob**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="e7d61-116">Přihláste se do [PowerBI.com](https://app.powerbi.com/) a nahrajte soubor sestavy **Globální účtování zásob** Power BI pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="e7d61-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="e7d61-117">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-117">Select **New**.</span></span>
    1. <span data-ttu-id="e7d61-118">Vyberte **Odeslat soubor**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="e7d61-119">Vyberte soubor sestavy **Globální účtování zásob** Power BI.</span><span class="sxs-lookup"><span data-stu-id="e7d61-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="e7d61-120">Nakonfigurujte sestavu **Globální účtování zásob** Power BI podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="e7d61-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="e7d61-121">Přejděte do **Můj pracovní prostor**, vyhledejte datovou sadu pro Globální účetnictví zásob a poté v nabídce **Možnosti** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="e7d61-122">V **Nastavení pro globální účtování zásob** rozbalte **Parametry** a podle potřeby aktualizujte všechny parametry.</span><span class="sxs-lookup"><span data-stu-id="e7d61-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="e7d61-123">Zaregistrujte aplikaci podle popisu v [Konfigurace integrace PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="e7d61-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="e7d61-124">Integrujte soubor sestavy **Globální účtování zásob** Power BI do Dynamics 365 Supply Chain Management podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="e7d61-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="e7d61-125">Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace PowerBI.com**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="e7d61-126">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="e7d61-127">Vyberte **Povolit integraci PowerBI.Com**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="e7d61-128">V poli **ID aplikace** zadejte ID aplikace.</span><span class="sxs-lookup"><span data-stu-id="e7d61-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="e7d61-129">V poli **Klíč aplikace** zadejte klíč aplikace.</span><span class="sxs-lookup"><span data-stu-id="e7d61-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="e7d61-130">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-130">Select **Save**.</span></span>

1. <span data-ttu-id="e7d61-131">Obnovte stránku tak, aby se zobrazilo přihlašovací dialogové okno Power BI.</span><span class="sxs-lookup"><span data-stu-id="e7d61-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="e7d61-132">Na kartě **Možnosti** vyberte **Otevřít katalog sestav** a potom vyberte soubor sestavy **Globální účtování zásob** Power BI, který jste nahráli dříve.</span><span class="sxs-lookup"><span data-stu-id="e7d61-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="e7d61-133">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="e7d61-133">Refresh the page.</span></span> <span data-ttu-id="e7d61-134">Měli byste vidět, že vaše zpráva byla přidána.</span><span class="sxs-lookup"><span data-stu-id="e7d61-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="e7d61-135">V nabídce **Sestavy Power BI** vyberte odkaz **Globální účtování zásob**.</span><span class="sxs-lookup"><span data-stu-id="e7d61-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="e7d61-136">Další informace naleznete v tématu [Konfigurace integrace PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="e7d61-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
