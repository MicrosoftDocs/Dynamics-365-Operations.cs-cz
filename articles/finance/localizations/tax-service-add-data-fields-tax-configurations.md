---
title: Přidání datových polí do daňových konfigurací
description: Toto téma vysvětluje, jak přizpůsobit daňové konfigurace přidáním datových polí.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819417"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="d2020-103">Přidání datových polí do daňových konfigurací</span><span class="sxs-lookup"><span data-stu-id="d2020-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d2020-104">Toto téma vysvětluje, jak přizpůsobit daňové konfigurace pomocí [datových polí, která jsou přidána do daňové integrace](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="d2020-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="d2020-105">Přizpůsobení datového modelu daně</span><span class="sxs-lookup"><span data-stu-id="d2020-105">Customize the tax data model</span></span>

1. <span data-ttu-id="d2020-106">V Microsoft Dynamics 365 Finance přejděte do **Elektronické výkaznictví** \> **Konfigurace daní**.</span><span class="sxs-lookup"><span data-stu-id="d2020-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="d2020-107">Ve stromu konfigurace vyberte položku **Daňový datový model - Evropa**.</span><span class="sxs-lookup"><span data-stu-id="d2020-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="d2020-108">Poté v podokně akcí vyberte příkaz **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="d2020-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="d2020-109">V rozevíracím dialogovém okně vyberte možnost **Model zdanitelného dokladu odvozený z názvu: Daňový datový model – Evropa, Microsoft**, zadejte název nového daňového datového modelu a poté vyberte příkaz **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="d2020-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="d2020-110">Vyberte daňový datový model, který jste právě vytvořili, a poté v podokně akcí vyberte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="d2020-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="d2020-111">Rozbalte strom datového modelu, vyberte **Řádky** a potom vyberte příkaz **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d2020-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="d2020-112">V dialogovém okně **Vytvořit uzel** zadejte název, zadejte typ položky a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="d2020-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="d2020-113">Přidejte všechny povinné sloupce.</span><span class="sxs-lookup"><span data-stu-id="d2020-113">Add any required columns.</span></span>
8. <span data-ttu-id="d2020-114">V podokně akcí vyberte příkaz **Uložit** a potom vyberte možnost **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="d2020-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="d2020-115">Zavřete stránku a zobrazte dokončenou verzi daňového datového modelu.</span><span class="sxs-lookup"><span data-stu-id="d2020-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="d2020-116">Přizpůsobení konfigurace daně</span><span class="sxs-lookup"><span data-stu-id="d2020-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="d2020-117">Ve Finance přejděte do nabídky **Elektronické výkaznictví** \> **Konfigurace daní**.</span><span class="sxs-lookup"><span data-stu-id="d2020-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="d2020-118">Ve stromu konfigurace vyberte položku **Konfigurace daně – Evropa**.</span><span class="sxs-lookup"><span data-stu-id="d2020-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="d2020-119">Poté v podokně akcí vyberte příkaz **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="d2020-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="d2020-120">V rozevíracím dialogovém okně vyberte možnost **Konfigurace daňové služby odvozená z názvu: Konfigurace dně – Evropa, Microsoft**, zadejte název nové daňové konfigurace a poté vyberte příkaz **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="d2020-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="d2020-121">Vyberte konfiguraci daně, kterou jste právě vytvořili, a poté v podokně akcí vyberte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="d2020-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="d2020-122">V části **Vlastnosti** v poli **Datový model** vyberte přizpůsobený daňový datový model, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="d2020-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="d2020-123">V poli **Verze datového modelu** vyberte dokončenou verzi daňového datového modelu.</span><span class="sxs-lookup"><span data-stu-id="d2020-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="d2020-124">Vyberte příkaz **Přidat** a přidejte požadovaná daňová opatření.</span><span class="sxs-lookup"><span data-stu-id="d2020-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="d2020-125">V podokně akcí vyberte příkaz **Uložit** a potom vyberte možnost **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="d2020-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="d2020-126">Zavřete stránku a zobrazte dokončenou verzi daňové konfigurace.</span><span class="sxs-lookup"><span data-stu-id="d2020-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="d2020-127">Implementujte daňové funkce v přizpůsobené daňové konfiguraci</span><span class="sxs-lookup"><span data-stu-id="d2020-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="d2020-128">Ve službách Regulatory Configuration Services (RCS) přejděte do nabídky **Funkce globalizace** \> **Daň**.</span><span class="sxs-lookup"><span data-stu-id="d2020-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="d2020-129">Vyberte příkaz **Přidat**, zadejte informace o nové funkci a poté vyberte **Vytvořit funkci**.</span><span class="sxs-lookup"><span data-stu-id="d2020-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="d2020-130">Na kartě **Verze** vyberte funkci a poté vyberte příkaz **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="d2020-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="d2020-131">Na kartě **Obecné** v poli **Verze konfigurace** vyberte přizpůsobenou konfiguraci a verzi daně.</span><span class="sxs-lookup"><span data-stu-id="d2020-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="d2020-132">V dialogovém okně **Spravovat sloupce** vyberte sloupce záhlaví a řádků, které chcete zahrnout do přizpůsobeného daňového opatření, a poté je kliknutím na tlačítko se šipkou doprava přidejte do seznamu **Vybrané sloupce**.</span><span class="sxs-lookup"><span data-stu-id="d2020-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>