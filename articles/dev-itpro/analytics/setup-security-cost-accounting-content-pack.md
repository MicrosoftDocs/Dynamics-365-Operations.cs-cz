---
title: "Nastavení zabezpečení pro obsah Power BI analýzy nákladového účetnictví"
description: "Toto téma vysvětluje, jak můžete rozšířit zabezpečení na úrovni přístupu v nákladovém účetnictví na zabezpečení na úrovni řádku v aplikaci Microsoft Power BI. Tato funkce pomáhá zajistit, aby uživatelé viděli pouze Power BI data, ke kterým mají udělen přístup."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="db4a7-104">Nastavení zabezpečení pro obsah Power BI analýzy nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="db4a7-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="db4a7-105">Toto téma vysvětluje, jak můžete rozšířit zabezpečení na úrovni přístupu v nákladovém účetnictví na zabezpečení na úrovni řádku v aplikaci Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="db4a7-106">Tato funkce pomáhá zajistit, aby uživatelé viděli pouze Power BI data, ke kterým mají udělen přístup.</span><span class="sxs-lookup"><span data-stu-id="db4a7-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="db4a7-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="db4a7-107">Overview</span></span>
--------

<span data-ttu-id="db4a7-108">Obsah **Analýza nákladového účetnictví** v Microsoft Power BI používá Power BI zabezpečení na úrovni řádku k omezení přístupu uživatelů.</span><span class="sxs-lookup"><span data-stu-id="db4a7-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="db4a7-109">Zabezpečení je založeno na organizační hierarchii úrovně přístupu, která je nastavena v parametrech nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="db4a7-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="db4a7-110">Další informace o obsahu **Analýza nákladového účetnictví** v Power BI najdete v tématu [Obsah analýzy nákladového účetnictví v Power BI](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="db4a7-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="db4a7-111">Nastavení</span><span class="sxs-lookup"><span data-stu-id="db4a7-111">Setup</span></span>
<span data-ttu-id="db4a7-112">Chcete-li rozšířit Power BI o zabezpečení na úrovni přístupu, musí vlastník obsahu Power BI postupovat podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="db4a7-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="db4a7-113">**Poznámka:** Uživatel, který publikuje obsah **Analýzy nákladového účetnictví** v Power BI se automaticky stane vlastníkem.</span><span class="sxs-lookup"><span data-stu-id="db4a7-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="db4a7-114">Pouze vlastník může nastavit zabezpečení v Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="db4a7-115">Navíc dokud vlastník nepřidá další uživatele na PowerBI.com, nikdo kromě vlastníka nemůže zobrazit jakákoliv data v obsahu **Analýzy nákladového účetnictví** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="db4a7-116">Publikujte soubor definice do Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="db4a7-117">Přihlaste se k PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="db4a7-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="db4a7-118">Vyhledejte soubor dat pro obsah **Analýzy nákladového účetnictví** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="db4a7-119">Otevřete stránku zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="db4a7-119">Open the security page.</span></span> 

    ![Otevření stránky zabezpečení](./media/CA-picture-1.png)

5.  <span data-ttu-id="db4a7-121">Role **Kontrolor objektu nákladů** role je již vytvořena.</span><span class="sxs-lookup"><span data-stu-id="db4a7-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="db4a7-122">Přidejte další členy, kteří jsou součástí organizační hierarchie na úrovni přístupu pro nákladové účetnictví.</span><span class="sxs-lookup"><span data-stu-id="db4a7-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![Přidání členů](./media/CA-picture-2.png)

<span data-ttu-id="db4a7-124">Uživatelé, kteří jsou přidáni do role **Kontrolor objektu nákladů** uvidí pouze data, která mohou vidět, podle definice v organizační hierarchii úrovně přístupu nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="db4a7-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="db4a7-125">**Poznámka:** Zabezpečení na úrovni řádku platí pro dlaždice a sestavy v aplikaci Microsoft Dynamics 365 for Finance and Operations, které jsou vloženy z Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="db4a7-126">Aktualizace zabezpečení</span><span class="sxs-lookup"><span data-stu-id="db4a7-126">Updating security</span></span>
<span data-ttu-id="db4a7-127">Pokud provedete aktualizace zabezpečení na úrovni přístupu v nákladovém účetnictví a chcete, aby Power BI odráželo tyto aktualizace, je nutné aktualizovat úložiště entit pro obsah **Analýzy nákladového účetnictví** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="db4a7-128">Po dokončení aktualizace úložiště entity z aplikace Finance and Operations je nutné aktualizovat artefakty na PowerBI.com. Více informací o aktualizaci úložiště entity získáte v části [Aktualizace úložiště entit](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="db4a7-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="db4a7-129">Vlastník obsahu **Analýzy nákladového účetnictví** v Power BI musí také provést aktualizaci úložiště entit, je-li novým uživatelům udělen přístup k organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="db4a7-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="db4a7-130">Navíc musí vlastník přidat nové uživatele do role **Kontrolor objektu nákladů** roli na PowerBI.com, aby se na ně vztahovalo zabezpečení na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="db4a7-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="db4a7-131">Zakázání zabezpečení</span><span class="sxs-lookup"><span data-stu-id="db4a7-131">Disabling security</span></span>
<span data-ttu-id="db4a7-132">Předpokládáme, že vaše organizace chce omezit přístup k datům.</span><span class="sxs-lookup"><span data-stu-id="db4a7-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="db4a7-133">Pokud jsou z nějakého důvodu parametry zabezpečení zakázány, pokud spustíte nákladové účetnictví, musí vlastník místo toho přidat uživatele do role **Nákladový účetní** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="db4a7-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="db4a7-134">Pokud změníte zabezpečení ze stavu povoleno na stav zakázáno, je vhodné odebrat uživatele z role **Kontrolor objektu nákladů**.</span><span class="sxs-lookup"><span data-stu-id="db4a7-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="db4a7-135">A naopak, pokud znovu zabezpečení povolíte.</span><span class="sxs-lookup"><span data-stu-id="db4a7-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="db4a7-136">Uživatelé mohou patřit k oběma rolím.</span><span class="sxs-lookup"><span data-stu-id="db4a7-136">Users can belong to both roles.</span></span> <span data-ttu-id="db4a7-137">Společný přístup je spojení obou rolí.</span><span class="sxs-lookup"><span data-stu-id="db4a7-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="db4a7-138">U případě obsahu **Analýzy nákladového účetnictví** v Power BI mají uživatelé, kteří mají společný přístup, neomezený přístup k datům.</span><span class="sxs-lookup"><span data-stu-id="db4a7-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="db4a7-139">Chcete-li použít omezený přístup, uživatelé musí být přiřazeni pouze k roli **Kontrolor objektu nákladů**.</span><span class="sxs-lookup"><span data-stu-id="db4a7-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="db4a7-140">Tyto aktualizace zabezpečení na úrovni řádku se projeví okamžitě.</span><span class="sxs-lookup"><span data-stu-id="db4a7-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="db4a7-141">Příslušní uživatele by měli obnovit zobrazení prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="db4a7-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db4a7-142">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="db4a7-142">Additional resources</span></span>
<span data-ttu-id="db4a7-143">Další informace o zabezpečení na úrovni řádku v Power BI naleznete v tématu [Správa zabezpečení na vašem modelu v Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="db4a7-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




