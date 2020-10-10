---
title: Vytvoření požadavků na údržbu
description: Toto téma vysvětluje, jak vytvořit požadavek na údržbu v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 22d5e371c386abc71946bf64ed8792647f78cf1b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889211"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="82864-103">Vytvoření požadavků na údržbu</span><span class="sxs-lookup"><span data-stu-id="82864-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="82864-104">Požadavky na údržbu lze použít, pokud pracovníci údržby nebo výrobní pracovníci zjistí, že zařízení vyžaduje opravu, ale opravu nelze provést ihned.</span><span class="sxs-lookup"><span data-stu-id="82864-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="82864-105">**Příklad:** V době, kdy pracovník údržby provádí opravu, zjistí, že je nutné provést servis jiného majetku ve stejném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="82864-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="82864-106">Pracovník údržby však nemá čas nebo požadované náhradní díly k provedení úlohy opravy.</span><span class="sxs-lookup"><span data-stu-id="82864-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="82864-107">Z tohoto důvodu vytvoří pro majetek požadavek na údržbu a zadá krátký popis výdeje.</span><span class="sxs-lookup"><span data-stu-id="82864-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="82864-108">Část **Aktivní požadavky na údržbu** v podokně **Související informace** na pravé straně stránky **Všechen majetek** nebo **Aktivní majetek** (**Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**) ukazuje aktivní požadavky na údržbu, které jsou připojeny k vybranému majetku.</span><span class="sxs-lookup"><span data-stu-id="82864-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="82864-109">Vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="82864-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="82864-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="82864-110">Select **New**.</span></span>
3. <span data-ttu-id="82864-111">V dialogovém okně **Vytvořit požadavek** vyberte typ požadavku na údržbu v poli **Typ požadavku na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="82864-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="82864-112">Je navržen výchozí typ.</span><span class="sxs-lookup"><span data-stu-id="82864-112">A default type is suggested.</span></span>
4. <span data-ttu-id="82864-113">Do pole **Popis** zadejte název nebo titul, který stručně popisuje požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="82864-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="82864-114">V polích **Funkční místo** a **Majetek** vyberte podle potřeby funkční místo nebo majetek nebo kombinaci funkčního místa a majetku.</span><span class="sxs-lookup"><span data-stu-id="82864-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="82864-115">Požadavek na údržbu můžete vytvořit bez výběru majetku a majetek lze později přidat do požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="82864-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="82864-116">Pokud pracovník údržby, který je přihlášený, souvisí se zdrojem, který souvisí s majetkem, bude pole **Majetek** nastaveno automaticky.</span><span class="sxs-lookup"><span data-stu-id="82864-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="82864-117">Pokud je požadavek na údržbu již připojen k vybranému majetku, zobrazí se v horní části dialogového okna **Vytvořit požadavek** panel zpráv s upozorněním na ID existujícího požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="82864-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="82864-118">Panel zpráv vás také upozorní, když je majetek kryt záruční smlouvou.</span><span class="sxs-lookup"><span data-stu-id="82864-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="82864-119">V poli **Úroveň služby** vyberte úroveň služby označující naléhavost požadavku.</span><span class="sxs-lookup"><span data-stu-id="82864-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="82864-120">Pokud jste v kroku 5 vybrali majetek, můžete vytvořit registraci chyb pomocí polí **Příznak chyby**, **Oblast chyby** a **Typ chyby**.</span><span class="sxs-lookup"><span data-stu-id="82864-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="82864-121">Pokud požadavek na údržbu způsobil výpadek údržby, zadejte počáteční datum a čas prostoje.</span><span class="sxs-lookup"><span data-stu-id="82864-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="82864-122">Pole **Zahájil/a** je automaticky nastaveno na vaše jméno.</span><span class="sxs-lookup"><span data-stu-id="82864-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="82864-123">Pole **Skutečný začátek** je automaticky nastaveno na aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="82864-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="82864-124">Hodnotu v tomto poli však můžete podle potřeby měnit.</span><span class="sxs-lookup"><span data-stu-id="82864-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="82864-125">Do pole **Poznámky** zadejte libovolné další požadované poznámky.</span><span class="sxs-lookup"><span data-stu-id="82864-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="82864-126">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="82864-126">Select **OK**.</span></span>

![Vytvořit požadavek na údržbu](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="82864-128">Následné zpracování požadavků na údržbu</span><span class="sxs-lookup"><span data-stu-id="82864-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="82864-129">Po vytvoření požadavku na údržbu, ale před jeho převodem na pracovní příkaz, je třeba v něm aktualizovat různé informace.</span><span class="sxs-lookup"><span data-stu-id="82864-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="82864-130">Tento úkol obvykle dokončuje plánovač nebo jiný administrativní zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="82864-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="82864-131">Na stránce **všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** vyberte požadavek, se kterým chcete pracovat, a pak vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="82864-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="82864-132">V zobrazení podrobností lze aktualizovat různé informace.</span><span class="sxs-lookup"><span data-stu-id="82864-132">In the details view, you can update various information.</span></span> <span data-ttu-id="82864-133">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="82864-133">Here are some examples:</span></span>

- <span data-ttu-id="82864-134">Vyberte a ověřte majetek.</span><span class="sxs-lookup"><span data-stu-id="82864-134">Select and verify the asset.</span></span> <span data-ttu-id="82864-135">Pokud je nutné později vybrat jiný majetek, můžete nastavit možnost **Majetek ověřen** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="82864-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="82864-136">Vyberte odpovědnou skupinu pracovníků údržby nebo odpovědného pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="82864-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="82864-137">Další informace o požadovaném nastavení naleznete v části [Zodpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="82864-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="82864-138">Vyberte typ práce údržby, a pokud jsou tyto informace relevantní, pak příslušnou variantu údržby a odvětví práce.</span><span class="sxs-lookup"><span data-stu-id="82864-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="82864-139">Do polí **zeměpisná šířka** a **Zeměpisná délka** zadejte zeměpisné souřadnice.</span><span class="sxs-lookup"><span data-stu-id="82864-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="82864-140">Všechny souřadnice přidané k požadavku na údržby jsou automaticky převedeny do související pracovní objednávky.</span><span class="sxs-lookup"><span data-stu-id="82864-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Aktualizace požadavku na údržbu](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="82864-142">Pokud při vytváření požadavku na údržbu vyberete určitý majetek, můžete k majetku přidat jednu chybu.</span><span class="sxs-lookup"><span data-stu-id="82864-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="82864-143">Po vytvoření požadavku na údržbu můžete podle potřeby přidat další chyby.</span><span class="sxs-lookup"><span data-stu-id="82864-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="82864-144">Pokud chcete přidat chyby, vyberte **Chyba majetku** na stránce **Všechny požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="82864-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
