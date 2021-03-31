---
title: Vyhodnocení stavu
description: Toto téma vysvětluje, jak vytvořit šablonu hodnocení podmínky a registraci majetku v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d84520413659db32713711ad5ac980f1e8b5519
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217166"
---
# <a name="condition-assessment"></a><span data-ttu-id="43290-103">Vyhodnocení stavu</span><span class="sxs-lookup"><span data-stu-id="43290-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="43290-104">Toto téma vysvětluje, jak vytvořit šablonu hodnocení podmínky a registraci majetku v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="43290-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="43290-105">Vyhodnocení stavu se provádí v pravidelných intervalech a primárním cílem je vytvořit a udržovat údaje o stavu majetku.</span><span class="sxs-lookup"><span data-stu-id="43290-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="43290-106">Z hlediska preventivní údržby je důležité sledovat klíčové informace, jako je aktuální stav a zbývající životnost.</span><span class="sxs-lookup"><span data-stu-id="43290-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="43290-107">Dále, pokud budete provádět hodnocení stavu v pravidelných intervalech, budete moci monitorovat a porovnávat podmínky strojního zařízení ve vaší továrně.</span><span class="sxs-lookup"><span data-stu-id="43290-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="43290-108">Posouzení podmínek lze použít k měření a sledování mnoha podmínek vašeho zařízení.</span><span class="sxs-lookup"><span data-stu-id="43290-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="43290-109">Příklad: můžete měřit vibrace vašeho strojního zařízení.</span><span class="sxs-lookup"><span data-stu-id="43290-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="43290-110">Poté, co jste zaregistrovali měření vibrací v modulu Správa majetku u různých typů zařízení, můžete vyhledat nejnovější registrované hodnocení a zobrazit měření vibrací.</span><span class="sxs-lookup"><span data-stu-id="43290-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="43290-111">Vyhodnocení podmínek se vytváří u majetku.</span><span class="sxs-lookup"><span data-stu-id="43290-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="43290-112">Před provedením postupu posouzení podmínek nastavíte pro typ majetku šablonu zhodnocení stavu.</span><span class="sxs-lookup"><span data-stu-id="43290-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="43290-113">Důvodem pro použití šablon pro posouzení stavu je zamezit změnám dat o podmínkách podobného majetku.</span><span class="sxs-lookup"><span data-stu-id="43290-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="43290-114">Posloupnost pro nastavení a použití vyhodnocení podmínek v modulu Správa majetku je: nejprve nastavte požadované šablony vyhodnocení podmínek.</span><span class="sxs-lookup"><span data-stu-id="43290-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="43290-115">Dále přidružíte šablony k typům majetku ve formuláři **Typy majetku**.</span><span class="sxs-lookup"><span data-stu-id="43290-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="43290-116">Nakonec můžete vytvořit registrace vyhodnocení podmínky u majetku ve formuláři **Majetek**.</span><span class="sxs-lookup"><span data-stu-id="43290-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="43290-117">Vytvoření šablony vyhodnocení podmínek</span><span class="sxs-lookup"><span data-stu-id="43290-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="43290-118">Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Vyhodnocení podmínek**.</span><span class="sxs-lookup"><span data-stu-id="43290-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="43290-119">Zvolte **Nový** pro vytvoření nové šablony.</span><span class="sxs-lookup"><span data-stu-id="43290-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="43290-120">V poli **šablona** zadejte ID šablony.</span><span class="sxs-lookup"><span data-stu-id="43290-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="43290-121">Do pole **Název** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="43290-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="43290-122">Na pevné záložce **Řádky hodnocení podmínky** přidejte řádky požadované pro posouzení podmínky, včetně výběru příslušného typu podmínky a měrné jednotky.</span><span class="sxs-lookup"><span data-stu-id="43290-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="43290-123">Na pevné záložce **Typy majetku** přidejte typy majetku, které by měly používat šablonu vyhodnocení podmínky.</span><span class="sxs-lookup"><span data-stu-id="43290-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="43290-124">V polích **Řádky** a **Typy majetku** skupiny **Detaily** v horní části obrazovky uvidíte počet řádků hodnocení a typy majetku související s vybranou šablonou hodnocení podmínky.</span><span class="sxs-lookup"><span data-stu-id="43290-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="43290-125">Vytvoření registrace vyhodnocení podmínky u majetku</span><span class="sxs-lookup"><span data-stu-id="43290-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="43290-126">Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.</span><span class="sxs-lookup"><span data-stu-id="43290-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="43290-127">V seznamu vyberte majetek, pro který chcete vytvořit registraci hodnocení majetku.</span><span class="sxs-lookup"><span data-stu-id="43290-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="43290-128">Na kartě **obecné** klepněte na tlačítko **vyhodnocení podmínky**.</span><span class="sxs-lookup"><span data-stu-id="43290-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="43290-129">Kliknutím na **Nový** vytvořte novou registraci.</span><span class="sxs-lookup"><span data-stu-id="43290-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="43290-130">V poli **datum** vyberte datum pro vyhodnocení podmínky.</span><span class="sxs-lookup"><span data-stu-id="43290-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="43290-131">Vyberte jméno pracovníka, který provedl registraci vyhodnocení v poli **pracovník**.</span><span class="sxs-lookup"><span data-stu-id="43290-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="43290-132">V poli **řádky** uvidíte počet řádků vyhodnocení nastavených pro vyhodnocení podmínky.</span><span class="sxs-lookup"><span data-stu-id="43290-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="43290-133">V poli **šablona** vyberte šablonu pro vyhodnocení podmínky.</span><span class="sxs-lookup"><span data-stu-id="43290-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="43290-134">Název šablony je automaticky vložen do pole **název** a související řádky registrace se vloží na pevnou záložku **řádky vyhodnocení podmínky**.</span><span class="sxs-lookup"><span data-stu-id="43290-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="43290-135">Můžete vložit poznámky vztahující se k vybranému vyhodnocení podmínky na pevné záložce **Poznámky**.</span><span class="sxs-lookup"><span data-stu-id="43290-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="43290-136">Pro každý řádek hodnocení podmínek vložte data měření do pole **hodnota**.</span><span class="sxs-lookup"><span data-stu-id="43290-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="43290-137">Můžete vložit poznámku vztahující se k vybranému řádku registrace na pevné záložce **řádky vyhodnocení podmínky** > **poznámky**.</span><span class="sxs-lookup"><span data-stu-id="43290-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="43290-138">Pokud přidáte komentář k řádku, bude automaticky zaškrtnuto políčko **Komentář**.</span><span class="sxs-lookup"><span data-stu-id="43290-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="43290-139">Po provedení registrace pro zhodnocení stavu majetku můžete vytisknout sestavu vyhodnocení podmínek.</span><span class="sxs-lookup"><span data-stu-id="43290-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="43290-140">Vyhodnocení podmínky můžete také zaregistrovat v pracovním příkazu (tlačítko **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** > **Vyhodnocení podmínky**.)</span><span class="sxs-lookup"><span data-stu-id="43290-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]